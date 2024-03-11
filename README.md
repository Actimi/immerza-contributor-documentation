# Contributor's Guide: IMMERZA VR Application
Welcome to the IMMERZA VR application contributor's guide! We appreciate your interest in contributing to our project. This guide is designed to assist designers and developers in understanding the project's structure, workflow, and best practices for contributing effectively.

![Error](https://raw.githubusercontent.com/kahveciozan/ImmerzaContributorDoc/main/ImmerzaLogo.png)
# Project Overview
IMMERZA is a VR App for mood on demand available initially on SideQuest, with plans for launch on Applab and later on the Oculus Official Store. It's compatible with Meta Quest, Quest 2, Quest 3, and Quest Pro devices. IMMERZA offers four main categories: Focus, Calm, Awe, and Motivation, each featuring multiple unique environments to explore.

### [Immerza Website](https://www.immerza.com/)
### [Immerza Contributor Website](https://contributor.immerza.com/)

# Content Creation Guidelines for IMMERZA Contributors
IMMERZA is developed using the Unity3D Game Engine, offering an opportunity for contributors to enhance its content. Here are guidelines to ensure consistency and quality in your contributions:

## Overview of Creating a New Scene. (You can upload scene in 3 basic steps)
**[STEP-1]: Create and develop your scene in your own project. (Use Unity Version 2022.3.XX.X)**  <br/>
**[STEP-2]: Build the scene with Addressables.**  <br/>
**[STEP-3]: Upload files to the website respectively.**  <br/>

Now let's move on to the detailed explanation
---
### [STEP-1]: Creating and Development in Unity Step by Step

* Decide in which category you want to create a scene(Focus,Calm,Awe or Motivation). Then create the scene you imagine.

1. Create Unity 3D (URP) Project
2. Setting up your Project for Mobile VR
> * Files > Build Settings (Ctrl+Shift+B)
> * Select Android
> * Click the Switch Platform Button.
> * Texture Compression : ASTC

3. Click Project Setting.
> * Project Settings > Player > Other Settings > Deselect Auto Graphics API
> * Project Settings > Player > Other Settings > Graphics APIs : Remove Vulkan
> * Project Settings > Player > Other Settings > Minimum API Level : API Level 29
> * Project Settings > XR Plug-in Managemnet > Click Install Plugin Management ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img/XRPlug%C4%B0nManagagement.png)
 >> * Android Settings : Click Oculus
 >> * Windows Settings : Click Oculus
 >> * Server Settings : Click Oculus
 ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img/XRDetailsForOculus.png)
 
4. Create new scene. 
5. Name your scene uniquely as in the following example. Yourname-Scenename. (Example scene naem: Immerza-AboveTheClouds)
6. Change the Camera for XR:
> * In Hierarchy, Right click > XR > Convert Main Camera To XR Rig
7. Now you can desing your original scene.
---
### [STEP-2]: Build Your Scene with Addressables

### [Click here for video explanation](https://drive.google.com/file/d/19uNoAKjbgJdicGTybX_TLvXmk1a8WFW0/view?usp=share_link)

1. Import Addressables
> * Go to Windows > Package Manager. 
> * In the Packages menu, select Unity Registry.
> * Choose and import Addressables library(Addressable Version 1.21.20.) to your unity project. This is very important to avoid problems loading the scenes. ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img2/AddressablesInstall.png)

2. Addressable Settings.
> * Click Windows > Asset Management > Addressables > Groups. 
 >> * Click Create Addressables Settings
 
> * Click Windows > Asset Management > Profiles
 >> * Local : Editor Hosted
 >> * Remote : Editor Hosted ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img2/AddressableProfiles.png)
 
> * Click Windows > Asset Management > Settings
 >> * Click Build Remore Catalog
 >> * Build & Load Paths : Remote
 >> * Path Preview
 >>> * Built Path:
 >>> * Load PAth: ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img2/AddressableSettings.png)

4. Scene build with Addressable.
 > * Open Addressable Group. Windows > Click Windows > Asset Managemnet > Addressables > Groups
 > * Drag and Drop your scene to Default Local Group.
 > * Click Build > New Build > Default Build Script 
 ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img2/SceneBuild.gif)
 
6. Addressables will give 3 files in ProjectFile/ServerData/Android ![This is an image]![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img2/ServerFiles.gif)

7. Now We can upload these files to the website respectively.

---
### [STEP-3] Uploading .bundle files to the website
1. Go to [Immerza Contributor Website](https://contributor.immerza.com/)
2. Upload these files to the website respectively. >  * ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Img/BuiltFiles.png)
> * Find from file location in order. (Go to ...YourUnityProjectRootFile/ServerData)
> * Upload file in order to website.
3. Add title and descriptionon website.
4. Upload the scene.

Thats all.

## Requirements, Concept and Categories
- Make sure the gameplay length is longer than 3 minutes and less than 12 minutes.
-  Decide what category your target scene will be in. There are 4 category offers from the team. You can contribute a scene in one existing category. Consider the requirements of the category you choose.


## Avoid doing these
- Don't add any C# script. (Addressables don't support extenal code)
- Don't change any ready prefabs, you can use it in your scene but never change it.
- Don't delete or modify any files in the project
- Don't use coptright audios, logos , 3D models and any assets.
- Don't use canvas and UI objects.


