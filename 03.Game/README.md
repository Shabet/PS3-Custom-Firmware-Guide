# 게임 설치

## 0. 계획 @@@
* 4.88 OFW 에서 커펌 시작
* 커펌전 PSN 미국 계정을 마련
* 커펌전 PSN 미국 계정으로 로그인 후 기기 인증 필요
> NOTE. PSN 로그인하고 기기 인증한 정보를 나중에 커펌이후 사용하게 됨.(반드시 필요한 과정)

## 1. 설치
```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
o PC에 PS3 에뮬 설치
https://gamepublish.tistory.com/115

o XMB 폴더 구성하기
https://youtu.be/SovS4R-Q_OE

o webman ftp 암호설정
https://github.com/aldostools/webMAN-MOD/discussions/469
web 설정에 있음
NOTE. ******** 로 설정함

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

NOTE. 사실 cfw에서 /dev_hdd0/packages, usb는 /packages/, / 디렉토리 에서 pkg 파일을 설치하게끔 메뉴를 만들어 두었기 때문에 이디렉토리를 유지하는게 가장 좋음.
즉, 내부 HDD는 packages 디렉토리에, usb는 /packages/ 또는 root 디렉토리에 pkg 파일을 두면 된다.

o RetroArch 설정 방법
https://youtu.be/XUn5bEX5dk4

o 폴더 형식 게임 설치 방법
https://youtu.be/Y4IOllFamjQ
(Vimm's Lair) How to convert JB folder to .ISO file using an ird (PS3 Games) (Rebuilding an ISO)

1. https://vimm.net/vault/PS3 와 같은곳에서 download한게 폴더형식의 파일이면 ird 파일도 같이 다운로드
2. 압축받은 게임을 압축해제
3. PS3-ISO-Rebuilder.exe 를 실행
   1) Open -> JB 폴더 선택하고 압축해제한 root 폴더를 지정
   => PS3UPDAT.PUP 파일이 없다는 에러가 나면 무시하고 No 선택
   2) Open -> IRD 선택 하고 ird 파일 선택
   3) Build/Extract -> Build ISO without IRD 선택
   => Build ISO 는 활성화 되어 있지 않아서 위의 메뉴를 선택(왜 그런지는 잘 모르겠음)
   4) split output 할거냐 물어보는데 FAT32로 옮길때에는 4GB 미만으로 쪼개는게 필요할때 쓰는거고(Yes 선택) FTP로 전송하거나 NTFS를 쓰면 상관없으면 No 선택
4. 결과 iso 파일을 PS3의 PS3ISO 폴더에 복사
5. 멀티맨이나 아이리스맨을 통해 실행한 후 CD로 마운트되면 실행하여서 설치 진행

o PS3 게임 설치 방법(feat. cfw)
https://www.superpsx.com/inject-ps3-games-super-slim-ofw-4-82/amp/

NOTE. 용어 설명 등 잘 되어 있음.
```

___
.END OF PACKAGE