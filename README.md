ロボシスの課題１
１４２６０５２佐藤諒我

LEDが点滅する
```
$ git-clone https://github.com/ryuichiueda/raspberry_pi_kernel_build_scripts.git

$ cd raspberry_pi_kernel_build_scripts

$ sudo ./kernel_build_and_install_for_pi2_pi3.bash

$ sudo reboot
```
この後リポジトリをクローンし、以下のようにコマンドを入力する  
```
$ cd RaspberryPi_LEDbrink

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

$ echo 1 > /dev/myled0  

$ sudo rmmod myled
```

https://github.com/kato-masahiro/RaspberryPi_LEDbrink

のものを一部カスタマイズした
