# Extracting_from_PDF
Use camelot to extract tables from a PDF
The camelot need following dependencies:
1. camelot-py[cv]
if the istallation did not work i.e you cant import camelot then uninstall camelot and pip install camelot-py[all]

2. Tyhen you need to install the ghostscripts 
- For this download the gs9550w64.exe (for 64bit) from https://ghostscript.com/releases/gsdnld.html
- After download then install the gs. 
- Then set the set adapt your system’s Path variable:
- Go to Control Panel → System and Security → System → Advanced System Settings → computer name, domain and workgroup settings → Advanced → Environment Variables
- Find the Path variable within System Variables, select it and click on edit.
- Your path should be: C:\Program Files\gs\gs9.55.0\bin

3. Check the ghostcript is installed sucessfully:
- In the cmd run following
-import ctypes
-from ctypes.util import find_library
-find_library("".join(("gsdll", str(ctypes.sizeof(ctypes.c_voidp) * 8), ".dll")))

 The output of the find_library function should not be empty.

4. If you get some output then ghostscript is installed correctly. The camelot will work fine
