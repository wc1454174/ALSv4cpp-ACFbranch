# Advanced Locomotion System V4 on C++ with ACF Hooks

This takes the awesome ALSv4Cpp plugin and adds hooks for ACF so that you can drop it into existing ACF projects and get the functionality of ACF with the locomotion of ALS.  

NOTE: This is extremely bare bones and at this time does not port over any of the attack animations from the ACF character into ALS, this is strictly ALSv4 working under the ACF system.

![image](https://github.com/dyanikoglu/ALSV4_CPP/raw/main/Resources/Readme_Content_2.gif)

Replicated & optimized C++ port of [Advanced Locomotion System V4](https://www.unrealengine.com/marketplace/en-US/product/advanced-locomotion-system-v1) for **Unreal Engine 4.25** with additional bug fixes.

## Supported Systems
- Windows 64-bit
- Linux

*Mac, Android, IOS, and console builds are not tested and supported at the moment*

## Features
- Full replication support with low bandwidth usage
- Plugin structure
- Highly optimized for production
- Lots of bug fixes additional to marketplace version

## Known Issues
- See [Issues](https://github.com/dyanikoglu/ALSV4_CPP/issues) section

## Setting Up The Plugin
- Clone the repository inside your project's `Plugins` folder, or download the latest release and extract it into your project's `Plugins` folder.
- Put `Config/DefaultInput.ini` from the plugin folder inside your project's config folder. If your project already have this .ini file, merge it into yours.
- Add the lines below into your `DefaultEngine.ini`, below `[/Script/Engine.CollisionProfile]` tag (Create the tag if it doesn't exist):
```
+Profiles=(Name="ALS_Character",CollisionEnabled=QueryAndPhysics,bCanModify=True,ObjectTypeName="Pawn",CustomResponses=((Channel="Visibility",Response=ECR_Ignore),(Channel="Camera",Response=ECR_Ignore),(Channel="Climbable",Response=ECR_Ignore)),HelpMessage="Custom collision settings for the capsule in the ALS_BaseCharacter.")
+DefaultChannelResponses=(Channel=ECC_GameTraceChannel2,DefaultResponse=ECR_Block,bTraceType=True,bStaticObject=False,Name="Climbable")
```
- Launch the project, and enable plugin content viewer as seen below. This will show contents of the plugin in your content browser:
![image](https://github.com/dyanikoglu/ALSV4_CPP/raw/main/Resources/Readme_Content_1.png)

## License & Contribution
**Source code** of the plugin is licensed under MIT license, and other developers are encouraged to fork the repository, open issues & pull requests to help the development.
