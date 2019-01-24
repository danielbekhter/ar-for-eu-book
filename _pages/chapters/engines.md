---
layout: page
title: Unity / Unreal Engine
permalink: /chapter/engines/
categories: chapter
visualizations:
---

Developers of AR applications do not have to start from scratch and (re-)implement the complete graphics pipeline and physics simulations.
Instead, 3D engines like Unity {% cite Unity %]} or the Unreal Engine {% cite UnrealEngine %} already offer this functionality as a foundation for the development of real-time graphics applications.

## Unity

Unity is a real-time graphics engine by Unity Technologies which developers can utilize to create 2D and 3D applications {% cite Unity %}.
This means that Unity’s graphics can be adapted to different graphic qualities, performances and visual styles.
Applications can be deployed on more than 25 platforms, including Android, iOS, Windows Standalone and Universal Windows Platform.
Unity is available in different pricing levels ranging from a free personal edition to a Pro version with additional support for larger companies.
The required license level depends on the annual revenue.
Many of the presented AR SDKs can be added to Unity projects so that their functionality is available directly in the 3D engine.

### Project Structure and Project Setup

Once a new Unity project has been created, the project's folder contains a subfolder called "Assets".
Here, all resources for the project, e.g. 3D model files,textures, scripts, etc. can be placed.
Everything in this Assets folder and its subfolders is automatically imported into the project and can be integrated into the application.
It makes sense to keep the Assets folder organized so that all developers know where ressources are stored.
One recommended way of setting up an Assets folder is to create indiviual folders for each type of ressource, e.g. "Animations", "Models", "Textures", "Scripts", etc.

Some folder names are special since they are treated in a particular way by Unity {% cite UnitySpecialFolders %}.
For instance, a folder called "Plugins" will be searched for C/C++ DLLs which are integrated into Unity.
Another example is a folder named "Resources".
Any file which is placed in this folder can be accessed by application scripts using the command ```Resources.Load```.

A Unity project consists of different scenes.
Each scene is a virtual space which can be populated with 3D objects and user interface elements.
In the application, scenes can be loaded and unloaded individually or they can replace a opened scene.
Unity's WYSIWYG editor allows developers to graphically set up the 3D scene and arrange the 3D models accordingly.

### User Interface

### Importing and Placing 3D Models

In order to import a 3D model, its file needs to be placed in Unity's Assets folder.
After this, it can be created in the 3D scene by dragging and dropping it into the 3D view of the editor.
Unity supports popular and application independent file formats like .fbx, .dae, .3ds, .dxf, .obj and .skp {%cite UnityFileFormats %}.
Additionally, Unity is also capable of reading application-specific save-files from Autodesk 3ds Max, Autodesk Maya, Blender, Cinema4D, Modo, LightWave and Cheetah3D.
Both application-independent and application-specific formats enable different workflows for the object import.
The application-specific format require less work when the 3D model is modified regularly.
Any saved changes made in the 3D modelling application are immediately propagated to Unity.
This enables 3D artists to view the 3D model in parallel in the modelling application and a preview in the developed application.

### Programming in Unity

The same folder also stores the application logic which is defined by C# scripts.
These scripts can change properties on 3D models in a scene like their position, rotation, scale or material.
In order to execute a script’s functionality, it needs to be added to a 3D object as a component.
This can also be done in an inspector panel in the scene editor.
Scripts can only be added to objects in a scene if they inherit from the MonoBehavior class.
Once a script is attached to an object, Unity calls special functions in the script if certain events happened.
For instance, developers can implement an Update() function which is called once for every frame which is rendered.
Similarly, different callback-methods can be implemented which are raised at different points in the application’s or object’s lifecycle, e.g. `Awake()`, `Start()` and `OnDestroy()`.
Details on available callback methods and the data structures which can manipulate an object’s properties can be found in Unity’s documentation {% cite UnityUserManual %}.

### Supporting Material

Unity also provides an Asset Store {% cite UnityAssetStore %} which contains scripts, 3D models and usage examples which have been created by other developers.
It contains a mixture of free and paid content which can be downloaded for the own project to save development time.