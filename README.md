# MedNeurIPS_2019

This work has been made and shared by the team Institut Hypercube (https://www.institut-hypercube.org/en/, https://www.facebook.com/InstitutHyperCube/), in collaboration with Margaux Luck (MILA), Clare Kelly (Trinity College Dublin).

The model stored here corresponds to the VAE used in the study "Towards Autism Detection on brain structural MRI scans using deep unsuervised learning methods." (files poster.pdf and Towards_a_pipeline_for_the_detection_of_Autism_last.pdf)

To use the model: 


- Install Niftynet (https://niftynet.readthedocs.io/en/dev/installation.html)


- Clone blackPacha/MedNeurIPS_2019/* in your niftynet/extensions; my_collection_network is a python module repository.
(more info: https://niftynet.readthedocs.io/en/dev/extending_net.html)


- Train from niftynet/extensions with command line: 

net_autoencoder train -c my_collection_network/vae_config.ini --name my_collection_network.my_vae.VAE


- Encode from niftynet/extensions with command line: 

net_run inference -c my_collection_network/vae_config.ini --inference_type encode -a niftynet.vae_application.AutoencoderApplication
