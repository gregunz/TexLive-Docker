# TexLive-Docker
A Docker container running on Ubuntu with TexLive full system 

## How to use

### Example 1: `pdflatex filename.tex`

```bash
docker run -it --rm -v <path>:/opt/app/ gregunz/texlive <filename.tex>
```

Note that `<path>` here should be the absolute path to the directory where `<filename.tex>` and its dependencies are stored.

I personnaly set an alias like that:

```bash
pdflatex='docker run -it --rm -v $(pwd):/opt/app/ gregunz/texlive'
```

And use it that way:

```bash
cd <path>
```

```bash
pdflatex <filename.tex>
```

Remarks appreciated, just open an issue.

gregunz.
