# Latent Walk

We're using the Pytorch implementation of Stylegan2, available [here](https://github.com/NVlabs/stylegan2-ada-pytorch).

There was no need to change the code as it contains everything to easily train on a new dataset. The one we used in the project contains a little more than 800 images. The dataset is available on the lab's server. It was created using the `dataset_tool.py` script as follows: 

`python dataset_tool.py --source /home/ambroise/dataset/delany_cropped --dest /home/ambroise/dataset/delany_cropped.zip --width=1024 --height=1024`

or 

 `python dataset_tool.py --source /home/ambroise/dataset/delany_cropped --dest /home/ambroise/dataset/delany_cropped_without_resize.zip`
 
This creates a zip containing the images needed to train the model. 

The model can then be trained using: 

`python train.py --outdir /home/ambroise/stylegan_log --data /home/ambroise/dataset/delany_cropped_without_resize.zip --cfg stylegan2`

Other configurations are listed on the repository of Stylegan2. 
