# CSE 168 Final Project
# Tobey Pineda

UCSD Online Username: tpineda

UCSD Online Email: tpineda@ucsd.edu 

CSE 168 Final Project

I implemented a procedural wood material based on the research paper:
https://www.cs.cornell.edu/projects/wood/simulating_the_structure_and_texture_of_solid_wood.pdf

Basic Growth rings were implemented with a square wave as a function of the radius from the origin
of the wood grain and a user defined grain width.

Color was defined with a Beer's Law Curve, along with a Perlin Noise function, allowing the growth rings
to naturally fluctuate colors.
	Futhermore both growth rings and color were further modulated with Perlin Noise to reduce the regularity
of the pattern and increase realism.

Distortion and fiber direction was implemented with a texture map that is rotated about the "cylinder" of
wood. Values are fetched from the texture map as a function of the radius and "height" of the object. 

Usage:
    wood [on/off]		
    woodtype [oak/mahogany/walnut]
	woodtypeman earlywoodcolor.x earlywoodcolor.y earlywoodcolor.z latewoodcolor.x latewoodcolor.y latewoodcolor.z
	wooddim origin.x origin.y origin.z direction.x direction.y direction.z witdth

Images:
![Screenshot](ggx.png)
ggx.test displays the 3 different types of wood built into the program: oak, mahogany, and walnut.
The left 3 spheres display the same grain direction, while the right 3 spheres display varying grain direction.

![Screenshot](dragon.png)
dragon.test displays the use of the wood material as a wall or floor material.

![Screenshot](dragon2.png)
dragon2.test displays the use of the wood material on a complex, high polygon-count object.

# Raytracer w/ Optix - Simulating Wood
### UCSD ENG 100D, Spring 2021

ShelterBox Liaison: Carrie Baptista

An interactive map for ShelterBox built with Mapbox, HTML/CSS, and Javascript.

| Team Members | Description |
| ----------- | ----------- |
| Andy Liu | Software Developer |
| Collin Kawahara | Software Developer |
| Tobey Pineda | Software Developer |
| Sam Burkholder | Software Developer |
| Selena Somvilay | UX Researcher |
| Michelle Tenin | UX Researcher |
| Santino Espiritu | Community Liaison  |
| Brian Han | UX Researcher |

---

<p align="center">
  <img width="512" height="262" src="https://github.com/TobeyPineda/Shelterbox-InteractiveCaseStudyMap/blob/main/Images/ShelterboxDemo.gif">
</p>
<p align="center">
  <a href="https://ckawahar.github.io/ShelterBoxCaseStudyMap/">Final Deliverable</a>
</p>

---

### About Shelterbox:
Since 2000, ShelterBox has helped 1.7 million people by providing emergency shelter following more than 300 disasters in 95 countries.

ShelterBox responds urgently to earthquake, volcano, flood, hurricane, cyclone, tsunami, or conflict by delivering emergency shelter and other aid, including blankets, water filter and carriers, solar lights, and other essential tools for survival.

#### Case Studies:
Case Studies are ShelterBox's way of documenting the stories and struggles of people who are affected by natural disasters or conflict. This typically includes a personal story and photos of the people and their current living situation.

---
### Objective:
- To increase exposure and access to ShelterBox’s asset bank/fundraising page. 
- Implement a user-friendly visualization to the platform while making tools and resources available to future teams’ continuity. 
- A mapping system that displays ShelterBox’s intriguing case studies from all around the world. 
- Creating a visually appealing and easy to use map to imbed onto their website. 
- Ability to hand-off project to Shelterbox and/or future groups

---

### About the Project:
ShelterBox wants a deliverable that will not only attract more users but also retain the existing donors and encourage younger generations to start gaining interest. We aimed to improve the overall experience and visuals designs of the map to make the first impression appealing to first time visitors while also offering a seamless experience. Furthermore, we wanted to demonstrate the impact Shelterbox has had on communities throughout the world, so that it would resonate with users. Lastly, the workflow to add features and update data is significantly simplified by utilizing only Google Spreadsheets and basic web development languages


#### Design Team:
- Figma

#### Development Team:
- Mapbox
- Glitch
- HTML
- CSS
- JavaScript

#### Data:
- Spreadsheets to input and manage case studies

#### Design Requirements:
- Discoverability
- Desirability
- Simplicity
- Ease of Maintenance

---
