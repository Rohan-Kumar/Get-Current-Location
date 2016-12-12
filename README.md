# Get-Current-Location
A tutorial to get the current location in your android app

Add the library in build.gradle
> compile 'com.google.android.gms:play-services:8.4.0'

Add permission in manifest
>     <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
>     <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>

Connect to google api. Once it is connected you can get the location by LocationServices.FusedLocationApi.requestLocationUpdates() method
It takes 3 parameters
- GoogleApiClient
- LocationRequest
- LocationListener

LocationListener will give you a call back <b><i>onLocationChanged</i></b> with a <b><i>Location</i></b> object.

You can get the latitude by calling getLatitude() method on the location object

You can get the longitude by calling getLongitude() method on the location object

Note: You will get the location only if gps is on. For a tutorial on how to programmatically switch on gps refer <a href="https://github.com/Rohan-Kumar/Enable-GPS" target="_blank"> this </a>
