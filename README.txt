Aspherical singlet following Wassermann-Wolf equations

Takatoshi Yamada, Ayase corporation

e-mail: takatoshi.yamada@ayasecorporation.com

web cite: https://www.ayasecorporation.com

##Aims of this repository

1.Aspherical lens design for everyone

You can design an aspherical singlet (single lens) only giving few
paraxial parameters and highest N.A.. If your parameters are consistent,
you can get your lens shape by typing few commands (evaluation of some
function written in Mathematica language) and show cross-section of the
lens and traced rays.

A demonstration file named “demonstrations.nb” shows the design
procedure for an aplanatic (free of both spherical and coma aberrations)
aspherical singlet step by step.

2. Demonstration of numerical integration of Wassermann-Wolf equation

Classic Wassermann-Wolf equation[1] is a set of simultaneous first-order
nonlinear ordinary differential equations and expresses what shape the
two aspheres of the singlet should have have when an incoming and
outgoing ray congruence (a bundle of consistent rays) are determined. A
file named “Wasserman-WolfAndFurther.nb” shows derivation of
Wassermann-Wolf equation from Snell’s law and formulae of numerical
integration of the equation for specific paraxial conditions.

Packages in this repository have a solver of the equation using
numerical integration, a ray tracer in meridional plane (i.e.,
two-dimensional) and other utilities. All packages and demonstration
codes are written in Mathematica (Wolfram language) and these can be
executed of course by Mathematica app. in Windows, macOS or linux also
by Mathematica bundled in Raspberry pi OS (former, called Raspbian).
Raspberry Pi 3B+ or 4B can execute the codes without user patience.

If you are not familiar to Mathematica, it is better to visit its
tutorial first.

3. Arousing other applications using Wassermann-Wolf equation

The classic equation are not limited for aplanatic singlet. An afocal
singlet and a gaussian-to-tophat converter are taken up in the
“Wasserman-WolfAndFurther.nb” as examples. These examples do not satisfy
aplanatism, but can be handled and determined by Wassermann-Wolf
equation. There may be many other applications of the equation.

To solve the equation, Mathematica may not necessarily required. Other
symbol manipulation systems such as Maple, SymPy+SciPy can also handle
the equation and perform its numerical integration. Furthermore, once a
specific application is formulated, numerical computations can be
written in a compiler language, which will increase execution
efficiency.

demonstrations.nb file

demonstrations.nb is a Mathematica notebook file and demonstrates
designing aspherical aplanatic singlets.

In the file, you can perform in turn,

1.  import DiffractionLimited package
2.  assign paraxial parameters for an infinite conjugate lens
3.  perform numerical integration to generate a solution of two
    aspherical surfaces as interpolation functions.
4.  show a lens shape solved and result of traced rays.
5.  show longitudinal aberrations, spherical aberration and OSC (Offense
    against the Sine Condition)
6.  fit the interpolation functions to aspherical formula.
7.  output text that can be read in Zemax as .zmx file.
8.  and other conditions, singlet with cover glass, finite conjugate,
    etc…

Wassermann-WolfAndFurther.nb

Wassermann-WolfAndFurther.nb shows deriving Wassermann-Wolf equations
from Snell’s law. In the file,

1.  Wassermann-Wolf equations from Snell’s law is derived
2.  classic Schwarzschild reflective telescope solution is followed
3.  explicit equations for infinite conjugate singlet are derived
4.  explicit equations for infinite conjugate singlet with a cover glass
    are derived
5.  explicit equations for finite conjugate singlet without cover
    glasses are derived
6.  explicit equations for finite conjugate singlet with cover glass in
    the image space are derived
7.  explicit equations for finite conjugate singlet with cover glass in
    the object space are derived
8.  explicit equations for finite conjugate singlet with cover glass in
    both spaces are derived
9.  explicit equations for afocal singlet are derived
10. explicit equations for one-dimensional gaussian-to-tophat converter
    are derived
11. Bessel beam generator is considered but it is not correct.

How to install:

for Raspberry Pi OS, run this script on the top level of the
demonstration directory.

    % sudo ./installPackages

for other OS, linux, macOS or Windows, move the DiffractionLimited
folder at anywhere on $Path, for example, on macOS,

  ~/Library/Mathematica/Applications/

[1] G.D.Wasermann,E.Wolf, “On the Theory of Aplanatic Aspheric Systems”
Proc.Phys.Soc.B62,2 (1949) ## Descriptions of files
