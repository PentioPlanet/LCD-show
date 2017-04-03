LCD driver for the Raspberry PI Installation
====================================================

Update:
  v1.2-20170302
  Add xserver-xorg-input-evdev_1%3a2.10.3-1_armhf.deb to support Raspbian-2017-03-02
Update:
  v1.1-20160815
  
1.Instalar Raspbian desde el repositorio oficial.
  https://www.raspberrypi.org/downloads/
  Use“SDFormatter.exe”to Format your TF Card
  Use“Win32DiskImager.exe” Burning mirror to TF Card
     
2)Clone my repo onto your pi<br>
```git clone https://github.com/pentioplanet/LCD-show.git```<br>
```chmod -R 755 LCD-show```<br>
```cd LCD-show/```<br>
  
3)According to your LCD's type, excute:
<br>
In case of 2.8" LCD<br>
  ```sudo ./LCD28-show```<br><br>
In case of 3.2" LCD<br>
  ```sudo ./LCD32-show```<br><br>
In case of 3.5" LCD<br>
  ```sudo ./LCD35-show```<br><br>
In case of 3.97" LCD<br>
  ```sudo ./LCD397-show```<br><br>
In case of 4.3" LCD<br>
  ```sudo ./LCD43-show```<br><br>
In case of 5" LCD<br>
  ```sudo ./LCD5-show```<br><br>
In case of 7inch(B)-800X480 RPI LCD<br>
  ```sudo ./LCD7B-show```<br><br>
In case of 7inch(C)-1024X600 RPI LCD<br>
  ```sudo ./LCD7C-show```<br><br>
If you need to switch back to the traditional HDMI display<br>
  ```sudo ./LCD-hdmi```<br><br>

Aguarde unos momentos, el sistema se reiniciará automáticamente.<br><br>

  NOTA:<br>
  ===========================================================================================
  En caso de estar usando la última versión de Raspbian (al momento de realizar este tutorial
  es la fechada el 2017-03-03) necesitarás ejecutar dos comandos adicionales luego de haber 
  realizado los pasos detallados en los apartados 1), 2) y 3) para que tu touchscreen
  funcione correctamente.<br><br>
  
sudo apt-get install xserver-xorg-input-evdev<br>
sudo cp -rf /usr/share/X11/xorg.conf.d/10-evdev.conf /usr/share/X11/xorg.conf.d/45-evdev.conf<br>
sudo reboot<br>
