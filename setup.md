uv venv causal-pymc-env --python python3.9
source causal-pymc-env/bin/activate
# Install the required packages from causal-pymc.yml
uv pip install numpy numba arviz matplotlib pandas scipy statsmodels pydot tqdm ipywidgets "pymc>=4" "CausalPy==0.0.8"
# Install the Jupyter kernel
uv pip install ipykernel
#register the kernel
python -m ipykernel install --user --name=causal-pymc-env --display-name="Python (causal-pymc-env)"
# install pytorch for macOS
# conda has to be installed
conda env create -f causal_book_py39.yml
conda activate causal_book_py39
conda install -c conda-forge python-graphviz
brew install graphviz
python -m ipykernel install --user --name=causal_book_py39 --display-name="Python (causal_book_py39)"