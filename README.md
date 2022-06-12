# Minimal autotools example

Also see https://www.gnu.org/software/automake/manual/html_node/Autotools-Introduction.html

## Dependencies

```
sudo apt install automake autoconf make
```

## Developer usage

```
autoreconf --install  # creates scripts and makefile
./configure           # configures default settings
make dist             # creates tarball with source code, configure script, and makefile
```

## Builder usage

From the extracted tarball, build as usual:

```
./configure
make
sudo make install
```

## Compile comands for LSP (CCLS)

Use bear (`sudo apt install bear`).
Running bear with the compile command creates the database needed by the lsp.

```
autoreconf --install
./configure
bear -- make
```
