./scripts/feeds update -a
./scripts/feeds install -a
移动.config和diy.sh到目标目录，直接diy.sh
make defconfig
make download -j8
find dl -size -1024c -exec ls -l {} \;
find dl -size -1024c -exec rm -f {} \;
make -j$(nproc)
