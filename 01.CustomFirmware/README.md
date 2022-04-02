# 커펌 설치

## 0. 계획
* 4.88 OFW 에서 커펌 시작
* 커펌전 PSN 미국 계정을 마련
* 커펌전 PSN 미국 계정으로 로그인 후 기기 인증 필요
> NOTE. PSN 로그인하고 기기 인증한 정보를 나중에 커펌이후 사용하게 됨.(반드시 필요한 과정)

## 1. 설치
ref) How to Jailbreak your PS3 Version 4.88 (2022):
      https://youtu.be/XT52VK2GDNg

1. 하드디스크를 MBR방식의 NTFS로 포맷(WINDOWS키+R distmgmt.msc 실행에서 하는게 좋음)
2. 포맷한 HDD 장착
3. 최신의 OFW 를 USB의 PS3/UPDATE 폴더에 넣고 USB 두번째에 연결(포트는 상관없으나 두번째에 연결하는게 좋음)
* HDD를 새로 장착하였으므로 USB를 통해 공식 펌웨어 설치
* 이미 커펌한 PS3의 경우에는 마지막으로 커펌한 펌웨어를 USB에 넣고 해야함! (따라서 커펌한 PS3은 공식 펌웨어로 되돌리고 하는 것을 추천. 되돌리는 방식은 아래에 따로 설명)
4. 설치후 Create User로 psn이란 이름으로(아무이름이나 상관없음) 계정을 생성하고 생성한 계정으로 로그인한 다음 만들어둔 psn 로그인 계정으로 로그인
5. 로그인 한 다음 빠져나와서 account management 세모 버튼 클릭후 나오는 메뉴에서 activate system에서 GAME 선택후 activate
6. ~~create user로 hen 계정생성하고 hen 계정으로 로그인~~ <= 필요없음
7. web browser에서 ps3xploit.com 연결
8. flash를 usb로 dump
9. dump한 파일을 pc로 가져와 PyPS3checker dump 파일 체크(python 2.7 설치 필요)
* dump 파일은 잘 보관할 것!
10. 다시 ps3으로 와서 나머지 처리이후 reboot
11. 재기동후 설정
* Trophy Notification off
* Diusc Auto-Start off
* Display [What's New] off
12. USB의 PS3/UPDATE 폴더에 EVILNAT 4.88.2 버전의 CFW를 복사한다음 PS3에 연결(크게 상관은 없지만 2번째 USB에 연결하자!)
13. System Update를 선택하고 USB를 통해서 설치
14. reboot
15. app 설치(rebog tool, webman, multiman, sen enabler, psnpatch 등)
16. webman 기동(full) 후 삭제
17. 멀티맨 기동
18. Rebug cfw 설치는 옵션
> NOTE. 여기서는 4.84.2 버전을 설치(DEX 버전이 있는 마지막 버전)
+ I. Rebug REX 설치 (옵션)
   - 1단계) Network Settting(Setting의 최하위 메뉴)에 가져다 놓고 L1 + L2 + R1 + R2 + L3 + Dpad Down 키 입력후 아래의 세개의 메뉴가 생기는 것을 확인(Edy Viewer, Debug Settings, Install Package Files)
   - 2단계) Rebug REX FW 를 USB의 PS3/UPDATE 폴더에 넣고 system update
+ II. Rebug D-REX 설치 (옵션)
   - 1단계) Rebug Tool box 실행
   - 2단계) info system에서 cex 인것 확인(두개 메뉴가 cex)
   - 3단계) dump eid root key 실행
   - 4단계) reboot
   - 5단계) Rebug Tool box 실행
   - 6단계) rewrite target id in flash 실행
   - 7단계) swap LV2 Kernel 실행
   - 8단계) reboot
   - 9단계) Rebug Tool box 실행
   - 10단계) info system에서 dex 인것 확인(두개 메뉴가 dex)
* III. spoof 설정
   - 1단계) sen enabler app 실행(없으면 app 설치가 필요)
   - 2단계) sen/psn options 선택
   - 3단계) custom spoof 선택
   - 4단계) version 에서 4.87 선택(현재는 4.88 버전이 없음. 그래서 설정을 해도 PSN 로그인은 안됨)
   - 5단계) custom spoof 선택
     + => install 진행
   - 6단계) reboot
   - 7단계) system info 에서 버전 확인하면 4.87 인것을 알수 있음.

> NOTE. EVILNAT 4.88.2 은 PSN이 현 시점(2022-04-01)에서는 가능한 것으로 보이고 Rebug은 안됨.

## 2. 커펌한 이후 다시 HDD교체하는 경우
마지막 커펌한 버전의 펌웨어를 USB에 넣어서 설치(정펌으로는 안됨)
> NOTE. O, X키가 US기준으로 변경됨.

## 3. Rebug 커스텀 펌웨어의 cex, dex 란?
Rex in I would say 99% of cases.

D-Rex for DEX firmware which is developer firmware.

Rex is for CEX or retail firmware.

## 4. Rebug dex 에서 cex로 변경하는 방법
Rebug Toolbox app을 이용
1. dex, cex인지는 app내 system information에서 확인 가능 : LV2 Kernel, Target Type 항목 확인
2. app에서 rewrite target id in flash에서 dex를 cex로 변경(dump eid root key가 없다면 생성 필요)
3. 그런다음 cex 버전의 Rebug firmware를 system update를 통해서 설치
> NOTE. 현재 Rebug는 4.84버전은 dex까지 나온 상황(4.86은 dex가 없음)

## 5. Rebug cex에서 evilnat으로 cfw 변경 하는 방법
USB의 PS3/UPDATE에 cfw를 담은후 system update를 이용하여 설치

## 6. evilnat에서 정펌으로 변경하는 방법
USB의 PS3/UPDATE에 ofw를 담은후 system update를 이용하여 설치

## 7. Rebug에서 정펌으로 변경하는 방법
1. dex 버전이면 cex 로 변경
2. cex 버전의 CFW 를 설치
3. evilnat 버전의 CFW 를 설치
4. 정펌을 설치
> NOTE. 설치의 역순
 
## 8. 에러 대처 
```
o ps3 하드 교체시 에러 발생 대처
결론 - NTFS 로 포맷후 Firmware 설치
https://www.reddit.com/r/PS3/comments/b4eadg/hard_drive_replacement_from_hell_help_please/

o PSN 연결 문제
https://www.reddit.com/r/ps3homebrew/comments/pykpdy/on_484_rebug_dex_ps3_has_never_connected_to_psn/

chance ban is high in that old version, use updated CFW evilnat 4.88.2 for updated and normal online play/services (follow correct setup and options in changelog is adviced) not use spoof, psntool, multiman etc not neccesary anymore (games run from xmb with webmamond install) and use only .ISO dumps or store instaled content for online (not use JB old folder dumps or modded content), Rebug DEX setup is usefull for homebrew developers / debuggers only but common user is not neccesary or have any advantages

=> evilnat 4.88.2 버전이 좋긴 한데 JB folder 형식의 게임은 실행이 안되는듯?

o PSN 연결
How To Switch From CEX To DEX 4.84 And Get Back Online Rebug 4.84 CFW 2021
https://youtu.be/ZTT3blhcWNw

=> 안되는듯...


```

___
.END OF CUSTOMFIRMWARE