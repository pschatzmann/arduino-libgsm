
# GSM 06.10 13 kbit/s RPE/LTP speech compression 

The Communications and Operating Systems Research Group (KBS) at the
Technische Universitaet Berlin is currently working on a set of
UNIX-based tools for computer-mediated telecooperation that will be
made freely available.

As part of this effort we are publishing an implementation of the
European GSM 06.10 provisional standard for full-rate speech
transcoding, prI-ETS 300 036, which uses RPE/LTP (residual pulse
excitation/long term prediction) coding at 13 kbit/s.

GSM 06.10 compresses frames of 160 13-bit samples (8 kHz sampling
rate, i.e. a frame rate of 50 Hz) into 260 bits; for compatibility
with typical UNIX applications, our implementation turns frames of 160
16-bit linear samples into 33-byte frames (1650 Bytes/s).
The quality of the algorithm is good enough for reliable speaker
recognition; even music often survives transcoding in recognizable 
form (given the bandwidth limitations of 8 kHz sampling rate).

The interfaces offered are a front end modelled after compress(1), and
a library API.  Compression and decompression run faster than realtime
on most SPARCstations.  The implementation has been verified against the
ETSI standard test patterns.

## Installation Arduino 

You can download the library as zip and call include Library -> zip library. Or you can __git clone__ this project into the Arduino libraries folder e.g. with

```
cd  ~/Documents/Arduino/libraries
git clone pschatzmann/arduino-libgsm.git
```

The use of git is recommended because you can easily update to the latest version just by executing the ```git pull``` command in the project folder.

## Documentation

I recommend to use this library together with my [Arduino Audio Tools](https://github.com/pschatzmann/arduino-audio-tools). 
This is just one of many __codecs__ that I have collected so far: Further details can be found in the [Encoding and Decoding Wiki](https://github.com/pschatzmann/arduino-audio-tools/wiki/Encoding-and-Decoding-of-Audio) of the Audio Tools.


## Copyright

Jutta Degener (then jutta@cs.tu-berlin.de, nowadays jutta@pobox.com)
Carsten Bormann (then cabo@cs.tu-berlin.de, nowadays cabo@tzi.org)

Communications and Operating Systems Research Group, TU Berlin
Fax: +49.30.31425156, Phone: +49.30.31424315

Copyright 1992 by Jutta Degener and Carsten Bormann, Technische
Universitaet Berlin.  See the accompanying file "COPYRIGHT" for
details.  THERE IS ABSOLUTELY NO WARRANTY FOR THIS SOFTWARE.
