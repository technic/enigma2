enigma2
-------

enigma2 is a gui frontend for linux powered set-top-boxes. 
This fork is for running enigma2 on a regular linux pc, that may be usefull for plugin developers.

On target devices video stream is decoded by hardware and blit to tv screen together with osd framebuffer layer.
In case of simple TS stream multimedia file is directly routed from dvb card to hardware decoder or pushed to 
/dev/dvb device from user space memory.
To play more complecated multimedia files enigma2 uses gstreamer multimedia framework with dvbsink plugin.

On pc rendering is perfomed with SDL2. We use gstreamer appsink plugin to output video frames to SDL_Texture.
Rendering of video that comes from DVB is not implemented.
