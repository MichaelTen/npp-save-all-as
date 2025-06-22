# npp-save-all-as
save all open files in notepad++. 

# npp-save-all-buffers

A lightweight PythonScript for Notepad++ that exports every open buffer to UTF-8 text files in a folder of your choice.

## Description

This script automates the “Save As…” process for all tabs in Notepad++. You simply configure a target directory, run the script, and each open buffer—whether already saved or brand new—will be written out as a `.txt` file. Unsaved tabs are named `new 1.txt`, `new 2.txt`, and so on, while existing files keep their original names and extensions.

Under the hood the script decodes any byte-strings into Unicode before writing, so it gracefully handles non-ASCII characters without raising encoding errors. It was built for the PythonScript plugin’s bundled Python 2.7.18 interpreter and requires nothing more than Notepad++ and the PythonScript plugin.

## Features

1. Saves every open buffer in Notepad++ to a designated folder  
2. Automatically names unsaved buffers `new N.txt`  
3. Preserves original filenames and extensions for saved files  
4. Decodes and handles non-ASCII text to avoid encoding errors  
5. Compatible with Python 2.7.18 (default PythonScript interpreter)  

## Prerequisites

Notepad++ (any recent version) with the PythonScript plugin installed. No external Python installation is required, as the plugin uses its built-in Python 2.7.18 runtime.

## Installation

1. Download or clone this repository  
2. Copy `npp-save-all-buffers.py` into your Notepad++ PythonScript “scripts” folder  
3. Restart Notepad++ (or reload the PythonScript plugin)  
4. (Optional) Assign a keyboard shortcut via Plugins → PythonScript → Shortcut Mapper  

## Usage

To export all open buffers:

1. Open the files or create new tabs in Notepad++  
2. Go to Plugins → PythonScript → Scripts → npp-save-all-buffers.py  
3. After running, check your configured folder for `.txt` files  

A confirmation dialog will tell you how many files were saved and display the target directory path.

## Configuration

Edit the `target_dir` variable at the top of `npp-save-all-buffers.py` to point to any existing or new folder on your system. The script will create the directory automatically if it does not already exist.

## Disclaimer

Utilize or do not utilize this at your own risk. This is shown for learning purposes only. 
