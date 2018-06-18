# A2DPSourcePiZeroW
How to connect a A2DP Sink to a Raspberry PI

sudo apt-get install alsa-utils bluez bluez-tools pulseaudio-module-bluetooth # I hope thats it, cannot remember completely!

pulseaudio -D # to start a pulseaudio daemon
bluetoothctl # to start the bluetooth control then
pair xx:xx:xx:xx:.. #to pair your bluetooth device
connect xx:xx:xx:xx:.. # to connect your bluetooth device
pacmd list-sinks # to have a look at all the sinks, this should now include the bluetooth device
pacmd set-default-sink 1 # to set the newest member of the club as the default
pacmd set-sink-volume 1 0x30000 # to set the volume to the sink

#if you use kodi enable the passthrough in the audio settings. Enjoy!
