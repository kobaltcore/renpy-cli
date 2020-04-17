# renUtil
A toolkit for managing Ren'Py instances via the command line.

renUtil can install, update, launch and remove instances of Ren'Py. The instances are completely independent from each other. It automatically sets up and configures RAPT so new instances are instantly ready to deploy to many different platforms. Best of all, renUtil automatically configures Ren'Py in such a way that you can run it headless, making it well suited for build servers and continuous integration pipelines.

## Installation
renUtil can be installed via pip:
```bash
$ pip install renutil
```

Please note that renUtil requires Python 3 and will not provide backwards compatibility for Python 2 for the foreseeable future.

Since the Android SDK installation process requires `pygame_sdl2`, this will have to be compiled and installed during the Ren'Py installation process. This process depends on SDL2 headers being installed on the system, which have to be installed through external means.

### macOS
```bash
brew install sdl2 sdl2_image sdl2_mixer sdl2_ttf
```

### Linux
```bash
sudo apt install libsdl2-dev
```

## Usage
```bash
Usage: renutil [OPTIONS] COMMAND [ARGS]...

  Commands can be abbreviated by the shortest unique string.

  For example:
      clean -> c
      la -> launch
      li -> list

Options:
  -d, --debug / -nd, --no-debug  Print debug information or only regular
                                 output

  --help                         Show this message and exit.

Commands:
  cleanup    Clean temporary files of the specified Ren'Py version.
  install    Install the specified version of Ren'Py (including RAPT).
  launch     Launch the specified version of Ren'Py.
  list       List all available versions of Ren'Py.
  uninstall  Uninstall the specified Ren'Py version.
```

# Disclaimer
renUtil is a hobby project and not in any way affiliated with Ren'Py. This means that there is no way I can guarantee that it will work at all, or continue to work once it does. Commands are mostly relayed to the Ren'Py CLI, so any issues with distribution building or startup are likely the fault of Ren'Py and not mine. renUtil is not likely to break on subsequent updates of Ren'Py, but it is not guaranteed that any available version will work correctly. Use this at your own discretion.
