# Snort Listings Syntax Highlighting in LaTeX

## Example

LaTeX Code:

    \documentclass{article}
    \usepackage{listings}
    \usepackage{color}
    \usepackage{textcomp}
    
    \lstset{
      language=Snort
    }
    
    \begin{document}
    
    \title{A LaTeX Listing in \LaTeX}
    \date{\today}
    \maketitle
    
    \begin{lstlisting}
	    alert tcp any any -> any any (msg:"A TCP message was detected."; sid:100001)
    \end{lstlisting}
    
	\end{document}
  
![Example:](https://github.com/adlerzei/snort-listings/blob/master/example.png)

## Installation

The `snort-listings` directory must be on your TeX search path.

To use LaTeX from the Bash shell, add this to your shell config file (e.g. `.bashrc`):

    export TEXINPUTS=/path/to/snort-listings/:$TEXINPUTS
    
For Emacs, use:

    (setenv "TEXINPUTS" (concat "/path/to/snort-listings/:" (getenv "TEXINPUTS")))

As an alternative you can insert `lst-snort.sty` into an arbitrary folder and add the following line into your TeX file:
  
    \input{/path/to/lst-snort/lst-snort.sty}
