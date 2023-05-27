:rotating_light: **The project has moved to a self-hosted git instance!**<br/>
:rotating_light: **Please use the new URL for an up-to-date version:** https://code.apps.glenux.net/glenux/sensefs

# SenseFS

## Requirements

SenseFS requires 'rfuse-ng' rubygem 

 gem install rfuse-ng -v=0.4.0

## Description

SenseFs is toy-project and a naive approach to semantic filesystems. It was
essentially inspired by Tx0's TagSistant project.

The main idea is that a file can exist at multiple locations... and as long as
it is the same file, its metadata should be the same everywhere.

The other thing is that using a filesystem with semantic information should not
require more than the usual filesystem-accessing tools (your favorite
filemanager, command line or whatever).


## Roadmap 

* file storage
* support for simple tags
* tags should be accessible via xattr

== Storage of files

A file is a sequence of data "chunks" of (at most) a given size. 
Each one of these "chunks" is identified by a hash.

A file should keep a link to each of its references

 mountpoint/
  |- tags/       # where the tagging happens and can be queried
  |- archive/    # where all the objects are stored
  |- relations/  #

 storage
  |-- files

### File creation

### File modification

### Storage of directories

### Semantic requests

## Related projects

* Tagsistant: http://www.tagsistant.net/
* TagFS: http://code.google.com/p/tagfs/
