# codeblocks_gd_cbps
This repository contains .cbp files (CodeBlocks Projets), for Windows only, and a workspace, to generate Code::Blocks itself.
They are wxWidgets version independant.
This is achieved by configuring global environment variables.
Have a look to Env_Vars.pdf to set them correctly.
Copy the src directory in your codeblocks sources src directory.
All cbps are named *_Windows.cbp and do not interfere with already standard .cbp project files.
codeblocks_Windows.cbp always creates an updateWindows.bat file. This file contains parameters to update the outputxx_yy directory

