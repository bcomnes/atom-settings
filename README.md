# atom-settings
Atom editor settings.  

Sublime text is dead in the water, and pacakge control uses a super dated model.  Also, package management in python isn't much fun.

Some notes about syncing atom setting below, but the goal is to get settings check in to the repo itself.

## Which folders to ignore:

> I was considering excluding from the sync process the following folders:

```
.atom/.node-gyp
.atom/compile-cache
.atom/storage
```

Can anyone confirm if it is ok to exclude those folders?
To my understanding, which isn't as complete as it should be, the following are for:

~/.atom/.node-gyp — Storage of npm modules that your apm packages depend upon
~/.atom/compile-cache — Compiled V8 code?
~/.atom/storage — Serialized windows and their state
These are all probably reasonably machine-specific, so I don't think excluding them should be a problem at all.

- https://discuss.atom.io/t/syncing-settings-packages-between-machines/1385/10?u=bret

I also noticed that my .atom folder has a .gitignore in it, with the following:

storage
compile-cache
dev
.npm
.node-gyp
But I'd add to it:

.apm/
packages/
atom-shell/
I'd also like to see a packages.cson file so the references and preferences are kept, not the entire packages themselves.

https://discuss.atom.io/t/syncing-settings-packages-between-machines/1385/23?u=bret

## Intalling from stars

> If you mark your commonly-used packages with stars516 now, you can install them super-simple by typing: `apm stars --install`. [leedohm](https://discuss.atom.io/t/syncing-settings-packages-between-machines/1385/12?u=bret)

- [my stars](https://atom.io/users/bcomnes)


http://www.atomtips.com/how-to-synchronize-atom-between-computers/

## Plugins for syncing

https://atom.io/packages/package-sync
https://github.com/Hackafe/atom-sync-settings
