# Pharos_documentation


clone the source files of Pharos Documentation
```bash
git clone  https://github.com/AdvanceServices/Pharos-Documentation.git
```


## install [MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)

```bash
docker pull squidfunk/mkdocs-material
```



## start MkDocs localhost server
run in PowerShell
```bash
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

open [localhost](http://localhost:8000/) to walk-through the documentation 
