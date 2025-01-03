# mosaik2-gui
A simple GUI I created for mosaik2. The aim is to make creating a mosaic as simple as possible.  
This gui project is in no way "official", I'm just not good at picking names so I just called it what it is. Also, I am not a good ui designer, so please feel free to create a better gui frontend.

# mosaik2
The real magic is done by mosaik2 (https://f7a8.github.io/mosaik2/). If you want to have more control over the creation I highly recommend taking a look at the mosaik2 command line (https://github.com/f7a8/mosaik2)

# Flatpak
The Flatpak build is the only supported build of mosaik2-gui. It is not yet on Flathub, but I want to put it there after it is better tested.

## building the Flatpak manually
If you want to build and install the flatpak manually from the source in this repository, you can do it this way:

First, clone this repository:  
`git clone https://github.com/Best-HeyGman/mosaik2-gui.git`

Then, make sure you have flathub added as a repository:  
`flatpak remote-add --if-not-exists --user flathub https://dl.flathub.org/repo/flathub.flatpakrepo`  

Create the build dir:  
`mkdir flatpak-builddir`

Build and install:  
`flatpak-builder --user --force-clean --install ./flatpak-builddir ./mosaik2-gui/flatpak/com.github.Best_HeyGman.mosaik2-gui.yml`

Clean up the builddirs:  
`rm -r flatpak-builddir .flatpak-builder`