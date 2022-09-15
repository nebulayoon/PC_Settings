# PC_Settings

### windows10 WSL 설정
```
[wsl 활성화]
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

[vm 활성화]
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

[커널 패키지 설치]
https://docs.microsoft.com/ko-kr/windows/wsl/install-manual

[wsl 버전2 설정]
wsl --set-default-version 2

[store에서 ubuntu 설치]
```

### windows Bing 검색 비활성화
```
[대상 경로]
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Search

[값 생성(DWORD(32비트))]
BingSearchEnabled 0
CortanaConsent 0
```

### Window10 자동 업데이트 해제
```
[windows service]
service -> windows update ->disable

[자동 업데이트 해제(gpedit.msc)]
로컬 컴퓨터 정책 -> 컴퓨터 구성 -> 관리 템플릿 -> Windows 구성 요소 -> Windows Update -> 자동 업데이트 구성
Computer Configuration > Administrative Templates > Windows Components > Windows Update > Configure Automatic Updates

```

### ZSH 설정
```
[zsh 및 oh my zsh 설치]
sudo apt-get install zsh -y
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

[테마]
vim ~/.zshrc
ZSH_THEME="agnoster"

[폰트]
https://github.com/powerline/fonts
https://github.com/naver/d2codingfont/releases/tag/VER1.3.2

[플러그인]
<syntax highlighting>
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
vim ~/.zshrc
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

### Windows Terminal 테마(theme)
```
[settings.json]
"defaults":
        {
            // Put settings here that you want to apply to all profiles.
            "colorScheme": "Solarized Dark",
            "fontFace": "D2Coding",
            "fontSize": 11
        }
```