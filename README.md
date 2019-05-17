# TerminalImageViewer-win (tiv-win)

tiv-win is a native Win32 port of the [tiv](https://github.com/stefanhaustein/TerminalImageViewer), a small C++ program to display images in a (modern) terminal using RGB ANSI codes and unicode block graphic characters.

![Screenshot](https://i.imgur.com/nCn3mxY.png)

## Windows-specific notes
Requires Windows 10 build 15xx (1803 or newer recommended). ImageMagick's `convert.exe` is expected to be found in one of the locations CImg expects (like ".\").
**Default Windows fonts do not support almost all of the characters needed. Use `-0` switch or install a font that covers more unicode characters. Fira Code covers *most* of the required ones.**
 
When output is redirected the app will run as if launched on an 80-column wide terminal.

## Usage

    tiv-win [options] <filename(s)>

or

    tiv-win [options] <directory> 2> NUL

The `2> NUL` is needed to supress ImageMagick complaining about metadata and files that are not images.

By default, thumbnails and file names will be displayed if more than one image is provided. To display a list of options, just run the command without any parameters. 

## Contributions

Please refer to the [original repository for the *nix tiv](https://github.com/stefanhaustein/TerminalImageViewer)

