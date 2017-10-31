# Medical-Image-Modality-Conversion

Motivation:
Explore the possibility of converting medical images between modality while preserving information that's important to diagnosis. Specifically, we are looking at CT and MRI of tumors in brain, lung, etc. as those ave the most abundantly available data publically.

Proposed Method: training GAN alongside an encoder, and possibly use perceptual loss to ensure the preservation of lesions/tumors. May use Recursive Cortical Network as a way to build GAN/encoder

Validation Method: Vision Inspection?

Dataset: 

http://www.aylward.org/notes/open-access-medical-image-repositories

https://github.com/beamandrew/medical-data


specifically: MedPix, TCIA
