# Illumia Basespace Sequence Hub CLI
### Ben Lorentz

This tool is used to download DNA sequneces that were produced on an Illumina machine. While it is possible to download these DNA files (typically a .fastq format) through a browser, most clusters do not have a gui to open a browser on. A second case is when building pipelines it is much easier to invoke a command line command as opposed to managign a queiry through a browser. To solve this Illumina has built a CLI tool to download these raw reads. 
Illumina's [website](https://developer.basespace.illumina.com/docs/content/documentation/cli/cli-overview) is probably the best resouce for this tool, so if this short guide does not cover what you are looking for, take a look there.

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

This must only be done once, after completion your illumina account will be linked
```shell
bs auth
```

## Downloading Sequences
```shell
#You will need to find the project ID one way to do this is by using the bs list command
bs list projects

#An alternate way is to login to the basespace website and finding the project id, then this can be dowloaded as below
bs download project -i $PROJECT_ID -o $PROJECT_DIR
```

Previously I have had a project where the first sequencing run was lower quality so all of the samples were re-sequenced. This resulted in two files with the same name but one set with much greater amount of data. I put together a script called [Illumina Unpack](https://github.com/lorentzben/Illumina_Unpack/tree/d18d983cc961414898420bd2236ff8f162f41c81) which will unnest folders and chose the larger of two duplicate files. 