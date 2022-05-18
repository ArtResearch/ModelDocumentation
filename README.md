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
run  PowerShell in Pharos-Documentation/ and then run:
```bash
docker run -d --rm -it -p 10000:8080 -v ${PWD}:/docs squidfunk/mkdocs-material
```

open [localhost](http://localhost:10000/) to walk-through the documentation 
