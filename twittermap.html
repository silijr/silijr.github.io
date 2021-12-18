// namespace
var maptwitter = {};
var map;
var infowindow = new google.maps.InfoWindow();
var markers = [];

// initialize function
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
// initialize function
maptwitter.init = function()
{
	// event listener on the "go" button
	$('#search-button').click(function(){
		maptwitter.getTweets();
	})
 
	//center lat/lon
	var latlng = new google.maps.LatLng(-1.09626573, 37.01288458);
 
	//map configutations
	var myOptions = {
		zoom: 10,
		center: latlng,
		mapTypeId: google.maps.MapTypeId.ROADMAP
	};
 
	//create the map
	map = new google.maps.Map(document.getElementById("map_canvas"), myOptions);
}
// run the init function on page load
$( document ).ready(function() {
	maptwitter.init();
});

//get tweets
maptwitter.getTweets = function() 
{
	// clear any content from the tweet list
	$('#tweetlist').empty();
 
	// get the search keyword
	var search_keyword = $('#search-text').val();
 
	// get the center of the map
	var centerLat = map.getCenter().lat();
	var centerLng = map.getCenter().lng();
 
	// construct the geocode query string
	var geocodequery = centerLat + ',' + centerLng + ',20mi';
	 
	// set the proxyurl
	var proxyurl = 'search.php?q=' + search_keyword + '&geocode=' + geocodequery;
 
	// call the proxy file to get tweets from Twitter
	$.getJSON(proxyurl,function(data){
		$.each(data.statuses, function(i,item){
			$('#tweetlist').append('<div>'+item.text+'</div><hr>');
 
			// add each tweet to the map
			if(item.geo)
			{
				var tweet = 
				{
					lat: item.geo.coordinates[0],
					lng: item.geo.coordinates[1], 
					name: item.text,
					icon: item.user.profile_image_url
				}
 
				// map it
				maptwitter.createMarker(tweet)
			}
		});		
	})
}
maptwitter.createMarker = function(options){
	var markerLatLng = new google.maps.LatLng(options.lat,options.lng);
	var marker = new google.maps.Marker({
		position: markerLatLng,
		map: map,
		title: options.name,
		icon: options.icon
	});
 
	// add to markers array
 	markers.push(marker);
 
	//the event listener that activates the infowindow on user click
	google.maps.event.addListener(marker, 'click', function() {
		infowindow.setContent(options.name);
		infowindow.open(map,marker);
	});
}