# truecaps (v0.7)
Unicode TʀᴜᴇCᴀᴘꜱ with LuaLaTeX.

## Purpose

Tʜᴇ ᴘᴜʀᴘᴏꜱᴇ ᴏꜰ ᴛʜɪꜱ LᴜᴀLᴀTᴇX ᴘᴀᴄᴋᴀɢᴇ ɪꜱ ᴛᴏ ꜱᴇᴀᴍʟᴇꜱꜱʟʏ ᴘʀᴏᴠɪᴅᴇ ʀᴇᴀʟ Uɴɪᴄᴏᴅᴇ Sᴍᴀʟʟ
Cᴀᴘꜱ, ᴜꜱɪɴɢ ᴛʜᴇ Pʜᴏɴᴇᴛɪᴄ Exᴛᴇɴꜱɪᴏɴꜱ Uɴɪᴄᴏᴅᴇ ʙʟᴏᴄᴋ. (U+1D00 .. U+1D7F)

## Usage

`\usepackage{truecaps}` will provide a new command `\texttc{…}`, while
`\textsc{…}` continues to work as before.

### Full Example

```
\documentclass{article}

\usepackage{truecaps}

\usepackage{pifont}
	\def\mypointer{\raisebox{-1ex}{\llap{\LARGE\ding{43}~}}}

\usepackage{fontspec}
	\setmainfont[Ligatures={TeX,Common}]{Charis SIL}

\begin{document}

\noindent\texttc{\mypointer The purpose of this LaTeX package is to seamlessly
 provide real Unicode Small Caps, using the Phonetic Extensions Unicode
 block.}

\vspace{1.5em}
\noindent\textsc{\mypointer Classic Small Caps continue to work as before.}

\end{document}
```

## Supported Languages

Albanian • Bosnian • Catalan • Croatian • Czech • Danish • Dutch • Esperanto •
Estonian • Faroese • Finnish • French • Gaelic • German • Hungarian •
Icelandic • Italian • Latvian • Lithuanian • Luxembourgish • Moldovan •
Norwegian (Bokmål and Nynorsk) • Polish • Portuguese • Romanian • Romansh •
Serbian • Slovak • Slovene • Spanish • Swedish • Turkish • Vietnamese •
Welsh • Yoruba • others.

Basically, all letter characters from the "Latin-1 Supplement", the 
"Latin Extended-A" and B and the "Latin Extended Additional" Unicode blocks 
are fully supported.

## Todo

* Test suite for common Latin (European) languages (>80% done)
* Take care of punctuation and numbers (OTF features?)
* Look into support for more exotic Latin languages, perhaps some other
  African or Native American writing systems
* "silent" option "silent" to disable warnings (Letters X, Þ and others will
   have to remain unsupported for the foreseeable future)
* "oldstylesharps" option, to have ß written as SZ instead of SS 
* Sanity checks for missing glyphs?
* Normalize input? (= use only pre-composed glyphs)
* Simplify and optimize code, remove redundancies
* Some more documentation and examples
* Submit v1.0 to CTAN

## Known Issues

The glyphs produced by `truecaps` are from Unicode's “Phonetic Extensions”
block. They were never meant to be used as small caps the way we use them
here. CEDILLAS and OGONEKS can look ugly (ᴀ̨ ʜ̧ ᴋ̧ ᴊ̂ ᴊ̌ ɴ̧  ɪ̨) This is
especially true if you stack them (Looking at you, HORN!) (ᴏ̛̀ ᴏ̛́ ᴏ̛̉ ᴏ̛̃) 

Some of the language files (Turkish) need more work

## History
* v0.7 All usable characters (Latin-1 Supplement; Latin Extended-A, B; Latin
  Extended Additional) are fully supported now.
* v0.6 Internal code cleanup continues. Added support for Finnish, Slovenian,
  Icelandic (partial), Polish.
* v0.5 Reversed the command structure: `textsc{…}` continues to work as
  expected, `texttc{…}` becomes a new command.
* v0.4 Dropped XeLaTeX compatibility. Added support for Italian, Swedish,
  Danish, Icelandic, Serbian, Croatian.
* v0.3 Full support for Czech, Slovenian, Hungarian, Spanish and Catalan.
* v0.2 Full support for English, German and French.
* v0.1 Initial fork from निरंजन's "unisc.sty" v0.1
  (2022-04-21). https://puszcza.gnu.org.ua/projects/unisc
