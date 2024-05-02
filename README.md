# Text-to-2d-Floorplan-Generation-using-GANs
Generating 2d Floorplan images from text prompt using a custom GAN Model (Archi-GAN). Implemented in python using tensorflow, numpy, pandas, and transformers.

<a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/output%20images/real_vs_generated.jpg?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/output%20images/real_vs_generated.jpg?raw=true" height="300" /></a>

## Dataset Used
A subset of this dataset: Tell2Design (https://github.com/LengSicong/Tell2Design) has been used to implement our project. 
It contains almost 4000 human annotated floorplan images with its natural language descriptions 5-6 sentences long and specifying the position of rooms, the dimensions and the overall layout.

## Intuition and Methodology
<a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/Archi_gan_simple.png?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/Archi_gan_simple.png?raw=true" height="200" /></a>

Archi-GANs is a simple yet effective GAN model which  combines the properties of Conditional Gans (CGANs) and Deep Convolutional Gans (DCGans). It uses text embeddings in the generator as extra condition and upsamples it using 2d Transpose convolutional layers (or fractional convolutional layers) and generates a synthetic image.
The Discriminator used Convolutional layers to learn spatial patterns in the image to distinguish it between real and fake data.

<a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/generator_logic_diagram.png?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/generator_logic_diagram.png?raw=true" height="400" /></a><a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/discriminator_logic_diagram.png?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/discriminator_logic_diagram.png?raw=true" height="400" /></a>

## Future Work
