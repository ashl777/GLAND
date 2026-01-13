Installation
============

Follow these steps to set up GLAND on your local machine. We recommend using a Conda environment to maintain a clean workspace and manage dependencies effectively.

1. Clone the Repository
-----------------------
Start by cloning the GLAND repository from GitHub and entering the project directory:

.. code-block:: bash

   git clone https://github.com/CSUBioGroup/GLAND.git
   cd GLAND

2. Environment Setup
--------------------
Create a new Conda environment with Python 3.8 and activate it:

.. code-block:: bash

   conda create -n GLAND python=3.8
   conda activate GLAND

3. Install Dependencies
-----------------------
GLAND requires several core bioinformatics and deep learning libraries. You can install all necessary packages directly using the provided ``requirements.txt`` file:

.. code-block:: bash

   pip install -r requirements.txt

4. Install R Dependencies (Optional)
------------------------------------
For high-performance spatial clustering using the ``mclust`` algorithm, you need to have R installed and the ``mclust`` library available in your environment:

.. code-block:: bash

   # Install R base
   conda install -c conda-forge r-base=4.0.3

   # Install mclust package inside R
   R -e "install.packages('mclust', repos='http://cran.us.r-project.org')"

.. note::
   If you are using a GPU, please ensure that your PyTorch installation is compatible with your local CUDA version (e.g., CUDA 11.7). You may need to reinstall a specific version of ``torch-scatter`` and ``torch-sparse`` if you encounter compatibility issues.
