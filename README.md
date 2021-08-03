# GsmaeB

GsmaeB is a simple, modern Beamer theme suitable for anyone to use. It tries to minimize noise and maximize space for
content; the only visual flourish it offers is an (optional) progress bar added to each slide. The core design
principles of the theme were described in a blog post
[here](http://bloerg.net/2014/09/20/a-modern-beamer-theme.html).

Not convinced? Have a look at the [demo slides][].

![Sample](https://gsminspire.com/wp-content/uploads/2021/08/gsmaeb_screenshot.png)

## Installation

Installing GsmaeB from source, like any Beamer theme, involves four easy steps:

1. **Download the source** with a `git clone` of the [GsmaeB repository](https://github.com/yongzhengqi/gsmaeb).
2. **Compile the style files** by running `make sty` inside the downloaded directory. (Or run LaTeX directly
   on `source/beamerthemegsmaeb.ins`.)
3. **Move the resulting `*.sty` files** to the folder containing your presentation. To use Metropolis with many
   presentations, run `make install`
   or move the `*.sty` files to a folder in your TeX path instead (might require
   `sudo` rights).
4. **Use the theme for your presentation** by declaring `\usetheme{GsmaeB}` in the preamble of your Beamer document.
5. **For best results** install Mozilla's [Fira Sans](https://github.com/bBoxType/FiraSans).

## Usage

The following code shows a minimal example of a Beamer presentation using GsmaeB.

```latex
\documentclass{beamer}
\usetheme{gsmaeb}           % Use GsmaeB theme
\title{A minimal example}
\date{\today}
\author{Gsm Inspire \LaTeX Team}
\institute{Guanghua School of Management, Peking University}
\begin{document}
   \maketitle


   \section{First Section}
   \begin{frame}{First Frame}
      Hello, world!
   \end{frame}
\end{document}
```

## Development

This theme is based on [Metropolis](https://github.com/matze/mtheme). If you've got more questions about implementation
details, you could refer to the [manual][] of Metropolis.

## License

The theme itself is licensed under
a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
This means that if you change the theme and re-distribute it, you *must* retain the copyright notice header and license
it under the same CC-BY-SA license. This does not affect the presentation that you create with the theme.


[demo slides]: http://mirrors.ctan.org/macros/latex/contrib/beamer-contrib/themes/metropolis/demo/demo.pdf

[manual]: http://mirrors.ctan.org/macros/latex/contrib/beamer-contrib/themes/metropolis/doc/metropolistheme.pdf

[CTAN]: http://ctan.org/pkg/beamertheme-metropolis
