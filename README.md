Mein debian grub2 theme, welches das breeze theme um einige Punkte ergänzt
1. ein icon für memtest
2. icons für reboot und shutdown
3. ein eigenes bokeh Hintergrundbild
4. ein größeres Menü, sodaß alle relevanten Einträge sichtbar sind.

Unter files ist das Theme für /boot/grub/themes/
die Datei default.grub enthält die Ergänzugen für die Datei /etc/default/grub

Damit memtest ein Icon bekommt, muss die Datei /etc/grub.d/20_memtest86+ in der Zeile mit dem menuentry ein »--class memtest« ergänzt bekommen:  
```
menuentry "Memory test (memtest86+)" --class memtest {
```
Die Einträge für reboot und shutdown kommen aus der Datei 40_custom,
die nach /etc/grub.d zu kopieren ist.

update-grub aktiviert danach das neue Theme und die Booteinträge - siehe screenshot.png

Der background wurde mit dem bokeh tool hergestellt: https://codepen.io/ajm13/full/Bvczj

## everybody loves screenshots:
![screenshot](./screenshot.png)
