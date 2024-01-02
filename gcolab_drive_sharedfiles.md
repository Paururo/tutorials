# Google Colab: Add Shared files

Paula Ruiz Rodríguez 

2024-01-02

Google Colab allows you to add shared drive files to your workspace. To do this, you first need to get a share link from the file you want to add. Then, in Google Colab, you can use the 'google.colab' module to import files from Google Drive.

**IMPORTANT:** To work with shared folders that are NOT owned by you, you have to add a shortcut to your local folder:

Import the 'google.colab' module with the following command:

```python
from google.colab import drive
```

Next, mount your Google Drive in the runtime with this command:

```python
drive.mount('/content/drive')
```

Finally, you can access your shared files. Replace 'path_to_your_file' with the path of the file you want to add:

```python
with open('/content/drive/My Drive/path_to_your_file', 'r') as f:
  file_content = f.read()
```

This process allows you to work with shared files directly in Google Colab.
