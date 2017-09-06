# benizar/texlive
Docker container with a complete list of LaTeX tools installed.

*Check the [Dockerfile](Dockerfile) for versions and dependencies.*

This package list was generated by running `apt-cache depends texlive-full` and then excluding *-doc packages and other languages than spanish and english.

Maybe other packages are not required.


## Custom LaTeX resources

If you want to use any customized beamer theme, you can find inspiration in [The Ultimate Beamer Theme List](https://github.com/martinbjeldbak/ultimate-beamer-theme-list).

It is [recommended](http://tex.stackexchange.com/a/199480) not to put your custom themes into the official texmf directory. 

Create an appropiate folder:

```bash
mkdir -p $(kpsewhich -var-value TEXMFLOCAL)/tex/latex/beamer/
```

Copy your themes into that folder and then refresh the database:

```bash
texhash
```