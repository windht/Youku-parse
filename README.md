# Youku-parse
An angular directive for parsing youku video id into real mp4 urls.

# Last Update
Last update the algorithm on 2016 Nov 29th.
Functional test on 2016 Nov 29th, worked well.
Added the cross domain support using jsonp.

# Source
All the parse functions are from MAMA2 [https://github.com/zythum/mama2/blob/master/src/seeker_youku.js](https://github.com/zythum/mama2/blob/master/src/seeker_youku.js).

I just did the wrapping for angular.

# Usage
* Inject the module

        angular.module('YourModule','windht.youku')
    
* Use the service!

        angular.controller('YourCtrl',[Youku,function(Youku){
          Youku.getVideoSrc(anyVideoID).then(function(url){
              // Maybe directly use this url to load a video! No ads!
              angular.element('ChooseAPlayer!').attr('src',url);
          });
        }])
        
* Or directly and simply use a nice directive
        
        <video youku youku-id="XOTY1MjQ2OTc2"></video>

* Or You may want to do dynamic loading

		//place a video with "youku" attr
		<video youku></video>

		angular.controller('YourCtrl',function($rootScope){
			var vid;
          	$rootScope.$broadcast("$video.update",vid)
          	// broadcast the vid
        })

* And there you go!

* Check the demo!

# Updating
In case of any change of the parsing functions, this service will update in a periodically of one months. Post any issues for hurry update.