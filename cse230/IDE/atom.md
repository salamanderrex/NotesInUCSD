Since Mac OS X does not 10.11 `El Capitan`  does not support haskell cabal yet. https://github.com/haskell/cabal/issues/2653

(EI Caption has some rootless new feature. )

We use linux to build our IDE here.

## Install ATOM
https://atom.io/

##  Install Haskell for ubuntu
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

The last line to enable to directly in your current shell. If you use some other shell, like zsh, you can run the last line every time you run atom. OR add to you shell environment.

## Install hlint
### If you can use cabal, good idea
```
cabal install happy
cabal install hlint
cabal install ghc-mod
```
- happy is a dependency for hlni
- hlint is a lint for haskell
- ghc-mod is for a Atom package, install it , it is good for you

If cabal tells you cannot locate hlint, then `  cabal update `

### if you want to stack, bad idea
If you want to use ` stack `, I recommend you just give up.  `stack` seems to have problem here. Of course, I know someone success use `stack` here. If you install the hlint success fully ,remembet to run atom in stack environment.
```
stack exec atom .
```
if you are a window user
```
stack exec atom.cmd .
```

## packages for haskell in atom
you can install package by
```
apm install package
```
or, in graphic mode
```
open Atom
open setting (command + ,)
b```
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
