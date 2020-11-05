# Illumia Basespace Sequence Hub CLI
### Ben Lorentz
This tool is used to download DNA sequneces that were produced on an Illumina machine. While it is possible to download these DNA files (typically a .fastq format) through a browser, most clusters do not have a gui to open a browser on. A second case is when building pipelines it is much easier to invoke a command line command as opposed to managign a queiry through a browser. To solve this Illumina has built a CLI tool to download these raw reads. 
Illumina's [website](https://developer.basespace.illumina.com/docs/content/documentation/cli/cli-overview) is probably the best resouce for this tool, so if this short guide does not cover what you are looking for, take a look there. 
-------------------------------------------------

## Installation
```shell
#Linux x86
wget "https://api.bintray.com/content/basespace/BaseSpaceCLI-EarlyAccess-BIN/latest/\$latest/amd64-linux/bs?bt_package=latest" -O $HOME/bin/bs
chmod u+x $HOME/bin/bs
bs

#Mac OS x86
wget"https://api.bintray.com/content/basespace/BaseSpaceCLI-EarlyAccess-BIN/latest/\$latest/amd64-osx/bs?bt_package=latest" -O $HOME/bin/bs

# Windows x86 v 1.2.1
wget https://basespace.bintray.com/BaseSpaceCLI-EarlyAccess-BIN/latest/1.2.1/amd64-windows/bs.exe -o bs.exe
```

## Authentication 
```shell


```