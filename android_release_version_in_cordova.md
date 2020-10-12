# How to build release version of app in cordova using android studio

1. First need to generate signing key using the following command:

```cmd
keytool -genkey -v -keystore YOUR_KEY_STORE_NAME -alias YOUR_ALIAS_NAME -storepass PASSWORD -keypass PASSWORD -keyalg RSA -validity 36650
```
Here,
YOUR_KEY_STORE_NAME = anything you want
YOUR_ALIAS_NAME = anything you want 
PASSWORD = anything you want

after running this command you will get some promt and answer them then you will get a certificate file name as YOUR_KEY_STORENAME.cert

2. Then keep this certificate file anywhere you want and run the following command:

```cmd
cordova platform add android
```

3. Then, you will get a folder named platforms and under this folder you will get android folder. Into anroid folder root you have too create a file named :

### release-signing.properties

inti this file you need to insert the following settings:

```cmd
storeFile=YOUR_CERT_FILE_LOCATION
storeType=jks
keyAlias=YOUR_ALIAS
keyPassword=YOUR_KEY_PASSWORD
storePassword=YOUR_STORE_PASSWORD
```

4. Finally, run the following command to build a release version of app

```cmd
cordova build android --release
```
