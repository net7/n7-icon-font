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
2. In the **dependencies** section add: `"@n7-frontend/icon-font": "git+ssh://git@github.com/net7/n7-icon-font.git#master",` (double quotation marks included). In this way the last version of the `master` branch will be used. If you need to use a specific **tag** release of the font you can add the tag identifier after the character `#`.
3. To use the font you will also have to **import** the main `style.css` file, writing something like this in your main project's scss import file:
```
// ------------------------------------ //
// #N7-ICON-FONT
// ------------------------------------ //
@import '<path-to-node-modules>/node_modules/@n7-frontend/icon-font/Font/n7-icon/style.css';
```

## 4. Use the icons

#### 4.1 Available icons

To check the available icons open the file: `7-icon-font/Font/n7-icon/demo.html`.

#### 4.2 HTML use

Use the icons by adding the corresponding class to HTML elements. We suggest to use span elements:

```
<span class="n7-icon-lightbulb"></span>
```
#### 4.3 CSS use

You can also use the icons directly in CSS, adding them as `content` of HTML elements like in this example:

```
.class:after {
    content: "\e902";
    font-family: 'n7-icon';
    ...
}
```

The code to use in the `content` can be found in the **demo** page.

## 5. New icons request

You can request new icons by opening new issues here: https://github.com/net7/n7-icon-font/issues. Please describe the icon that must be designed.
