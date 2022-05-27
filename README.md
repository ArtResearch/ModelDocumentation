# Artresearch_documentation


clone the source files of Artresearch Documentation
```bash
git clone https://github.com/ArtResearch/ModelDocumentation.git
```


## install [MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)

```bash
cd ModelDocumentation/
docker pull squidfunk/mkdocs-material
```



## start MkDocs localhost server
(run in PowerShell if you are in Windows and) run:
```bash
docker run -d --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

open [localhost](http://localhost:8000/) to walk-through the documentation

## start MkDocs cloud server with Let's Encrypt
(run in PowerShell if you are in Windows and) run:
```bash
docker-compose up -d
```

