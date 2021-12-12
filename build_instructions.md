# Build Instructions

The following instructions show how to build the program into a single `.exe`
file that can be run to install the software.

1. Install the required modules from [`requirements.txt`](requirements.txt) if
   you haven't already.
2. Open a terminal in the root directory.
3. Use a markdown to PDF converter to generate a `manual.pdf` file and place it
   in `./code/assets`.
4. Install NSIS if you haven't already, and add the install location to your
   system's PATH variable.
5. Run the build command:
   ```sh
   pyinstaller -p code --add-data="code;." -y -w --icon=code/assets/icon.ico --name=open-mcr code/main_gui.py; makensis installer.nsi
   ```
