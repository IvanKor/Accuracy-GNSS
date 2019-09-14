# Accuracy-GNSS
Експериментальное исследование точности GNSS в зависимости от коррекции и внешних условий

Использовалась [quadrifilar backfire helix](http://lea.hamradio.si/~s53mv/navsats/n16.gif)  антенна, NEO-M8T и [RTKLIB](http://www.rtklib.com) в режиме Solution: SINGLE, т.е. обычный GNSS приемник. Наличие source RTKLIB  позволяет производить любые эксперименты с "сырыми" данными GNSS. С общей антенны NEO-M8T в одно и то же время выдает независимые данные от 3-х GNSS систем:
### GPS  GLONASS GALILEO
Подключив выход передатчика [Real-time GPS signal simulator](https://github.com/IvanKor/hrfGPS) через аттенюатор на антенный вход NEO-M8T
на 1.5 часа и включив все коррекции убеждаемся что за это время суммарная погрешность (RMS) ~ 0.1 метра.
![](https://raw.githubusercontent.com/IvanKor/hrfGPS/master/outpu5_2_mhz2.jpg)

Запись "сырых данных" (RAWX) на открытой местности неподвижно в течении 1ч 50 мин с частотой 5Hz  находится в файле quadrifilar_backfire_helix_antenna.zip (4 части).

В условиях когда возможны переотражения, например, городские улицы, ошибка может быть и 300 метров и более.
![](./gps_300m.jpg)
![](./gps_all_ok.jpg)
![](./gal_all_ok.jpg)
![](./beyd_all_ok.jpg)
![](./glo_no_chl_corr.jpg)
![](./glo_all_ok.jpg)
![](./gps_iono_off.jpg)
![](./gal_iono_off.jpg)
![](./glo_iono_off.jpg)
![](./gal_tropo_off.jpg)
![](./gps_tropo_off.jpg)
![](./glo_tropo_off.jpg)
![](./glo_sun_moon_correction_off.jpg)
![](./gps_relativity_correction_off.jpg)
![](./gal_relativity_correction_off.jpg)
![](./glo_relativity_correction_off.jpg)

