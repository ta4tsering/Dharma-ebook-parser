## Prerequisite

### Data format
 
The buda apis used in the function to parse instance information are :

- https://purl.bdrc.io/graph/<instance_id>.trig
- https://purl.bdrc.io/graph/<work_id>.trig
- https://purl.bdrc.io/graph/<sub_text_id>.trig

You will also require the base text files ready which can be downloaded from this [link](https://gitlab.com/bdrc-data/etextcontents).
### Environment Setup

 - python version 3.8 >=

    Python installation in windows: Refer to this [link](https://www.tutorialspoint.com/how-to-install-python-in-windows)

    Python comes by default for Linux and Mac users.

 - git
    
    Refer this [link](https://git-scm.com/downloads) for git installation

 - openpecha toolkit
    
    To install the openpecha toolkit run this line on your cmd or terminal.
 
    `pip install openpecha`

    **Note**: You need to install pip. 
    
    [Pip installation](https://pip.pypa.io/en/stable/installation/)
 - You need to set your GitHub token as an environment variable. 

## Usage

    ```
    from pathlib import Path
    from openpecha.formatter.bdrc import creat_opf


    instance_id = "IE00KG08439"
    opf_path = Path('./data/opfs')
    base_text_dir = Path('./data/base_texts')
    create_opf(instance_id, base_text_dir, opf_path)
    ```
- First and foremost you need to import `Path` from `pathlib` and `create_opf` function from `bdrc` module.
- Then you need to initialize instance id.
- You need to prepare base text files in the base text directory. You will then initialize the base_text_dir
- Next step is to initialize the path where you want to save the opf
- After that, you need to call the `create_opf` function by passing initialized instance id, base text directory path, and opf path
- If the script runs without any error your opf will be ready at opf path you have mentioned above. 

**Note**

You will be required to have an internet connection as instance information will be extracted from the buda api responses of the instance you are going to parse. 