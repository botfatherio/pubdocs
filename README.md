# Botfather Public Documentation

Anyone is welcome to make botfathers documentation more usefull by adding examples, writing guides and fixing errors.

There are conventions and requirements in order to make the documentation look consitent and keep it importable by the website.

## Good to know

All filenames and foldernames within `/docs` and `/static` must be [slugs](https://en.wikipedia.org/wiki/Clean_URL#Slug).

Document categories are named `doctypes`. To create a new doctype, add a new directory to `/docs` and create a new entry in `/doctypes.yaml`.

## File location and naming convention

The `docs` and `static` directories mirrors the website. The document `/docs/apiref/image.md` can be found on the website at `botfather.io/docs/player/image/`.

Static resources used by documents, such as images, belong in the `static` directory. Use relativ paths within documents to access static resources. Accessing static resources works on the website the same as locally.

Imagine the document `/docs/wizard/document-name.md`. Its static resources would be in `/static/docs/wizard/document-name/`. To access them from within the document use `../../static/docs/wizard/document-name/image.png`.

## Branches

Each major and minor botfather release may have its own git branch. Such branches shall be named after the release they belong to. Use the following format to do so: `major.minor.x`