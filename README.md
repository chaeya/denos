# Create Minimal Debian Based Linux with Deboostrap

데비안 기반 커스텀 리눅스 제작 스크립트

 * upstream : https://github.com/dinooz/denos

# How to build

1) `sudo ./01_denos_pre_reqs.sh`

2) `./02_denos_debootstrap.sh`

3) Start chroot environment

* chroot 환경으로 진입하면, 어떤 환경을 구성할지 03_denos_chroot_xxxx 파일 중 선택해서 실행한다.

* 만약 lxde 를 설치하고 싶은 경우에는 다음과 같이 실행한다.

>> ```./03_denos_chroot_lxde.sh```

* 설치가 끝나면 chroot 환경을 빠져 나간다.

>> `CTRL+D` 또는 `exit`

4) squash filesystem 생성

>> `./04_denos_MakeSquashfs.sh`

5) ISO 이미지 제작

>> `./05_denos_BiosUEFI_ISO.sh`

