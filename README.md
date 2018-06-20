
# Short description
**CEVPlayer** - plugin for CRYENGINE V allowing you to play video on the screen and on the game objects

**It's includes :** 
* Flowgraph nodes for creating video player (Screen video / Texture video)
* VideoPlayerComponent for easy integration with new components system
* Schematic functions for easy creation schematic entitys with video player component
* Example project for fast study functionality 
* Full source code 
* Absolutly free license

# Building
## Before compiling
* Go to 3rd folder and unpack `3rd.7z` archive
* Also you need installed CRYENGINE V
## Compiling
* Use CEVPlayer.cryproject for generation solution
* Open solution with Visual Studio and build it

# Branches 
* `master` - Main branch for latest CRYENGINE version (CRYENGINE 5.5.0 Preview 4)
* `cryengine_5.4` - If you need build plugin for CRYENGINE 5.4
* `cryengine_5.3` - If you need build plugin for CRYENGINE 5.3

# Using
* After compiling plugin go to `bin/win_x64` folder and copy plugin to you project bin folder
* Also you need copy `avutil-54.dll` and `swscale-3.dll` from `3rd/libav/bin` folder to you project bin folder and also to `CRYENGINE/bin/win_x64` folder
* Add CEVPlayer to you .cryproject file

```bash
{
    "type": "EPluginType::Native",
    "path": "bin/win_x64/CEVPlayer.dll"
}
```
* That's all. Now you can start sandbox and create logic for playing video in you game

# Additional information
**Warning №1 : CEVPlayer uses code of <a href=https://libav.org>Libav</a> licensed under the <a href=https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html>LGPLv2.1</a> and its source and binaries can be downloaded <a href=http://builds.libav.org/windows/>here</a>**

**Warning №2 : CEVPlayer can play video only in .webm format**

**Warning №3 : All video files should be in `Videos` folder**

**Warning №4 : TextureVideoPlayer not playing audio - use audio triggers for this**

**Warning №5 : Don't use for TextureVideoPlayer video in very hight resolution - it's can be perfomance problems (optimal HD and low)**

**Warning №6 : Don't play video when level loading - you game will be crash!**

# TODO
* Add ability to play video when level loading (Problem with blocking OnPostUpdate event)
* Maybe create special shader for YUV->RGBA conversion
* Audio triggers for in-game video
* ~~Make plugin compatible with CRYENGINE 5.3~~ ([See this](https://github.com/afrostalin/CEVPlayer/tree/cryengine_5.3))

# WIKI and lessons
Please see [WIKI](https://github.com/afrostalin/CEVPlayer/wiki)

Fast study functionality with [example project](https://github.com/afrostalin/VideoPluginExample) project

# GitHub community

I will be happy with any help from the community, so I'm waiting for your pull requests 

If you have any problem with this plugin please use [GitHub issues](https://github.com/afrostalin/CEVPlayer/issues) mechanism

# Contacts

If you need more from me, write me directly to my email : chernecoff@gmail.com
