# 패키지 설치

## 0. 계획 @@@
* 4.88 OFW 에서 커펌 시작
* 커펌전 PSN 미국 계정을 마련
* 커펌전 PSN 미국 계정으로 로그인 후 기기 인증 필요
> NOTE. PSN 로그인하고 기기 인증한 정보를 나중에 커펌이후 사용하게 됨.(반드시 필요한 과정)

## 1. 설치
```
o 소니 정식 펌웨어
https://www.playstation.com/en-us/support/hardware/ps3/system-software/

o game list
https://www.pushsquare.com/ps3/games/browse
https://psndl.net/packages

https://jkimgametips.tistory.com/769
NPS 브라우저 <= PSVita에도 해당

https://vimm.net/vault/PS3

https://www.gametdb.com

https://www.psdevwiki.com/ps3/CFW2OFW_Compatibility_List

https://store.brewology.com/

o ps3 하드 교체시 에러 발생 대처
결론 - NTFS 로 포맷후 Firmware 설치
https://www.reddit.com/r/PS3/comments/b4eadg/hard_drive_replacement_from_hell_help_please/

o PC에 PS3 에뮬 설치
https://gamepublish.tistory.com/115

o  아이리스맨 사이트
https://github.com/aldostools/IRISMAN/releases

o 웹맨 사이트
https://github.com/aldostools/webMAN-MOD/wiki

o PSN 연결 문제
https://www.reddit.com/r/ps3homebrew/comments/pykpdy/on_484_rebug_dex_ps3_has_never_connected_to_psn/

chance ban is high in that old version, use updated CFW evilnat 4.88.2 for updated and normal online play/services (follow correct setup and options in changelog is adviced) not use spoof, psntool, multiman etc not neccesary anymore (games run from xmb with webmamond install) and use only .ISO dumps or store instaled content for online (not use JB old folder dumps or modded content), Rebug DEX setup is usefull for homebrew developers / debuggers only but common user is not neccesary or have any advantages

=> evilnat 4.88.2 버전이 좋긴 한데 JB folder 형식의 게임은 실행이 안되는듯?

o PS3 연결
How To Switch From CEX To DEX 4.84 And Get Back Online Rebug 4.84 CFW 2021
https://youtu.be/ZTT3blhcWNw


o 게임(PKG)을 가장 쉽게 설치하는 방법(USB 메모리카드 사용)
How to Install PS3 PKG Files from exFAT & NTFS USB Drives | Large 4 GB+ PKG Support!
https://youtu.be/wOxQBuoefQg

1. NTFS 포맷한 USB 하드디스크 준비
2. PKG/ 디렉토리에 pkg 게임 파일 넣기
3. PS3에 USB 끼운후 preISO 실행
4. webMAN Games -> Blu-ray and DVD에 n Video content 확인(여기서 n은 pkg 파일 개수)
5. 설치한 게임(pkg)를 선택 (우측 상단에 loaded 라는 caption이 뜸)
   => USB에서 internal HDD로 복사하는 과정 (/dev_hdd0/tmp/wmtmp/ 폴더에 복사하고 완료되면 loaded라고 우측 상단에 caption 이 뜸). 이후 /dev_hdd0/game/ 하위에 Title ID로 디렉토리를 생성하고 그곳에 설치.
   => 80029563 error 가 발생하는 경우에는 USB 메모리스틱이나 HDD에 문제가 있는 경우가 대부분(전원 공급이 문제인것으로 짐작.)
6. 선택하고 나서 메뉴로 나와서 Package Manager -> Install Package Files -> Standard 선택하면 앞서 선택한 게임이 나옴. 선택
7.  상위 메뉴로 나와서 Playstation Network Contents 선택하고 나오는 설치할 게임을 선택
   => 여기가 실제로 게임을 설치하는 과정
8. 설치가 끝나면 다시  Playstation Network Contents 선택하고 나오는 설치할 게임에서 세모 선택하고 삭제
??? 조금 다른거 같음.

NOTE. MLB The Show 16은 BCUS01089 을 설치해야함.

o ISO 파일 실행하기
https://youtu.be/uKdUT5whfQw

영상에서는 아이리스맨을 이용하지만 여기서는 멀티맨을 사용하는 방법

1. 멀티맨에서 ISO 파일을 실행
2. XMB로 돌아오면 CD로 마운트 되어있는데 실행

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
                  /PS3ISO    : iso 로 된 게임
                  /exdata     : (rap) 디렉토리는 생성해야함.
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