# Visualize RPN proposals using pre-trained Faster RCNN detector

This repository contains jupypter notebook for qualitatively analyzing the quality of proposals obtained from a trained Region Proposal Network (RPN). Specifically support for topK and max-size proposals is provided.
<ol>
  <li>
  TopK: Plot topK RPN proposals on a given input image (order based on the objectness score of proposals)
  </li>
  <li>
  Max-Size: Take top32 proposals for a given image and plot the one which covers the maximum area within its bounding box
  </li>
  </ol>
  
## Installation
This repo is completely based on official detectron2 library. You will need to install the required packages by running the following commands.
```shell 
  # Install torch and torchvision
  pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113
  # Install Detectron2 (for more details visit : https://detectron2.readthedocs.io/en/latest/tutorials/install.html)
  python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'
  # Install matplotlib for visualizations
  python -m pip install -U matplotlib
  pip3 install Pillow
```
## Usage 

Simply run the cells of the notebook ```RPN_proposals.ipynb```, for getting started.

### Example
For top5 proposals on a given image, you can run the cell
``` shell
# TOP5
plot_RPN_proposals(image_file_name, 0, batched_inputs,proposals,5)
```
Sample Output:


  
