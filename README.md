Camera
======
A camera that uses PiFace Control and Display and Raspicam.

Images are stored at `/home/pi/snap-camera/images/`.

Overlays are stored at `/home/pi/snap-camera/overlays/`.

Videos are stored at `/home/pi/snap-camera/videos/`.

Documentation
=============
Documentation can be found at: [http://piface.github.io/snap-camera/](http://piface.github.io/snap-camera/)

Install
=======
Enable the camera with:

    raspi-config

Enable HDMI to start even when unplugged by uncommenting:

    hdmi_force_hotplug=1

in `/boot/config.txt`.

Download the latest debian package and install with:

    sudo dpkg -i python3-snap-camera_0.0.0-1_all.deb

Start/stop the camera service with:

    sudo service snap-camera start
    sudo service snap-camera stop

Enable the service at boot:

    sudo update-rc.d snap-camera defaults

The camera should start up on boot.

Development
===========

Todo:

- Change to use `PiCamera <https://github.com/waveform80/picamera>`_ rather
  than just calling Raspistill.
- Timelapse mode should create a video after taking all of the images.
- Cancel current operation.