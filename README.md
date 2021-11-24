# Raytracer w/ Optix - Simulating Wood
### UCSD CSE 168 Final Project, Spring 2021

Professor: Ravi Ramamoorthi

---

### The Raytracer:
This raytracer makes use of state of the art techniques and algorithms including real-time ray and path tracing in OptiX, and a modern path tracer with multiple importance sampling.

For the final project, implemented a procedural wood material based on the research paper:
https://www.cs.cornell.edu/projects/wood/simulating_the_structure_and_texture_of_solid_wood.pdf

---

### Direct Lighting

|Analytic|9 Samples|3x3 Subdivided|Multiple <br> Light Sources|Cornell Box|
|:-:|:-:|:-:|:-:|:-:|
| <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/analytic.png" width="150" /> |  <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/direct9.png" width="150" /> | <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/direct3x3.png" width="150" /> |<img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/sphere.png" width="150" /> |<img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/cornell.png" width="150" /> |

### Indirect Lighting - Different Sampling Methods
	
|Simple Sampling|Cosine Sampling|Nearest Event <br> Estimation Sampling|Round Robin <br> Sampling|BRDF Sampling|
|:-:|:-:|:-:|:-:|:-:|
| <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/cornellSimple.png" width="150" /> | <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/cornellCosine.png" width="150" /> |  <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/cornellNEE.png" width="150" /> |<img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/cornellRR.png" width="150" /> | <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/cornellBRDF.png" width="150" /> |

### Importance Sampling
	
|Multiple <br> Importance Sampling|GGX BRDF - Different Materials|Final Dragon|
|:-:|:-:|:-:|
| <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/mis.png"  height="150" /> | <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/ggxHighSamples.png"  height="100"/> |  <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/dragonBRDF.png" height="150" /> |

### Wood Sampling

|Wood Floor|Different types of wood|Wood Dragon|
|:-:|:-:|:-:|
| <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/dragonWoodFloor.png"  height="150" /> | <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/ggxWood.png"  height="100"/> |  <img src="https://github.com/TobeyPineda/Raytracer-with-Optix-and-Wood-Simulation/blob/main/Images/dragonWood.png" height="150" /> |

Basic Growth rings were implemented with a square wave as a function of the radius from the origin of the wood grain and a user defined grain width.

Color was defined with a Beer's Law Curve, along with a Perlin Noise function, allowing the growth rings to naturally fluctuate colors. Futhermore both growth rings and color were further modulated with Perlin Noise to reduce the regularity of the pattern and increase realism.

Distortion and fiber direction was implemented with a texture map that is rotated about the "cylinder" of wood. Values are fetched from the texture map as a function of the radius and "height" of the object.

