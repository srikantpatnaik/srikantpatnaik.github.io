---
layout: post
title: Chrome from a custom directory
---

If you have limited space in your system directory, and you still need to install 
Chrome, this might help you. Please note, this method may not work for all the deb
packages. 

Assuming you have a seperate partition for `/var` which has free space for the Chrome installation. 

```bash 
cd /var
sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo mkdir /var/chrome && sudo chown -R $USER.$USER /var/chrome
dpkg-deb -x google-chrome-stable_current_amd64.deb chrome/
```

That being done, you can simply open the `chrome` from the command line
```bash
/var/chrome/opt/google/chrome/chrome
```
That's it.