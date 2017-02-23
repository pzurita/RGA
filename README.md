# RGA (Radeon GPU Analyzer) Command Line Tool - Fork #

RGA CLI is an offline compiler and a performance analysis tool for DirectX shaders, OpenGL shaders,
Vulkan shaders and OpenCL kernels. Using this product, you can compile source code for a variety of AMD GPUs and APUs,
independent from the GPU/APU that is physically installed on your system, and generate AMD ISA, intermediate language 
and performance statistics for each target platform. **NOTE: This is a fork to get RGA working without any AMD hardware present.**

# Fork changes #
* Made it work without requiring AMD hardware to be present.
* It doesn't automatically setup the OpenCL backend unless the input is set to process OpenCL. **NOTE: The OpenCL backend still needs AMD hardware. Haven't solved that since I don't use OpenCL myself.**
* Fixed an issue with the Vulkan backend where it would fail if the input file was inside the active directory.

# Tested input #
* Vulkan
* DirectX
* AmdIL

# Tested OS #
* Windows 10 64-bit

# How to use in Windows #
1. Get the source of this fork and build it following the steps in https://github.com/GPUOpen-Tools/RGA
2. Download the latest AMD Radeon driver executable installer from http://support.amd.com/en-us/download
3. Using http://www.7-zip.org/ open that executable and extract atiadlxx.dll and atidxx64.dll next to the compiled RGA executable.
  * In my case I found both files in Packages\Drivers\Display\WT6A_INF\B311170 within the installer executable.
4. Use as indicated in https://github.com/GPUOpen-Tools/RGA

## Running ##
Run the rga executable.

* Usage: 
  * General: rga -h
  * DirectX: rga -hlsl -h
  * OpenGL:  rga -opengl -h
  * OpenCL:  rga -cl -h
  * Vulkan:  rga -vulkan -h

## License ##
Radeon GPU Analyzer is licensed under the MIT license. See LICENSE file for full license information.

## Copyright information ##

**Boost**

Copyright Beman Dawes, 2003.
    
**TinyXML**

TinyXML is released under the zlib license
Files: *
Copyright: 2000-2007, Lee Thomason, 2002-2004, Yves Berquin 
Files: tinystr.*
Copyright: 2000-2007, Lee Thomason, 2002-2004, Yves Berquin, 2005, Tyge Lovset
    
**glew**

The OpenGL Extension Wrangler Library
Copyright (C) 2002-2007, Milan Ikits <milan ikits@ieee org>
Copyright (C) 2002-2007, Marcelo E. Magallon <mmagallo@debian org>
Copyright (C) 2002, Lev Povalahev
All rights reserved.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" 
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE 
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR 
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF 
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF
THE POSSIBILITY OF SUCH DAMAGE.
    
**OpenCL**

Copyright (c) 2008-2015 The Khronos Group Inc.

**RSA Data Security, Inc.**

Copyright (C) 1990, RSA Data Security, Inc. All rights reserved.
License to copy and use this software is granted provided that
it is identified as the "RSA Data Security, Inc. MD5 Message
Digest Algorithm" in all material mentioning or referencing this 
software or this function.
License is also granted to make and use derivative works
provided that such works are identified as "derived from the RSA
Data Security, Inc. MD5 Message Digest Algorithm" in all
material mentioning or referencing the derived work.

RSA Data Security, Inc. makes no representations concerning
either the merchantability of this software or the suitability
of this software for any particular purpose.  It is provided "as
is" without express or implied warranty of any kind.

These notices must be retained in any copies of any part of this
documentation and/or software.
 
**Glslang**
Copyright (C) 2002-2005 3Dlabs Inc. Ltd.
Copyright (C) 2012-2013 LunarG, Inc.
