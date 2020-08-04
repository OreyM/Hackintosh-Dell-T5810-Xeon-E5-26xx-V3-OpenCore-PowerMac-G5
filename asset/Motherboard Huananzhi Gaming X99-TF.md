# Huananzhi Gaming X99-TF

Huananzhi X99-TF — материнская плата для сокета 2011 v3.

[img](_img/logo-1.jpg)

<table id="wpsm-table-159" class="wpsm-comptable center-table-align"><thead class="wpsm-thead wpsm-thead-blue"><tr><th>Модель</th><th>Huananzhi X99-TF</th></tr></thead><tbody class="wpsm-tbody"><tr><td class=""> Сокет</td><td class=""> LGA 2011-3</td></tr><tr><td class=""> Чипсет</td><td class=""> X99 \ C612</td></tr><tr><td class=""> Поддерживаемые процессоры</td><td class=""> Intel Core, Xeon 1600, 2600 (v3, v4)</td></tr><tr><td class=""> Поддерживаемая оперативная память</td><td class=""> 4 х DDR4 DIMM + 4 х DDR3 DIMM,  четырехканальная, поддержка ECC и non-ECC памяти<br> Максимальная частота для DDR4: 2400 Мгц<br> Максимальная частота для DDR3: 1866 Мгц</td></tr><tr><td class=""> Управление таймингами</td><td class=""> Есть</td></tr><tr><td class=""> Слоты расширения</td><td class=""> 3 x PCI-e x16 <br> 2 x PCI-e X1</td></tr><tr><td class=""> Дисковая подсистема</td><td class=""> 8 x SATA 3.0<br> 2 x M2 Nvme</td></tr><tr><td class=""> Разъемы для вентиляторов</td><td class=""> 1 x для процессорного кулера (4 pin)<br> 4 x для корпусных вентиляторов</td></tr><tr><td class=""> Порты</td><td class=""> 2 x PS/2<br> 4 x USB 3.0 (+ выносные на корпус)<br> 4 x USB 2.0 (+ выносные на корпус)<br> 1 x LAN <br> 7.1 audio (ALC892) <br> Spdf out <br> 1 x Wi-fi M2</td></tr><tr><td class=""> Форм-фактор и Размеры, мм</td><td class=""> ATX, 300 x 244 mm.</td></tr></tbody></table>

Список процессоров, работающих с DDR3: 
* Xeon E5-2678 v3
* Xeon E5-2696 v3
* Xeon E5-2629 v3
* Xeon E5-2649 v3
* Xeon E5-2669 v3
* Xeon E5-2672 v3
* Xeon E5-2673 v3

Дисковая подсистема состоит из целых 8 портов Sata 3.0 и 2 портов M2 Nvme, работающих на шине pci-e. Правда создание raid-массива возможно только с Sata, а не с M2-накопителями. 

Слот NVMe 1 работает на нормальной скорости x4, второй на скорости в 2 раза ниже

Дополнительно распаян еще один порт M2, предназначенный для установки модуля wi-fi.

### Совместимость с оперативной памятью

К сожалению, не вся оперативная память совместима с системами на китайском LGA2011-3. Так, судя по всему, не будут работать десктопные DDR4 модули, содержащие 8 банков (по мнению Aida64) памяти. Модули на 16 банков при этом работают исправно. Одноранговая или двухранговая память - значения, видимо, не имеет. Проблема в том, что определить такие модули на вид не получится, так как количество банков и количество чипов памяти могут не совпадать. Однако, известно, что точно не заработают модули с 4 чипами.

ECC REG память такой проблемы лишена и работает вся.  Еще один нюанс - в spd должна быть записана информация для работы на поддерживаемой процессором частоте, в большинстве случаев это 2133 или 1866 Мгц.

К памяти стандарта DDR3 у платы претензий гораздо меньше. Работают как обычные, так и серверные модули. Единственное условие — не смешивать десктоп и ECC REG планки.

Работают серверные модули с ёмкостью вплоть до 32 Гб. Максимальный объём — 128 Гб (32Гб x 4).

Модель HUANANZHI X99-F8 - все слоты только под память DDR4.

[Huananzhi Gaming X99-TF](https://aliexpress.ru/item/4000120773162.html?af=1926521&cv=27786001&cn=42q6w70nw408haaa77nsbj9t3gr9cogp&dp=v5_42q6w70nw408haaa77nsbj9t3gr9cogp&utm_source=epn&utm_medium=cpa&utm_campaign=1926521&utm_content=27786001&afref=&aff_platform=api&sk=qXefYqDE&aff_trace_key=3ca77137bcf5436e8d5c486e45f491ef-1583700359792-01268-qXefYqDE&terminal_id=55f41d8968f647b9bbcfe0d82c737669&aff_request_id=3ca77137bcf5436e8d5c486e45f491ef-1583700359792-01268-qXefYqDE)
[Huananzhi Gaming X99-TF](https://aliexpress.ru/item/4000221285759.html?af)
[HUANANZHI X99-F8](https://aliexpress.ru/item/4000419793962.html?spm=a2g0o.detail.1000060.1.72a06317KLCr6y&gps-id=pcDetailBottomMoreThisSeller&scm=1007.13339.146401.0&scm_id=1007.13339.146401.0&scm-url=1007.13339.146401.0&pvid=1e9459cf-88ce-43ae-ae62-4742004cbf79)

[Источник](https://xeon-e5450.ru/socket-2011-3/huananzhi-gaming-x99-tf/)