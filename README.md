# truecaps (v0.1.2)
True Unicode Small Caps with LuaLaTex/XeLaTeX

## Purpose

Tʜᴇ ᴘᴜʀᴘᴏꜱᴇ ᴏꜰ ᴛʜɪꜱ LᴀTᴇX ᴘᴀᴄᴋᴀɢᴇ ɪꜱ ᴛᴏ ꜱᴇᴀᴍʟᴇꜱꜱʟʏ ᴘʀᴏᴠɪᴅᴇ ʀᴇᴀʟ Uɴɪᴄᴏᴅᴇ Sᴍᴀʟʟ
Cᴀᴘꜱ, ᴜꜱɪɴɢ ᴛʜᴇ Pʜᴏɴᴇᴛɪᴄ Exᴛᴇɴꜱɪᴏɴꜱ Uɴɪᴄᴏᴅᴇ ʙʟᴏᴄᴋ. (U+1D00 .. U+1D7F)

## Usage

`\usepackage{truecaps}` will redefine `\textsc{…}` and additionally provide `\oldtextsc{…}`. There are no further options or parameters at this time. 

### Full Example

```
\documentclass{article}

\usepackage{truecaps}
\usepackage{fontspec}
	\setmainfont[Ligatures={TeX,Common}]{Charis SIL}

\begin{document}

\noindent\textsc{The purpose of this LaTeX package is to seamlessly provide 
real Unicode Small Caps, using the Phonetic Extensions Unicode block.}\newline
\par
\noindent\oldtextsc{The purpose of this LaTeX package is to seamlessly provide 
real Unicode Small Caps, using the Phonetic Extensions Unicode block.}

\end{document}
```
## Todo

* Add modifiers, accents, umlaute etc. for all letters.
* Take care of punctuation and numbers
* Special cases like Ŀ, ß/ẞ etc. =>
* Full Support for 
	- `Basic Latin` (U+0000 .. U+007F), 
	- `Latin-1 Supplement` (U+0080 .. U+00FF), 
	- `Latin Extended-A` (U+0100 .. U+017F) and 
	- `Latin Extended-B` (U+0180 .. U+024F)
	- possibly `Latin Extended Additional` (U+1E00 ..U+1EFF)
* Modularization with `\input`
* Add checks for missing glyphs
* Switch from `\oldtextsc{…}` and `\textsc{…}` to `\textsc{…}` and `\texttc{…}`
* Simplify code
* Testsuite for common Latin (European) languages
* Submit to CTAN

## History

*v0.1* Initial fork from निरंजन's "unisc.sty" v0.1 (2022-04-21).
https://puszcza.gnu.org.ua/projects/unisc

