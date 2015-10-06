---
ID: 278
post_title: >
  How to Export Your Last.fm Listening
  History on a Mac
author: Joseph J. Ross, Esq.
post_date: 2013-03-07 20:31:00
post_excerpt: ""
layout: post
permalink: >
  http://joeross.me/blog/links/how-to-export-your-last-fm-listening-history-on-a/
published: true
tumblr_geek-esq_permalink:
  - >
    http://geek-esq.tumblr.com/post/44802226238/how-to-export-your-last-fm-listening-history-on-a
tumblr_geek-esq_id:
  - "44802226238"
gfonts_meta_no_font:
  - "1"
---
<p>My goal was simple: I wanted to export all of the tracks I&#8217;ve listened and stored in <a href="http://last.fm/user/arcane14" target="_blank">my Last.fm account</a>. I don&#8217;t have any real experience working with APIs, but thanks to <a href="http://www.forceflow.be/2012/07/10/backing-up-last-fm-scrobbles/" target="_blank">Jeroen Baert&#8217;s post</a>, which I found via <a href="http://webapps.stackexchange.com/questions/3080/how-can-i-export-track-scrobble-data-from-last-fm/36735#36735" target="_blank">this StackExchange thread</a>, I found a handy Python script that even a newb can run.</p>

<p>The script was originally written for use in <a href="http://bugs.foocorp.net/projects/librefm/wiki/LastToLibre" target="_blank">moving your Last.fm data</a> to <a href="http://libre.fm/" target="_blank">Libre.fm</a>, but it works just as well as a standalone backup.</p>

<p>I saved <a href="http://gitorious.org/fmthings/lasttolibre/blobs/raw/master/lastexport.py" target="_blank">lastexport.py</a> to my home folder (the one with your Mac username) and opened up a Terminal window. Then, I just pasted the following command into the Terminal prompt and pressed Enter:</p>

<p><code>python lastexport.py -u last.fm_user_name</code></p>

<p>Make sure you replace <code>last.fm_user_name</code> with your own Last.fm user name. The script will store the results in a text file called exported_tracks.txt, located in your Home folder or whatever other folder you saved the script in. The data in the text file is a little messy, but it&#8217;s all there.</p>

<p>If you know how to make the data prettier, don&#8217;t hesitate to <a href="http://joeross.me/contact" target="_blank">get in touch with me</a>.</p>