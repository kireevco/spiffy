spiffy
======

Build a [spiffs](https://github.com/pellepl/spiffs) file system binary for embedding/writing
onto the [Sming](https://github.com/anakod/Sming) ESP8266 spiffs file system.
This code forked to https://github.com/alonewolfx2/spiffy and changed for bigger fs and file sizes and stability.

### What is it
spiffy builds a binary spiffs image for you to write_flash to a esp8266 runing Sming so you can
get all the files onto your cool IoT device in one fell swoop.

### Usage
Basic usage is `spiffy 196608 webFiles` after build. 

#### Building spiffy
Clone the repo and build spiffy & build it

```bash
git clone https://github.com/xlfe/spiffy.git
cd spiffy
mkdir build
make
```

#### Create a folder with the webFiles you'd like to embed
```
mkdir webFiles
```

#### Run spiffy to build the rom

```bash
spiffy 196608 webFiles
```

Will result to:
```
Creating rom spiff_rom.bin of size 196608 bytes
Adding files in directory webFiles
Unable to read file .
Unable to read file ..
bootstrap.css.gz added to spiffs (15615 bytes)
index.html added to spiffs (12466 bytes)
jquery.js.gz added to spiffs (30153 bytes)
settings.html added to spiffs (4210 bytes)
style.css added to spiffs (7710 bytes)
wifi-sprites.png added to spiffs (1769 bytes)
```

#### Done!




