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
