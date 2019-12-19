
# Extract all zip files from a folder

### Install libraries and import into workspace


```python

import os, zipfile

```

## Loop through all files in a folder and unzip 


```python
zip_dir = "INSERT DIRECTORY NAME"   
for subdir, dirs, files in os.walk(zip_dir):
    for zipp in files:
        filepath= os.path.join(subdir, zipp)
        zip_ref = zipfile.ZipFile(filepath, 'r')
        zip_ref.extractall(zip_dir)
        zip_ref.close()
```
