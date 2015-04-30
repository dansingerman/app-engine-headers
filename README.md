# App Engine Headders

This is a trivial Google App Engine application that is the server side counterpart to https://github.com/dansingerman/jQuery-Browser-Language

You can use it to retrieve any http request headers via JSONP.

You can also get useful geolocation headers that Google App Engine provides.

Here is an example http://ajaxhttpheaders.appspot.com/?callback=gimme_headers

Example response: 

    gimme_headers({
      'Accept-Language': 'en,en-US;q=0.8,fr-CA;q=0.6,fr;q=0.4', 
      'Accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8', 
      'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/42.0.2311.90 Safari/537.36', 
      'Host': 'ajaxhttpheaders2.appspot.com', 
      'X-Appengine-Region': 'eng', 
      'X-Appengine-City': 'croydon', 
      'X-Appengine-Citylatlong': '51.376165,-0.098234', 
      'Content-Type': '; charset="utf-8"', 
      'X-Appengine-Country': 'GB'
    })

## Usage

1. Go to https://console.developers.google.com/ , sign in, and select "Create a project..." in the top menu.
2. Create the project and make a note of the project ID.
3. Clone this repo, and add the project ID to the app.yaml file where it says YOUR_APP_ID.
4. Follow the instructions here to deploy it: https://cloud.google.com/appengine/docs/python/gettingstartedpython27/uploading
5. It should be available at http://YOUR_APP_ID.appspot.com/?callback=some_callback
