---
tags: runtime-traditionalweb; 
summary: Section Index organizes the content of a screen, enabling quick navigation within the page.
---

# Section Index

You can use the Section Index UI Pattern to organize the content of a screen, enabling quick navigation within the page.

![](<images/sectionindex-7-ss.png>)

**How to use the Section Index UI Pattern**

1. In Service Studio, in the Toolbox, search for `Section Index`.

    The Section Index widget is displayed.

    ![](<images/sectionindex-8-ss.png>)

    If the UI widget does not display, it may be because you used a ready-made app, which deletes unused widgets from the module. To make additional widgets available in your app:

    a. Go to **Module > Manage dependencies**.

    b. Search for and select the relevant Producer, for example OutSystemsUI. Ensure Show All is selected. 

    c. On the Public elements for the selected Producer displayed on the right, ensure Show All is selected.
    
    d. Search for and select the element you want to add, and click **Apply**. 
    
    e. In Service Studio, in the Toolbox, search for the widget again.

1. From the Toolbox, drag the Section Index widget into the Main Content area of your application's screen.

    In this example, we drag the Section Index widget into a column. 

    ![](<images/sectionindex-2-ss.png>)

1. In the Toolbox, search for and drag the Section widget into the Main Content area of your application's screen. Add as many sections as you require for your app.

    In this example, we drag 4 Section widgets [into a column](../../../../../develop/ui/patterns/web/structure/columns.md). Each section widget contains Title, Actions, and Content placeholders. 

    ![](<images/sectionindex-5-ss.png>)

1. Add the relevant content to Section widget's **Title** and **Content** placeholders.

    In this example, we add employee names to the **Title** placeholders, and Card Sectioned widgets with some text and images to the **Content** placeholder.

    ![](<images/sectionindex-1-ss.png>)

    A link is automatically created to every section you have on the screen. The name of the link is based on the text you entered in the **Title** placeholder of each section. In the following example, the links are set to the employee names we entered in step 2.

    ![](<images/sectionindex-3-ss.png>)

1. On the **Properties** tab, you can customize the Section Index's look and feel by setting any of the optional properties.

    ![](<images/sectionindex-6-ss.png>)

After following these steps and publishing the module, you can test the pattern in your app.

## Properties

| **Property** |  **Description** |
|---|---|
| IsSmooth (Boolean): Optional  |  If True, the navigation to the destination is animated. If False, the navigation is instant. This is the default. |
| IsFixed (Text): Optional  | If True, the Section Index Pattern is always in the same position on the screen. This is the default. If False, the Section Index Pattern scrolls with the page content. |
| TopPosition (Integer): Optional  |  Distance in pixels from the top of the page to the first item in the section index.  |
| ExtendedClass (Text): Optional | Adds custom style classes to the Pattern. You define your [custom style classes](../../../../../develop/ui/look-feel/css.md) in your application using CSS. <p>Examples <ul><li>_Blank_ - No custom styles are added (default value).</li><li>_''myclass''_ - Adds the _myclass_ style to the UI styles being applied.</li><li>_''myclass1'' ''myclass2''_ - Adds the _myclass1_ and _myclass2_ styles to the UI styles being applied.</li></ul></p>You can also use the classes available on the OutSystems UI. For more information, see the [OutSystems UI Live Style Guide](https://outsystemsui.outsystems.com/StyleGuidePreview/Styles). |
  
## Additional notes

Remember to use the **Title** placeholder in the Section Index pattern as this defines the text for each Section Index link.

## Device compatibility

In Internet Explorer, `position: fixed` is used instead of `position sticky` as the latter is unsupported.

## Compatibility with other patterns

This UI pattern only works with the Section Pattern in the same screen.
