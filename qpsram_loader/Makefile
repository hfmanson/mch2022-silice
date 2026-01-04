all : write read stream


write: write.si prepare
	silice-make.py -s write.si -b mch2022 -p basic,uart,psram -o BUILD_$(subst :,_,$@)
	cp BUILD_write/build.bin bitstreams/write.bin

read: read.si prepare
	silice-make.py -s read.si -b mch2022 -p basic,uart,psram -o BUILD_$(subst :,_,$@)
	cp BUILD_read/build.bin bitstreams/read.bin

stream: stream.si prepare
	silice-make.py -s stream.si -b mch2022 -p basic,uart,psram -o BUILD_$(subst :,_,$@)
	../common/ext/fpga.py BUILD_stream/build.bin

simulation: simul.si prepare
	silice-make.py -s simul.si -b icarus -p basic -o BUILD_$(subst :,_,$@)

fill: fill.si
	silice-make.py -s fill.si -b mch2022 -p basic,psram -o BUILD_$(subst :,_,$@)
	cp BUILD_fill/build.bin bitstreams/fill.bin

write_spi: write_spi.si
	silice-make.py -s write_spi.si -b mch2022 -p basic,psram,espspi -o BUILD_$(subst :,_,$@)
	cp BUILD_write_spi/build.bin bitstreams/write_spi.bin

dump_spi: dump_spi.si
	silice-make.py -s dump_spi.si -b mch2022 -p basic,uart,espspi -o BUILD_$(subst :,_,$@)
	cp BUILD_dump_spi/build.bin bitstreams/dump_spi.bin

prepare:
#	pushd . ; cd ../common/ext ; ./download_all.sh ; popd
	echo prepare

clean:
	rm -rf BUILD_*
