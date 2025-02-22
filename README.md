# xcopen

__xcopen__ is a shortcut to open the Xcode workspace or project in the current directory.

__xcopen__ will try to open the `.xcworkspace` file of the directory. If one is not found, it will then look for a `.xcodeproj` file.


### Before `xcopen`

```bash
open -a Xcode "My Awesome App.xcworkspace"
```


### After `xcopen`

```bash
xcopen
```

## Installation

xcopen can be installed using [Homebrew](http://brew.sh).

```bash
brew install macecchi/tap/xcopen
```


## Usage

```bash
xcopen
```

That's all you need to open the workspace/project in the current directory. If you want to specify a different directory, just pass it as an argument:

```bash
xcopen /path/to/MyAwesomeApp/
```

You can also use the flag `--beta` or simply `-b` to open the project using Xcode-beta, if you have it installed:

```bash
xcopen --beta /path/to/MyAwesomeApp/
```

Specifying `--default` or `-d` will open the project with the default application:

```bash
xcopen --beta /path/to/MyAwesomeApp/
```

This can be useful if your Xcode installations contain a version number (e.g. when using [xcode-install](https://github.com/KrauseFx/xcode-install)), in which case the first two options will not work.

Finally, the `--path` or `-p` flag can be used to specify the path to a specific Xcode app if necessary (the `-d` and `-b` flags are ignored if also passed)

```bash
xcopen --path /Applications/Xcode-14.1.0.app/
# or
xcopen --path /Applications/Xcode-14.1.0.app/ /path/to/MyAwesomeApp/
```

## License

This project is licensed under the terms of the GNU GPL v3 license. See the LICENSE file.
