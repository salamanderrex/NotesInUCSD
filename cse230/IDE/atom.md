Since Mac OS X does not 10.11 `El Capitan`  does not support haskell `cabal` yet. https://github.com/haskell/cabal/issues/2653

(EI Caption has some rootless new feature. )
You can try to disable it by

- In recovery mode. `csrutil`
- Or, `sudo nvram boot-args="rootless=0";sudo reboot`

However, I fail in both way.

Of course, a workaroud is to use `homebrew` to do all the thing. Someone made it in this way.


I choose to use linux to build our IDE here.

## Install ATOM
https://atom.io/

##  Install Haskell for ubuntu
If you use other sys, use this [link](https://www.haskell.org/downloads)
```
sudo apt-get update
sudo apt-get install -y software-properties-common
sudo add-apt-repository -y ppa:hvr/ghc
sudo apt-get update
sudo apt-get install -y cabal-install-1.22 ghc-7.10.3
cat >> ~/.bashrc <<EOF
export PATH="\$HOME/.cabal/bin:/opt/cabal/1.20/bin:/opt/ghc/7.10.3/bin:\$PATH"
EOF
export PATH=~/.cabal/bin:/opt/cabal/1.22/bin:/opt/ghc/7.10.3/bin:$PATH
```

The last line add PATH to your current shell. If you use some other shells, like zsh, you can run the last line every time before you run atom. Or add to your shell environment path.

## Install hlint
### If you can use cabal, good idea
```
cabal install happy
cabal install hlint
cabal install ghc-mod
```
- `happy`  is a dependency for hlnit
- `hlint` is a lint for haskell
- `ghc-mod` is for Atom package. Install it , it is good for you

If cabal tells you cannot locate hlint, then `  cabal update `

### If you want to use stack, bad idea
If you want to use ` stack `, I recommend you just give up.  `stack` seems to have problems here.

 I know someone success use `stack`(use homebrew to install) to install `hlint`. If you install the hlint in this way successfully ,remember to run atom in stack environment.
```
stack exec atom .
```
if you are a window user
```
stack exec atom.cmd .
```

## packages for haskell in atom
you can install packages by
```
apm install package
```
or, in graphic mode
```
open Atom
open setting (command + ,)
```
| install following packages |
|:---------------------------|
| autocomplete-haskell       |
| haskell-ghc-mod            |
| hover-tooltips-hdevtools   |
| linter                     |
| linter-hdevtools           |
| linter-hlinter             |

## End
Ok, now you are all set. Enjoy the homework. :smiling_imp:
