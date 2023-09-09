# EdenOS
This is EdenOS

just trying out OS dev to see if im interested

setup:
docker build buildenv -t edenos-buildenv

build:
docker run --rm -it -v %cd%:/root/env edenos-buildenv
make build-x86_64
exit

emulate:
qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso