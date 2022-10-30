# TeXOps 

A simple instrument for creating TeX projects from a cookie-cutter template. Three project types are available:

:page_facing_up: **handout** -- regular paper-style A4 document<br>
:chart_with_upwards_trend: **poster** -- beamer poster in [https://github.com/anishathalye/gemini](Gemini theme)<br>
:name_badge: **slides** -- beamer presentation<br>

## Installation

1. Clone the texops directory to your home directory:

`cd ~
git clone git@github.com:thddbptnsndshs/texops.git`

2. Move the texops file with a zsh script to `/usr/local/bin`:

`sudo cp ~/texops/texops /usr/local/bin/`

3. Give necessary access permissions to the script:

`cd /usr/local/bin 
sudo chmod -x ./desktop
sudo chmod 755 desktop`

4. Open the `~/.zshrc` file and append the following lines:

`texops() {
   bash ~/texops/texops $1 $2
}`

5. Restart your Terminal. Done!

## Usage

Open Terminal and use the `texops` command:

`texops [-h | -p | -s] <path/to/working/dir>`

:pushpin: `-h` -- handout, paper-style<br>
:pushpin: `-p` -- poster<br>
:pushpin: `-s` -- slides<br>

The working directory is initialised by the command. The following files appear:

:paperclip: `slides.tex`, `handout.tex` or `poster.tex` -- TeX code<br>
:paperclip: `images/` -- image directory<br>
:paperclip: `ref.bib` -- empty bibliography file<br>
:paperclip: `templates.tex` -- file with useful code pieces for formatting tables, examples, etc.<br>
:paperclip: `.sty` style files (poster format only)<br>
