# AI-Developer-Toolset-Plugin-for-Eclipse
## What is AI-Developer-Toolset-Plugin-for-Eclipse
The AI Developer Toolset (AIDT) is a plugin that enables you to use Azure Open AI capabilities in your Eclipse based developments. The plugin uses generative AI with codex model to create code and documentation that improve developer’s efficiency. It lets you generate templates from your current code base to apply in similar developments. You can act as a technical lead with high level program flow, code templates and the plugin will help you to generate the code.

The AI Developer Toolset plugin enables you to seamlessly integrate AI features into your text editor based projects. It supports various SAP based developments, such as ABAP Report, Class, Function Module, BADI, User Exits, CDS Views, Rest APIs. It is compatible with the latest SAP based developments. It is tested to work with SAP based developments in the current release.

In future, it will be enhanced to work with most of the known Eclipse based development objects. The AI Developer Toolset plugin will help you create innovative applications that can automate manual tasks, make smarter business decisions, and provide more personalized customer experiences

The plugin is in experimental stage. It will be refined in newer versions as we receive more feedbacks.

## Prerequisites
An Azure subscription  https://azure.microsoft.com/en-us/free/ai-services/

The Code generation works with GPT 4 or GPT 3.5 Turbo Model. Ensure your access includes one of this model.

Eclipse IDE Minimum Version: 2023-06

## Download and Installation
1. Download the zip file given in the repository to your local drive.

2. Extract the zip and locate aidttools .

3. Adding the Update Site to your Eclipse installation:
In Eclipse, choose in the menu bar Help > Install New Software and add the URL file:/<folder_path>/aidttools

4. Select the plugin AIDTTools. Click on Next and allow it to get installed.
  
For detailed steps refer document provided in the git folder
[Step by Step guide to Install AIDT Tools for Eclipse Plugin](https://github.com/MonaDevAI/AI-Developer-Plugin-for-Eclipse/blob/main/Step%20by%20Step%20guide%20to%20Install%20AIDT%20Tools%20for%20Eclipse%20Plugin.pdf)

## What it offers
### Generate Code
You can use this feature to auto generate code by providing requirement in text format. 

Type a single line of comment like below and press enter then Ctrl + 8 to generate code.

If you need to give multiple lines , there are two ways to give instruction 
sorround with #START #END and press enter then Ctrl + 8 
or select lines to be passed as prompt then Ctrl + 8.

### Generate Template
You can use this feature to generate template from existing code base to reuse this feature. 

Type a single line of comment like below and press enter then Ctrl + 4 to generate template.

If you need to give multiple lines , there are two ways to give instruction 
sorround with #START #END and press enter then Ctrl + 4
or select lines to be passed as prompt then Ctrl + 4.
### Contacts 
Developed by : Monalisa Biswal

Advisory : Ram Bairavarsu, Krishna Ankam, Gopal Nair

Help on Prompt Engineering : Alice Vinogradova

Additional Contacts : Anuj Shah, Pareen Karpe 


   




