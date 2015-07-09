# tvh.build.tmp
Temporary sandbox for trying out pbuilder

Just playing around...

Informal testing of the pbuilder approach inside docker. Depending if it works or not - can then be moved over into a proper repository.

## Starting point

    [23:38] <@adamsutton> just try this:
    [23:38] <@adamsutton> sudo apt-get install qemu-user-static pbuilder-dist
    [23:38] <@adamsutton> pbuilder-dist sid armhf create
    [23:38] <@adamsutton> git clone tvheadend.git
    [23:38] <@adamsutton> cd tvheadend
    [23:38] <@adamsutton> TVH_BUILD="sid:armhf" ./support/pbuilder
    [23:38] <@adamsutton> I think...

## Pbuilder guides & reference materials

http://jodal.no/2015/03/08/building-arm-debs-with-pbuilder/

https://wiki.ubuntu.com/PbuilderHowto#Building_an_i386_pbuilder_on_amd64

https://wiki.ubuntu.com/ARM/BuildArmPackages

https://wiki.debian.org/PbuilderTricks

https://pbuilder.alioth.debian.org/

## Others?

sbuilder - not as simple?

http://askubuntu.com/questions/53014/why-use-sbuild-over-pbuilder

cross-compiling from scratch?

https://github.com/tvheadend/tvheadend-build#cross-compiling-for-arm

I'm going to assume / accept adam's recommendation that `pbuilder` is the better solution and investigate that first foremost.

