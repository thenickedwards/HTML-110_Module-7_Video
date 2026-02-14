# HTML - Videos and Multimedia

**Code References:** <https://github.com/thenickedwards/htML-110_Module-7_Video/ >

**Deployed Page:** <https://thenickedwards.github.io/HTML-110_Module-7_Video/ >

Hi, I’m Nick Edwards and in this video I’ll be going over how to include a video in your HTML.

The first method we’ll use leverages HTML’s video tag. Similarly to using the <img> tag, you will need to specify the src attribute with a value that references the video. We can path relatively to the video.

Here is an example of an img tag. The source specifies the image rendered to the page.

<img src="assets/success.png" width="500px" alt="Success" />

(View this in the browser.)

But we want a video. We can try and cheat by making the source a gif.

<img src="assets/thumbs-up.gif" alt="Thumbs up!" />

(View this in the browser.)

But HTML has a better way!

<h1>Testing Video Element - local files</h1>
   <video src="assets/dramatic-chipmunk.mp4"></video>

(View this in the browser.)

This will render the video to the page but there are a few more steps. You can always review the attributes for an HTML tag, for example W3 Schools or MDN have great documentation. Let’s add controls and a few other attributes as a test. This code should render the video to the page, automatically start playing the video muted and on a loop. We’ve also specified a width.

<h1>Testing Video Element - local files</h1>
   <video
     src="assets/dramatic-chipmunk.mp4"
     width="500px"
     controls
     autoplay
     muted
     loop
   ></video>

(View this in the browser.)

The source doesn’t always need to be local. For example if you have a video hosted somewhere, you can reference the URL. In this example, I’m uploaded the file to GitHub and am referencing it directly.

   <h1>Testing Video Element - URL</h1>
   <video controls>
     <source
       src="https://thenickedwards.github.io/HTML-110_Module-7_Video/assets/double-rainbow.mp4"
     />
   </video>

(View this in the browser.)

It’s important to consider that not every user who visits your site to watch your incredible viral video will have a browser that supports your video filetype. You can help them out by specifying backups.

   <h1>Testing Video Element - with backups</h1>
   <video height="250" controls autoplay muted loop>
     <source src="assets/dramatic-chipmunk.mp4" type="video/mp4" />
     <source src="assets/keyboard-cat-backup.webm" type="video/webm" />
     Your browser does not support the video tag.
   </video>

(View this in the browser.)

The browser will try each source in the order listed and display the message if the video cannot be played. We can test this by using a different video as the backup. I’ll break the pathing to the chipmunk video and this we get this cat video instead.

   <h1>Testing Video Element - with backups</h1>
   <video height="250" controls autoplay muted loop>
     <source src="asset /dramatic-chipmunk.mp4" type="video/mp4" />
     <source src="assets/keyboard-cat-backup.webm" type="video/webm" />
     Your browser does not support the video tag.
   </video>

(View this in the browser.)

Another way to insert a video into your HTML is by embedding it. Many video platforms will have an “embed” option. For example I have copied some code from a very popular video platform. This varies depending on where the video is hosted but usually you can look for “embed” within the “share” function. In any case, once I have the code, I can paste it into my site.

   <h1>Testing Video Element - Embed</h1>
   <!-- EMBED - code copied from YouTube video share option -->
   <iframe
     width="560"
     height="315"
     src="https://www.youtube.com/embed/dQw4w9WgXcQ?si=vSWi_4CguO-F2Kox"
     title="YouTube video player"
     frameborder="0"
     allow="
       accelerometer;
       autoplay;
       clipboard-write;
       encrypted-media;
       gyroscope;
       picture-in-picture;
       web-share;
     "
     referrerpolicy="strict-origin-when-cross-origin"
     allowfullscreen
   ></iframe>

This is a pretty famous video that I want to make available but it’s important to remember that the host or owner of the video controls its access. If the user were to delete this video or their account or if the platform restricted access to the video or shut down, the video on my site would show as broken. Let’s check to make sure everything is working correctly.

(View this in the browser.)

Perfect!
