CATMAID-to-Blender
==================

Plugin for [Blender](www.blender.org "Blender Homepage") to interface with [CATMAID](https://github.com/acardona/CATMAID "CATMAID Repo") servers and request data. Tested with Blender 2.77

## Installation:
First download CATMAIDImport.py, then:

######Option A:
2. Directly place CATMAIDImport.py in \Blender\...\scripts\addons
3. Start Blender -> 'File' -> 'User Preferences' -> 'Addons' -> Search for 'CATMAID' addon and activate by checking box -> 'Save User Settings' (see [here](http://wiki.blender.org/index.php/Doc:2.6/Manual/Extensions/Python/Add-Ons) for more detailed description)

######Option B:
2. Start Blender -> 'File' -> 'User Preferences' -> 'Addons' -> 'Install from File' and select CATMAIDImport.py
3. Activate by checking box and 'Save User Setting'

## Before First Use:
Open User Preferences, navigate to 'Add-ons' -> 'CATMAIDImport' and change 'CATMAID Server URL' in 'preferences' to your server.
You may also set credentials to be saved for convenience.

![server_url](https://cloud.githubusercontent.com/assets/7161148/13985056/9b915b22-f0fa-11e5-8b8f-ecac97405708.PNG)

## Tokens:
The CATMAID API authorizes requests using an API token tied to user account instead of a username and password.
For Information on how to retrieve your Token look [here](http://catmaid.github.io/dev/api.html#api-token).

## Quickstart Guide:
Import/Export panel will show up under the 'Scene' tab in the 'Properties' windows

![import_panel](https://cloud.githubusercontent.com/assets/7161148/5356718/c244a7a6-7f9f-11e4-8cef-b69b3cf20b32.PNG)

- Functions (e.g. Retrieving skeletons/connectors) that need you to be logged into your CATMAID server will be grayed-out until did so by hitting 'Connect 2 CATMAID'
- Skeletons can be retrieved by their skeleton ID, by annotations or based on connectivity (Retrieve Partners)
  - Important side node: in order to identify cell bodies, the script searches for nodes with a radius > 10
- Once imported, skeleton/connector data can be readily exported to vector graphics (SVG) with a broad range of options (e.g. coloring, filters, scaling). Look at lower left panel when exporting for these options.

![export_options](https://cloud.githubusercontent.com/assets/7161148/5356716/bf994da4-7f9f-11e4-8e10-c5c628baab47.PNG)

## Pro Tip of the Day:
Open Blender's console to e.g. see error messages or follow the progress while importing.
'Window' -> 'Toggle System Console'

## License:
This code is under GNU GPL V3
