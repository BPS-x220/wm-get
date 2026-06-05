# wm-get
WinCE/WindowsMobileで使用可能なパッケージマネージャ
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
- 7zip
- wince
# 入手先
[7zip/7z920-arm.exe](https://www.7-zip.org/a/7z920-arm.exe)  
[wget/wgetce10.zip](https://web.archive.org/web/20020207180926/http://www.tenik.co.jp/~adachi/gnu/wgetce10.zip)
