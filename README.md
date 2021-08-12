# ODH s2i Jupyter Notebook Minimal Python 3.9


## 1. Build Image

Clone https://github.com/jupyter-on-openshift/jupyter-notebooks
Under jupyter-notebooks/minimal-notebook add the Dockerfile-py39 file
Build the image:
  
  podman build --file Dockerfile-py39 --tag quay.io/repo/image:tag
  
  podman push 
  
  
 ## 2. Create image stream on Openshift in the ODH project's name space.
 
 Use image stream sample, replacing your image with above created image. The magic happens in the annotations, spefically opendatahub.io/notebook-image tags, which will be used to display the information when starting a notebook server in Jupyter Hub.
