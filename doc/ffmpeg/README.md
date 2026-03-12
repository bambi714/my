## 1. ffmpeg 설치 방법
## 목차
<!-- TOC start -->
 * [Mac 용](#mac-용)
   * [1.homeBrew 설치](#1homebrew-설치)
   * [2. FFmpeg 설치](#2-ffmpeg-설치)
   * [3.맥에서 사용시](#3-맥에서-사용시)
 * [Window 용](window-용)
 * [1. FFmpeg 다운(zip 파일 다운)](#1-ffmpeg-다운zip-파일-다운)
 * [2. 사용방법1 (특정 폴더에서 사용 가능)](#2-사용방법1-특정-폴더에서-사용-가능)
 * [3. 사용방법2 (전체 폴더에서 사용 가능)](#3-사용방법2-전체-폴더에서-사용-가능)
<!-- TOC end -->

## Mac 용
### 1.homeBrew 설치

[homebrew 공식페이지](https://brew.sh/ko/) 참고
1. command + space 로 Spotlight 열고 `터미널` 입력
2. 아래 설치 명령어를 터미널에 입력
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
3. 암호를 입력하라고 하면 맥비밀번호 입력 (경우에따라 암호 입력없이 진행)

    <img width="513" height="30" alt="스크린샷 2026-03-13 오전 2 17 41" src="https://github.com/user-attachments/assets/3646661f-1b63-47c6-8c40-c1cc70652ec7" />

4. 위에처럼 계속 진행하고 싶으면 엔터를 누르라고 뜨면 `Enter`

5. **Apple Silicon Mac의 경우 필수** 설치 완료 후 터미널 출력되는 "Next steps"의 명령어를 복사 후 붙여넣기 후 엔터 입력
   - 아래처럼 **PATH:** 이후 **- Run brew help to get started** 이전에 출력되는 `echo;` ~ `shellenv)"` 까지 복사
   - 출력되는 명령어는 사용자에따라 mac os 버전에따라 다를 수 있으니 터미널에 출력되는 것을 복사하기
```
- Run these two commands in your terminal to add Homebrew to your PATH:
  (echo; echo 'eval "ș(/usr/local/bin/brew shellenv) "') > .....
  eval "$(/usr/local/bin/brew shellenv)"
- Run brew help to get started
- Further documentation:
https://docs.brew.sh
```

6. 설치 완료 확인 방법 : 터미널에 `brew --version`를 입력후 엔터를 누르면 `Homebrew 버전숫자`가 뜸.
```
brew --version
```

### 2. FFmpeg 설치
1. 아래 명령어를 터미널에 입력(command + space 로 Spotlight 열고 `터미널` 입력하여 터미널 열기)
```
brew install ffmpeg
```

2. 터미널에 `ffmpeg -version`입력 후 버전 번호가 뜨면 설치 완료


### 3. 맥에서 사용시 
- ffmpeg를 사용하기 위해서는 터미널에서 명령어를 입력하여 사용함.
- 터미널을 열었을 때 경로가 `User/사용자이름`에서 시작 되는데 여기 위치가 finder의 위치 탭의 `집모양 + 사용자이름`위치랑 같은 위치
- ffmpeg 명령어를 쓸때 타겟이 되는 파일의 폴더 위치에서 하거나 해당 파일의 전체 위치 경로를 알아야함.(해당 폴더 위치로 이동하는게 더 쉬움.)
- 터미널에서 알아야할 명령어
   - pwd : 현재 위치의 폴더 경로를 출력
   - cd 경로 : 현재 폴더 아래 폴더들의 경로를 입력하여 현재 위치를 원하는 폴더로 옮김
   - cd .. : 현재 폴더의 상위(부모)폴더로 이동
  <img width="614" height="207" alt="Frame 4" src="https://github.com/user-attachments/assets/9e84591c-261f-438d-93b7-cccd847bb208" />
- ffmpeg를 사용할때 cd 명렬어로 폴더 위치를 이동하여 사용


## Window 용

### 1. FFmpeg 다운(zip 파일 다운)
1. [FFmpeg 공식페이지](https://www.gyan.dev/ffmpeg/builds/)로 이동
  
2. release builds 의 latest release에서 `.zip` 다운로드

  <img width="1090" height="272" alt="image" src="https://github.com/user-attachments/assets/b15e85f8-d4b6-4d10-85a0-762f0e4a9335" />

3. 원하는 곳에 해당 zip파일 압축 풀기
4. 압축을 풀면 ffmpeg~~폴더에 bin, doc 폴더등이 있고, bin 폴더에 들어가면 `ffmpeg.exe` 파일이 있으면 설치 완료 됨

<br>

### 2. 사용방법1 (특정 폴더에서 사용 가능)

환경변수 설정 하지않고 `ffmpeg~~폴더/bin` 폴더에서만 사용 가능 (ffmpeg.exe 파일이 있는 곳에서만)

1. 사용시 cmd에서 해당 폴더로 이동 후 `./ffmpeg.exe` 명령어로 사용(윈도우 기준)
- ex) cmd에서 `./ffmpeg.exe -i "url" -c copy myviedo.mp4`로 사용

<br>

### 3. 사용방법2 (전체 폴더에서 사용 가능)
환경변수 설정하고, PC 전체에서 사용가능함.
1. 윈도우검색(win키 누르기)에서 "환경 변수" 입력 ->  `시스템 환경 변수 편집` 클릭

   <img width="428" height="91" alt="image" src="https://github.com/user-attachments/assets/7da04351-e478-4cd2-a97d-84876c71cc8d" />

2. 환경 변수(N)... 클릭

   <img width="607" height="699" alt="image" src="https://github.com/user-attachments/assets/c1a961b3-ad75-403b-af2b-2c4008e302df" />
   
3. 시스템 변수(S) 에서 `Path`를 찾아 클릭 -> 편집(I) 버튼 클릭

<img width="612" height="703" alt="image" src="https://github.com/user-attachments/assets/265bcb60-f5e1-4085-816e-caa6fdf2aee8" />

  
4. `새로 만들기`를 누르고 ffmpeg의 bin 폴더 경로를 입력해준다. (`ffmpeg.exe` 파일이 있는 폴더 경로 입력) 후 `확인` -> `확인` -> `확인`

  <img width="664" height="657" alt="image" src="https://github.com/user-attachments/assets/8e33622a-4ea4-4c10-8caa-d715195a96eb" />

5. cmd 창을 열어 `ffmpeg -version` 입력해서 설치한 버전이 제대로 나오면 (빨간 글씨가 안나오면) 성공

   <img width="860" height="95" alt="image" src="https://github.com/user-attachments/assets/4e924391-efdc-4ef6-83b2-9ae03c88088c" />

6. 사용 방법 : cmd 창에서 자신이 원하는 폴더 어디든지 이동해서 `ffmpeg` 명령어로 사용
   - ex) ffmpeg -i "url" -c copy myviedo.mp4"

