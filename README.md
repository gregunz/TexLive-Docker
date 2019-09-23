# TexLive-Docker

A Docker container running on Ubuntu with TexLive full system 

## How to use

### Example 1: `docker run ...`

```bash
docker run -it --rm -v cd /path/to/dir/:/opt/app/ gregunz/texlive filename.tex
```

Note that `/path/to/dir/` should be the absolute path to the directory where `filename.tex` and its dependencies are stored.
The command run is the one defined in the Dockerfile as entrypoint (pdflatex).
It can be overriden using the `--entrypoint` argument.

For example for the `latex` command:

```bash
docker run -it --rm -v $(pwd):/opt/app/ --entrypoint latex gregunz/texlive filename.tex
```


### Example 2: `pdflatex filename.tex`

Set an alias:

```bash
pdflatex='docker run -it --rm -v $(pwd):/opt/app/ gregunz/texlive'
```

And use it that way:

```bash
cd /path/to/dir/
```

```bash
pdflatex filename.tex
```

You can setup an alias that way for each command you use regularly.

## Issues ?

Any problems? Also remarks appreciated, just open an issue.

gregunz.
