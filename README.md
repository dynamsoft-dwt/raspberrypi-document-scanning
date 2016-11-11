# Scanner Sidecar Solution with Raspberry Pi

The sample shows how to write a simple HTML page to use the remote document scanning service that deployed on Raspberry Pi. 

## Download 
* [Dynamic Web TWAIN for Raspberry Pi][1].

## How to Install and Uninstall the Scanning Service
* Install:

    ```
    sudo dpkg -i dynamic_web_twain-arm-trial.deb
    ```

* Uninstall: 

    ```
    sudo dpkg -r dynamsoft-webtwain-service
    ```

## How to Run the Sample
1. Set the IP address of Raspberry Pi:

    ```JavaScript
    var remoteIP = "192.168.8.51";
    ```
2. Disable the property **AutoLoad**:

    ```JavaScript
    Dynamsoft.WebTwainEnv.AutoLoad = false;
    ```
3. Set the product key:

    ```JavaScript
    Dynamsoft.WebTwainEnv.ProductKey = "";
    ```
   You can now use the trial license.
4. Create Dynamic Web TWAIN object:

    ```JavaScript
    Dynamsoft.WebTwainEnv.CreateDWTObject('dwtObjectContainer', remoteIP, HTTP_PORT, HTTPS_PORT, function(obj) {}, function(e){});
    ```
5. Open **index.html** in HTML5 supported web browsers: Chrome, Firefox, Opera, Edge, Safari and so on.

## Video
https://www.youtube.com/watch?v=v6cImg95u0c

## Contact
To get more detailed information, please contact support@dynamsoft.com.

[1]:http://labs.dynamsoft.com/dwt-for-raspberry-pi.htm