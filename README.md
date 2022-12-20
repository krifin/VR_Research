# VR_Research
Aim: To test our Virtual reality multi-sensorial experience

a revolutionary discovery experience that mixes touch, smell, sound and sight for a fully immersive journey across the world of Metaverse & Gaming.

![d3bcd68dc28c78f6a5ecc593a37f24d1](https://user-images.githubusercontent.com/121123118/208746937-391810dc-550b-412b-87bd-b079e40ae61e.jpg)


Virtual reality "Is memory data?" experience
When we were asked by our partners to try to creatively envision the question "Is memory data?", we have to admit - we scratch our heads for a little bit. In the same time, One of the research lab envisioned an activation which would be more of an art installation than your average marketing activation.  What we have envisioned for this project was very simple in its elegance. Using nothing more than a bucket, a garden hose and a virtual reality headset, we have placed the user into the center of the experience in which the element of water was presented in a way not seen before.
Upon placing the VR headset on them, visitors would be asked to place their hands under the running water. Achieving synesthesia while combining the element of water with rich graphical content, we strived to show that there is more to life and living than it can be seen with the naked eye.


![c09c57d64d39d531dd1bbc29eb70416b](https://user-images.githubusercontent.com/121123118/208746940-60e4f744-06ab-4d95-a381-1c1e17026393.jpg)

To conduct this research study, we plan to work with several pyschologist & neuroscientist & use the Morris Water Maze(MWM) Methodology.

#About Morris Water Maze (MWM)

The Morris Water Maze is a widely used behavioral task in neuroscience for studying spatial learning and memory. This test is based on the fact that an animal will try to escape a stressful situation or stimulus, which in this case is a large pool of water. The pool contains a small platform, either visible above the water level, or just below the surface of the water. This small platform allows the animals to escape the water and allows them to stand without the stress of swimming, and is designed with a mesh or grooved material that allows for easy handling. Pre-training occurs by introducing the location of the escape platform and using a platform that is visible above the water surface. On the following days, the actual test is performed, in which the platform is hidden beneath the water surface. To escape swimming in the water, the animal must remember the location of the escape platform using visual cues in the testing area, which requires use of hippocampal-dependent spatial reference memory, and this ability to remember the location of the platform can be effected by the administration of certain drugs or disease models.

The MWM was first used by Richard Morris at the University of St. Andrews in Scotland in the early 1980s. Since then, it has become one of the most widely used tools in behavioral neuroscience because of its easy of use and training, its many variations, and its ability to test various areas of brain function. Morris published a series of papers describing the maze and its evaluation of hippocampal-dependent learning over several years (Morris 1981, Morris 1982, Morris 1984, Morris 1986). The maze also gained popularity when it was used by Ian Whishaw’s group in Canada (Kolb et al. 1982, Kolb et al. 1983). Since these initial papers, the maze has been used to study various disease models, including endocrine abnormalities, strokes, Alzheimer’s disease, other neurodegenerative diseases, and their effects on learning and memory

##Research_Method

The virtual reality environment can be created as per the need of the experiment. In the Simian version multiple environments can be configured.

The Morris Water Maze (MWM) is a widely used behavioral task developed by Richard G. Morris in the year 1981 as a response to the Radial Arm Maze (RAM). As opposed to the Radial Arm Maze, the Morris Water Maze doesn’t provide the subject with a choice point. Further, the task utilizes the fear of drowning to motivate the subject to learn the location of the escape platform quickly. The navigational task is effective in the assessment of spatial learning, and over the course of years has seen modifications and adaptations such as the Water T-Maze, the Water Y-Maze, and the Water RAM.

Reference Video 


freeglut (local library, included in the project)
FreeImage (local library, included in the project)


OpenGL and GLU
What is it?
A fountain built with OpenGL fixed piepline.

Note: this can look quite different on different machines:

The computational power(or, the optimization performed by the compiler) will affect the frame rate, therefore affect the speed of the fountain water. If your computer is powerful enough, the frame rate will be around 58fps.
The resolution of the screen will affect the overall experience, including font size, texture, and the size of water particles.
Under normal resolution, it looks like this:

Normal screenshot

Under HiDPI, it looks like this:

HiDPI scrennshot

Techniques Used
First person camera(see "Operation" below for information about the keyboard controls)
Texture(basin, ground, skybox)
Lighting(two-side)
Skybox
Simulated water(particles)
Simulated waves(oscillators)
Display list(skybox, ground, fountain basin)
Fonts and text(there is a frame rate counter at the bottom left)
Explanation about the water and the waves
The water is just semi-transparent particles(points) moving along calculated parabolas.
The waves are simulated by oscillators. They change the vertices of the pool and update the normals accordingly to create ripples. The position of these oscillatiors are affected by their neighbors, and the oscillators on the edge will always have a constant y. Therefore the waves will bounce back when they reach the edge.
Look closer and take a screenshot, then you will know what is going on. For more information, checkout Fountain.cpp and Pool.cpp and read the comments.





Shapes
       

To lower down the burden on the CPU, the preset shapes are rather simple(with not many rays per level or drops per ray). If you want to see some fancier shapes, you can go tweak the initializers in main.cpp.

Operations
1 - 8: Change the shape of the fountain
f: Toggle fullscreen mode
c: Toggle mouse mode
ESC: exit
Under Keyboard Mode
→, ←: Turn camera right / left
↑, ↓: Move camera forward / backword
r, v: Turn camera up / down
w, s: Move camera up / down
a, d: Move camera left / right
Under Mouse mode
Mouse move: Rotate camera
Mouse scroll: tMove forward / backward


File structure
  - doc  // report goes here
  - include  // header files
  - lib  // static libraries
  - resource  // e.g. textures
  - src  // source code
  - screenshot // screenshots

  // dynamic library for the prebuilt executable
  - freeglut.dll
  - FreeImage.dll
  - libstdc++-6.dll
  - libgcc_s_dw2-1.dll

  - Fountain.sln   // VS2013 project file
  - Fountain.exe  // prebuilt executable
  - premake5.lua  // premake5 script

  // preview of this demo
  - normal-preview.jpg
  - hidpi-preview.jpg

  - README.md   // you are reading it :)
  
About the executable
The executable is built for Windows with MinGW, the necessary libraries are all bundled inside this project. Just run Fountain.exe to see it at work.

If you want to run it under Linux, you need to build it from source.

How to build it?
You can build it with VS2013 and above, Make and MinGW(or just Make and g++ under Linux), or anything that premake5 supports and has some C++11 support(VS2010 or above should do the trick).

This has been tested under:

Windows 8.1 + VS2013
Windows 8.1 + MinGW(g++ (GCC) 4.8.1) + GNU Make 3.81(Win32 port)
Ubuntu 14.04 + g++ 4.8.2 + GNU Make 3.81
If you are using Windows, you don't need to copy any file to any location. All libraries files(.h, .lib and .dll) are locally included. Note that it is the libraries under include and lib that will actually get linked, not your global libraries.

Windows with VS2013
Open the Fountain.sln with VS and build the Fountain target. The executable will appear under the project directory, named Fountain.exe.

Windows with Make+MinGW / older VS
Download premake5 from here, extract the executable in the archive(e.g. premake5.exe), and put the path to the executable in your PATH environment variables. Then open cmd and run premake5 --help to see what project files you can generate. I've written the premake script premake5.lua to generate the proper project files.

For example, to generate the project files for VS2012, simply run premake5 vs2012 under the project directory, then open Fountain.sln with your VS and build the Fountain target. The executable will appear under the project directory, named Fountain.exe.

Linux with Make and g++
You need to install freeglut and FreeImage first. For example, if you are using Ubuntu, run

$ sudo apt-get install build-essential freeglut3 freeglut3-dev binutils-gold
$ sudo apt-get install libfreeimage3 libfreeimage-dev
Download premake5 from here, extract the executable in the archive(e.g. premake5), and put the path to the executable in your PATH environment variables(e.g. extract the file to /usr/local/bin with root permission so you don't have to touch PATH). To generate the project files for make, simply run premake5 gmake, then run make to build it. The executable will appear under the project directory, named Fountain.
