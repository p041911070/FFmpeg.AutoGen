##FFmpeg.AutoGen [![Build Status](https://travis-ci.org/Ruslan-B/FFmpeg.AutoGen.png)](https://travis-ci.org/Ruslan-B/FFmpeg.AutoGen)

Auto Generated FFmpeg wrapper for C#/.NET and Mono.  
Wrapper generated for FFmpeg 1.2.  

##Usage

The example of the library usage: video decoding, conversion and frame extraction to jpeg is included in ```FFmpeg.AutoGen.Example``` project.  

- on Windows:  
You should use aproach from the example project to specify fixed location of the FFmpeg libraries viz ```InteropHelper``` as well to get a location from the environment variable.  
Precompiled shared libraries bundled in repository but can be downloaded from [Zeranoe FFmpeg builds](http://ffmpeg.zeranoe.com/builds/).  
Here is direct links to FFmpeg 1.2 release for 
[32-bit](http://ffmpeg.zeranoe.com/builds/win32/shared/ffmpeg-1.2-win32-shared.7z) or
[64-bit](http://ffmpeg.zeranoe.com/builds/win64/shared/ffmpeg-1.2-win64-shared.7z) platform.  

- on OS X:  
Install FFmpeg via [MacPorts](http://www.macports.org):
```bash
sudo port install ffmpeg +universal
```
Before run the application please ensure that the environment variable ```LD_LIBRARY_PATH``` is inclides path to FFmpeg libraries.  
By default MacPorts keeps compiled libraries at ```/opt/local/lib```.

- on Linux:  
*todo*

##Download

Compiled wrapper:
http://sourceforge.net/projects/ffmpeg-autogen/files/

##Generation

The wrapper generator uses customized version of ctypesgencore package based on [ctypesgen](http://code.google.com/p/ctypesgen/) 0.r125.

Prerequisites:
 - FFmpeg library binaries (see **[Usage](#usage)**)
 - Python 2.7 with packages:
    - ctypes 1.0.2

 - gcc - OS dependent:
    - on OS X - XCode Command Line Tools
    - on Windows - [MinGW](http://www.mingw.org)

Steps to generate:
- Execute: python generate.py
- File ```./FFmpeg.AutoGen/FFmpegInvoke.cs``` will be regenerated.

##License

GNU Lesser General Public License (LGPL) version 3 or later.  
http://www.gnu.org/licenses/lgpl.html

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.