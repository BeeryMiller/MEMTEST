                                     MEMTEST
                                      V2.60

In the early 90's, Ron Walters created the first memory expansion card for the
Geneve 9640.  He added a program with it's release, MEMTEST, written in 9640
Fortran.  To my knowledge, the source code did not survive and was never
released before he passed away.

Ron had provided me with a modified version of the program as one of the first
customers of the MEMEX that would run in a continuous loop retesting the memory
for errors.  Unfortunately over time, I lost my copy of that program.

In 2020, I started rewriting in assembly language a new version of the program.
I got sidetracked with other projects, and completed this release.  This
release does entail a few updates to the original design written by Ron Walters
including a test for zero or one wait state memory along with identification of
whether the Geneve is using the normal eprom or a PFM enhanced eprom.

When loading the program, the program tests various memory pages to identify the
hardware configuration.

Once it has identified the memory configuration, MEMTEST will begin testing
individual memory pages.  Non-existent or partial memory pages will be flagged
along with the appropriate type of memory present.  Upon completion of the
memory scan, the current available virtual memory map will be displayed over
the pages. If a bad memory page is encountered, an ERROR count will increment
and a line will be displayed on the screen identifying the last page where
a memory error occured.

Allowing the program to continue to run, the lower right corner will report
identified errors and will keep track of the number of complete passes as it
scans all 256 potential memory pages on each pass.

I do need to thank several people for their code contributions I have borrowed
and used within the program.  Willsy (AtariAge name / River Patroller) from
Uzbekistan contributed a segment of code I use that is loaded onto the
TMS-9995 internal ram that allows one to test memory without overwriting itself.
Insanemultitasker (AtariAge name) provided the segment of code permitting the
identification of the presence of the PFM.  Mike Riccio provided a piece of
code I borrowed from his original GEME code for the boxes for each individual
memory page.  Michael Zapf (mizapf AtariAge) provided the routines I use to
calculate whether the memory is zero or one wait state.  This should allow one
to identify whether they are using a modified Myarc 512K card or a MEMEX card
and it's current speed based on switch positions.

The source code is being released with this zipped file in the event updates
need to be released and/or someone needs to use this code for any future
hardware updates that may come along such as the potential Geneve 2020 project.

I do request should you find unexpected results in the display with this
program or something you do not understand, please post a photo on AtariAge of
the screen so we can work through the issue and update the program as necessary.

When running the program, one can press the spacebar to pause the current
display and press space bar to resume.  Or, one can press the <ESC> key or
control-C to exit the program.

Enjoy, and may your Geneve 9640 always be trouble free.

Beery Miller

