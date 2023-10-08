<img width="492" alt="Screenshot 2023-10-08 at 5 36 55 AM" src="https://github.com/GalaxyGrooves/.github/assets/57195399/1f3142ee-6efd-4707-9ca9-40a8576d2321">

Our submission, Galaxy Grooves, is to the 2023 NASA Space Apps Challenge Open Source Hackathon. The challenge we tackled is: Immersed in the Sounds of Space, where we aimed to represent a high dimensional dataset into an audio output.

# Submissions posts
[NASA Space Apps Submission](https://www.spaceappschallenge.org/2023/find-a-team/galaxy-grooves/?tab=project)  
[Devpost Submission](https://devpost.com/software/galaxy-grooves)

# Check us out!
Our project is deployed live onto [Streamlit](https://galaxygrooves.streamlit.app/)

## Inspiration
How can we "hear" heat? NASA's Wide-field Infrared Survey Explorer (WISE) generates a high dimensional infrared dataset, extending an invitation to explore the cosmos beyond the visual spectrum. Our team was motivated to tackle this sensory challenge mainly because the WISE telescope captures information using infrared wavelengths, yet we cannot visually experience infrared light. To bridge this gap, we created an algorithm that transforms infrared measurements into audio output. Using our project as an auditory lens, we hope to enrich the sensory exploration of the unknown and reveal the visual silence of infrared data by allowing the public to "hear" the warmth of the cosmos.

## What it does
Our project starts with 4 images captured by the WISE telescope. Each image corresponds to an infrared wavelength band from WISE: 3.4, 4.6, 12, and 22μm. From one image, we first begin the process by forming subsections of 10 x 10 pixels and averaging the RGB values to determine the averaged RGB value for this subsection. Then, we perform a second calculation to average the R,G,B values to compute a decimal number. We use this decimal number as one parameter for our audio generator function.

Band 1: The Pitch
We use Band 1 as the source data to determine our pitch. The location of the celestial object determines the range of our pitch. We use the celestial object's right ascension and declination values to delineate the upper maximum frequency and the declination to delineate the lower minimum frequency.

Band 2: The Length
We use Band 2 as the source data to determine the length of each note. The greater the intensity of the subsection image, the longer our note.

Band 4: The Volume
We use Band 4 as the source data to determine the volume of each note. The higher the concentration of dust, the louder the note will be.

## How we built it
First, we used OpenCV to extract the RGB values from the image. Then, we used each infrared image to determine our note's pitch, volume, and length. We stored these values in a Numpy array as input for our audio, and finally, we used a Python library, Sounddevice, to output the data.

To deploy our web application, we used Streamlit to host our code. When we pushed our code onto the GitHub repository, we could see our deployed changes live immediately.

## Challenges we ran into
We brainstormed how to come up with the methodology to transform our infrared measurements to musical notes. We want to incorporate variety into each note, so we ultimately decided on varying the musical characteristics such as pitch, volume, and length of each note. Our team members were beginner hackers, and the NASA Space Apps Challenge was their first time participating in a hackathon, so many were new to trunk-based software development and advanced Git workflows. When we encountered Git issues, we collaborated to tackle and resolve any problems, and we all learned more about trunk-based software development.

## Accomplishments that we're proud of
Our project, Galaxy Grooves, presents a unique and unprecedented chance for the public to observe celestial objects in a completely original manner. Since humans cannot visually observe infrared data, we hope the general public can "hear" heat for the first time and experience this auditory unveiling of infrared datasets. Furthermore, our project offers members of the visually impaired community the newfound opportunity to enjoy and listen to celestial objects. For these reasons, we believe Galaxy Grooves is an engaging way for the general public to experience this sensory journey.

## What we learned
We learned the science behind infrared telescope measurements and found ways to convey the concept of radiation through auditory experiences. We also learned the value of open science as these images are publicly available, and everyone can see the raw data for themselves. By innovating new methods for the sonification of 3D data, we creatively applied our skills to understand and best represent note sounds to our audience.

## What's next for Galaxy Grooves
We're excited to implement an uploading feature on our deployed project. With this new feature, our users could upload images of their own. Users may be astronomy aficionados, so they may be eager to upload personal night sky images. Galaxy Grooves is elated to see the growth of incoming users excited to explore the unknown of infrared light. 

## What we learned
We learned the science behind infrared telescope measurements and found ways to convey the concept of radiation through auditory experiences. We also learned the value of open science as these images are publicly available, and everyone can see the raw data for themselves. By innovating new methods for the sonification of 3D data, we creatively applied our skills to understand and best represent note sounds to our audience.

## What's next for Galaxy Grooves
We're excited to implement an uploading feature on our deployed project. With this new feature, our users could upload images of their own. Users may be astronomy aficionados, so they may be eager to upload personal night sky images. Galaxy Grooves is elated to see the growth of incoming users excited to explore the unknown of infrared light. 
