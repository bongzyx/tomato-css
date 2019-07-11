# freshtomato-css
Custom CSS for FreshTomato Firmware.

Another quick edit based of [theredhood13's custom css](https://github.com/theredhood13/tomato-css) & [mReXiTuS's custom css](https://github.com/mReXiTuS/tomato-design). 
Modified to my own liking.
Original credit still goes to theredhood13.

## Screenshots
Coming Soon

## Installation

### Using Scripts

#### 1. Add Custom Script
1. Navigate to __Administration__ > __Scripts__
2. Choose __WAN Up__
3. Paste the following code: 

```
sleep 60
logger start downloading
wget https://raw.githubusercontent.com/brandonongzy/freshtomato-css/master/custom.css -P /var/wwwext/
```

4. Save changes and reboot router. 

#### 2. Enable Custom CSS
1. Navigate to __Administration__ > __Admin Access__
2. Change color scheme to __custom.css__
4. You may need to erase your brower's cache or force a refresh (ctrl + Refesh) before the new UI appears.
5. Theme will be downloaded and applied 60 seconds after boot.
