---
layout: post
title: Kivy on the Raspberry Pi
---

![](https://github.com/ElectronicsGeek/electronicsgeek.github.io/blob/master/public/images/kivypi.png?raw=true)

## What is Kivy?

[Kivy](https://kivy.org/#home) is an amazing, cross-platform user interface toolkit for python. It enables you to create sleek, stylish, modern and mobile-friendly interfaces like these shown below.

![](https://upload.wikimedia.org/wikipedia/en/0/0d/Kivy_showcase_screenshot.jpg)

## Using it with Raspberry Pi:

Amongst Windows, Mac, Linux, Android and iOS, Kivy is able to run well on a Raspberry Pi. I have been interested in getting it to work on the Pi since the release of the [offical Raspberry Pi touchscreen](https://shop.pimoroni.com/products/raspberry-pi-7-touchscreen-display-with-frame) a few months ago.

![](https://cdn.shopify.com/s/files/1/0174/1800/products/Touchscreen_group_1200_1024x1024.jpg?v=1441705859)

Whilst kivy works well on the Pi, installation is far less straightforward; requiring the manual entry and installation of dependencies. This prompted me to write a [useful script](https://github.com/ElectronicsGeek/Kivy-Raspberry-Pi-Installer) that automates the entire process (based upon the [documentation by Kivy](https://kivy.org/docs/installation/installation-rpi.html) and [Matt Richardson of the Raspberry Pi Foundation](https://github.com/mrichardson23/rpi-kivy-screen)).

## Installing Kivy

As mentioned earlier, with the script, installing Kivy is easy. It will however take some time to run, as many dependencies need to be satisfied, so I'd reccomend making a drink and finding something else to do whilst the script runs :)

First of all, you'll need to clone the repository on GitHub:

    git clone "https://github.com/ElectronicsGeek/Kivy-Raspberry-Pi-Installer"

After that, you'll want to use `chmod` so that you can execute the script. Simply type:

    chmod +x install_kivy_rpi
    
Following this, run the script using sudo:

    sudo ./install_kivy_rpi
    
Then, be paitent!

#### **OPTIONAL:** Setting up the Offical Touchscreen

If you intend to use Kivy with the official Pi touchscreen, you may wish to follow these steps.

Open the kivy configuration file with `nano` or other text editor of choice:

    nano ~/.kivy/config.ini
    
And enter the following in the `[input]` section

    mouse = mouse
    mtdev_%(name)s = probesysfs,provider=mtdev
    hid_%(name)s = probesysfs,provider=hidinput

## What's next?

In the next article, I'll go through how to get started with Kivy! Stay tuned!

In the meantime, you may want to check out Alexander Taylor's excellent [Kivy Crash Course video series on youtube](https://www.youtube.com/watch?v=F7UKmK9eQLY&list=PLdNh1e1kmiPP4YApJm8ENK2yMlwF1_edq)

##### Image Credits:

Official Pi Touchscreen - [Pimoroni](https://shop.pimoroni.com/)
