bucketListAppClient
===================

This is the Bucket List Todo Front End. This will be the face of the app and a site, if you so choose.

This front end goes into conjunction with the bucketListAppAPI.

Specific changes will need to be made to the services.js file in /js on line 3. Make the "base" URL the same as where you'll be hosting the server API.

var base = "http://localhost:3000;

My public facing API server is an AWS EC2 instance, so my variable is close to this:

var base = "http://ec2-11-22-33-44.us-west-2.compute.amazonaws.com:3000/";

After those changes, you should be able to submit the full code to Phone Gap Build to get your iOS, Android and Windows apps built.

UPDATE: The app will now let you edit your Bucket List entries.

