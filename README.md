[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/simonsfoundation/Th17_TRN_Networks/master)

# Th17_TRN_Networks

This repository contains interactive visualization of transcriptional regulatory networks and gene expression data from:

[Miraldi et al., Leveraging chromatin accessibility for transcriptional regulatory network inference in T Helper 17 Cells](https://genome.cshlp.org/content/early/2019/02/19/gr.238253.118).



The repository has been designed to run in the cloud based Binder service.
Click the binder link above to launch a binder container running the notebooks


The repository is designed to use 
[`repo2docker`](https://repo2docker.readthedocs.io/en/latest/)
to build a `docker` container which includes
the code for running the analysis and all needed dependencies.
The `repo2docker` tool requires the `docker` infrastructure
and Python 3 to run.  See the 
[installation instructions](https://repo2docker.readthedocs.io/en/latest/install.html).

To build the docker image from the command line

```bash
jupyter-repo2docker --no-run \
    --image-name th17 \
    https://github.com/simonsfoundation/Th17_TRN_Networks
```

To run the image after it has been built use `docker run`:

```bash
docker run -it --rm -p 8888:8888 th17:latest
```

When the docker instance starts up the log output looks like this:

```
[I 19:34:40.443 NotebookApp] Writing notebook server cookie secret to /home/rstudio/.local/share/jupyter/runtime/notebook_cookie_secret
[I 19:34:40.935 NotebookApp] Serving notebooks from local directory: /home/rstudio
[I 19:34:40.935 NotebookApp] 0 active kernels
[I 19:34:40.935 NotebookApp] The Jupyter Notebook is running at:
[I 19:34:40.935 NotebookApp] http://0.0.0.0:8888/?token=7baca1829f0665df26adf9943c6f04279647171eb3ffd12c
[I 19:34:40.935 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[W 19:34:40.935 NotebookApp] No web browser found: could not locate runnable browser.
[C 19:34:40.936 NotebookApp] 
    
    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://0.0.0.0:8888/?token=7baca1829f0665df26adf9943c6f04279647171eb3ffd12c
```

Paste the `http:...` URL into your browser including your token (which will be different
from the one shown above) to connect to the Jupyter server.  
