{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Extract all zip files from a folder"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Install libraries and import into workspace"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [],
   "source": [
    "\n",
    "import os, zipfile\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Loop through all files in a folder and unzip "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [],
   "source": [
    "zip_dir = \"INSERT DIRECTORY"   \n",
    "for subdir, dirs, files in os.walk(zip_dir):\n",
    "    for zipp in files:\n",
    "        filepath= os.path.join(subdir, zipp)\n",
    "        zip_ref = zipfile.ZipFile(filepath, 'r')\n",
    "        zip_ref.extractall(zip_dir)\n",
    "        zip_ref.close()"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
