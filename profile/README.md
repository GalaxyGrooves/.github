<img src="https://github.com/GalaxyGrooves/.github/assets/57195399/994f11df-c351-41c7-b2d4-08be5ad3d92e" width="200">


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
We used OpenCV to extract the RGB values from the image.

## Challenges we ran into

## Accomplishments that we're proud of

## What we learned

## What's next for Galaxy Grooves
