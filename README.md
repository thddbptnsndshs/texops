# TeXOps 

A simple instrument for creating TeX projects from a cookie-cutter template. Three project types are available:

:page_facing_up: **paper** -- regular paper-style A4 document<br>
:mailbox: **abstract** -- abstract (like paper but more space-efficient)<br>
:chart_with_upwards_trend: **poster** -- beamer poster in <a href="https://github.com/anishathalye/gemini">Gemini theme</a><br>
:name_badge: **slides** -- beamer presentation<br>

## Installation

1. Clone the texops directory to your home directory:

`cd ~`<br>
`git clone git@github.com:thddbptnsndshs/texops.git`<br>

2. Move the texops file with a zsh script to `/usr/local/bin`:

`sudo cp ~/texops/texops /usr/local/bin/`<br>

3. Give necessary access permissions to the script:

`cd /usr/local/bin` <br>
`sudo chmod -x .texops`<br>
`sudo chmod 755 texops`<br>

4. Open the `~/.zshrc` file and append the following lines:

`texops() {`<br>
   `bash ~/texops/texops $1 $2}`<br>

5. Restart your Terminal. Done!

## Usage

Open Terminal and use the `texops` command:

`texops [-a | -p | -P | -s] -t <path/to/working/dir>`

:pushpin: `-a` -- abstract<br>
:pushpin: `-P` -- paper<br>
:pushpin: `-p` -- poster<br>
:pushpin: `-s` -- slides<br>
:pushpin: `-t` -- add a file with templates<br>

The working directory is initialised by the command. The following files appear:

:paperclip: `slides.tex`, `paper.tex`, `abstract.tex' or `poster.tex` -- TeX code<br>
:paperclip: `images/` -- image directory<br>
:paperclip: `ref.bib` -- empty bibliography file<br>
:paperclip: `templates.tex` -- file with useful code pieces for formatting tables, examples, etc.<br>
:paperclip: `.sty` style files (poster format only)<br>
