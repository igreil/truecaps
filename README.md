# truecaps
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

## History

*v0.1* Initial fork from निरंजन's "unisc.sty" v0.1 (2022-04-21).
https://puszcza.gnu.org.ua/projects/unisc

