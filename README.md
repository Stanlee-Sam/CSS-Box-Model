<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [CSS BOX MODEL](#css-box-model)
    - [Parts of the CSS box model](#parts-of-the-css-box-model)
    - [How the CSS box model works](#how-the-css-box-model-works)
    - [Example](#example)
    - [Conclusion](#conclusion)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# CSS BOX MODEL
The CSS box model is a container that contains multiple properties including borders, margin, padding, and the content itself. It is used to create the design and layout of web pages. According to the CSS box model, the web browser supplies each element as a square prism.

***
### Parts of the CSS box model  

Explanation of the different parts:  
-**Content** - The content of the box, where text and images appear.  
-**Padding**- Clears an area around the content. The padding is transparent.

```css
/* Example CSS for padding */
.element {
  padding: 20px; 
  padding: 10px 20px; 
  padding: 10px 20px 30px 40px; 
}
```   
-**Border** - A border that goes around the padding and content.

```css
/* Example CSS for border */
.element {
  border: 2px solid black; 
  border-width: 2px; 
  border-style: solid; 
  border-color: black; 
}
```
-**Margin** - Clears an area outside the border. The margin is transparent.

```css
/* Example CSS for margin */
.element {
  margin: 10px; 
  margin: 10px auto; 
  margin: 10px 20px; 
  margin: 10px 20px 30px 40px; 
}
```
  
The below diagram shows these layers.  
![diagram of the CSS box model](./assets/box-model.png)

### How the CSS box model works
  
The CSS Box Model operates by breaking down each HTML element into a series of nested boxes, each with its own dimensions and properties. When you apply styles to an element, those styles affect the dimensions and appearance of each box in the hierarchy. 

-**Box Sizing**
The `box-sizing` property in CSS determines how the total width and height of an element are calculated. By default, the `box-sizing` property is set to `content-box`, which means that the specified width and height values only apply to the content area of the element, excluding padding, border, and margin.

```css
/* Example CSS for box-sizing */
.element {
  box-sizing: border-box; 
}
```
- **Calculating the total dimensions**
To calculate the total dimensions of an element, you need to consider the following:
1 **Content Width and Height**: The width and height of the content area, specified by the `width` and `height` properties in CSS.
2 **Padding**: The space between the content and the border, specified by the `padding` property.
3 **Border**: The visible boundary surrounding the padding and content, specified by the `border` property.
4 **Margin**: The space outside the border, creating separation between elements, specified by the `margin` property.

### Example    

```css
/* Example CSS */
.element {
  width: 200px;
  height: 100px;
  padding: 20px;
  border: 2px solid black;
  margin: 10px;
}
```

To calculate the total width of the element:

1. **Content Width**: 200px
2. **Padding**: 20px (left) + 20px (right) = 40px
3. **Border**: 2px (left) + 2px (right) = 4px
4. **Margin**: 10px (left) + 10px (right) = 20px

Total Width = Content Width + Padding + Border + Margin
             = 200px + 40px + 4px + 20px
             = 264px

### Conclusion

Understanding the CSS Box Model is crucial for web designers and developers to create well-structured and visually appealing layouts. By grasping the concept of content, padding, borders, and margins, you gain better control over the design and spacing of elements on a webpage.

With the knowledge of how the CSS Box Model works, you can create more consistent and responsive layouts across different screen sizes and devices. By effectively utilizing properties such as `padding`, `border`, and `margin`, you can fine-tune the appearance and spacing of elements to achieve the desired design.

In conclusion, mastering the CSS Box Model empowers you to create more professional and user-friendly websites, enhancing the overall user experience.

***
