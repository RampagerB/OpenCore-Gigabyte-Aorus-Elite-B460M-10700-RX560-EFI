### 相关信息 Info

- opencore version : 0.9.5
- latest update : 2023-10-25
- wireless card : BCM94360CD
- CPU : Intel 10700
- GPU : AMD RX560
- Motherboard : Gigabyte B460M Auros Elite

### 已知问题 Known issues

- 机箱后面 TypeC 接口无法工作
- Type C Back USB port not working

### 更新 Updates

- 2023-10-25

  - 升级到 OpenCorePkg 0.9.5
  - Update to OpenCorePkg version 0.9.5
  - 修复了 GPU 硬件加速和 DRM 视频播放问题
  - fix gpu codec & DRM video issue

- 2023-08-09

  - 升级到 OpenCorePkg 0.9.4
  - Update to OpenCorePkg version 0.9.4
  - 升级 kext 到最新版本
  - update kexts to latest version

- 2023-03-21

  - 升级到 OpenCorePkg 0.9.0
  - Update to OpenCorePkg version 0.9.0

- 2022-10-25
  - 适配 macOS Ventura 13.0
  - Able to update to macOS Ventura
  - 升级 kext 到最新版本
  - update kexts to latest version
  - 升级到 OpenCorePkg 0.8.5
  - Update to OpenCorePkg version 0.8.5
  -
- 2022-09-26
  - 升级到 OpenCorePkg 0.8.3
  - Update to OpenCorePkg version 0.8.3
- 2022-03-11
  - 升级到 OpenCorePkg 0.7.9
  - Update to OpenCorePkg version 0.7.9
- 2022-02-09
  - 升级到 OpenCorePkg 0.7.8
  - Update to OpenCorePkg version 0.7.8
- 2022-01-12
  - 升级到 OpenCorePkg 0.7.7
  - Update to OpenCorePkg version 0.7.7
- 2021-12-09
  - 升级到 OpenCorePkg 0.7.6
  - Update to OpenCorePkg version 0.7.6
- 2021-12-03
  - 修复 usb3.0 接口失效问题，手动进行了 USBMapping
  - fix USB3.0 ports not working issue, and did USBMapping[explain this](https://dortania.github.io/OpenCore-Post-Install/usb/)
- 2021-11-03
  - 升级到 OpenCorePkg 0.7.5，测试可以升级到 macOS Monterey
  - Update to OpenCorePkg version 0.7.5, and update to macOS Monterey test success.
- 2021-09-18
  - 昨天的版本不稳定，升级 Lilu 到最新版本后暂时没问题，请升级 EFI 前备份好之前的 EFI 文件
  - last version is not stable, update Lilu.kext to latest version resolved it , temporarily.please backup your previous EFI folder before every update.
- 2021-09-17
  - 升级 OpencorePkg 到 0.7.3,升级 kexts
  - Updated OpencorePkg to version 0.7.3 and updated some kexts
- 2021-08-13
  - update kexts to latest version
  - 升级 kext 到最新版本
  - Fix some DRM issues[DeviceProperties->Add->PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)->shikigva 80][explain this](https://dortania.github.io/OpenCore-Post-Install/universal/drm.html#fixing-drm)
  - 修复一些 DRM 视频播放的问题[参数解释](https://dortania.github.io/OpenCore-Post-Install/universal/drm.html#fixing-drm)
- 2021-08-12
  - 修改 SIP 参数以修复检测不到系统更新的问题[NVRAM->Add->7c...->csr-active-config from 'FF0F0000' to 'EF0F0000']
  - modify SIP config to fix System update
- 2021-08-09
  - 升级 OC 版本到 0.7.2
  - Opencore updated to version 0.7.2
  - ~~不要升级 WhateverGreen 到最新版本(1.5.2),会导致启动黑屏~~
  - ~~please don't update WhateverGreen to latest version(1.5.2),will cause boot fail~~
- 2021-06-09
  - 升级 OC 版本到 0.7.0
  - Opencore updated to version 0.7.0
- 2021-05-19
  - 美化开机界面
  - Boot UI beautify
- 2021-05-18
  - 升级 OC 版本到 0.6.9
  - Opencore updated to version 0.6.9
  - 请暂时不要尝试使用 opencore configurator 更新 kext，因为我试了，会无法启动, 问题出在 WhateverGreen、VirtualSMC、HibernationFixup 之中
  - Don't update kext by using opencore configurator,because when I did,boot failed. One of these cause problem:WhateverGreen、VirtualSMC、HibernationFixup
- 2021-04-07
  - 升级 OC 版本到 0.6.8
  - Opencore updated to version 0.6.8
  - 升级了 kexts
  - Update kexts
- 2021-02-23
  - 升级 OC 版本到 0.6.6
  - Opencore updated to version 0.6.6
  - 禁用 EFI 启动日志生成文件
  - Disable EFI log file generation
  - 添加了一些 kext
  - Add some kexts

![image](https://github.com/RampagerB/OpenCore-Gigabyte-Aorus-Elite-B460M-10700-RX560-EFI/raw/main/images/1.png)

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
