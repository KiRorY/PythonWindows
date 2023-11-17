# Unofficial Python Installers for Windows

For older Python versions in the *security* maintenance status, https://www.python.org/ officially releases only the source code and no installers. But what if you want an easy way to install these versions on Windows? Here, you can obtain unofficial Windows installers for security updates of Python 3.5 through 3.10.

For each Python version, this repository includes the following.

- 64-bit executable installer (e.g. python-3.5.5-amd64-full.exe)
- 32-bit executable installer (e.g. python-3.5.5-full.exe)
- 64-bit embeddable zip file (e.g. python-3.5.5-embed-amd64.zip)
- 32-bit embeddable zip file (e.g. python-3.5.5-embed-win32.zip)
- 64-bit NuGet package (e.g. python.3.5.5.nupkg)
- 32-bit NuGet package (e.g. pythonx86.3.5.5.nupkg)
- Windows help file (e.g. python355.chm)

These installers were built from the source distributions published at https://www.python.org/downloads/source/, patched to fix some bugs in the build scripts and to include debugging symbols and debug binaries. For the more technical among you, see [Notes.md](Notes.md) for further information about how I built the installers and how you may build them yourself.

## NuGet Packages

To install a `.nupkg` package, ensure that you have the [NuGet Command-Line Interface](https://learn.microsoft.com/en-us/nuget/reference/nuget-exe-cli-reference?tabs=windows) installed. Go to the directory containing the `.nupkg` file in Command Prompt. Replace `target\installation\directory` in the following commands with the desired location to install the package.

For 64-bit Python, run `nuget install python -Source %cd% -OuputDirectory target\installation\directory`

For 32-bit Python, run `nuget install pythonx86 -Source %cd% -OuputDirectory target\installation\directory`

## Git History

In an effort to keep the size of this repository low, the Git history will not be kept. All updates will be made via force-pushes. If you fork this repository and wish to update your fork, see https://stackoverflow.com/questions/9646167/clean-up-a-fork-and-restart-it-from-the-upstream.

## License

These files are provided under the MIT License. See [LICENSE.txt](LICENSE.txt).

## Who am I

I am Aohan Dang (https://www.linkedin.com/in/aohan-dang-536643a7/), a professional software developer and Python enthusiast.
