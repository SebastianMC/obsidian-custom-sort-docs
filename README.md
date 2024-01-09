# obsidian-custom-sort.github.io
Documentation for obsidian-custom-sort plugin for Obsidian.md



# Building the documentation

Using docker `squidfunk/mkdocs-material` instead of local installation

- source of documentation exits in `/src` of this repository
  - this local folder is mapped onto `/docs` in the docker container - MkDocs expects source in that location
- target documentation site is generated to `/docs` of this repository
  - Github Pages expects this exact location to be the root of website to be published Github Pages
  - the docker container folder `/generated-site` is mapped onto the `/docs` local (repository) folder
- the command to build documentation with the above setup is, when invoked from the repository root folder is:
  - `obsidian-custom-sort-docs % docker run --rm -it -p 8000:8000 -v ${PWD}/src:/docs -v${PWD}/docs:/generated-site squidfunk/mkdocs-mate
rial build --site-dir /generated-site`
