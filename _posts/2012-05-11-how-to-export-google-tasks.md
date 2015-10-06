---
ID: 531
post_title: How to Export Google Tasks
author: Joseph J. Ross, Esq.
post_date: 2012-05-11 12:16:00
post_excerpt: ""
layout: post
permalink: >
  http://joeross.me/blog/articles/how-to-export-google-tasks/
published: true
tumblr_geek-esq_permalink:
  - >
    http://geek-esq.tumblr.com/post/28065832527/how-to-export-google-tasks
tumblr_geek-esq_id:
  - "28065832527"
gfonts_meta_no_font:
  - "1"
---
<p><em>Thanks for visiting. I hope this post helps you. Consider <a href="http://joeross.me/subscribe" target="_blank">subscribing to new posts</a> or saying hello <a href="http://twitter.com/joeross" target="_blank">on Twitter</a> or <a href="mailto:joe@joeross.me?subject=From%20a%20recent%20visitor%20to%20joeross%2eme" target="_blank">via email</a>.</em>
<br /><br /></p>

<hr><p><br />
Lately I have been trying out <a href="http://smarterware.org" target="_blank">Gina Trapani&#8217;s</a> wonderfully-simple <a href="http://todotxt.com" target="_blank">todo.txt</a>. There&#8217;s something beautiful about updating my todo list from the command line, syncing it to <a href="http://dropbox.com" target="_blank">Dropbox</a>, and managing on the road with the <a href="http://www.todotxt.com/" target="_blank">Android app</a>. It&#8217;s minimal, elegant, and a tool that solves one problem really well. But I&#8217;m not sure it will work out for me in the long-run. I&#8217;m still a big fan of <a href="https://mail.google.com/mail/help/tasks/" target="_blank">Google Tasks</a>, first introduce <a href="http://gmailblog.blogspot.com/2008/12/new-in-labs-tasks.html" target="_blank">in 2008</a>. I want a way to own my data via todo.txt but maintain the convenience of Google Tasks. I didn&#8217;t quite find it, but I got close, and I at least got a copy of my Tasks data from Google&#8217;s servers.</p>

<p><!-- more --></p>

<h2>Todo.txt or not todo.txt?</h2>

<p>I live inside my Gmail account for much of the day, and Google Tasks has served me very well for many years. The ability to associate an email with a new task is particularly compelling, and always helps me stay on top of mid-to-long-term response requirements. I&#8217;ve been enjoying the <a href="https://play.google.com/store/apps/details?id=ch.teamtasks.tasks" target="_blank">Tasks Free</a> app for Android this week because it uses Google&#8217;s Ice Cream Sandwich design language and, like todo.txt, is a simple tool that solves one problem very well.</p>

<p>Unlike todo.txt, however, Google Tasks is easily accessed from the browser, either in Gmail, in a <a href="https://mail.google.com/tasks/canvas" target="_blank">full-page view</a>, or any number of <a href="https://chrome.google.com/webstore/search/%22Google%20Tasks%22?utm_source=chrome-ntp-icon" target="_blank">Chrome addons</a>. As much I like Trapani&#8217;s philosophy that you should own your data&#8212;that&#8217;s why todo.txt stores your lists in your Dropbox on all of your computers versus Google Tasks&#8217; only storing your lists on Google servers&#8212;getting it there isn&#8217;t terribly <em>convenient</em>.</p>

<h2>Best of both worlds?</h2>

<p>There&#8217;s a compromise insofar as you can install an addon to todo.txt that lets you manually sync to Google Tasks (<a href="https://github.com/ginatrapani/todo.txt-cli/wiki/Todo.sh-Add-on-Directory#wiki-google" target="_blank">get it here</a>), but the geek force isn&#8217;t strong enough with me to get it working. It involves creating and executing an additional script (I think it&#8217;s Python, but I&#8217;m not even sure) in a newly-created hidden folder within your todo.txt folder.</p>

<p>Yeah.</p>

<p>I&#8217;m not going to give up on todo.txt in general and the Tasks addon specifically because I love tinkering, even with code I know little or nothing about. But even <em>installing</em> todo.txt may be intimidating to those unused to the command line. I suspect I&#8217;ll come back to it eventually, but for now I&#8217;ll be using Google Tasks, a reflection on me and not on todo.txt&#8212;it&#8217;s an amazing app that targets a certain group of more saavy users and serves them extremely well.</p>

<p>If you spend any time in a terminal window or use launchers like <a href="http://qsapp.com" target="_blank">Quicksilver for Mac</a>, todo.txt is the easiest way to manipulate your tasks. I don&#8217;t spend that much time doing either of those things. Like I said, I spend most of my time in Gmail or on my Android phone.</p>

<h2>Can I use Google Tasks <em>and</em> own my data?</h2>

<p><em>But</em> I <em>do</em> like the idea of owning my data. So I wanted a way to own my Google Tasks data. If I can&#8217;t sync it to Dropbox, can&#8217;t I <em>at least</em> periodically download a history of what I&#8217;ve put in there?</p>

<p>A quick search for &#8220;export Google tasks&#8221; turned up <a href="http://dataliberation.blogspot.com/2011/08/introducing-google-tasks-porter.html" target="_blank">this blog post</a> from Google&#8217;s <a href="http://www.dataliberation.org/" target="_blank">Data Liberation Front</a>, the team responsible for creating the company&#8217;s data export suite, <a href="https://www.google.com/takeout/" target="_blank">Google Takeout</a>.</p>

<p>The <a href="https://google-tasks-porter.appspot.com/" target="_blank">Google Tasks Porter</a> is supposed to allow you to pull your Tasks data down from Google&#8217;s server, or import data from other productivity tools. However, whenever I try to use it to take a snapshot of my tasks, I get the message:</p>

<blockquote>
  <p><code>ERROR: Snapshot creation process failed unexpectedly.</code></p>
</blockquote>

<p>This error made me sad. It could be that I have so many current/completed/deleted tasks (over 100) that the exporter just chokes on all the data. But then again I&#8217;ve never thought of &#8220;too much data&#8221; as a problem for Google. Discouraged but not defeated, I went to Google Task Porter&#8217;s open source <a href="http://code.google.com/p/google-tasks-porter/" target="_blank">Google Code page</a> to see if others had the same problem.</p>

<p><a href="http://code.google.com/p/google-tasks-porter/issues/detail?id=14" target="_blank">They did</a>.</p>

<h2>The solution: Google Tasks Backup</h2>

<p>Lucky for me (and you), fellow Google Tasks user &#8220;Julie&#8221; <a href="http://code.google.com/p/google-tasks-porter/issues/detail?id=14#c11" target="_blank">decided</a> to make her own version of the tool, and <a href="https://tasks-backup.appspot.com/" target="_blank">Google Tasks Backup</a> was born.</p>

<p>The tool, which looks a little like Google&#8217;s version, just with (<em>much</em>) more explanation and some more options, is quick and easy to use. Authorize it by clicking a button, confirm, and select your desired output format. You can limit the export to include only compelted tasks, only deleted tasks, or those you have &#8220;cleared&#8221; from your lists after completion by clicking &#8220;Clear completed&#8221; in the Google Tasks interface. Output options include Outlook CSV, iCal ICS, raw CSV, raw CSV with date formatting, or an email formatted for inclusion in your <a href="http://www.rememberthemilk.com/" target="_blank">Remember the Milk</a> account.</p>

<p>You can also just display the output in HTML as a generated web page. This is what I did, clipping the resulting web page into my <a href="http://evernote.com" target="_blank">Evernote</a> account for permanent storage. Alternatively, you could save the web page as HTML to your hard drive or your Dropbox account, or copy and paste it into another piece of software, like a <a href="https://drive.google.com/" target="_blank">Google Doc</a>. The point is that now you have your Google Tasks history.</p>

<p>I don&#8217;t know of any way to automate this or any other export process for Google Tasks, but maybe someday automation service <a href="http://ifttt.com/" target="_blank">ifttt</a> (&#8220;if this, then that&#8221;) will plug into the Google Tasks API (released, coincidentally, <a href="http://googleappsdeveloper.blogspot.com/2011/05/getting-organized-with-tasks-api.html" target="_blank">one year ago today!</a>) to work its magic for users of Google Tasks. Maybe Google will even fix their own exporter.</p>

<p>For now though, I&#8217;m grateful for <a href="https://tasks-backup.appspot.com/" target="_blank">Google Tasks Backup</a>, and I&#8217;ll let you know if I ever find a good solution to syncing it with <a href="http://todotxt.com" target="_blank">todo.txt</a>.</p>