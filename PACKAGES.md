# Files in a folder AplanaticSinglet

Takatoshi Yamada @AYASE Co.,Ltd.

e-mail: takatoshi.yamada@ayasecorporation.com

web cite: https://www.ayasecorporation.com

AplanaticSinglet folder includes Mathematica packages of main part of aplanatic singlet solver and other utilities.

### in the AplanaticSinglet directory

#### Package files:

```
% ls -l *m
-rw-r--r--  1 yamada  staff   6478  7 30 16:25 AsphericalFittingForInterpolated.m
-rw-r--r--  1 yamada  staff  39607  7 30 16:25 BiasphericAplanatSolver.m
-rw-r--r--  1 yamada  staff  11416  7 30 16:25 BiasphericAplanatZemaxOutput.m
-rw-r--r--  1 yamada  staff   5223  7 30 16:25 GoldenSectionSearch.m
-rw-r--r--  1 yamada  staff  39440 10  6 12:09 RayTrace2D.m
-rw-r--r--  1 yamada  staff  22465  7 30 16:25 SingletParaxialConsistency.m
```



#### and their notebook files:

```
% ls -l *nb
-rw-r--r--  1 yamada  staff   36449  7 30 16:25 AsphericalFittingForInterpolated.nb
-rw-r--r--  1 yamada  staff  332084  7 30 16:25 BiasphericAplanatSolver.nb
-rw-r--r--  1 yamada  staff  296424  7 30 16:25 BiasphericAplanatSolverB.nb
-rw-r--r--  1 yamada  staff   50255  7 30 16:25 BiasphericAplanatZemaxOutput.nb
-rw-r--r--  1 yamada  staff   28843  7 30 16:25 GoldenSectionSearch.nb
-rw-r--r--  1 yamada  staff  290325 10  6 12:09 RayTrace2D.nb
-rw-r--r--  1 yamada  staff  104535  7 30 16:25 SingletParaxialConsistency.nb
```

The package files .m are automatically made from these notebook files by Mathematica.

#### Zemax compatible medium files:

```
% ls -l *agf *.AGF
-rw-r--r--  1 yamada  staff  679474  7 30 16:25 OHARA.AGF
-rw-r--r--  1 yamada  staff   14824  9  8 18:03 SCHOTTextracted.AGF
```

AGF files can be downloaded from each glass manufacturers. These two files are only for demonstration. "SCHOTTextracted.AGF" file is extracted from SCHOTT.AGF because the original file is very big.

## To show symbol descriptions in a package

All packages can show short messages about usage. To show the message, First load a package

```
Needs["AplanaticSinglet`BiasphericAplanatSolver`];
```

and ask

```
?AplanaticSinglet`BiasphericAplanatSolver`*
```

then all symbols are listed.

To show a usage message about specific symbol, ask

```
?AplanaticSinglet`BiasphericAplanatSolver`designWavelength
```

or only clicking on a text in the list, then shows

> designWavelength is a parameter for the solver specifying the wavelength to fix a refractive indices of materials.

Some packages have "Example" section at the bottom of each file to show simple explanation of its usage.

## Simple description of each packages

#### BiasphericAplanatSolver.m:

BiasphericAplanatSolver package performs numerical integration to solve the WW equation set for given paraxial conditions.

#### SingletParaxialConsistency.m:

SingletParaxialConsistency package checks given paraxial parameters to be consistent and fixes values of dependent parameters.

#### RayTrace2D.m

RayTrace2D package traces rays in a meridional plane, i.e., 2-dimensional trace, and draws lens outlines and traced rays.

#### GoldenSectionSearch.m

GoldenSectionSearch package performs a simple golden-section search for one parameter. It can be used to find aberration minimum for a parameter such as CSF (lens bending), lens thickness, etc...

#### BiasphericAplanatZemaxOutput.m

BiasphericAplanatZemaxOutput package outputs a string that can be read in Zemax as a lens definition. But currently the package can not produce a *.zmx file because a file that is made by other app. but Zemax can not be read in Zemax. However, it is currently not possible to create *.zmx files because Zemax cannot read files created by other applications.

Therefore, to read in Zemax app.,

1. make a blank file by Zemax
2. open the .zmx file in a text editor
3. copy and paste the produced string by the package into .zmx file
4. re-open in Zemax

If someone knows how to make a zmx file outside Zemax, please let me know.