# Youku-parse
an angular directive for parsing youku video id into real urls.

# Last Update
Last update the algorithm on March 23rd.

# Source
All the parse functions are from [http://runjs.cn/code/incos4te](http://runjs.cn/code/incos4te).

I just did the wrapping for angular.

# Usage
* Inject the module

        angular.module('YourModule','windht.youku')
    
* Use the service!

        angular.controller('YourCtrl',[Youku,function(Youku){
          Youku.getVideoSrc(anyVideoID).then(function(url){
              // Maybe directly use this url to load a video! No ads!
              $('#ChooseAPlayer!').attr('src',url);
          });
        }])

# Updating
In case of any change of the parsing functions, this service will update in a periodically of one months. Post any issues for hurry update.
