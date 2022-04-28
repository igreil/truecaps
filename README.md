# truecaps (v0.5)
Unicode TʀᴜᴇCᴀᴘꜱ with LuaLaTex.

## Purpose

Tʜᴇ ᴘᴜʀᴘᴏꜱᴇ ᴏꜰ ᴛʜɪꜱ LᴀTᴇX ᴘᴀᴄᴋᴀɢᴇ ɪꜱ ᴛᴏ ꜱᴇᴀᴍʟᴇꜱꜱʟʏ ᴘʀᴏᴠɪᴅᴇ ʀᴇᴀʟ Uɴɪᴄᴏᴅᴇ Sᴍᴀʟʟ
Cᴀᴘꜱ, ᴜꜱɪɴɢ ᴛʜᴇ Pʜᴏɴᴇᴛɪᴄ Exᴛᴇɴꜱɪᴏɴꜱ Uɴɪᴄᴏᴅᴇ ʙʟᴏᴄᴋ. (U+1D00 .. U+1D7F)

## Usage

`\usepackage{truecaps}` will create a new command `\texttc{…}`. `\textsc{…}` continues to work as before.

### Full Example

```
\documentclass{article}

\usepackage{truecaps}
\usepackage{fontspec}
	\setmainfont[Ligatures={TeX,Common}]{Charis SIL}

\begin{document}

\noindent\texttc{The purpose of this LaTeX package is to seamlessly provide 
real Unicode Small Caps, using the Phonetic Extensions Unicode block.}\newline
\par
\noindent\textsc{Classic Small Caps continue to work as before.}

\end{document}
```

## Todo

* Add modifiers, accents, umlauts etc. for all letters. (70% done)
* Take care of punctuation and numbers
* Special cases like Ł, ß/ẞ etc. =>
* Testsuite for common Latin (European) languages (90% done)
* Full Support for 
	- `Basic Latin` (U+0000 .. U+007F), 
	- `Latin-1 Supplement` (U+0080 .. U+00FF), 
	- `Latin Extended-A` (U+0100 .. U+017F) and 
	- `Latin Extended-B` (U+0180 .. U+024F partial support)
	- possibly `Latin Extended Additional` (U+1E00 ..U+1EFF partial support)
* Modularization with `\input`
* Look into support for more exotic (Latin-based) languages, 
like Vietnamese, Yoruba and some other African or native American writing systems
* Add sanity checks for missing glyphs
* Silent option to disable warnings (Letter X will remain unsupported)
* Simplify and optimize code
* Submit to CTAN

## History

* v0.5 Reversed the command structure: `textsc{…}` works as always, `texttc{…}` becomes a new option.
* v0.4 Dropped XeLaTeX compatibility. Added support for Italian, Swedish, Danish, Icelandic.
* v0.3 Full support for Czech, Slovenian, Hungarian, Spanish and Catalan.
* v0.2 Full support for English, German and French.
* v0.1 Initial fork from निरंजन's "unisc.sty" v0.1 (2022-04-21).
https://puszcza.gnu.org.ua/projects/unisc

