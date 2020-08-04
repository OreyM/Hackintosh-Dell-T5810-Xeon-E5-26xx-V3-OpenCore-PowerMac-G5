# Загрузчики Clover

## Huanan LGA2011 + Xeon E5-2680 v2 macOS Catalina

**Сборка 6 февраля 2020 года.**

Загрузчик операционной системы macOS Catalina для материнских плат Huanan и Runing на сокете LGA2011 с процессорами Intel Xeon E5-26xx и E5-16xx и графикой AMD RX.

В архиве вместе с EFI загрузчиком Clover версии 5103 находятся все необходимые кексты и патчи. Кекст сетевой карты заменен на RealtekRTL8111.kext и теперь сеть не отваливается при высоких скоростях upload.

Конфигурация работает на следующей конфигурации:

* процессор Intel Xeon E5-2680 v2
* материнская плата Huanan 2.49b
* видеокарта Saphire AMD RX 580 8 ГБ
* NVMe SSD Transcened 25 ГБ.

Протестировано на материнских платах Huanan 2.49 и Runing X79 LGA 2011.

ACPI пропатчен для корректной работы TurboBoost всех ядер процессора Intel Xeon E5-2680 v2.

ACPI SSD пропатчен для того, чтобы NVMe SSD система считала не съемным диском. Корректно распознается NVMe SSD в M.2 разъеме материнской платы и NVMe SSD во втором разъеме PCI-e 16x.

Помните, что для создания загрузочной флешки с операционной системой macOS Catalina теперь понадобится накопитель объемом 16 ГБайт или более. Не загружайте образы флешек с торрентов — многие из них работают некорректно. Используйте только чистую установку образа системы с последующим копированием загрузчика на EFI-раздел записанной флешки.

[Data](_arhive/Clover-huanan-catalina-february-2020.zip)
[Source](https://andrew-lazarev.com/sdm_downloads/clover-bootloader-huanan-lga2011-xeon-e5-2680-v2-macos-catalina/)


## Clover для Huanan LGA2011 + Xeon E5-2680 v2 и macOS Mojave

**Сборка 6 апреля 2019 года**

В загрузчик включены все необходимые кексты (в том числе кекст файловой системы APFS) и работают все устройства. Возможна загрузка с PCIe NVMe SSD. Lilu.kext и Evergreen.kext обновлены до последней версии.

Протестировано на материнских платах Huanan 2.49 и Runing X79 LGA 2011.

ACPI пропатчен для корректной работы TurboBoost всех ядер процессора Intel Xeon E5-2680 v2.

Если у Вас графический адаптер от NVidia и проблемы с разверткой монитора, попробуйте в секции Options -> SMBIOS прописать Board-ID = Mac-F221BEC8.

[Data](_arhive/Clover-huanan-mojave-april-2019.zip)
[Source](https://andrew-lazarev.com/sdm_downloads/clover-bootloader-huanan-lga2011-xeon-e5-macos-mojave/)


## Clover SZMZ X99-8D3 + Xeon E5-2678 v3

**Сборка 2019-11-13**

* CPU: Intel Xeon E5-2678 v3 (12 core, 2.5 GHz / 3.3 GHz Boost)
* Motherboard: SZMZ X99-8D3
* RAM: 16GB DDR3-14900R 1866Mhz ECC RDIMM modules
* GPU: Radeon RX Vega 64 8GB
* Storage: Phison E12 m.2 NVMe PCI-E 3.0 x4 SSD
* Water blocks: BARROW CPU + GPU
* Radiator: 360mm x 25mm slim
* Pump: DDC

#### BIOS

Reset to Defaults
 
#### Clover
 
Install Clover_v2.5k_r5066 (tested).
 
If you try a newer version, post your experience.
 
 
#### UEFI

* ApfsDriverLoader.efi
* HFSPlus.efi
* AptioMemoryFix.efi
* SMCHelper.efi
* AudioDxe.efi
 
#### Kexts

* Lilu
* WhateverGreen
* FakeSMC
* AppleALC
* RealtekRTL8111-V2.2.2
* USBInjectAll
 

 
#### config.plist
 
**ACPI > DSDT > Patches > "change AZAL to HDEF"**

```
Boot > Arguments =
        Debug: -v dart=0 npci=0x2000 keepsyms=1 debug=0x100
        Production: dart=0 npci=0x2000
CPU > Type = 0x0A01
```

**KernelAndKextPatches > KernelToPatch**

```
xcpm_pkg_scope_msrs © Pike R. Alpha

find <31d2e8b4 fcffff>

replace <31d29090 909090>
```
 
```
_xcpm_ performance_patch © Pike R. Alpha

find <c1e30848 63d389d0 48c1ea20>

replace <c1e308b8 00ff0000 31d29090>
```
 
```
_xcpm_SMT_scope_msrs 1 © Pike R. Alpha

find <be0b0000 005de908 000000>

replace <be0b0000 005dc390 909090>
```

```
_xcpm_SMT_scope_msrs 2 © Pike R. Alpha

find: <31d2e87e fcffff>

replace: <31d29090 909090>
```
 

**KernelAndKextPatches > KextsToPatch**

 
```
IOPCIFamilyPatch ©PMHeart

find: <483d0000 0040>

InfoPlistPatch: NO

name: IOPCIFamily

replace: <483d0000 0080>
```
 
```
RtVariables

BooterConfig: 0x28

CsrActiveConfig: 0x67

ROM: UseMacAddr0
```
 
```
************************** [ IMPORTANT ] **************************

 

Must specify:  SMBIOS > Memory > Modules

 

Otherwise, system will not boot past / get stuck at / freeze at :

 

End RandomSeed

+++++++++++++++++++++++++++++++++

 

******************************************************************

 

 

Set SMBIOS for iMacPro1,1

```

[Data](_arhive/X99-8D3-Clover-master.zip)
[Source](https://www.insanelymac.com/forum/topic/340396-guide-x99-xeon-v3-haswell-ep-mojave-1014x-2019/)
[GitHub](https://github.com/xe97/X99-8D3-Clover)




Другие инструкции:

* [EFI Folder for mATX X79 8-Core Xeon macOS High Catalina Hackintosh](https://github.com/mighildotcom/X79-Hackintosh-Catalina)
* [12-core X99 Hackintosh Pro build](https://www.tonymacx86.com/threads/12-core-x99-hackintosh-pro-build.170818/)