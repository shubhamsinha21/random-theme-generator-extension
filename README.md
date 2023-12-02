# Build a 3rd Party Extension (Random Theme Generator) for Adobe Illustrator 🌟
  
Introducing 🥁 a sophisticated Adobe Illustrator plugin/extension. This innovative tool🤖 seamlessly leverages the power of CEP (Common Extensibility Platform) and Extendscript to establish seamless ☑️communication with the host application. The frontend, elegantly built with Vite-React, embraces the efficiency of TypeScript for robust development, while its visual📹appeal is meticulously shaped with the timeless charm of vanilla CSS. Elevate your design experience with this cutting-edge solution that effortlessly combines creativity and professionalism.

## Features 💁‍♂️

1. Generates random color palettes with 5 colors each.
2. Applies random themes to your Adobe Illustrator document, including color, opacity, and text options.
3. Allows you to select a color from the palette and apply it to your document.
4. Toggles between RGB and HSL color value display.
5. Exports your document as AI, JPEG, or PNG.

## Usage 🤔

1. Click the "Random Palette" button to generate a new random palette of 5 colors.
2. Click a color in the palette to apply it to your document.
3. Click the "Random Theme" button to apply a random theme to your document.
4. Select the desired file type (AI, JPEG, or PNG) and click the "Export" button to export your document.
5. Check the "Show Theme Values" checkbox to display the RGB, HSL, and theme values for the selected color.

## Project Structure 🪜

![theme](https://github.com/shubhamsinha21/random-theme-generator-extension/assets/84564814/4bb536aa-07ac-4aae-92d4-a62476082f49)

### Code Struture of App.js file of client 

  - App.js: The main component of the application.
  - randomizeColors.js: A function that generates a random array of 3 RGB values.
  - randomizePalette.js: A function that generates a random palette of 5 colors.
  - randomizeTheme.js: A function that applies a random theme to the document.
  - colorDoc.js: A function that sets the active color.
  - handleText.js: A function that toggles between RGB and HSL color value display.
  - saveFile.js: A function that exports the document.
  
Make sure you have node installed prior to executing this command -  
  > `node createPackage.js`  
  
This should copy the essential assets required for the functioning of your extension to the com.adobe.randomtheme folder (such as CSXS, index.html, jsx, client/assets/CSInterface.js, index.js, main.css, .debug).  
  
## Installation 👇🏻
  
To effectively integrate this extension, you have two options contingent on your objectives:

### For Customization: ©️

  1. Should you wish to modify the application, employ the drag-and-drop method for the entire folder.
  2. Alternatively, deposit the com.adobe.randomtheme folder if your intent is solely to utilize the application without alterations.
  3. The designated path for both scenarios is: C:\Users\UserName\AppData\Roaming\Adobe\CEP\extensions
  4. Notably, the directory hierarchies remain unaltered, obviating the necessity for any further adjustments.
     
###  For Seamless Operation: 👇🏻

  1. If your package is signed, no additional actions are required for smooth operation.
  2. Conversely, if dealing with an unsigned package and manually placing folders within the extensions directory, it becomes imperative to activate debug mode to facilitate the loading of unsigned extensions.
  3. Execute the following steps to enable debug mode:
    - Initiate a search for regedit (REGISTRY EDITOR) and press ENTER.
    - Navigate to HKEY_CURRENT_USER/SOFTWARE/ADOBE/CSXS.XX (where XX denotes your installed version).
    - Right-click on the right side, opt for New > String Value.
    - Specify the name as PlayerDebugMode and assign the data value of 1.
     
Note: The precise location may vary contingent on your Adobe version or product. Should the provided pathway prove ineffective, ascertain your extensions folder by conducting a targeted search based on your Adobe application version and subsequently situate the package accordingly.
  
## Deployment 🤔
  
  For deployment, the transformation of this application into an Adobe Illustrator extension involves the encapsulation within a .zxp file. Subsequently, the installed .zxp file through the Extension Manager       seamlessly integrates the application into Adobe Illustrator.

Noteworthy Details: 🧐

  - Tailored for utilization with Adobe Illustrator CC 2017 and subsequent versions.
  - Execution of the application does not necessitate any specialized permissions.
  - The architectural composition comprises a manifest residing within CSXS, extendscript (js/jsx) files housed in jsx, and essential scripts located within            client/assets. During development, the presence of client/assets/session is imperative, yet inconsequential upon release. This holds true for the index.html        within client/assets, rendering it redundant. The pivotal index.html, pivotal to the extension's     
    functionality, is situated in the root folder.
