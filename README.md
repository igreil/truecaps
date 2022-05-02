# truecaps (v0.6.6)
Unicode TʀᴜᴇCᴀᴘꜱ with LuaLaTeX.

## Purpose

Tʜᴇ ᴘᴜʀᴘᴏꜱᴇ ᴏꜰ ᴛʜɪꜱ LᴜᴀLᴀTᴇX ᴘᴀᴄᴋᴀɢᴇ ɪꜱ ᴛᴏ ꜱᴇᴀᴍʟᴇꜱꜱʟʏ ᴘʀᴏᴠɪᴅᴇ ʀᴇᴀʟ Uɴɪᴄᴏᴅᴇ Sᴍᴀʟʟ
Cᴀᴘꜱ, ᴜꜱɪɴɢ ᴛʜᴇ Pʜᴏɴᴇᴛɪᴄ Exᴛᴇɴꜱɪᴏɴꜱ Uɴɪᴄᴏᴅᴇ ʙʟᴏᴄᴋ. (U+1D00 .. U+1D7F)

## Usage

`\usepackage{truecaps}` will provide a new command `\texttc{…}`, while `\textsc{…}` continues to work as before.

### Full Example

```
\documentclass{article}

\usepackage{truecaps}

\usepackage{pifont}
	\def\mypointer{\raisebox{-1ex}{\llap{\LARGE\ding{43}~}}}

\usepackage{fontspec}
	\setmainfont[Ligatures={TeX,Common}]{Charis SIL}

\begin{document}

\noindent\texttc{\mypointer The purpose of this LaTeX package is to seamlessly provide 
real Unicode Small Caps, using the Phonetic Extensions Unicode block.}

\vspace{1.5em}
\noindent\textsc{\mypointer Classic Small Caps continue to work as before.}

\end{document}
```

## Todo

* Add modifiers, accents, umlauts etc. for all letters. (A-O done fully, >80% all in all)
* Take care of punctuation and numbers (OTF features?
* Test suite for common Latin (European) languages (>80% done)
* Full Support for 
	- `Basic Latin` (U+0000 .. U+007F), done
	- `Latin-1 Supplement` (U+0080 .. U+00FF), WIP
	- `Latin Extended-A` (U+0100 .. U+017F), WIP
	- `Latin Extended-B` (U+0180 .. U+024F partial support), WIP
	- `Latin Extended Additional` (U+1E00 ..U+1EFF partial support), WIP
* Modularization with `\input` (>50% done)
* Look into support for more exotic (Latin-based) languages, 
like Vietnamese, Yoruba and some other African (Native American?) writing systems
* Normalize input (= use only pre-composed glyphs)
* Sanity checks for missing glyphs?
* Option "silent" to disable warnings (Letters X and Þ and others will remain unsupported for the foreseeable future)
* Option "oldstylesharps" to have ß written as SZ instead of SS 
* Simplify and optimize code, remove redundancies
* Some more documentation and examples
* Submit v1.0 to CTAN

## History

* v0.6.6 Number of supported glyphs: ~400 and counting. (A-O fully, including Vietnamese letters with double diacritics.)
* v0.6 Internal code cleanup continues. Added support for Finnish, Slovenian, Icelandic (partial), Polish.
* v0.5 Reversed the command structure: `textsc{…}` continues to work as expected, `texttc{…}` becomes a new command.
* v0.4 Dropped XeLaTeX compatibility. Added support for Italian, Swedish, Danish, Icelandic, Serbian, Croatian.
* v0.3 Full support for Czech, Slovenian, Hungarian, Spanish and Catalan.
* v0.2 Full support for English, German and French.
* v0.1 Initial fork from निरंजन's "unisc.sty" v0.1 (2022-04-21).
https://puszcza.gnu.org.ua/projects/unisc

