📊 Dataset Overview
This dataset consists of 2,624 grayscale images, each with a resolution of 300×300 pixels and 8-bit depth. The images represent both healthy and defective solar cells exhibiting various levels of degradation. These cells were extracted from 44 unique solar modules.

Defects shown in the dataset fall into two categories:

Intrinsic

Extrinsic

Both types are known to impact the power efficiency of the solar panels.

All images have been preprocessed to maintain a uniform size and orientation, and any distortions introduced by the camera lens during EL imaging were corrected before cell extraction.

🏷️ Image Annotations
Each image in the dataset includes:

A defect probability score (a float between 0 and 1)

The type of solar module it came from — either:

monocrystalline

polycrystalline

Image data is stored in the images/ directory, while annotations are found in the labels.csv file.

🛠️ Loading the Data in Python
To load the dataset programmatically, you can use the load_dataset() function provided in utils/elpv_reader.py:

python
Copy
Edit
from elpv_reader import load_dataset

images, proba, types = load_dataset()
This will return:

images: a list of loaded image objects

proba: a list of defect probabilities

types: a list of module types