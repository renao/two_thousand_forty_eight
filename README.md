[travis]: https://travis-ci.org/neopoly/two_thousand_forty_eight

# 2048

Console based "2048" game.

[![Travis](https://img.shields.io/travis/neopoly/two_thousand_forty_eight.svg?branch=master)][travis]

## Game rules

* 2048 is played on a plain 4×4 grid, with numbered tiles that slide when a player moves them.
* Every turn, a new tile randomly appears in an empty spot on the board with a value of either 2 or 4.
* Tiles slide as far as possible in the chosen direction until they are stopped by either another tile or the edge of the grid.
* If two tiles of the same number collide while moving, they will merge into a tile with the total value of the two tiles that collided.
* The resulting tile cannot merge with another tile again in the same move.
* If a move causes three consecutive tiles of the same value to slide together, only the two tiles farthest along the direction of motion will combine. If all four spaces in a row or column are filled with tiles of the same value, a move parallel to that row/column will combine the first two and last two.


## Example

```shell
$ bin/two_thousand_forty_eight
```

Assume "WASD"-control:

* w: up
* a: left
* s: down
* d: right

```shell
[     ] [     ] [    2] [     ]
[     ] [     ] [     ] [     ]
[     ] [     ] [    2] [     ]
[     ] [     ] [     ] [     ]
```

Moves up:

```shell
[     ] [     ] [    4] [     ]
[    2] [     ] [     ] [     ]
[     ] [     ] [     ] [     ]
[     ] [     ] [     ] [     ]
```

Moves left:

```shell
[    4] [    2] [     ] [     ]
[    2] [     ] [     ] [     ]
[     ] [     ] [     ] [     ]
[     ] [     ] [     ] [     ]
```

### Many moves later...

```shell
[   64] [   16] [     ] [     ]
[   16] [    8] [    4] [    2]
[    4] [    2] [     ] [     ]
[    4] [     ] [     ] [    4]
```


## Setup

Fork from https://github.com/neopoly/two_thousand_forty_eight

```shell
git clone git@github.com:YOURNAME/two_thousand_forty_eight.git
cd two_thousand_forty_eight
gem install bundler
```

Install ruby-2.7.0 and ensure version with:

```shell
ruby -v # => 2.7.0
```

Install dependencies with:

```shell
bundle
```

## Test

```shell
 $ rake test
```

## Development

A test driven approach is appreciated.

Tests should be written with `minitest/spec` syntax using minitest assertions.
