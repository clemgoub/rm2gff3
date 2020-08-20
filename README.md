# rm2gff3

[](Screenshot1.jpg)

**rm2gff3** converts the ".out" output file of RepeatMasker (this file must include the original 3 lines header) to a [gff3](http://www.sequenceontology.org/gff3.shtml) annotation file. **For IGV users, the script also adds colors to the main TE classes:**
- The script considers TE headers to be on the Repeat Masker format --> **NAME#Order/Superfamily**
- **Orders**:LINE, SINE, DNA, LTR, RC, Low_complexity, Satellite and Simple_repeat will be colored
- All others Classes/Order will be colored in light grey
- Colors can be changed using HTML RGB syntax *e.g.: #3399ff*
- The script will parse any .out file regarding the format of the TE header, beware that in that case the coloring may be inconsistent
