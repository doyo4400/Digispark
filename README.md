# Tutorial dispark 2k23

## Made with
usb : Digispark Attiny 85
software : arduino

## Step-by-step

Install arduino

````md
tar -xJf arduino-X.X.X-linux64.tar.xz
mv arduino-X.X.X /usr/share
cd /usr/share/arduino-X.X.X
./install.sh
````


Add http://digistump.com/package_digistump_index.json on management packer

Install additional package "digistump"

Swipe to digistump mode (tools > car type > Digispark (Default 16.5 Mhz))

Gif explain : https://digistump.com/wiki/digispark/tutorials/connecting


## Configure attack

Cf. attack.duck

Paste on this site : https://payloadstudio.hak5.org/community/

(Don't forget to select the language of keyboard you attack), generate payload and download the file (inject.bin)

Download https://github.com/mame82/duck2spark
On the folder of duck2spark, put the inject.bin
Run : 
````md
python2 duck2spark.py -i inject.bin -l 1 -f 2000 -o Payload.bin
````

Run arduino as root, paste content of payload.bin
televerse the arduino projet BEFORE insert USB (if you have error, try with usb-hub)
