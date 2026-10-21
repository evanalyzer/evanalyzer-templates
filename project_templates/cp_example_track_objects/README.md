This example identifies the nuclei of a time-lapse movie frame by frame and tracks them from frame to frame. Each sequence is analyzed independently; export the tracks with `evanalyzer cli export csv --group-by track`.

About these images:

A portion of a time lapse movie of a syncytial blastoderm stage Drosophila embryo with a GFP-histone gene which renders chromatin fluorescent in live embryos. The movie shows nuclear divisions 10 through 13.

Victoria Foe made this movie on a Bio-Rad Radiance 2000 laser scanning confocal microscope using a 40X 1.3NA oil objective. The frames are 7 seconds apart.

GFP-histone transformed files provided by Rob Saint.

V. Foe and G. Odell, 26 July 2001

The 21 RGB frames of each CellProfiler sequence folder are combined into one gray time stack per sequence (`Sequence1.tif` ... `Sequence3.tif`, gray = (R+G+B)/3 like CellProfiler's ColorToGray 'Combine').
