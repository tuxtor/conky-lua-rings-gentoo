conky-lua-rings-gentoo
======================

A little customisation of [Conky Lua Rings][0] with Gentoo website colors and Gentoo logo.

Example:

![Settings](https://raw.github.com/tuxtor/conky-lua-rings-gentoo/master/example.png)

Features:
* Adapted for 8 cores
* Exactly the same colors of Gentoo website
* Compatible with Guayadeque (depends on conkyGuayadeque)
* Added a status bar for the battery
* Added last portage sync
* Added nvidia GPU temperature

How to instal it:
* As the original conky script edit the conkyrc and change the line: ${font ubuntu:size=12}${color FFFFFF}${alignr}${weather http://weather.noaa.gov/pub/data/observations/metar/stations/ LQBK
LQBK my city, find the code for your city: http://weather.noaa.gov
* Copy clock_rings.lua to: ~/.lua/scripts
* Copy conkyrc to ~/.conkyrc file
* Copy Gentoo logo to ~/.conky/gentoo-logo.png

Other:
* If you don't use guayadeque just comment the line ${color 7A5ADA}${font ubuntu:size=8}Guayadeque: ${color FFFFFF} ${execi 10 conkyGuayadeque --datatype=AR -n} - ${execi 10 conkyGuayadeque --datatype=TI -n}
* If you don't have an nvidia chip just comment the line ${color 7A5ADA}${font ubuntu:size=8}GPU: ${color FFFFFF} ${nvidia temp} degrees 

Dependencies:
* app-admin/conky with at least "X imlib iostats lua lua-cairo lua-imlib nvidia wifi" use flags enabled
* app-admin/conkyguayadeque (available at sunrise overlay)
* media-fonts/ubuntu-font-family

Licence:
WTFPL - [Do What The Fuck You Want To Public License][1]
The name "Gentoo" and the "g" logo are currently trademarks of [Gentoo Foundation, Inc][2]

[0]: http://gnome-look.org/content/show.php/Conky+lua?content=139024
[1]: http://en.wikipedia.org/wiki/WTFPL
[2]: http://www.gentoo.org/main/en/name-logo.xml
