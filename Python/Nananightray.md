# nananightray x PIP

## Command

All command x pthon and pip

### Install package

Use the file to download all the packages you need at once.  
To do this, run the following command :

` pip install -r requirements.txt `

or for ` macOS `

` pip3 install -r requirements.txt `

### Remove pip cache

For remove file on pip chache use `pip cache purge`

### Remove pip package

For remove a specific package ` pip uninstall package_name `

### Remove all package

[DOC](https://stackoverflow.com/a/11250821/21670678)

On Unix
`pip freeze | xargs pip uninstall -y`

On Windows
`pip freeze --exclude-editable | ForEach-Object { pip uninstall -y $_ }`

### pip Info

Check path ` which pip `  

Check version ` pip --version `
