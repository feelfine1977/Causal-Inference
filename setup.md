uv venv causal-pymc-env --python python3.9
source causal-pymc-env/bin/activate
# Install the required packages from causal-pymc.yml
uv pip install numpy numba arviz matplotlib pandas scipy statsmodels pydot tqdm ipywidgets "pymc>=4" "CausalPy==0.0.8"
# Install the Jupyter kernel
uv pip install ipykernel
#register the kernel
python -m ipykernel install --user --name=causal-pymc-env --display-name="Python (causal-pymc-env)"
