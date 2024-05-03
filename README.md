# Text To 2D Floorplan Generation using GANs

Generating 2d Floorplan images from text prompt using a custom GAN Model (Archi-GAN). Implemented in Python using tensorflow, numpy, pandas, and transformers.

<p align='center'><a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/output%20images/real_vs_generated.jpg?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/output%20images/real_vs_generated.jpg?raw=true" height="300" /></a></p>

## Dataset Used
A subset of this dataset: [Tell2Design](https://github.com/LengSicong/Tell2Design) has been used to implement our project. 
It contains almost 4000 human annotated floorplan images with its natural language descriptions 5-6 sentences long and specifying the position of rooms, the dimensions and the overall layout.

## Intuition and Methodology
<a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/Archi_gan_simple.png?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/Archi_gan_simple.png?raw=true" height="200" /></a>

Archi-GANs is a simple yet effective GAN model which  combines the properties of Conditional Gans (CGANs) and Deep Convolutional Gans (DCGans). It uses text embeddings in the generator as extra condition and upsamples it using 2d Transpose convolutional layers (or fractional convolutional layers) and generates a synthetic image.
The Discriminator used Convolutional layers to learn spatial patterns in the image to distinguish it between real and fake data.

### Generator
<a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/generator_logic_diagram.png?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/generator_logic_diagram.png?raw=true" height="400" /></a>
### Discriminator
<a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/discriminator_logic_diagram.png?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/diagrams/discriminator_logic_diagram.png?raw=true" height="400" /></a>

## Output from Text prompt
We ask user for a text prompt which accurately describes the floorplan with the layout and size desized by the user. Then it is converted to text embeddings using BERT to feed into the model and the generator returns the generated image based on the text description provided by the user.

<a href="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/output%20images/text_prompt.jpg?raw=true" target="blank"><img align="center" src="https://github.com/Harsh-Ratna/Text-to-2d-Floorplan-Generation-using-GANs/blob/main/output%20images/text_prompt.jpg?raw=true" height="400" /></a>

## Future Work
We will apply 3D gans to generate the wall structure for the 2D plan and generate an actual structure of a home which can be used for 3D visualisation of the house and its structural design.

## Contributors
This work has been completed by our team comprising of:
- Kermi Kotecha
- Anvesha Raikwar
- Harsh Ratna
- Kanika Gulati

