# Creating a release version

## Needed tools

To create a release version like the ones available for download, you need to have the following tools:

### For Linux

- **zip**. It comes in most distributions, e.g. for Debian or Ubuntu use `sudo apt-get install zip`; if it isn't available in yours, try this link: <http://www.info-zip.org/Zip.html#Downloads>
- **Python 2.7**. It comes in most distributions, e.g. for Debian or Ubuntu use `sudo apt-get install python`; if it isn't available in yours, try this link: <https://www.python.org/downloads/>. **Important:** Python 3.x won't work; only Python 2.x will. Usually Python 2 and Python 3 can be installed side-by-side.
- **make**. It comes in most distributions, e.g. for Debian or Ubuntu use `sudo apt-get install make`; if it isn't available in yours, try this link: <https://www.gnu.org/software/make/#download>
- **GNU cpp**. It comes in most distributions, e.g. for Debian or Ubuntu use `sudo apt-get install cpp`. If it isn't available in yours, or you have trouble installing it, you can instead use **mcpp**, which is much more lightweight and is included in most distributions. It is also available at this link: <http://mcpp.sourceforge.net/download.html>.
- [**LSL-PyOptimizer**](https://github.com/Sei-Lisa/LSL-PyOptimizer). Currently the latest master branch is used to create the releases, which you can download by clicking on "Clone or Download" in the top right.

### For Mac OS/X

- **zip** (*)
- **Python 2.7** (*) **Important:** Python 3.x won't work; only Python 2.x will.
- **make** (*)
- [**mcpp**](http://mcpp.sourceforge.net/download.html). Alternatively you can use GNU cpp if you have it installed.
- [**LSL-PyOptimizer**](https://github.com/Sei-Lisa/LSL-PyOptimizer). Currently the latest master branch is used to create the releases, which you can download by clicking on "Clone or Download" in the top right.

(*) If you're an OS/X user and you know how to obtain these tools or whether they come pre-installed with the base system, we'd appreciate if you can help us by telling us how to do so, or even better, submit a pull request with the necessary changes to this file.

### For Windows

- [**zip**](http://www.info-zip.org/Zip.html#Downloads)
- [**Python 2.7**](https://www.python.org/downloads/) **Important:** Python 3.x won't work; only Python 2.x will.
- [**make**](http://gnuwin32.sourceforge.net/packages/make.htm#download)
- [**mcpp**](http://mcpp.sourceforge.net/download.html)
- [**LSL-PyOptimizer**](https://github.com/Sei-Lisa/LSL-PyOptimizer). Currently the latest master branch is used to create the releases, which you can download by clicking on "Clone or Download" in the top right.

## Creating the release

Once you have the required tools, edit the Makefile in the AVsitter2 folder to suit your needs, then using a terminal (also called command interpreter, shell, console... depending on the operating system) change to that folder using `cd <path-to-folder>` and type `make`. That should generate a file called `AVsitter2.zip` with the packaged version.

If you only want the optimized scripts without zipping them, use `make optimized`. The optimized files will have an `.lslo` extension, and they are ready to be copied and pasted each into a Second Life script.

If you want to remove the optimized scripts and the zip file, use `make clean` (you can regenerate them at any time by typing `make`).