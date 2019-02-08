# Marvel Themed Intro

漫威的电影片头特点非常鲜明——伴随着翻动漫画书的背景，『Marvel Studios』的标题渐渐浮现出来。使用After Effects、Final Cut Pro或者Motion就可以做出这样的效果，在YouTube上可以找到许多教程。不过，对于这样的搬砖工作，也许用脚本来处理会更加灵活和方便。

## 依赖 Dependencies

需要Python3环境，并安装OpenCV相关组件。这可以通过包管理工具完成，例如在macOS上执行`brew install opencv`，而debian系执行`sudo apt install libopencv-dev`。  
还需要使用pip3安装`numpy`和`opencv-python`。当然，这也可以在后面一步执行。  
如果视频的编码出现问题，可以试试使用`ffmpeg`。

## 安装 Install

```bash
# Clone this repository
git clone https://github.com/stevenjoezhang/marvel-themed-intro.git
# Go into the repository
cd marvel-themed-intro
# Install dependencies
pip3 install -r requirements.txt
```

## 使用 Usage

将你要用来制作片头的图片放在一个文件夹里，例如`images/`文件夹，我们假定其绝对目录为`/path/to/your/images/`。这些图片最好分辨率足够高，并且宽高比与期望输出视频的宽高比接近。该脚本会对所有图片进行预处理，以使得它们适合进行进一步的操作。  
这一步完成后，执行
```bash
python3 marvel.py
```
然后按提示输入参数即可，例如前面提到的绝对目录。视频默认为1920x1080，24fps，每张图片持续3帧。  
为了制作时间足够长的片头，你可以准备更多的图片，或者增加每张图片持续的帧数。如果这些照片都是漫威的漫画截图，那么就可以做出一个高仿的片头了。  
完成后，会在你的执行目录下生成`save.mp4`，看看效果如何吧！  
当然，这个脚本只是处理了一部分的（搬砖）工作。你还是需要使用视频后期处理软件，加上你的字幕等内容（对应于MARVEL STUDIOS标志），这里不再赘述。

## Credits
* [Mimi](https://zhangshuqiao.org) Developer of this project.

## License
Released under the GNU General Public License v3  
http://www.gnu.org/licenses/gpl-3.0.html