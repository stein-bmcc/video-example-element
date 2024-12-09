# Video on a Web Page Example
This is an example template file for how to show a video element on a web page.

1. **index.html** has examples of both using a video element and embedding a YouTube video
    1. For the video element you have to upload your video file to the folder named __media__ for this one

## Instructions

For this you will edit index.html and upload your video to the media folder.

To use this template you will need to:

1. Upload your video file to the media folder.
2. Change the src attribute in the source element. Also change the type if your video is not mp4
3. Change the figcaption content to fit your video. If you made it then give yourself credit.
4. Change all of the instances of YOUR_NAME in the header and footer.
5. Change the text in the h1 from Your Project Name to your project's name.
6. Delete these instructions
7. You can also change the CSS to update the styling if you like (not required).
	
When you are editing source element for your video you will also need to make sure the **type** attribute is correct. This is a list of file types with the type attribute values
	

| File    | MIME Type attribute    |
|---------|------------|
| .mp4  | video/mp4   |
| .mpeg  | video/mpeg  |
| .webm  | video/webm  |
| .avi  | video/x-msvideo |
| .ogv  | video/ogg      |

For example
`<source src="videoFileName.mp4" type="video/mp4">`

You can see more here [https://developer.mozilla.org/en-US/docs/Web/HTTP/MIME_types/Common_types](https://developer.mozilla.org/en-US/docs/Web/HTTP/MIME_types/Common_types)

### Multiple video file types

To make sure that anyone can view your video you can either upload it to YouTube and then embed it or you can save it as a few different file types and then upload all of these and have a source element for each. The browser will play the first file for which it has the right codec installed.

```
<video controls>
    <source src="media/filename.mp4" type="video/mp4">
    <source src="media/filename.webm" type="video/webm">
    <source src="media/filename.ogv" type="video/ogg">
</video>
```

### Note on .mov files
.mov is what is called a wrapper file type which means that it can have different types of video files inside of it. **The simplest and safest way to make sure your video plays in a broswer is to save it as .mp4 instead.** However, if you can't and have a .mov that uses the h.264 codec (a way of encoding a video file) then it _may_ play if you add it like this:

`<source src="videoFileName.mov" type="video/mp4">`

