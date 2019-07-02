# Deep_CLEM

## Install and run Fiji plugin DeepCLEM

**1. Install Fiji**

[source](https://imagej.net/Fiji/Downloads)


**2. Install Fiji plugin CSBDeep**

[source](https://github.com/CSBDeep/CSBDeep_website/wiki/CSBDeep-in-Fiji-%E2%80%93-Installation)


**3. Clone this repo**

```sh
git clone https://github.com/Rickmic/Deep_CLEM.git
cd Deep_CLEM
```

**4. Copy Deep_CLEM.py into your Fiji.app/plugins directory**

```sh
cp Deep_CLEM.py [path to Fiji]/Fiji.app/plugins/
```

**5. Restart Fiji**

Now you should be able to finde the plugin (Plugins > Deep_CLEM)

**6. Start Deep_CLEM**


<ul>
  <li>
    <p align="justify">
      If you run the plugin Deep_CLEM, the following window should be visible:
    </p>
  </li>
</ul>



<p align="center"> 
  <img src="../assets/GUI1.png">
</p>


<ul>
  <li>
    <p align="justify">
      Select an electron microscopic image, a light microscopic image, several light microscopic channels of interest, a   working directory and a model file. After that select Run.
    </p>
  </li>
  <li>
    <p align="justify">
      If you have selected show process dialog, the process window of CSBDeep will be visible.</li>
    </p>
  </li>
</ul>



<p align="center"> 
  <img src="../assets/GUI2.png">
</p>


<ul>
  <li>
    <p align="justify"> 
      After a short time (depending on your CPU/GPU) another window will be visible. This window shows you the electron microscopic and the predicted ligth microscopic image. Check if the predicted light microscopic image shows roughly the shape of the chromatin in the electron microscopic image and proceed with OK. 
    </p>
  </li>
  <li>
    <p align="justify"> 
      If the plugin is ready you can see <i>Command finished: Deep CLEM</i> in the Status Bar.
    </p>
  </li>
    <li>
      <p align="justify"> 
        Deep CLEM has created two directories and one xml file in the working directory. The directory <i>COIoutput</i> contains the images of the channels of interest, that are already aligned to the electron microscopic image. The Directory <i>output</i> contains the predicted light microscopic image (pLM.tif) and the light microscopic image of the chromatin channel (rLM.tif). The file <i>transformation_LM_image.xml</i> contains all transformations, that are made to the light microscopic images to align them to the electron microscopic images.
      </p>
    </li>
    <li>
      <p align="justify">
        You can use the xml file for example with the Fiji plugin [Transform Virtual Stack Slices](https://imagej.net/Transform_Virtual_Stack_Slices) to repeat the transformation with another, not selected image.
      </p>
    </li>
  </ul>



# Train your own network

**1. Set up the python environment**


<ul>
  <li>
    <p align="justify">
      Install [Anaconda](https://www.anaconda.com/distribution/)
    </p>
  </li>
  <li>
    <p align="justify">
      Install [Anaconda](https://www.anaconda.com/distribution/) 
    </p>
  </li>
</ul>



**2. Preprocess images**

Preprocess your images for training with the jupyter notebook _load_data.ipynb._ This jupyter notebokk script is based on [this script](https://nbviewer.jupyter.org/url/csbdeep.bioimagecomputing.com/examples/denoising3D/1_datagen.ipynb)


**3. Train network**

Train your network with the jupyter notebok _train_network.ipynb_, that is based on [this script](https://nbviewer.jupyter.org/url/csbdeep.bioimagecomputing.com/examples/denoising3D/2_training.ipynb)
