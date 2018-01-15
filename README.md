ロボシスの課題１

1426052 佐藤諒我

LEDが点灯・消灯・点灯を繰り返す
```
$ git-clone https://github.com/ryuichiueda/raspberry_pi_kernel_build_scripts.git

$ cd raspberry_pi_kernel_build_scripts

$ sudo ./kernel_build_and_install_for_pi2_pi3.bash

$ sudo reboot
```
reboot後、このリポジトリをクローンし、以下のようにコマンドを入力する  
```
$ cd RaspberryPi_LEDbrink

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

$ echo 1 > /dev/myled0  

$ sudo rmmod myled
```

https://github.com/kato-masahiro/RaspberryPi_LEDbrink

から許可を得て点灯・消灯時間が早くなるよう一部カスタマイズした
