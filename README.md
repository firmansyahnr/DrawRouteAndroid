# DrawRouteAndroid
<h3>How To Use</h3>
<br>
Declare
<pre>
GoogleMap mGoogleMap;
LatLng newLocation = new LatLng(10,10);
LatLng newMyLocation = new LatLng(20, 20);
</pre>
<br>
Draw Marker
<pre>
DrawMarker.getInstance(this).draw(mGoogleMap,newLocation,R.drawable.marker_icon,"Marker Title");
</pre>
<br>
Draw Route
<pre>
DrawRouteMaps.getInstance(this).draw(newLocation,newMyLocation, mGoogleMap);
</pre>
<br>
Get Center Position
<pre>
LatLngBounds bounds = new LatLngBounds.Builder().include(newLocation).include(newLocationKu).build();
Point displaySize = new Point();
getWindowManager().getDefaultDisplay().getSize(displaySize);
mGoogleMap.moveCamera(CameraUpdateFactory.newLatLngBounds(bounds,displaySize.x,250,30));
</pre>
