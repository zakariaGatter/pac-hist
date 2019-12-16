# pac-hist

## Table of Contents

- [About](#about)
- [Quick Start](#quick-start)
- [Using Pac-hist](#using-zshing)
- [Examples](#examples)
- [TODO](#todo)

## About

[Pac-hist] Pacman Log Viewer

[Pac-hist] allows you to...

* List all Actions in log file
* List by Action
* List by Date
* Search for a Package
* Search for a Package in a Date
* Search for a Package with a Action

[Pac-hist] automatically...

* check for correct Date or Action

[Pac-hist] is undergoing an interface change, please stay up to date to get latest changes.

## Quick Start

1. Introduction:

   Installation requires :
    * [Coreutils](https://www.gnu.org/software/coreutils) for Everything else

2. Set up [Pac-hist]:

	``` bash
	git clone https://github.com/zakariaGatter/pac-hist.git ~/brash
	mkdir -p ~/.local/bin
	cp ~/pac-hist/bin/pac-hist ~/.local/bin
	chmod +x ~/.local/bin/pac-hist
	```

## Using Pac-hist

```
PAC-HIST(16-12-2019) Pacman Log Viewer
Usage: pac-hist [OPTIONS] ...

OPTIONS:
 -a <ACTION>    Search for giving ACTION
 -d <DATE>      Set Date and Time to search
 -s <PKG>       Searh for Special Package
 -l             List Search resoult
 -h             Show this help dialog

ACTIONS:
 install; remove; reinstall; upgrade; downgrade

DATE:
 Date Syntax: YYYY-MM-DD HH:MM:SS
```

## Examples

* Show everything in the log

    `pac-hist -l`

* Show everything with a action

    `pac-hist -a install -l`

* Show everything with a action and a date

    `pac-hist -a install -d "2019-10-21 13:38:00" -l`

* Search for package

    `pac-hist -s socklog-void`

* Search for package with action

    `pac-hist -a install -s socklog-void`

* Search for package with action and date

    `pac-hist -a install -d "2019-10-21 13:38:00" -s socklog-void`

## TODO
[Pac-hist] is a work in progress, so any ideas and patches are appreciated.

[Pac-hist]:http://gitlab.com/zakariagatter/pac-hist
