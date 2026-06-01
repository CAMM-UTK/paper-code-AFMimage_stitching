
# A Fourier-Based Global Denoising Model for Smart Artifacts Removing of Microscopy Images 

**Huanhuan Zhao**, **Connor Vernachio**, **Laxmi Bhurtel**, **Wooin Yang**, Ruben Millan-Solsona, Spenser R. Brown, Marti Checa, Komal Sharma Agrawal, Adam M. Guss, Liam Collins, **Wonhee Ko**, **Arpan Biswas**

 	
[https://doi.org/10.48550/arXiv.2503.08735](https://arxiv.org/abs/2511.09734)
Zhao, H., Millan-Solsona, R., Checa, M. et al. A bi-channel aided stitching of atomic force microscopy images. Sci Rep 15, 41897 (2025). https://doi.org/10.1038/s41598-025-25855-y


### Abstract
Microscopy such as Scanning Tunneling Microscopy (STM), Atomic Force Microscopy (AFM) and Scanning Electron Microscopy (SEM) are essential tools in material imaging at micro- and nanoscale resolutions to extract physical knowledge and materials structure-property relationships. However, tuning microscopy controls (e.g. scanning speed, current setpoint, tip bias etc.) to obtain a high-quality of images is a non-trivial and time-consuming effort. On the other hand, with sub-standard images, the key features are not accurately discovered due to noise and artifacts, leading to erroneous analysis. Existing denoising models mostly build on generalizing the weak signals as noises where the high signals are enhanced as key features, which is not always the case in microscopy images, thus can completely erase a significant amount of hidden physical information. To address these limitations, we propose a global denoising model (GDM) to smartly remove artifacts of microscopy images while preserving weaker but physically important features. The proposed model is developed based on 1) first designing a two-imaging input channel of non-pair and goal specific pre-processed images with user-defined trade-off information between two channels and 2) then integrating a loss function of pixel- and Fourier-transformed (FFT) based on training the U-net model. We compared the proposed GDM with the non-FFT denoising model over STM-generated images of Copper (Cu) and Silicon (Si) materials, AFM-generated Pantoea sp. YR343 bio-film images and SEM-generated plastic degradation images. We showcased the tuning effect between two imaging input channels in trading-off performance between artifacts removal vs feature preservation. We believe this proposed workflow can be extended to improve other microscopy image quality and will benefit the experimentalists with the proposed design flexibility to smartly tune via domain-experts’ preferences.

<img width="792" height="440" alt="image" src="https://github.com/user-attachments/assets/470a6c31-b8c7-4342-a8ef-8f9897564d4c" />


Figure1: Architecture of the proposed Fourier-Based Global Denoising Model (GDM).

### Description
This repository includes links, code, scripts, and data to generate the figures in the paper.
This repository includes links, code, scripts, and data to generate the figures in a paper. 

### Data


### Usage
There are two jupyter notebook files in the **src** folder, [AFM_image_preprocessing.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_image_preprocessing.ipynb) is used to generate flattened topographical images, amplitude images, and differential images. [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb) is used to stitch the images together. To test the code with the AFM images used in the paper, the user needs to:
- Step 1: Install environment using `pip install -r requirements.txt`.  [requirements.txt](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/requirements.txt) contains the necessary libraries for executing the notebook.
- Step 2: Download the datasets from the **Data** folder [here](https://github.com/arpanbiswas52/Stitching_AFMimage/tree/main/data) and unpack it within the same folder as [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb). 
- Step 3: Run the [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb) notebook. 
- If you are using your own data, you can either preprocess it using [AFM_image_preprocessing.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_image_preprocessing.ipynb) or prepare the flattened images and second channel images by yourself. Remember to change the input path to your own data path when running [AFM_stitching_V2.ipynb](https://github.com/arpanbiswas52/Stitching_AFMimage/blob/main/src/AFM_stitching_V2.ipynb).




### Support
The authors (H.Z and A.B) acknowledge the use of facilities and instrumentation at the UT Knoxville Institute for Advanced Materials and Manufacturing (IAMM) and the Shull Wollan Center (SWC) supported in part by the National Science Foundation Materials Research Science and Engineering Center program through the UT Knoxville Center for Advanced Materials and Manufacturing (DMR-2309083) [DMR-2309083](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2309083&HistoricalAwards=false). The STM experiment was supported by the National Science Foundation Materials Research Science and Engineering Center program through the UT Knoxville Center for Advanced Materials and Manufacturing (DMR-2309083) [DMR-2309083](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2309083&HistoricalAwards=false). AFM and SEM imaging was performed at the Center for Nanophase Materials Sciences (CNMS), which is a US Department of Energy, Office of Science User Facility at ORNL.

<img width="400px" src="https://mrsec.org/sites/default/files/MRSEC%20logo_clear%20background.png">


### Reference
[1]Millan-Solsona, R., Brown, S.R., Zhang, L. et al. Analysis of biofilm assembly by large area automated AFM. npj Biofilms Microbiomes 11, 75 (2025). https://doi.org/10.1038/s41522-025-00704-y


