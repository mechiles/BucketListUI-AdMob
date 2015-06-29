Bucket List Front End with Ads
===================

This is the Bucket List Todo Front End. This will be the face of the app and a site, if you so choose. I have updated this to now have ad serving through Google AdMob.

This front end goes into conjunction with the [bucketListAppAPI](https://github.com/mechiles/bucketListAppAPI).

Specific changes will need to be made to the *services.js* file in /js directory on `line 3`. Make the `base` URL the same as where you'll be hosting the server API.

`var base = "http://localhost:3000;`

My public facing API server is an AWS EC2 instance, so my variable is close to this:

`var base = "http://ec2-11-22-33-44.us-west-2.compute.amazonaws.com:3000/";`

####AdMob Updates####

There is now a `cordova AdMob` package installed to serve the Google Ads.
In `config.xml` the following line represents the required call for using PhoneGap to produce your app:

`  <gap:plugin name="com.google.cordova.admob" version="2.7.7" source="plugins.cordova.io"/>`

In order to serve your AdMob ads, you'll need to update `lib/angular-admob/admob_simple.js` with your relevant AdMob IDs on lines `4`, `9` and `14`. This js file is called on `index.html` and will render your ads at the bottom of the app. You can change placement by updating `position: AdMob.AD_POSITION.BOTTOM_CENTER,` on line `30`.

After those changes, you should be able to submit the full code to Phone Gap Build to get your iOS, Android and Windows apps built.
