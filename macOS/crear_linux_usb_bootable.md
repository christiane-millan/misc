# Cómo crear un USB bootable en macOS

1. Tener la .iso de Linux 
2. Ir a terminal
3. Convertir la ISO a DMG

```terminal
hdiutil convert -format UDRW -o ~/ruta/al/archivo.img ~/path/to/ubuntu.iso
```

4. Identificar la USB a utilizar con

```terminal
diskutil list
```

5. Desmontar el USB

```terminal
diskutil unmountDisk /dev/diskN
```

7. Cargar el DMG a la USB

```terminal
sudo dd if=/ruta/al/archivo.img of=/dev/diskN bs=1m
```

8. Se retira la unidad USB


```terminal
diskutil eject /dev/diskN
```
