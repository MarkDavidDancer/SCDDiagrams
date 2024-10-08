# SCDDiagrams

## Purpose

`SCDDiagrams` produces diagrams used in the full instructions for 
Scottish Country Dances in the R.S.C.D.S. style.

The diagrams are produced in SVG format, so they can be resized 
without looking pixelated (A0 diagrams anyone?), and can be easily 
embedded in many word processing and page layout programs. SVG can 
be easily converted into PNG and other bitmapped formats if need be
(the converse is not the case).

Note: `SCDDiagrams` does ***not*** produce diagrams in the Pillings 
or Keith Rose styles.

## Who might benefit from this program

`SCDDiagrams` is a solution for anyone wanting to produce high quality diagrams 
for Scottish Country Dancing. It *may* also be suitable for producing dances for:
- English Country Dance;
- Australian Colonial Dance;
- Contradance; and
- other styles of social dancing done in sets.

## What are S.C.D. Diagrams?

Scottish Country Dancing is a form of social dancing which evolved 
from the assemblies and ballrooms of the 17th, 18th and 19th 
centuries. Unlike couples dancing like ballroom dancing, in S.C.D. 
the dancers are traditionally arranged in longwise sets of dancers 
(small groups of dancers in lines—think of dancing in Jane Austen 
movies), in square (quadrille) sets, or in circles around the room. 
Modern dances may also be danced in triangles and other formations. 
You can learn more about Scottish Country Dance from the 
[Royal Scottish Country Dance Society](https://rscds.org/).

The dances are described by written instructions, which are often 
supplemented by diagrams. These diagrams have taken on a standard 
form, with a “top is at the bottom” orientation†, specific symbols 
for both male and female dancers, indicators for which direction 
they are facing, hand holds, and lines of movement. A typical S.C.D. 
diagram is as below:

![Example S.C.D. Diagram](docs/assets/example.png)

† the diagrams are drawn from the teacher’s perspective. The obvious 
analogy is turning a map upside down when travelling from north to 
south.

## Project History: Why this program?

As hosts of the 2001 Australian Winter School, the Queensland 
Branch of the R.S.C.D.S. published a book of dances (entitled 
*2001: A Dance Odyssey*). As hosts of the winter school in 2024, 
we originally decided to republish the book. At first this intended 
to be just reissuing the book as is, but it was then decided we 
would publish a revised and expanded book:
- bringing the dances in to line with current R.S.C.D.S. terminology 
and formatting; and
- add dances which had been written since the book was first 
published.

One of our big problems was that we no longer had an electronic copy 
of the original book. As the original book was not to R.S.C.D.S.
standards of its day, the text needed to be retyped. The diagrams *could* 
have been simply scanned and pasted into the new book, but this had a 
number of issues:
- there would be a stylistic difference between the diagrams for the 
dances from the 2001 and the new edition;
- some of the older dances really needed a few extra diagrams added; and
- the original printing was done a quite a low resolution, and the 
diagrams (and text) looked pixelated.

Between the old and the new dances, we needed to produce almost 60 diagrams. 
As the person designated to produce them, I will be the first to admit I have 
as much artistic ability as a lump of putty, so I looked for a program that 
could assist with the diagrams.

Searching the archives of the 
[Strathspey mailing list](https://www.strathspey.org/) showed there were a 
number of requests for such a program, but none were available.

Searching for 
diagramming tools threw a a swathe of candidates, which basically fall into 
two camps:
- generic drawing programs like [Inkscape](https://inkscape.org/), which are 
very powerful in the hands of the artistically talented, but provide no 
assistance for drawing structured diagrams; and
- diagramming programs like [Dia](http://dia-installer.de/index.html.en), which 
create structured digrams specific to domains like flowcharts and UML diagrams, 
but provide no assistance when used outside those domains (and features like 
automatic path routing are actually a hinderance).

The result was I wrote some [Python](https://www.python.org/) code that provided 
a domain specific solution. It had no user interface (it was just a back end 
that drew the diagrams—the front end was code to directly call the back end 
routines), but it produced some very nice diagrams for the book with considerably 
less hair tearing than trying to draw them manually.

Once the revised book was published and Winter School was over, I found I was 
still using the program for my own dances, so I decided to make it available to 
other dance devisors. This means:
- getting it set up as a modern project with all the bells and whistles like 
automated test suites (“that diagram looks right” isn’t going to cut it). Since 
the last time I worked as an application developer was sometime around 1990, and 
that was using CSP on an IBM mainframe (a.k.a. the Jurassic period), this has 
meant learning all about things like:
  - GUIs ([Qt for Python](https://www.qt.io/qt-for-python)) since running batch 
scripts isn’t end user friendly
  - automated testing suites ([PyTest](https://docs.pytest.org/en/stable/))—we 
had actual users sit down with hand-written scripts typing stuff into the screens 
and checking the output was what was on the paper;
  - source code control and repositories ([Git](https://git-scm.com/) & 
[GitHub](https://github.com/))—we had a source and binary library at each level of
development, test, and production, and moved the code and modules up and down 
between the levels (having batch scripts to do this was considered state of the 
art);
  - continuous integration ([Jenkins](https://www.jenkins.io/));
  - documentation from code ([Sphinx](https://www.sphinx-doc.org/en/master/))—code 
was on the mainframe, documentation was in Word;
- getting it restructed into something more logical that one script;
- designing/implementing a user interface;
- designing/implementing a file structure;
- getting it packaged so an end user can install it (on multiple platforms).

## Getting started

Sorry, but at the moment it's just check out the source from GitHub. More coming.

## Getting help

Awaiting a alpha release.

## Contributing

Not yet in a state where contributions make sense.
