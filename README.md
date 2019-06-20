# N7 Icon Font
This is the custom Net7 font that is intented to be used in all frontend applications: Muruca (Digital Humanities), DataViz (Industry 4.0) and all Nautical applications.

## 1. Sketch source file
The Sketch folder contains the source file where you can edit and add icons. Each icon must be contained in a 20 x 20 pixel artboard. The name of the artboard will be the name used to display the icon in the frontend. Keep the artboards and the list on the left sorted alphabetically.

## 2. How to generate the font with Icomoon

1. Select all icons in Skecth (select all the artboards).
2. Export as **SVG**.
3. Open the **Icomoon App** (https://icomoon.io/app/) and create a new empty project.
4. Click on the **Import icons** button.
5. Select all the icons.
6. Click on the little **burger menu** top right and select **Properties**.
7. In the Properties dialog click on **Reset Grid Size**.
8. In the Reset Grid Size dialog set the **New Grid Size** value to 16 (should be the default value) and click Reset.
6. Click "Generate font" bottom right.
7. Click on the "Preferences" button and set: (A) Font name: **n7-icon** (B) Class prefix: **n7-icon-**.
8. Download the font clicking on the button **Download** bottom right.

To update the font in the repo, replace the downloaded files in the **n7-icon-font/Font/** folder.

## 3. Include the font in your project

The font can be used as a NPM package:

1. Open the **package.json** file of your project.
2. In the **dependencies** section add: `"@n7-frontend/icon-font": "git+ssh://git@github.com/net7/n7-icon-font.git#master",`.

In this way the last version of the `master` branch will be used. If you need to use a specific **tag** release of the font you can add the tag identifier after the character `#`.

## 4. Use the icons

Use the icons by adding the corresponding class to HTML elements. We suggest to use span elements:

```
<span class="n7-icon-lightbulb"></span>
```

To check the available icons open the file: `7-icon-font/Font/n7-icon/demo.html`

## 5. New icons request

You can request new icons by opening new issues here: https://github.com/net7/n7-icon-font/issues. Please describe the icon that must be designed.
