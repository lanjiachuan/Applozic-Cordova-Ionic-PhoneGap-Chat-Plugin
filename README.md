# Applozic Cordova PhoneGap Chat Plugin

Applozic powers real time messaging across any device, any platform & anywhere in the world. Integrate our simple SDK to engage your users with image, file, location sharing and audio/video conversations.

Signup at https://www.applozic.com/signup.html to get the application key.



## Using
    
Install the plugin

    $ cd hello
    $ cordova plugin add https://github.com/AppLozic/Applozic-Cordova-PhoneGap-Chat-Plugin.git
    

Edit `www/js/index.js` and add the following code inside `onDeviceReady`


#### Login/Register User
```js
    var alUser = {
            'userId' : $("#userId").val(),
            'password' : $("#password").val(),
            'authenticationTypeId' : 1,
            'applicationId' : 'applozic-sample-app'
        };

   applozic.login(alUser, function() {
        		applozic.launchChat(function() {}, failure);
        	}, failure);
```

#### Launch Chat


##### Main Chat screen

```
applozic.launchChat(function() {console.log("success");}, function () {console.log("error");});
```

##### Launch Chat with a specific User

```
applozic.launchChatWithUserId(userId, function() {console.log("success");}, function () {console.log("error");});
```

##### Launch Chat with specific Group 

```
applozic.launchChatWithGroupId(groupId, function() {console.log("success");}, function () {console.log("error");});
```


#### Logout

```
applozic.logout(function() {console.log("success");}, function () {console.log("error");});
```



Install iOS or Android platform

    cordova platform add ios
    cordova platform add android
    
Run the code

    cordova run 

## More Info

For more information on setting up Cordova see [the documentation](http://cordova.apache.org/docs/en/latest/guide/cli/index.html)

For more info on plugins see the [Plugin Development Guide](http://cordova.apache.org/docs/en/latest/guide/hybrid/plugins/index.html)
