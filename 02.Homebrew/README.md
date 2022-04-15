# 홈브류 설치

## 0. 홈브류
* 사전적의미는 직접 제작한 제작물이란 뜻으로 커펌한 기기에 실행할수 있도록 직접 만든 프로그램을 의미


## 1. 설치
```
o pkg 파일 위치
hdd는 /dev_hdd0/packages
usb는 /packages/ 또는 / 디렉토리에 pkg 파일을 복사

@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

o PC에 PS3 에뮬 설치
https://gamepublish.tistory.com/115

o 커펌후 디렉토리
변환 할필요없이 쉽게 설명해서 USB 기준 게임 담는 방법을 알려드릴께요
1. USB > PACKAGES 폴더생성>PKG파일 넣기
2. USB > GAMES & GAMEZ 둘중 하나 폴더생성>폴더형식 파일 넣기
3. USB > PS3ISO 폴더생성>ISO 파일 넣기
참고로 4GB 넘는 파일은 NTFS로 포맷 후에 실행해야되요

192.168.0.194 <= My PS3

내부 HDD 구성은,
/dev_hdd0/GAMES    : 디렉토리로 된 게임
         /PS3ISO   : iso 로 된 게임
         /exdata   : (rap) 디렉토리는 생성해야함.
                     확장자는 소문자일것! 소문자가 아니면 나중에 psnpatch에서 읽지를 못함!
                     evilnat은 문제없지만 rebug 커펌은 소문자만 인식
                     참고로 rap 파일명은 절대 변경하면 안됨.
         /packages : pkg 파일 (인스톨할 게임이나 app). 간편한 이름으로 변경가능(특수문자를 제거하자)

NOTE. ps3 80010006 error <- pkg 파일명에 특수문자가 있거나 너무 길면 생기는 듯.
           ps3 80029563 error <- USB가 문제인 경우가 대부분

USB 구성은,
/PKG/ 폴더에 pkg 파일
```

## 기타 설정
```
o XMB 폴더 구성하기
https://youtu.be/SovS4R-Q_OE

o webman ftp 암호설정
https://github.com/aldostools/webMAN-MOD/discussions/469
web 설정에 있음
NOTE. ******** 로 설정함
```

___
.END OF HOMEBREW