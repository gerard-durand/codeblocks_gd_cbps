# codeblocks_gd_cbps
This repository contains `.cbp` files (CodeBlocks Projets), for Windows only, and a workspace, to generate Code::Blocks itself.
They are wxWidgets version independant.
This is achieved by configuring `global environment variables`.
Have a look to [Env_vars.pdf](Env_vars.pdf) or [Env_vars.md](Env_vars.md) to set them correctly.
Copy the src directory in your codeblocks sources src directory.
All cbps are named `*_Windows.cbp` and do not interfere with already standard `.cbp` project files.
`Codeblocks_Windows.cbp` always creates an `updateWindows.bat` file. This file contains parameters to update the `outputxx_yy` directory.
