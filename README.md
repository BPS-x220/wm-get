# wm-get
WinCE/WindowsMobileで使用可能なパッケージマネージャ
##動作確認 
※Advanced/W-ZERO3[es]で動作確認済み
# ディレクトリ構造
```
wm-get
　┃
　┣━repo-list
　┣━lib
　┃　┣━wmg-lib
　┃　┃　┣━7zip
　┃　┃　┗━wgetce
　┃　┗━bat-lib
　┗━pkg
　　　┃
　　　┣━zpkg
　　　┗━lpkg

```
```
//wmg-lib

wmg-lib
　┃
　┣━7zip
　┃　┣━7z.sfx
　┃　┣━7zS2.sfx
　┃　┗━7zFM.exe
　┗━wgetce
　　 　┗━wget.exe
　　　

```
# 手動で構築
### 1.下記の手順でディレクトリを構築します

```
wm-get-dev.bat
```
### 2.ライブラリを配置する
WinCE向け7zipとwgetceを用意する  
`wmg-lib`へ7zipとwgetceを移動する
# 必須
- cmd
- 7zip
- wgetce
# 入手先
[7zip/7z920-arm.exe](https://www.7-zip.org/a/7z920-arm.exe)  
[wget/wgetce10.zip](https://web.archive.org/web/20020207180926/http://www.tenik.co.jp/~adachi/gnu/wgetce10.zip)  
[WindowsMobilePowerToys.msi](https://web.archive.org/web/20260406224151/http://am.net/lib/TOOLS/Microsoft/Mobile/WindowsMobilePowerToys.msi)
  
# cmdの導入方法
### 1.WindowsMobilePowerToys.msiダウンロードする
[Mobile/WindowsMobilePowerToys.msi](https://web.archive.org/web/20260406224151/http://am.net/lib/TOOLS/Microsoft/Mobile/WindowsMobilePowerToys.msi)  
インストール後に作られた`C:\Program Files\Windows Mobile Developer Power Toys\PPC_Command_Shell\arm`の中身を`Windows`ディレクトリへコピーする  
  
C:\Program Files\Windows Mobile Developer Power Toys\PPC_Command_Shell\armの中身
```
// C:\Program Files\Windows Mobile Developer Power Toys\PPC_Command_Shell\arm
    ┃
    ┣━cmd.exe
    ┣━console.dll
    ┗━shell.exe

```
### 2.レジストリを編集する
下記と同じようにレジストリを書き換える
```
[HKEY_LOCAL_MACHINE\Drivers\Console]
"OutputTo"=dword:0
```
