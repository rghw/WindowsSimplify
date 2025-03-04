# Win7 boot.wim

### 簡介：
使用精簡系統時若因為驅動等原因而無法安裝，這裡會提供一個手動修復的方案，只要使用精簡版遇到問題一律改用原版boot，如果使用原版還遇到問題請注意是否符合以下條件
1. 使用USB開機安裝
2. 映像語系是否相同 (boot & install)
3. 位元是否相同 (boot & install)

### 使用說明：
使用方式有兩種，一種是先製作USB開機碟再替換檔案，一種是製作新的ISO檔，如果是給虛擬機使用就只能製作新的ISO，不過...如果使用虛擬機在安裝時遇到問題首先要檢查的是虛擬機設定而不是我製作的系統= =

首先介紹先製作USB開機碟的方式
1. 保留以下檔案，其餘刪除
<pre><code>X:\autounattend.xml (如果有的話)
X:\sources\install.wim
X:\sources\$OEM$ (如果有的話)</code></pre>
2. 將壓縮檔內的檔案解壓到開機碟的根目錄

製作新的ISO檔
1. 將壓縮檔內的檔案解壓到自訂的目錄 (以 D:\iso 舉例)
2. 將以下ISO內的檔案複製到自訂的目錄中
<pre><code>autounattend.xml (如果有的話)
sources\install.wim
sources\$OEM$ (如果有的話)</code></pre>
3. 確認各檔案路徑是否正確
<pre><code>D:\iso\autounattend.xml (如果有的話)
D:\iso\sources\install.wim
D:\iso\sources\$OEM$ (如果有的話)</code></pre>
4. 利用DISM++或MSMG等工具建立ISO檔

![preview.png](/tutorial/iso.png)

### 注意事項：
- 盡量避免使用覆蓋檔案的方式替換檔案，除非你對ISO裡面的檔案架構非常了解
- 精簡版建議配合我製作的autounattend.xml一起使用，否則可能出現預期外的狀況

----

#### 繁體中文精簡版

下載：
- x86 (146MB) - [Github](https://github.com/WhatTheBlock/WindowsSimplify/releases/download/boot/boot_7_ct_x86_lite.7z)
- x64 (158MB) - [Google雲端](https://drive.google.com/uc?export=download&id=1vl2lbfc4pUr-IGTy_eAl_s_pn9FYujBt)、[Github](https://github.com/WhatTheBlock/WindowsSimplify/releases/download/boot/boot_7_ct_x64_lite.7z)

----

#### 繁體中文原版

下載：
- x86 (176MB) - [Github](https://github.com/WhatTheBlock/WindowsSimplify/releases/download/boot/boot_7_ct_x86.7z)
- x64 (192MB) - [Github](https://github.com/WhatTheBlock/WindowsSimplify/releases/download/boot/boot_7_ct_x64.7z)

----

#### 英文精簡版

下載：x64 (115MB) - [Google雲端](https://drive.google.com/uc?export=download&id=1RqqBaAFLkUafDu0psnqT2pOX7KT5x3Em)、[Github](https://github.com/WhatTheBlock/WindowsSimplify/releases/download/boot/boot_7_en_x64_lite.7z)

----

#### 英文原版

下載：none
