# GPU

То, что нужно запомнить:
* macOS не поддерживает SLI, Crossfire или GPU с несколькими процессарами (например, Radeon Pro Duo). Это может измениться с выходом Radeon Pro Vega II Duo в Mac Pro
* Для получения звука через HDMI / DisplayPort может потребоваться дополнительная работа как с AppleALC.kext, так и с некоторыми другими изменениями IO-REG
* Разгон GPU ограничен графическими процессорами Vega 10 с PyVega

## Совместимость

### Официально поддердиваемые

Mojave и выше:

**ATI**

* Radeon RX 460
* Radeon RX 470
* Radeon RX 480
* Radeon RX 560
* Radeon RX 570
* Radeon RX 580
* Radeon RX 590
* Radeon Pro WX 2100
* Radeon Pro WX 3100
* Radeon Pro WX 4100
* Radeon Pro WX 5100
* Radeon Pro WX 7100
* Radeon RX Vega 56
* Radeon RX Vega 64
* Radeon RX Vega Frontier Edition
* Radeon Pro WX 9100

Единственная марка GPU, которую вам следует избегать в серии **Polaris**, - это **XFX**, поскольку у многих пользователей были проблемы с этими картами при просмотре загрузки Clover и MacOs, но другие пользователи нашли исправления / обходные пути. Это вызвано наличием нечетного VBIOS, который плохо взаимодействует с MacOs, единственным реальным решением является перепрошивка другого VBIOS, который не идеален.

**NVIDIA**

* GTX Titan (ядро GK 110 Maxwell)
* GTX Titan Black (ядро GK 110 Maxwell)
* GTX Titan Z (одна из немногих карт с двумя GPU, поддерживаемыми в MacOS)
* GTX 780 Ti
* GTX 780 
* GTX 770
* GTX 760 Ti
* GTX 760
* GT 740
* GT 730
* GT 720
* GT 710
* GTX Titan (ядро GK 110 Maxwell)
* GTX Titan Black (ядро GK 110 Maxwell)
* GTX Titan Z (одна из немногих карт с двумя графическими процессорами, поддерживаемая в MacOS, к сожалению, никогда не использовалась по-настоящему)
* GTX 690 (еще одна карта с двумя графическими процессорами, совместимая с MacOS)
* GTX 680
* GTX 670
* GTX 660 / TI (ДОЛЖЕН БЫТЬ РАБОТАЕТ с ядром GK 104, НЕ GK 106)
* GTX 660 (ДОЛЖЕН БЫТЬ РАБОТАЕТ с ядром GK 104, НЕ GK 106)
* GTX 650 (ДОЛЖЕН БЫТЬ РАБОТАЕТ с ядром GK 107, НЕ GK 106)
* GTX 645 (GT 645 - Fermi)
* GT 640 (издание Kepler, ядро ​​GK 107/208)
* GT 630 (издание Kepler, ядро ​​GK 208)

**Intel**

* HD 4200
* HD 4400
* HD 4600
* HD 5000
* HD 5100
* HD 5300
* HD 5500
* HD 5600
* HD 6000
* HD 6100
* HD 6200
* Iris Pro P6300
* HD 510
* HD 515
* HD 520
* HD 530
* HD P530
* Iris 540
* Iris 550
* Iris Pro 580
* Iris Pro P555
* Iris Pro P580
* HD 615
* HD 620
* HD 630
* Iris Plus 640
* Iris Plus 650
* UHD 610
* UHD 620
* UHD 630
* Iris Plus 655

Обратите внимание, что i3 8100 и 8350k используют другой UHD 630, чем остальные процессоры семейства.

### Работает, но требует вмешательства 

Mojave и выше:

**ATI**

* R7 240
* R7 250
* R9 260
* R7 260x
* R7 265
* R7 270
* R9 270X
* R9 280
* R9 280x
* R9 290
* R9 360
* R7 360x
* R7 370
* R9 370X
* R9 380
* R9 380x
* R9 390  (необходим FakeID)
* R9 Nano
* R9 Fury
* R9 Fury x

Вам нужно использовать **FakeID**, чтобы запустить не **Х** варианты.


### Неподдерживаемые карты

**ATI**

* RX 5700
* RX 5700 XT (будет работать только на MacOS Catalina 10.15.2+)

Максимальная поддерживаемая ОС High Sierra:

* GTX Titan X (ядро GP 102-400 Pascal)
* GTX Titan Xp (ядро GP 102-450 Pascal)
* GTX 1080 Ti
* GTX 1080 
* GTX 1070 Ti
* GTX 1070 
* GTX 1060
* GTX 1050 Ti
* GTX 1050
* GT 1030
* GTX Titan X (ядро GM 200 Maxwell)
* GTX 980 Ti
* GTX 980
* GTX 970
* GTX 960
* GTX 950
* GTX 750 Ti
* GTX 750
* GTX 745
* Intel HD 4000 (аппаратное ускорение не поддерживается)
* Intel HD 3000
* Intel HD 2000

Не заработает даже на High Sierra:

* Titan RTX
* RTX 2080 Ti
* RTX 2080 Super
* RTX 2080
* RTX 2070 Super
* RTX 2070
* RTX 2060 Super
* RTX 2060
* GTX 1660 Ti
* GTX 1660
* GTX 1650
* Intel HD 610

Графические процессоры Fermi (nVidia GTX 4xx, 5xx) Поддерживаемые наивысшие операционные системы: Sierra. При некоторых условиях можно запустить на Majave

# Some GPU Benchmark

| Model | 3D Vark | $ | Support |
|-------|-------|---|---------------------------|
| R7 260 | 2891  | 40-60  |  Custom |
| R9 270 X | 4698 | 40-60 | Custom |
| R9 280 |  5386 | 40-60  |  Custom |
| R9 280 X |  5850 | 40-60  |  Custom |
| R9 360 |  3320 | 40-60  |  Custom |
| R7 370 | 4639  | 40-60  | Custom  |
| R9 380 |  6170 |  60-70 |  Custom |
| R9 Fury | 9216  | 130-160  |  Custom |
| GT 740 |  1568 |  3040 |  Native |
| GTX 760 | 4939  | 50-60  | Native  |
| GTX 770 | 6062  |  70-80 |  Native |
| GTX 780 | 7956  | 110-120  |  Native |
| GTX 1050  | 4811  | 100-120  |  No Mojave |
| GTX 1050 Ti | 6078  | 110-130  |  No Mojave |
| RX 460 |  4332 | 60-70  | Native  |
| RX 470 | 7825  | 70-80  |  Native |
| RX 480 |  8156 | 80-90  |  Native |
| RX 560 | 4284  |  50-80 |  Native |
| RX 570 | 6969	  |  80-100 |  Native |
| RX 580 |  8610 |  130-150 |  Native |
| RX 590 | 9459  |  150-170 | Native  |
| Radeon RX Vega 56 | 11915 | 220-240 | Native |
| Radeon RX Vega 64 | 11455 | 240-260 | Native |
| GTX 1650 | 7928 | 150-170 | No |
| RTX 2060 | 12802 | 400 | No |


## Самые рекомендованные к покупке

Так вы просто хотите получить рекомендацию по GPU? Честно говоря, в текущей ситуации единственные карты, которые мы бы порекомендовали, будут от AMD, которые либо Polaris (Rx 4xx, 5xx), либо новее, поскольку GCN 3 и старше могут потерять поддержку в любое время, и то же самое относится и к Kepler. Вот карты, которые мы рекомендуем и помним, что эталонные карты, как правило, являются наиболее безопасным решением ** (ИЗБЕГАЙТЕ XFX ВСЕХ СТОИМОСТЬЮ) **:

* Rx 460/560
* Rx 470/570
* Rx 480/580
* Rx 590
* Rx Vega 56
* Rx Vega 64
* Rx Vega VII

### Карты по производителям

* Asus GTX 650
* Gyabyte RX 460 4GB
* Sapphire RX 550 Pulse 4GB
* Sapphire RX 560 Pulse
* Gyabyte RX 560 14CU
* Gyabyte RX 560 Gaming 16CU
* MSI RX 560 Aero
* MSI RX 560 ITX
* Asus ROG Strix RX570 (4gb)
* Sapphire RX 570 Nitro+ 4GB (c 8GB надо пилить)
* Gyabyte RX 570 Gaming
* Gyabyte RX 570 AORUS
* MSI RX 570 ARMOR
* Sapphire RX 580 Pulse
* Sapphire RX 580 Pulse 11265-05-20G 8GB 256-Bit GDDR5
* Sapphire RX 580 Nitro+ 4GB
* Sapphire RX 580 Nitro+ 8GB
* MSI RX 580 ARMOR
* Gyabyte RX 580 AORUS
* 

Гайды:

* [Гид покупателя Mojave GPU (eng)](https://www.reddit.com/r/hackintosh/comments/b91vf5/mojave_gpu_buyers_guide/)
* [Мега таблица по бенчмаркам GPU](https://www.videocardbenchmark.net/GPU_mega_page.html)
* [Сравнение видеокарт]()