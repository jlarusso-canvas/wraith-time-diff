#Wraith-time-diff
This is a modified version of [wraith](https://github.com/BBC-News/wraith).<br />
It is used to track daily changes to multiple urls on a single domain.<br />
The changes are visually tracked by taking screenshots and generating diff images.
<br />
<br />

####Look here first if you are trying to understand what's going on under the hood:
- `/Rakefile`
- `/lib/wraith/manager.rb`
- `/lib/wraith/wraith.rb`
<br />
<br />

####This is where you can configure things:
- `/configs/config.yaml`<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Change domain, fuzz, and other things.<br />
- `/lib/wraith/javascript/snap.js`<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mess with timeout to fix situations when the screenshot is taken before page finishes loading.<br />
<br />

####Here are the commands:
- `rake cap`<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Reads spider.txt and captures an image for each path found.<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Moves images to a timestamped directory.<br />

- `rake diff`<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Uses imagemagick to compare the two most recent sets of images.<br />


