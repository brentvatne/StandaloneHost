![Icon](https://www.larrymtaylor.com/images/standalonehost.png)  

# StandaloneHost

## Description

StandaloneHost is a utility that can host one V2 Audio Unit soft synth.
This is useful for playing soft synths that do not provide a standalone
program, without starting up a DAW or other hosting app. It is essentially
the Mac equivalent of the popular SAVIHost program for Windows with
additional features.

## Wrappers

Rename a copy of StandaloneHost.app to open one synth directly: `Ctrl-E.app` loads the AU named Ctrl-E. The name can also add a label to the AU's name, so several wrappers can use one AU: `Rhodes (RdPiano).app` loads Giulio Zausa: RdPiano.

In a wrapper, **Save Plugin State** (⌘S) keeps the current sound. The wrapper restores it at launch from `~/Library/Application Support/StandaloneHost/<wrapper name>.aupreset`. Delete that file to start again from the plugin's default sound.

## Dependencies

StandaloneHost builds with Xcode 27 and requires macOS 12 or later.

It requires [LTCommon](https://github.com/brentvatne/LTCommon) and Apple's
[CoreAudioSDK](https://github.com/nerrons/CoreAudioSDK) version 1.1, cloned
next to this repository:

```sh
git clone https://github.com/brentvatne/StandaloneHost
git clone https://github.com/brentvatne/LTCommon
git clone https://github.com/nerrons/CoreAudioSDK
cd StandaloneHost
xcodebuild -scheme "StandaloneHost Release" -derivedDataPath build build
```

## Contributing

Contributions that enhance StandaloneHost or fix bugs are very much 
appreciated. However, please note that I can't promise that all 
contributions will be accepted.

### Use Github Issues and Pull Requests

If you're capable of implementing the feature or bug fix yourself,
please open a pull request rather than opening an issue.

If you're not able to make the change yourself, please open an issue
after checking to be sure there's not already an existing open issue.

Contributions must be submitted using Github. Contributions sent as
code dumps via email are difficult to merge in, don't promote discussion
and iteration, and don't leave a comment trail explaining the change.

### Code style

StandaloneHost doesn't have a style guide document, but its
style should be easy to infer by reading the existing code. Please try
to match this style closely. Two rules are mandatory: 1) no tabs;
and, 2) indents are four spaces.

## License

The code in this repository is licensed under the MIT license unless
otherwise noted within specific files.

Copyright &copy; 2020-2026 Larry M. Taylor <software@larrymtaylor.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

