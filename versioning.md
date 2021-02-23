# Fivnex Versioning Guidelines
This guideline sheet is to help Fivnex developers with versioning. To keep versioning consistent,
these Guidelines have been set up. This guide is set up into sections by type. 

> NOTE: This is for versioning identifiers, NOT for version names. Versioning names are custom to every project.

## Hardware
All hardware components sold by Fivnex will follow the same versioning schemes. There are TWO scheme
types in hardware. INCRE, and SERIES.

### Hardware: INCRE Versioning
INCRE simply means to increase or more specifically, increment. INCRE versioning in Fivnex is very simple,
if you can count, without skipping numbers, this will be easy. INCRE has 3 sub-types, PROTO, POC, and
RELEASE models. PROTO is just short for prototype, which are usable designs that will set the guidelines
for the final product. POC, which is just proof of concepts, are hardware designs, similar to prototypes but
different in that POC products do not set any final design guidelines. Lastly is RELEASE, you can guess what
this is. Each of these has their own identifier. The list of identifiers is below:

```
PROTO   : PR
POC     : PX
RELEASE : RL
```

> Note that for RELEASE models, the identifier is OPTIONAL.

Let's show examples of a first generation PC group. The name for these will be Maka for the PROTO, Mako for the POC, and Maku for the release. Here is how all of these versioning schemes work.

```
Maka PR1
Mako PX1
Maku RL1
Maku 1 // If chosen to remove prefix for RELEASE versions
```

----
 
### Hardware: SERIES versioning
SERIES versioning is a versioning scheme that releases into series. SERIES identifiers start with one to three letter string, depending on the SERIES line. Next is the iteration number, which as hardware upgrades increments by one. The final OPTIONAL item is the final issue identifier. Like in Intel's CPU's, each line MIGHT have a higher powered or more experimental version of the hardware. There are 4 FII (Final Issue Identifiers) that new products can use.

```
E : Experimental
M : More powerful
X : Cheaper/Budget
I : Servers 
```

SERIES line letters and iteration numbers all are different, depending on the product. Hardware developers are not forced to stick with any specific setup.

In an example of a SERIES versioning scheme, there is a CPU's second line called the LZ, it is on iteration 2, and they are releasing versions with all 4 FIIs. Here is how the versioning scheme looks in action. For context, let's call the CPU line the Compi.

```
Compi LZ02E
Compi LZ02M
Compi LZ02X
Compi LZ02I
```

----

## Desktop Applications (DA)
Desktop applications include graphical applications, as well as CLIs built for users or businesses. There are 8 versioning types, SER1, SER2, SER3, SER4, SER5, SER6, SER7, SER8. I know, creative names. Each one of these is simple, 