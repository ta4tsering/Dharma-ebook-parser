## Prerequisite

### Data format
 
 Input Data is

- Dharma ebook(.epub)

Dharma Ebook[link](https://gitlab.com/bdrc-data/etextcontents).
### Environment Setup

 - python version 3.8 >=

    Python installation in windows: Refer to this [link](https://www.tutorialspoint.com/how-to-install-python-in-windows)

    Python comes by default for Linux and Mac users.

 - git
    
    Refer this [link](https://git-scm.com/downloads) for git installation

 - Requirements:
    - `pip install openpecha`
        
        Openpecha toolkit
        To install the openpecha toolkit run this line on your cmd or terminal.
    
    - `pip install BeautifulSoup`

    - `pip install uuid`


    **Note**: You need to install pip. 
    
    [Pip installation](https://pip.pypa.io/en/stable/installation/) 

## Usage

    ```
    from pathlib import Path
    from openpecha.formatter.dharma_ebook import ebook_to_opf


    if __name__=='__main__':   
        epub_name = "ཇོ་མཇལ་ཁྲིད་ཡིག་ཡིད་བཞིན་ནོར་བུ།"
        epub_path = Path(f"./data/epubs/{epub_name}")
        data_path = Path("./data")
        pecha_path = ebook_to_opf(epub_path, data_path)
    ```
- First you need to import `Path` from `pathlib` ,`ebook_to_opf` function from `dharma_ebook` module.
- Then you need to give a pecha_id or if you sent None it will create standard Openpecha pecha id.
- you will need to create a folder called data and then a folder called epubs and put the dharma ebook (.epub) in the epubs folder.
- next you will us the name of the ebook to create the `epub_path` and `data_path`.
- After that you will pass those paths and to create the opf of the epub.
- If the script runs without any error it will return the `pecha_path`.

**Note**

You will be required to have the ebook in .epub format. 