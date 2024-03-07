#Instal library split-folders
!pip install split-folders

#Impor library yang diperlukan
from google.colab import files
from tensorflow.keras.preprocessing.image import ImageDataGenerator
from keras.preprocessing import image
import time
import zipfile,os
import splitfolders
import tensorflow as tf
import matplotlib.pyplot as plt
import numpy as np

#Download data
!wget --no-check-certificate https://github.com/dicodingacademy/assets/releases/download/release/rockpaperscissors.zip -O /content/rockpaperscissors.zip

#Install Root Directory, Ekstrak ZIP, dan Sortir Data
root_dir="/content/data"

#Extrak ZIP
local_zip="/content/rockpaperscissors.zip"
zip_ref=zipfile.ZipFile(local_zip,"r")
zip_ref.extractall(root_dir)
zip_ref.close()
