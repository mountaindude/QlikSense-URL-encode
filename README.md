# QlikSense-URL-encode
**URL encoding for QlikView and Qlik Sense**

Many/most web services except parameters passed as part of the URL to be hex encoded, a.k.a. URL encoding.

In some cases you might get away without such encoding, but in order to handle special characters (space,
%, #, /, \, to name a few) you need to encode the URL. This is easy enough to do in languages like
Javascript or Python, but there is no built-in function for this in QlikView or Qlik Sense.
This is particularly concerning as it is very easy to query URLs for data straight into these tools - but how
can you get those http queries into the needed format?

The code in this repository offers an easy solution to this.
The best use case is probably to load the data from the online source once, store the result to a local QVD, and then use that QVD in future calls. That way you avoid failed reloads if the online source changes or disappears.
