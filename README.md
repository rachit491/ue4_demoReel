# CSC 562 Advance Graphics Final Project

## Description
This demo reel, created as a final project for [Advanced Graphics class](http://cg4games.csc.ncsu.edu), demonstrates several graphics rendering techniques like Level of Detail, Terrain Rendering, Reflection, Global Illumination, Particle Effects. The scene shows a layout with mountains, hills, water bodies, natural vegetation, with effects of daytime and weather changes (rain/sunny) and involves a third person camera view.

## Live Demo
Visit the following URL to run the code:

http://www4.ncsu.edu/~rshriva/DemoReel/DemoReel.html

Note that it takes about 15-20 minutes to load before it becomes responsive due to the large size of the UE4 .data file.

### Requirements
1. Unreal Engine 4.15.0 or above - to open the project
2. Blender - to edit some meshes
3. Go to have a Dedicated Graphics Card in your Machine 

### Screencast
#### Overview of the scene
Focusing on the scene layout, level of detail, terrain rendering, meshes and models used, wind foliage effects, textures, global illumination.

[![Overview of the scene](https://img.youtube.com/vi/Sz1vAvZOFh4/0.jpg)](https://www.youtube.com/watch?v=Sz1vAvZOFh4)

#### Player wandering in the scene
Major focus on the rains (particle effects), clouds animations, weather changes, wind foliage effects, day-night cycle, buoyancy, reflection, refraction in water bodies.

[![Player wandering in the scene](https://img.youtube.com/vi/7SiBUEqVCrI/0.jpg)](https://www.youtube.com/watch?v=7SiBUEqVCrI)

## Controls
While using the Unreal Engine 4, launch the game in viewport. Left click within the viewport and the control goes to the viewport. Use the keys mentioned below to move around in the scene. And press Escape to exit from the game.

Walk around using the arrow keys, or regular W, A, S, D as you move a player in the third person camera angle. Use mouse to change the camera view angle. Press key toggles to changes options, as described below.

### Key Toggles
Just press R key to switch Rain on/off, it takes few seconds to come into effect.

## Build Steps
Building the project is pretty simple. Just few steps to keep in mind. 

1. Install Unreal Engine 4.15.0 or above, and paste the repository folder called "DemoReel" in the Unreal Projects folder in Documents in your system.
2. As the project opens in Unreal Engine 4, it starts to Compile Shaders which will take around 5 minutes to complete.
3. Once that is done, search for Engine Contents folder in your system and replace the contents of "Engine Sky" within it with the given "Engine Sky" in the repo under "Extras" folder.
4. Once that is done, refresh the project and rebuild the lights and compile the shaders again or reopen the project again.
5. Look for SkySphereBlueprint in the World Outliners tab in Editor and open the BluePirnt. Make sure you see some content for Cloud Opacity and Branch in the "Update Sun Direction" function of the BluePrint, as shown below
![skySphere BP Snapshot](https://raw.githubusercontent.com/rachit491/ue4_demoReel/master/Extras/updateSunDirection_skySphereBP.png)
6. If that is shown as expected, you're good to go and Play the game. 

## Claims
### Terrain 
I've used the Sculpt Tool provided in the Unreal Engine 4 to create the terrain of my own, alternative way was to use height maps of pre-defined terrains. The terrain is then painted with three different textures for grass, mud and rock. The terrain has been made uneven as it would be in a natural scene.
### Water Body
I've created multiple water bodies in the environment, and have made waves over them. Also these water bodies display reflections and refractions near to what is experienced in reality. 
### Global Illumination
I've used the Lightmass property of Unreal Engine 4 which enables to control the Global Illumination parameter. Although it is visible when you're in a closed room environment. It was a difficult task to implement in an open scene like this. For this I've created feww grass within the river water and when the camera view goes inside the water, slight greenish-blue can be observed near the grass area because of this lightmass settings.
### Particle Effect
The game shows particle effect, with the use of Particle Emitter functionality provided in the Unreal Editor. The rain drops created have a transluscent texture and also with refractive index, which can be seen from the screencast video.
### Multiple Weather/DayNight Cycle Effects (Extra)
The demo showcases the day-night cycle for the environment. It starts off with a stage where the clouds becomes denser and darker and it rains when you press R. When you stop the Rain, it starts to clear the dense clouds and at the same time the sun (directional light) rotates the sky sphere changing the color of the sky and shadows for the models/objects in the scene. With the sunrise, you can see a sunny day with clear blue skies.
### Wind Effect Foilage (Extra)
I've added wind effect to the vegetations - grass and tree leaves which can be seen from the demo videos on a closer look. It makes the vegetations swift away in the winds.

## Asset Credits
### Trees and Grass Models
Metal Game Studios for providing free assets for the vegetations which were used in the demo reel 
https://forums.unrealengine.com/showthread.php?59812-Free-Foliage-Starter-Kit

### Sky, Clouds, and some Terrain Textures
Unreal Engine Starter Kit which has materials for sky and clouds