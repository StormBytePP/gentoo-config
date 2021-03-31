# Gentoo Config
This repository will contain all /etc/portage files needed for the correct functions of Gentoo's portage (except profile, which is selected by eselect profile xx)

# Branches
Configuration will be stored in branches according to target system, like stage3, stage3-generic, stage4 and so (see definitions below)

# Definitions

## stage3
Stage3 contains the basic system to be used as a base for more complete systems, this is not bootable and only contains system basic stuff
*IMPORTANT*: Stage3 should not contain any USE variable which is not part of the inner core system, example: unicode IUSE is OK, python IUSE is ok, but X, bluetooth, and others are not in this step.

## stage4
Containing all of stage3 with the additions of any USE variable to make a CLI only bootable system
*IMPORTANT*: Stage4 should not contain any USE that enables any graphical framework (no X, no KDE, etc)

## stage5
Containing all of stage4 with the additions of any USE variable to make a full desktop system, no limitations here regarding USE flags but no DE should be installed here

## stage6
Containing all of stage5 but with a DE flavor installed
