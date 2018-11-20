# edxis_chromebook_ubuntu_setup
Guide to set up ubuntu only (no chromeOS) on Edxis laptop

1. Adjust trackpad sensitivity

```
cd
touch .xsessionrc
echo 'xinput set-prop "Elan Touchpad" "Synaptics Finger" 5 10 50' > .xsessionrc
source .xsessionrc
```

2. Enable audio

```
pgrep alsa
sudo cp ~/Downloads/asound.state /var/lib/alsa/asound.state
sudo alsa force-reload
alsactl init
sudo alsactl store --file /var/lib/alsa/asound.state
sudo alsa force-reload
```
