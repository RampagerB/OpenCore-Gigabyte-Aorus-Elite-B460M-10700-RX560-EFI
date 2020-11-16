### 相关信息 Info

- opencore version : 0.6.3
- update : 2020-11-16

### 主板设置 BIOS Settings

#### 启用 Enable

- Above 4G Encoding
- Erp

#### 禁用 Disable

- VT-d
- WakeOnLAN
- CSM
- Secure Boot
- CFG lock(if you can find it,but this is not necessary)

### 你需要设置 You need to...

- 如果你用的 CPU 跟我的型号不同，请使用 GenSMBIOS 重新生成机型信息，然后执行下一步。
- If your CPU is different one, use GenSMBIOS to regenerate Platform info then do next.
- 不管你的 CPU 是否跟我一致，都请更换你自己生成的新 MLB、SystemSerialNumber、SystemUUID。
- Please change MLB, SystemSerialNumber, SystemUUID for you own.(Config.plist -> PlatformInfo -> Generic).

### 其他情况 Other situations

- 如果你使用这款主板，但是显卡，网卡型号跟我不同，请查看以下教程进行相应配置。
- If your mainboard is same with me,but you have different GPU card or wireless network card,please read dortania tutorials below.
- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
