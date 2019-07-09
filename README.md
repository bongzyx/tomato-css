# freshtomato-css
Custom CSS for FreshTomato Firmware.

A quick edit of [mReXiTuS's custom css](https://github.com/mReXiTuS/tomato-design). 
Modified to a condensed dark/light theme for use with Fresh Tomato.

## Screenshots
Dark Theme
![Screenshot](https://raw.githubusercontent.com/theredhood13/tomato-css-dark/master/Screenshot.png)
Light Theme
![Screenshot](https://raw.githubusercontent.com/theredhood13/tomato-css-dark/master/Screenshot_light.png)

## Installation

### Using init script

#### 1. Upload script
1. Navigate to __Administration__ > __Scripts__
2. Choose __WAN Up__
3. Paste the contents of [tomato_wanup_dark](https://github.com/theredhood13/tomato-css/blob/master/tomato_wanup_dark) or [tomato_wanup_light](https://github.com/theredhood13/tomato-css/blob/master/tomato_wanup_light)
4. Save changes

#### 2. Enable Custom CSS
1. Navigate to __Administration__ > __Admin Access__
2. Change color scheme to __custom.css__
3. Save changes and reboot router
4. You may need to erase your brower's cache before the new UI appears.

#### 3. Custom Script
1. Navigate to __Administration__ > __Scripts__
2. Choose __WAN Up__
3. Paste the following code: 

```
sleep 60
logger start downloading
wget https://raw.githubusercontent.com/theredhood13/tomato-css/master/release/light/custom.css -P /var/wwwext/
```

4. Save changes and reboot router. 
5. You may need to erase your brower's cache before the new UI appears.
6. Theme will be downloaded and applied 60 seconds after boot.


### Using SSH

#### 1. Upload Custom CSS over SSH
1. Enable SSH deamon in __Administration__ > __Admin Access__
2. Connect to router over SSH
3. Create folder __wwwext__ in __/var/__
4. Upload custom.css file into __/var/wwwext/__

#### 2. Enable Custom CSS
1. Navigate to __Administration__ > __Admin Access__
2. Change color scheme to __custom.css__
3. Save changes and reboot router
4. You may need to erase your brower's cache before the new UI appears.

_After every reboot, this needs to be performed again. Router will automatically remove custom.css file after reboot_
