# GoSquashfs

A PURE Go library to read and write squashfs. Right now I'm focusing on unsquashing.
Currently IS NOT a functional library. Some things that are currently public IS going to become private. Not very well documented either.

It's roughly based on [distri's squashfs library](https://github.com/distr1/distri/tree/master/internal/squashfs)

Special thanks to https://dr-emann.github.io/squashfs/ for some VERY important information in an easy to understand format.
Thanks also to [distri's squashfs library](https://github.com/distr1/distri/tree/master/internal/squashfs) as I referenced it to figure some things out.

# Working

* Reading the header
* Reading data blocks (whether encrypted or not)
* Reading inodes
* Reading directories
* Basic gzip compression (Shouldn't be too hard to implement other, but for right now, this works)

# Not Working (Yet). Roughly in order.

* Give a list of files
    * In string & io.FileStat (?) form
* Figure out fragments
* Extracting files
    * from inodes.
    * from path.
    * from file info.
* Reading the UID, GUID, Xatt, Compression Options, Export, and Fragment tables.
* Implement other compression types (Should be relatively easy)
* Squashing

# Where I'm at.

* I CAN READ THE ENTIRE DIRECTORY!!!!! (This is a big ol' step)