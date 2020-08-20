# rm2gff3

**rm2gff3** converts [RepeatMasker](http://www.repeatmasker.org)'s `.out` output file (must include the original 3 lines header) onto a [gff3](http://www.sequenceontology.org/gff3.shtml) annotation file.

**For IGV users, the script also adds colors to the main TE classes.** This feature requires the following:
- The script considers TE headers to be on the Repeat Masker format --> **NAME#Order/Superfamily**
- **Orders**:LINE, SINE, DNA, LTR, RC, Low_complexity, Satellite and Simple_repeat will be colored
- All others Classes/Order will be colored in light grey
- Colors can be changed using HTML RGB syntax *e.g.: #3399ff*
- The script will parse any .out file regarding the format of the TE header, beware that in that case the coloring may be inconsistent

![](https://raw.githubusercontent.com/clemgoub/rm2gff3/master/Screenshot3.jpg)
List of colors (can be changed in script):
- LINE (blue, #3399ff)
- SINE (purple, #800080)
- DNA (salmon ,#ff6666)
- LTR (green, #00cc44)
- RC (orange, #ff6600)
- Low_complexity (grey/blue, #d1d1e0)
- Satellite (pink, #ff99ff)
- Simple_repeat (dark grey/blue, #8686ac)
- Unknown (grey, #f2f2f2)

![](https://raw.githubusercontent.com/clemgoub/rm2gff3/master/Screenshot1.jpg)
![](https://raw.githubusercontent.com/clemgoub/rm2gff3/master/Screenshot2.jpg)

## Usage
rm2gff3 is a simple shell script (bash) using awk to convert the .out into .gff3

`./rm2gff3.sh input.repeatmasker.out > output.gff3`

rm2gff3 can be piped but mind the 1 line header containing `##gff-version3`.

Please report **bugs** and **comments** in the [issue](https://github.com/clemgoub/rm2gff3/issues) sections.

Enjoy!
