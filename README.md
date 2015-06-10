# Stream webcam and microphone to a rtmp server

### FlashVars

* server : rtmp server
* stream : rtmp stream to publish
* token  : (optional)
* camerawidth : default 640
* cameraheight : default 480
* camerafps : default 15

### Example

Raw HTML:

        <embed src="webcam.swf"
               flashvars="server=rtmp://localhost/live&stream=plop"
               bgcolor="#ffffff"
               width="500"
               height="500"
               name="haxe"
               quality="high"
               align="middle"
               allowScriptAccess="always"
               type="application/x-shockwave-flash"
               pluginspage="http://www.macromedia.com/go/getflashplayer" />

With SwfObject:

        var flashvars = {server : "rtmp://localhost/live",
                         stream : "plop"};
        var params = {};
        var attributes = {};
        swfobject.embedSWF("webcam.swf", "myId", "300", "120", "9.0.0","expressInstall.swf", flashvars, params, attributes);

## Compile

        # debug version
        haxe -debug webcam.hxml

        # release version
        haxe webcam.hxml