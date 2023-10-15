---
title: "Mastering Responsive Web Design for Seamless User Experiences: CSS Flexbox (Part A)"
seoTitle: "HOW TO CREATE RESPONSIVE WEB LAYOUTS USING CSS FLEXBOX (Part A)"
seoDescription: "Learn how to create fully responsive 1-dimensional web layouts using the CSS Flexbox layout system"
datePublished: Fri Oct 13 2023 16:00:12 GMT+0000 (Coordinated Universal Time)
cuid: clnosorr6000409lccpc4bmbs
slug: mastering-responsive-web-design-for-seamless-user-experiences-css-flexbox-part-a
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696968816121/d78c270b-e36f-4c77-90d4-693c792a99b7.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696968902436/716f17c6-a46d-48ca-93ee-2c85ae7fd858.png
tags: flexbox, css, frontend-development, responsive-web-design, flex-container

---

Welcome to our second in the series on “**Mastering Responsive Web Design for Seamless User Experiences."** For this module, we will begin with the layout systems, starting with Flexbox. In this guide, you will learn the fundamental principles of Flexbox, a powerful layout model that simplifies web design.

We will explore how to structure and align elements, ensuring your web pages adapt seamlessly to various screen sizes. Whether a beginner or an experienced developer, this resource will empower you to craft dynamic and responsive web layouts. Let's dive in and enhance your web design skills with Flexbox.

## **Prerequisites**

* Before starting this, you must have a basic and solid familiarity with HTML.
    
* Must be familiar with the fundamentals of CSS.
    
* Must understand the CSS box model, how it works, and its application.
    
* A code editor (VS Code recommended).
    
* A web browser (preferably Google Chrome or Mozilla Firefox).
    

## **Introduction to CSS layout**

CSS layouts are essential in web development, as they organize web page structures for various screen sizes. This documentation focuses on a specific layout system. CSS layout is well explained on the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Introduction).

## **CSS layout systems**

1. **Normal flow:** Normal flow is the default way a web page renders HTML code when only HTML controls the layout of the page. The default display property is block. Read more about the normal flow [here](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow).
    
2. **Flexbox:** This layout method helps to lay out contents in a 1-dimensional format along either a row or column. To achieve this, the display on the stylesheet must be set to flex (i.e. display: flex;). We will explore Flexbox later in this article, but visit this [link](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout) to read the official documentation of Flexbox layout.
    
3. **Grid:** In contrast to the 1-dimensional layout of Flexbox, Grid is a 2-dimensional layout system for web pages. It displays content both in rows and columns together. The grid layout system accomplishes many other beautiful features. You can find more [here](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids).
    
4. **Floats:** This property aligns images with text by wrapping the text around the images either to the left or to the right, depending on the float direction you set it to. [Read more](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Floats) here.
    

## **CSS Flexbox and its properties**

CSS Flexbox, also known as Flexible Box Layout, is a smart way to organize and share space among contents inside a container, even if they change in size. It's perfect for making flexible and lively user interfaces, and it's a necessity for today's web development.

Flexbox makes it easier to handle layout challenges like aligning items, distributing spaces, and adapting to different screens and orientations. By mastering the concepts and properties of Flexbox, you can create responsive and appealing web layouts with ease.

* ## **Flex Containers**
    
    To use Flexbox, start by creating a flex container (often a div in HTML) that holds flex items. Below is an illustration of how to set a flex container using a div, and if you look in-depth, you will also notice the flex items nested into the container.
    

```xml
 <div class="flexbox-container">
                <div class="flexbox-item">Item-1</div>
                <div class="flexbox-item">Item-2</div>
                <div class="flexbox-item">Item-3</div>
                <div class="flexbox-item">Item-4</div>
                <div class="flexbox-item">Item-5</div>
                <div class="flexbox-item">Item-6</div>
                <div class="flexbox-item">Item-7</div>
                <div class="flexbox-item">Item-8</div>
            </div>
```

Below are flex properties that are directed to the Flexbox container:

### **1)    Flexbox direction**

Flexbox direction can be set to either row or column. Row is the default direction when flex-direction isn’t defined. Flex direction is set to the following:

* `row` (default)**:** the direction of items aligned from left to right, from the first to the last
    
* `row-reverse`**:** this is the opposite of a row, where alignment is from left to right but starting from the last to the first item.
    
* `column`**:** when aligned as columns, they arrange themselves from top to bottom, starting from the first to the last item.
    
* `column-reverse`**:** like row-reverse, this is the opposite of column. Here, the alignment of items is from top to bottom, starting from the last to the first item.
    
    ```css
    .flexbox-container{
        display: flex;
        flex-direction: row;
        flex-direction: row-reverse;
        flex-direction: column;
        flex-direction: column-reverse;
    }
    ```
    

The following images would help in the understanding of flex-direction.

![Flexbox description image](https://cdn.hashnode.com/res/hashnode/image/upload/v1696971220122/bd2843f5-b110-455d-8272-3901c05b1f4f.png align="center")

Image source….[CSS tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-direction)

Notice the arrow direction, which indicates the direction in which the contents are aligned. 1= row, 2= row-reverse, 3= column, 4= column-reverse.

### **2)    Flex-wrap property**

The wrap property helps flex items wrap into many lines, as flex items by default will be on one line. This property would make them respond to screen sizing so that as the screen reduces, the items wrap into various lines, making them responsive.

**Properties of flex-wrap include:**

* `nowrap`(default)**:** this is the default wrap property, as flex items align themselves to only one line and will not be responsive to screen sizes.
    
* `wrap`**:** this property makes flex items wrapped into many lines from top to bottom.
    
* `wrap-reverse`**:** this is the opposite of the wrap property in direction, as it wraps flex items into many lines from bottom to top.
    
    ```css
    .flexbox-container{
        display: flex;
        flex-wrap: wrap;
        flex-wrap: nowrap;
        flex-wrap: wrap-reverse;
    }
    ```
    

Refer to [CSS tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-direction) for more information and a [visual demonstration](https://css-tricks.com/almanac/properties/f/flex-wrap/).

### **3)    Flex-flow property**

The flex-flow property is a shorthand for defining both the flex-direction and flex-wrap properties as one. It can be any of the following:

![Visual demonstration of the flex flow property](https://cdn.hashnode.com/res/hashnode/image/upload/v1696972308801/88004418-f387-4220-81f0-e686c9345c7e.png align="center")

From your knowledge of 1 and 2 above, you can easily decode what the combinations will do, take note that the default flex-flow property is row nowrap. [Read more...](https://developer.mozilla.org/docs/Web/CSS/flex-flow)

### **4)    The gap property**

The gap property is used to specify the amount of space between one flex item and the other within a flex container. Units can be in pixels (px). The row-gap and column-gap can also be set.

```css
.flexbox-container{
    display: flex;
    gap: 20px;
}
```

### **5) Justify content**

This property aligns content across the main axis of the screen. To understand this better, in flexbox and grid, you will often hear the terms main and cross axis. In real-life scenarios, you can refer to the main axis as the x-axis on a graph as it aligns items from left to right. Justify content has its properties, and I will explain them below.

* **flex-start** (default)**:** by default, we style every flex item as flex-start; this will align items towards the start of the flex-direction of choice. For demonstration purposes, the direction of choice chosen in our demonstration is row. Check out the alignment in the image below.
    
    ![Justify Content: Flex Start](https://cdn.hashnode.com/res/hashnode/image/upload/v1696972803409/117af223-dffd-4d1d-ba5b-2090d276e014.png align="center")
    
* **flex-end:** This property sets the items toward the end of the chosen direction.
    

![Justify Content: Flex End](https://cdn.hashnode.com/res/hashnode/image/upload/v1696972870561/c3404605-81c3-4d28-b59b-19150768fc57.png align="center")

* **center:** the center property aligns the items to the middle or center of the viewport regarding the chosen direction of flex.
    
    ![Justify Content: Center](https://cdn.hashnode.com/res/hashnode/image/upload/v1696972963329/23847129-31cd-4ab8-a8da-b9827eb72d7c.png align="center")
    
* **space-between:** space-between, as the name implies, creates equal spaces in between the items, leaving the item spanned across the direction of flex but little or no space around the items.
    
    ![Justify Content: Space Between](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973005903/ed40b2be-4279-4bd4-a42b-41698e5213e9.png align="center")
    
* **space-around:** this property is almost the same as space between; it creates equal space between the items and equal space around them, but take note that the space between the items and the space around the items are not equal.
    
    ![Justify Content: Space Around](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973044816/97ecf0e9-dafa-4da0-9d16-a4a579577cc5.png align="center")
    
* **space-evenly:** space evenly creates equal spaces around and in between the items. Unlike space-around, all spaces are equal in dimension visually.
    
    ![Justify Content: Space Evenly](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973097896/9693c8ab-f35b-4459-b846-35db010dcf45.png align="center")
    
    Image source: [CSS tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-direction). Visit [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) Docs for detailed charts on their compatibility with various web browsers.
    

### 6)    Align items

The align-items property, unlike the justify-content property, aligns flex items across the cross-axis (y-axis in graphical illustrations) or vertical axis. The following are properties of align-items:

* **flex-start:** Like `flex-start` in `justify-content`, `flex-start` in `align-items` positions items at the beginning of the chosen direction.
    
    ![Align Items: Flex Start](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973353037/2efd2338-74a2-457c-8cbc-1a23d5c7dc72.png align="center")
    
    Notice that the contents are all aligned at the beginning of the cross-axis from the top as opposed to the left when using justify-content. Take note that the flex-direction is set to row.
    
* **flex-end:** flex-end in align-items sets the items to the end of the current line in the cross-axis concerning the flex-direction chosen.
    
    ![Align Items: Flex End](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973437370/044daef7-8fb1-4e34-8d15-af9a86b5e5d6.png align="center")
    
* **center:** the center property aligns the items to the middle or center of the cross-axis.
    
    ![Align Items: Center](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973475290/13bef97e-10b8-4944-91c6-c25d2f1e012e.png align="center")
    
* **stretch** (default)**:** This property of stretch, stretches the items to fill out the cross-axis from top to bottom. It is also the default property of align-items.
    
    ![Align Items: Stretch (Default)](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973520004/5587b5b7-53a2-4997-9730-dad96650531c.png align="center")
    
* **baseline:** this aligns the items such that their baseline aligns with each other.
    
    ![Align Items: Baseline](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973557113/45d5df4b-2aa5-4fbd-93dd-18cad76a40ec.png align="center")
    

### **7)    Align content**

Now we have heard about justify-content that aligns items across the main axis and the align-items that align items across the cross-axis. Note that these two properties take on only single line items, but now what is align-content? It aligns many flex lines across the cross-axis and only takes effect when the flex-wrap property is set to wrap or wrap-reverse.

Like align-items and justify-content above, align-content also has its properties which we will discuss below.

* **flex-start:** this value displays the flex lines at the start of the container relative to the flex-direction set. For illustration, the flex-direction is set to row.
    
    ![Align Contents: Flex Start](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973697734/f1aa1fad-59a1-48b3-a7ed-342d80ea60c6.png align="center")
    
* **flex-end:** this value displays the flex lines at the end of the container relative to the flex-direction chosen.
    
    ![Align Contents: Flex End](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973734192/811c6da2-3c44-4790-8cf7-f60fd3313866.png align="center")
    
* **center:** the center property aligns flex lines to the middle of the container.
    
    ![Align Contents: Center](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973769505/fc7bde1e-9453-49bf-8d4a-8a2cb028a6fe.png align="center")
    
* **stretch** (default)**:** the flex lines are being stretched to take up the remaining space. This is the default value when no align-content value is being set.
    
    ![Align Contents: Flex Stretch (Default)](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973808054/003fbaac-527a-466b-a96e-aac74446ef99.png align="center")
    
* **space-between:** this value provides equal space between the flex lines.
    
    ![Align Contents: Space Between](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973847102/8eecaab0-d218-4fca-b517-a5c6f7e6d3a2.png align="center")
    
* **space-around:** space-around displays the flex lines with spaces before, between, and after them but the spaces are not equal.
    
    ![Align Contents: Space Around](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973899283/ec07d0e4-acb0-40ec-8a50-2bc45c35c8a6.png align="center")
    
* **space-evenly:** this value distributes the flex lines with equal spaces before, between, and after.
    
    ![Align Contents: Space Evenly](https://cdn.hashnode.com/res/hashnode/image/upload/v1696973934658/3c354c25-26e9-4609-abcb-f67059262813.png align="center")
    
    Image source: [**Master Responsive Web Design CSS Grid, Flexbox & Animation**](https://www.udemy.com/share/1072T83@iWQXm9WJOqvzY74EdDmo1gefvZ5HHQXBvYBBecbdGQQR946kfkOqpp_T--BYs1mmmw==/)
    

## Conclusion

We have been able to cover the fundamentals of the CSS flexbox container in this article which is Part A in the flexbox module under this series, and thank you so much for reading thus far.

*In our next article, we are going to be exploring Part B of this topic, which is the flex items (more like the children). Follow this* [*link*](https://nezer.hashnode.dev/mastering-responsive-web-design-for-seamless-user-experiences-css-flexbox-part-b) *to read about it.*

See you on the next one!