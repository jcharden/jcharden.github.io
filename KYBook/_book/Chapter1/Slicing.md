# Section1:Slicing

The defination of program slicing first appears in the paper "Program Slicing" on `IEEE TRANSACTIONS ON SOFTWARE ENGINEERING, VOL. SE-10, NO. 4, JULY 1984` by `MARK WEISER`.

> Program slicing is a method for automatically decomposing programs by analyzing their **data flow and control flow**. **Starting from a subset of a program's behavior**, slicing reduces that program to a minimal form **which still produces that behavior**. The reduced program, called a "slice," is an independent program guaranteed to represent faithfully the original program within the domain of the specified subset of behavior.
> Some properties of slices are presented. In particular, finding statement-minimal slices is in general unsolvable, but **using data flow analysis** is sufficient to find approximate slices. Potential applications include automatic slicing tools for debuggng and parallel processing of slices.


