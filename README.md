# PyConfluenceToWikijs

**Note:** forked from [icl-rocketry/PyConfluenceToWikijs](https://github.com/icl-rocketry/PyConfluenceToWikijs)

Python scripts used to convert the Confluence based wiki to a format that is usable with Wiki.js.

Based loosely on [this tool by gkpln3](https://github.com/gkpln3/ConfluenceToWikiJS), though ported to python, and with enhanced capability.

Features:

 - Preserved page hierarchy, converted to use folders
 - Files renamed to their title rather than just their ID
 - Working links between pages
 - Working images
 - Working non-image attachments (though no previews)
 - HTML not formatted as a single line (which is what confluence does by default)
 - Metadata (page edit times) preserved, and saved to the footer of each page

## Usage

```py
# Inside the cloned repo
from wiki import Wiki

# Change the following three values as required
INPUT = "./Confluence-space-export-111123.html/EXAMPLE/"
TITLE = "EXAMPLE"
OUT_DIR = "./converted_output/"

wiki = Wiki(input_folder=INPUT, wiki_name=TITLE)
wiki.convert_pages()
wiki.export_pages(output_dir=OUT_DIR)
```
