# GsmaeB

GsmaeB is a simple, modern Beamer theme suitable for anyone to use. It tries to minimize noise and maximize space for
content; the only visual flourish it offers is an (optional) progress bar added to each slide. The core design
principles of the theme were described in a blog post
[here](http://bloerg.net/2014/09/20/a-modern-beamer-theme.html).

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
4. **Use the theme for your presentation** by declaring `\usetheme{gsmaeb}` in the preamble of your Beamer document.

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

This theme is based on [Metropolis](https://github.com/matze/mtheme). If you've got questions about implementation
details, the [manual][] of Metropolis would be a good starting point. As we are
using [Beamer](https://github.com/josephwright/beamer),
the [user guide of beamer](http://ctan.yazd.ac.ir/macros/latex/contrib/beamer/doc/beameruserguide.pdf) will be helpful
too.

### File Structure

When user use `\usetheme{gsmaeb}` to using this theme, latex will be searching for `beamerthemegsmaeb.sty`, which is
generated from `beamerthemegsmaeb.dtx`. In `beamerthemegsmaeb.dtx` the following files are imported:

- `beamercolorthemegsmaeb.dtx`: Defines color related settings.
- `beamerfontthemegsmaeb.dtx`: Defines font related settings.
- `beamerinnerthemegsmaeb.dtx`: Defines how contents in each slide are presented.
- `beamerouterthemegsmaeb.dtx`: Defines format of headers and footers.

In addition, `beamerthemegsmaeb.ins` defines how the above `.ins` files converted into `.sty` files.

In most cases, files mentioned above are everything we might be editing. See more
at [Design a custom Beamer theme from scratch](https://tex.stackexchange.com/a/146682).

### Development Workflow

1. Run `git clone https://github.com/gsm-inspire/gsmaeb.git` to clone GitHub repo to local machine.
2. Make some modification on your local machine.
3. Follow the _Installation_ section to generate `.sty` files and upload them to Overleaf to make sure changes you've
   made is valid.
4. Run `git add *` to include all new file you've added locally.
5. Run `git comment -m {$comment}` to make a summary what changes you've made.
6. Run `git push -u origin main` to push local changes to GitHub.

## License

The theme itself is licensed under
a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).
This means that if you change the theme and re-distribute it, you *must* retain the copyright notice header and license
it under the same CC-BY-SA license. This does not affect the presentation that you create with the theme.

[manual]: http://mirrors.ctan.org/macros/latex/contrib/beamer-contrib/themes/metropolis/doc/metropolistheme.pdf
