# 커펌 설치

## 0. 계획
* PSN 미국 계정을 마련
* PSN 미국 계정으로 로그인 후 기기 인증 필요

## 1. 설치
ref) How to Jailbreak your PS3 Version 4.88 (2022):
      https://youtu.be/XT52VK2GDNg

```
1. 하드디스크를 MBR방식의 NTFS로 포맷(WINDOWS키+R distmgmt.msc 실행에서 하는게 좋음)
2. 포맷한 HDD 장착
3. 최신의 OFW 를 USB의 PS3/UPDATE 폴더에 넣고 USB 두번째에 연결(포트는 상관없으나 두번째에 연결하는게 좋음)
4. 설치후 create user로 psn 계정생성하고 psn으로 연결후 마련한 psn계정으로 로그인
5. 로그인 한 다음 빠져나와서 account management 세모 버튼 클릭후 나오는 메뉴에서 activate system에서 GAME 선택후 activate
6. create user로 hen 계정생성하고 hen 계정으로 로그인
7. web browser에서 ps3xploit.com 연결
8. flash를 usb로 dump
9. dump한 파일을 pc로 가져와 PyPS3checker dump 파일 체크(python 2.7 설치 필요)
- dump 파일은 잘 보관할 것!
10. 다시 ps3으로 와서 나머지 처리이후 reboot
11. 재기동후 설정
- Trophy Notification off
- Diusc Auto-Start off
- Display [What's New] off
12. app 설치
13. webman 기동(full) 후 삭제
14. 멀티맨 기동
15. rebug cfw 설치는 옵션
   1) rebug rex 설치 (옵션)
   - network settting에 가져다 놓고 L1 + L2 + R1 + R2 + L3 + Dpad Down 키 입력후 아래의 세개의 메뉴가 생기는 것을 확인(Edy Viewer, Debug Settings, Install Package Files)
    - REX FW 를 USB의 PS3/UPDATE 폴더에 넣고 system update
   2) rebug d-rex 설치 (옵션)
    - rebug tool box 실행
    - info system에서 cex 인것 확인(두개 메뉴가 cex)
    - dump eid root key 실행
    - reboot
    - rebug tool box 실행
    - rewrite target id in flash 실행
    - swap lv2 kernel 실행
    - reboot
    - rebug tool box 실행
    - info system에서 dex 인것 확인(두개 메뉴가 dex)

    - sen enabler 실행
    - sen/psn options 선택
    - custom spoof 선택
    - version 에서 4.87 선택
    - custom spoof 선택
      => install 진행
    - reboot
    - system info 에서 버전 확인하면 4.87 인것을 알수 있음.
```

## 2. 커펌한 이후 다시 HDD교체하는 경우
```
마지막 커펌한 버전의 펌웨어를 USB에 넣어서 설치(정펌으로는 안됨)
```
> NOTE. O, X키가 US기준으로 변경됨.

## 3. Rebug 커스텀 펌웨어의 cex, dex 란?
```
Rex in I would say 99% of cases.
D-Rex for DEX firmware which is developer firmware.
Rex is for CEX or retail firmware.
```

## 4. Rebug dex 에서 cex로 변경하는 방법
```
- Rebug Toolbox app을 이용
1. dex, cex인지는 app내 system information에서 확인 가능 : LV2 Kernel, Target Type 항목 확인
2. app에서 rewrite target id in flash에서 dex를 cex로 변경(dump eid root key가 없다면 생성 필요)
3. 그런다음 cex 버전의 Rebug firmware를 system update를 통해서 설치
```
> NOTE. 현재 Rebug는 4.84버전은 dex까지 나온 상황(4.86은 dex가 없음)

## 5. Rebug cex에서 evilnat으로 cfw 변경 하는 방법
```
1. USB의 PS3/UPDATE에 cfw를 담은후 system update를 이용하여 설치
```

## 6. evilnat에서 정펌으로 변경하는 방법
```
1. USB의 PS3/UPDATE에 ofw를 담은후 system update를 이용하여 설치
```

___
.END OF CUSTOMFIRMWARE