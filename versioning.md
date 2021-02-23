# Fivnex Versioning Guidelines
This guideline sheet is to help Fivnex developers with versioning. To keep versioning consistent,
these Guidelines have been set up. This guide is set up into sections by type. 

> NOTE: This is for versioning identifiers, NOT for version names. Versioning names are custom to every project.

## Hardware
All hardware components sold by Fivnex will follow the same versioning schemes. There are TWO scheme
types in hardware. INCRE, and SERIES.

### Hardware: INCRE Versioning
INCRE simply means to increase or more specifically, increment. INCRE versioning in Fivnex is very simple,
if you can count, without skipping numbers, this will be easy. INCRE has three sub-types, PROTO, POC, and
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
 
### Hardware: SERIES Versioning
SERIES versioning is a versioning scheme that releases into series. SERIES identifiers start with one to three letter string, depending on the SERIES line. Next is the iteration number, which as hardware upgrades increments by one. The final OPTIONAL item is the final issue identifier. Like in Intel's CPU's, each line MIGHT have a higher powered or more experimental version of the hardware. There are 4 FII (Final Issue Identifiers) that new products can use.

```
E : Experimental
M : More powerful
X : Cheaper/Budget
I : Servers 
```

SERIES line letters and iteration numbers all are different, depending on the product. Hardware developers are not forced to stick with any specific setup.

In an example of a SERIES versioning scheme, there is a CPU's second line called the LZ, it is on iteration two, and they are releasing versions with all four FIIs. Here is how the versioning scheme looks in action. For context, let's call the CPU line the Compi.

```
Compi LZ02E
Compi LZ02M
Compi LZ02X
Compi LZ02I
```

----

## Software
Software applications include graphical applications, as well as CLIs built for users or businesses. There are eight versioning types, SER1, SER2, SER3, SER4, SER5, SER6, SER7, SER8. I know, creative names. Each one of these is simple, with simple rules for numbering. 

These are known as the SERX (Sear Ex, or Serix (as in Series but with an ending of an X and not S)) standards. Software Release X. 

> Operating Systems do NOT fall under the "Software" category in versioning, please read Operating Systems as there are different standards for versioning.

### SER1 Versioning
SER1 versioning is a very simple process, with no prefix or suffixes. There are three numbers. The format is simply X.YY.ZZZ, and the numbers are simple. Let's go through each section. 

X is for the release type identifier. X will be set to one of three numbers: 0, 1, 2. These numbers have special meanings:

```
0 : Indev testing/experimental release
1 : Mainline Release
2 : Indev upcoming release
```

For the YY, which can be ANY length of numbers, but it starts off with two. This is the release number itself. This goes up incrementally per included feature release.

For the final ZZZ, these are bug fix notifiers. This goes incremental per bug/security patch.

> Please note that bug/security patch numbers are ALWAYS (in SER1) connected to the release number.

To show an example, we will show an app's 3 versions for an application that is on release 23, and on it's 203rd patch. They are working on release 24, and testing release 25, each having their own bug/security patches.

```
0.25.004
1.23.203
2.24.002
```

### SER2
SER2 uses the format XX.YY.ZZZ. YY and ZZZ, like in SER1, are release and patch respectively. However, these change every year there is a release. The XX represents the year.

> Also note, that in SER2, the release number and patch number are separate from each other.

Let's say in the year 2021, a piece of software releases its 10th edition for the year, and it's 201st bug/security patch that year. Here is how the versioning will look like this year, and for the 1st release in 2022.

```
21.10.201
22.01.000
```

### SER3
The Fivnex SER3 standard is the most simple. XX.YYY. XX represents release number, YYY represents the patch number for that version.

For example, a piece of software release version 22, with 8 patches. 

```
22.008
```

### SER4
SER4 uses the date of release. YY.MM.DD. YY is for the last two digits of the year, MM is for the month, DD for the day. 

> SER4 is the ONLY Fivnex SERX versioning scheme WITHOUT patch numbers

Say a release of a piece of software comes out on April 30, 2021.

```
21.04.03
```

### SER5
SER5 versioning follows a YY.MM.ZZZ format. YY being the last two digits of the year, and MM being the month. The final ZZZ is the patch number.

In SER5 versioning, patch numbers DO NOT count as releases, and do not affect the rest of the version number, regardless when the patch was created. 

Let's say a release came out in April 2021, but eight months later the 192nd patch for said software releases.

```
21.04.192
```

### SER6
In SER6 versioning, the format is X.YY.ZZZ. The X is the edition number, which can be defined by the software developer on when to advance an edition. The YY is the release number. ZZZ is the patch release for the release. 

Say an application is on edition four, release 23, and a 4th patch is release.

```
4.23.004
```

### SER7
SER7 release numbers are the string of numbers for the release date, followed by the patch number. The format for the date is YYYYMMDD, or full year, month, date. 

For example, 2 patches were released with a release on April 30, 2021.

```
20210430.002
```

### SER8
SER8 is not a unique release format, but rather an optional change developers can make to certain aspects to the other formats. There are only four SER8 systems. 

For more information on how to label using a SER8 modification read the section entitled "How to label which SERX format you use?" which is written directly after the SER8 section.

#### SER8-1
In SER8-1, you are able to remove the preceding zeros of any patch number. Taking an example from SER7, `20210430.002` would instead be `20210430.2` 

#### SER8-2
In SER8-2, you can make up to three modifications to the date format:

1. Change the year format to be the full year (2021) or to instead be only two digits (21)
2. Change the month format to remove the preceding zero from the month (for months that prefix zero)
3. Change the day formate to remove preceding zeros from the day (for days that prefix zero).

#### SER8-3
SER8-3 allows you to change the date format to:
- DDMMYYYY
- YYYYMMDD
- DDMM
- MMDD
- MMYYYY
- YYYYMM

You only label using SER8-3 if changing the date format in the first place

#### SER8-4
The SER8-4 system basically allows you to add one of a preset group of letter prefixes. Developers are allowed to use multiple prefixes in any order they wish.

> Using ANY of these prefixes results in use of SER8-4.

```
A - Alpha (pre-release)
B - Beta (pre-release)
R - Release
T - Testing
E - Experimental
P - Private
C - Commercial
```

### How to label which SERX format you use?
If the developers are not using SER8 modifications, they simply label which SERX versioning standard you are using (i.e SER6, SER7). Developers are not allowed to change versioning standards (outside of SER8-listed modifications), nor are they allowed to mix and match aspects of each SERX standard.

Picking a SERX standard only shows you plan to use a standardized format in your project. Projects that use SERX standards SHOULD be labeled and link back to this document.

> NOTE: While optional, SERX standards are always able for change, and it is a recommendation. It also helps the standard be standardized.

#### For Fivnex
> This part is for developers within the Fivnex group (the same people who made these standardizations), if you do not work for, or on fivnex projects, please ignore this section.

If you are a Fivnex developer, meaning you develop anything for the developer group Fivnex, you HAVE to use SERX standards, and you HAVE to link back to them.

#### SER8 Modifications
When using SER8 modifications, listing them is different. You list them as SER8, with the selected modifications (in numerical order), and the original SERX standardization.

For example, if you were to use SER5, with SER8-1, SER8-2, and SER8-4, you will list the standard as:
```
SER8-124-5
```

The specific format is
```
SER8-ABCD-E
```

with ABCD being the SER8 modification you use, and the E being the original SERX version. 

> Developers only list the modifications in use. If you only use one of the four modifications, you only list the single modification (EX: SER8-1-7).

> Developers MUST list modifications in numerical order (EX, using SER8-1, SER8-3, and SER8-4, on SER7: SER8-134-7, NOT SER8-143-7)

> Developers MUST put both of the hyphens (only the two separating SER8 and the modified standards, and the modified standards and the original standard number) in SER8 modified standards. (EX: SER8-134-7. DO NOT USE: SER8-1347,SER81347, SER8-1-3-4-7, etc.) 

----

&copy; Fivnex;