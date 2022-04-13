# 게임 설치

## 0. 내부 HDD 폴더 구성 개요
```
내부 HDD 구성은,
/dev_hdd0/GAMES    : 디렉토리로 된 게임 (설정에 따라 GAMEZ 인 경우도 있음)
         /PS3ISO   : iso 로 된 게임
         /exdata   : (rap) 디렉토리는 생성해야함.
                     확장자는 소문자일것! 소문자가 아니면 나중에 psnpatch에서 읽지를 못함!
                     evilnat은 문제없지만 rebug 커펌은 소문자만 인식
                     참고로 rap 파일명은 절대 변경하면 안됨.
         /packages : pkg 파일 (인스톨할 게임이나 app). 간편한 이름으로 변경가능(특수문자를 제거하자)
```

```
o 커펌후 디렉토리
변환 할필요없이 쉽게 설명해서 USB 기준 게임 담는 방법을 알려드릴께요
1. USB > PACKAGES 폴더생성>PKG파일 넣기
2. USB > GAMES & GAMEZ 둘중 하나 폴더생성>폴더형식 파일 넣기
3. USB > PS3ISO 폴더생성>ISO 파일 넣기
참고로 4GB 넘는 파일은 NTFS로 포맷 후에 실행해야되요
```

* error
``` 
ps3 80010006 error <- pkg 파일명에 특수문자가 있거나 너무 길면 생기는 듯.
ps3 80029563 error <- USB가 문제인 경우가 대부분
```

* USB의 pkg파일 구성시 폴더
``` 
USB 구성은, /PKG/ 폴더에 pkg 파일
```
> NOTE. 폴더명이 packages가 아니라 PKG ???

## 1. 폴더 형식(JB Folder) 게임 설치
```
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
```

## 2. ISO 형식 게임 설치
```
1. HDD의 PS3ISO 폴더에 iso 파일 업로드
2. 멀티맨을 통해서 실행(게임 선택하고 X 키 누르고 나오는 메뉴에서 Load 선택)
3. XMB로 나오면 해당 게임이 CD로 마운트 되어 있음.
4. 실행하면 설치가 진행되면서 실행됨.
```

## 3. pkg 형식 게임 설치
* HDD
```
1. HDD 의 packages 폴더에 pkg 파일 없로드
2. HDD 의 exdata 폴더에 rap 파일 업로드
3. psnpatch app을 실행하여 rap 파일 적용
   => D패드의 방향키를 위아래를 눌러서 hdd로 선택한 다음 L1을 눌러서 적용 및 O 키를 눌러 exit
4. XMB의 Install Package 메뉴를 통해서 설치
``` 
> NOTE. 확장자는 소문자로 할것!(커펌 버전에 따라 대문자인경우 에러가 나는 경우가 있음.)

* USB
 ```
1. USB 의 PKG 폴더에 pkg 파일 없로드
2. USB 의 exdata 폴더에 rap 파일 업로드
3. psnpatch app을 실행하여 rap 파일 적용
4. XMB의 Install Package 메뉴를 통해서 설치
```

## 4. PS1, PS2, PS3, PSP ISO 게임 설치
ref) https://youtu.be/iSt6VpxE2c8

PS1, PS3은 폴더 형식으로 사용가능하고 PS2, PSP는 ISO로 변환해서 사용하자!

PSP는 내부 HDD에 복사한 다음 실행해야함. PS1, PS2 는 USB에서도 실행가능

디렉토리구조는, HDD와 USB가 동일

PSXISO/ : PS1용 iso파일 위치
PS2ISO/ : PS2용 iso파일 위치
PS3ISO/ : PS3용 iso파일 위치
PSPISO/ : PSP용 iso파일 위치

* PS2 ISO를 위한 bin to ISO 변환

ref) https://youtu.be/Axp4-M2srqw

  1. https://oplmanager.com/site/ 의 프로그램을 이용하여 bin 파일을 iso 파일로 변환

  2. PS2ISO 폴더에 iso 복사

  3. Webman refresh

  4. webman에서 ps2 게임을 선택하면 CD로 load됨

  5. CD 를 실행하여 게임 실행

  NOTE. PS2 게임을 처음 실행한다면 Internal Memory 가 필요하다고 팝업창이 뜨는데 그냥 하나 만들면 됨.(게임 세이브 용도임)

* PSP to ISO Tools
다운로드 링크
 
https://www.psx-place.com/resources/ps3-iso-tools.68/

* PSP Launcher
https://github.com/aldostools/webMAN-MOD/releases
> NOTE. 현재 설치한 Rebug 4.82 DEX 에서는 PSP Launcher가 설치가 안됨.
 
>  Cobra PSP Lancher v2.00 by Cobra에서 [Official by COBRA] 를 다운받아 설치하면 됨.

호환성은 아래에서 확인 할것!

https://www.psdevwiki.com/ps3/PSP_Emulator_Compatibility_List






## 5. RetroArch 설치
```
o RetroArch 설정 방법
https://youtu.be/XUn5bEX5dk4
```

## 6. 기타
```
o PC에 PS3 에뮬 설치
https://gamepublish.tistory.com/115

NOTE. 사실 cfw에서 /dev_hdd0/packages, usb는 /packages/, / 디렉토리 에서 pkg 파일을 설치하게끔 메뉴를 만들어 두었기 때문에 이디렉토리를 유지하는게 가장 좋음.
즉, 내부 HDD는 packages 디렉토리에, usb는 /packages/ 또는 root 디렉토리에 pkg 파일을 두면 된다.

o PS3 게임 설치 방법(feat. cfw)
https://www.superpsx.com/inject-ps3-games-super-slim-ofw-4-82/amp/

NOTE. 용어 설명 등 잘 되어 있음.
```

___
.END OF GAME