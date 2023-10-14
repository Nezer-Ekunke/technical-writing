---
title: "Mastering Responsive Web Design for Seamless User Experiences: Media Query"
seoTitle: "How to Design Responsive Web Layouts"
seoDescription: "Learn how to design responsive websites using media query and other css layout such as grid and flexbox"
datePublished: Sat Oct 07 2023 13:57:32 GMT+0000 (Coordinated Universal Time)
cuid: clng3nw11000908lg4dcvci5c
slug: mastering-responsive-web-design-for-seamless-user-experiences-media-query
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696617851145/ee33775a-1fda-442a-b20d-daef5b9623dc.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696617940624/5428ead6-a8e4-443e-a687-5e2978e0a611.png
tags: media-queries, css, web-development, frontend-development, responsive-web-design

---

Responsive design layout is like a magic trick for websites and web apps. It's the way they adjust themselves to fit nicely on different screens, like tablets, phones, laptops, and desktop computers. This way, no matter what kind of screen you're using, the website or app will arrange its contents to look great.

In this guide, we will dive through different methods of achieving responsive design but will focus on media queries for this article, and others in subsequent documentation under this series.

## **Prerequisite**

* A solid understanding of HTML and the CSS Box model.
    
* Limited or no prior experience in responsive web design and CSS-based layout systems.
    

## **i) Introduction to Responsive Web Design**

Responsive web design is an approach to designing and building websites that aim to make web pages look and function well on a variety of devices and screen sizes. Here's a simple explanation:

Imagine you have a website that looks great on a big computer screen. But what happens when someone tries to view it on a tiny smartphone screen? Without responsive design, the website might look all jumbled up and be hard to use.

Responsive web design solves this problem. It's like having a website that's smart and flexible. It adapts to different devices automatically, so it always looks good and works smoothly, whether you're on a computer, tablet, or phone.

To make a website responsive, the viewport meta tag must be added to all your HTML documents.

```xml
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Without this viewport meta tag, the website won’t be responsive, below is an example of a website without the viewport meta tag and with the viewport meta tag.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696541172314/7258cf31-8f73-4c54-b54b-b06b60e56005.png align="center")

Source: [w3schools](https://www.w3schools.com/html/html_responsive.asp)

### **A) Relevance of responsive web design to web development**

Responsive web design is important for web developers because it helps make websites look good and work well on all kinds of devices, like big computers and small phones. It's like making sure your clothes fit you, no matter if you're big or small.

This is essential because people use all sorts of gadgets to browse the web, and we want everyone to have a good experience. It also helps websites show up better in search engines like Google, which is like making your lemonade stand easy to find in a big park.

Responsive design makes it easier for developers to build websites that everyone can use, no matter what kind of device they have.

### B) **Methods of creating responsive web layouts**

Diverse techniques for implementing responsive web design include:

1. **Responsive Images**: This entails configuring the CSS width or max-width attribute of images using responsive units, like percentages. This adjustment ensures that images adapt seamlessly to the relative dimensions of the web page when accessed on different devices or screen resolutions.
    
2. **Responsive Text Sizing**: Achieving responsive text involves using measurement units such as viewport width (vw) or rem. These units leverage the dimensions of the user's browser window to dynamically determine text size. This methodology enables text to scale appropriately to accommodate a range of screen sizes.
    
3. **Responsive Layout Systems:** This approach involves the application of responsive CSS layout methodologies like CSS flexbox and CSS grids. These systems facilitate the creation of one-dimensional (1D) and two-dimensional (2D) layouts for content, organized along the main and cross axes. They prescribe how these layouts should adapt to varying screen resolutions, depending on the specific layout system employed.
    
4. **Media Queries**: Media queries utilize the `@media` tag to target specific screen resolutions across a spectrum of devices, encompassing desktops, laptops, tablets, and phones. They provide the means to customize and adjust content to suit each screen size precisely.
    
5. **Responsive web design frameworks:** Various CSS frameworks offer layouts for responsive web design such as W3.CSS and Bootstrap. Read the official documentation of W3.CSS [here](https://www.w3schools.com/w3css/default.asp) and [Bootstrap](https://getbootstrap.com/docs/5.0/getting-started/introduction/).
    

Today, our primary focus will be on the subject of media queries, and we will explore this topic further in forthcoming sessions.

## ii) **Understanding media queries**

Media queries are a crucial CSS feature that enables responsive web design by allowing web pages to dynamically adapt to various screen sizes and media types. The application of media queries depends on different device characteristics and media conditions.

Let's delve into the key components of media queries that play a pivotal role in styling web pages:

1. `@media` **Rule:** Media queries are initiated using the `@media` rule, followed by a set of curly brackets containing the CSS code to apply when specific conditions are met. Additionally, the `@media` rule specifies the target media type. An example is demonstrated below.
    
    ```css
    @media (max-width: 900px) {
            img{     
                max-width: 500px;
                }
    }
    ```
    
    In the illustrated example, take note of the `@media` declaration, which encapsulates the 'max-width: 900px' syntax. This declaration establishes a breakpoint that aims at a particular screen size, a concept we will delve into further in the 'breakpoint' section.
    
2. **Parentheses:** Within the parentheses of a media query, precise conditions are defined to dictate the behavior of content. For instance, to limit the maximum width of all images on mobile devices to 100px, the following code accomplishes this task:
    
    ```css
    @media (max-width: 480px) {
            img{     
                max-width: 100px;
                }
    }
    ```
    
    In the provided image, observe that the specified screen size has a maximum of 480px, exclusively targeting mobile devices. Larger devices, such as laptops and tablets, are excluded from this rule. As a result, when the screen width contracts to 480px or less, images automatically resize to 100px or smaller as the screen size diminishes.
    
3. **Media Types:** Following the `@media` rule, media queries must specify the intended media type. These media types fall into distinct categories:
    
    `all` — applicable to all media types.
    
    `print` — designed for printing devices.
    
    `screen` — tailored for computer screens, tablets, and smartphones.
    
    `speech` — intended for screen readers that vocalize content.
    
    Failure to specify a media type defaults the query to target all devices.
    
    For example, if the goal is to apply the rules from the previous example (point 2) exclusively to screens, the code can be amended to include 'screen,' ensuring it solely applies to screen devices, excluding printers and speech.
    
    The declaration 'screen and (max-width: 480px)' signifies the targeting of screens with a width of 480px or less.
    
    ```css
    @media screen and (max-width: 480px) {
            img{     
                max-width: 100px;
                }
    }
    ```
    
4. **Orientation:** This feature sets the rule for the content behavior along the browser orientation, usually as landscape or portrait.
    
    Let's take, for example, the default orientation of a mobile device as portrait and that of laptops are landscape.
    
    Now if the browser on a phone changes to landscape during auto-rotate, and a laptop user resizes the browser window, if the orientation feature is not applicable, contents may not align, but if the features are defined for both potrait and landscape, whatever mode the devices are been used, the contents align themselves following the preset rules.
    
    Take for instance on portrait the image is set to a width of 100px for devices with a max-width of 480px (mobile devices) once the browser screen shrinks to this level, the image automatically resizes to 100px. But what happens when the browser is then rotated to landscape? This is where the orientation of landscape comes in, where the width is longer than the height.
    
    Therefore in landscape, it can be adjusted by setting the orientation to landscape targeting devices with a max-width of 480px. We would agree that in the case of landscape, the image would be larger across its width, so we can then set the image to let's say a width of 150px.
    
    ```css
    @media screen and (max-width: 480px) and (orientation: portrait) {
            img {
              max-width: 100px;
            }
    }
    
    @media screen and (max-width: 480px) and (orientation: landscape) {
            img {
              max-width: 150px;
            }
    }
    ```
    
5. **Breakpoints**: Breakpoints represent pivotal screen size thresholds at which layout adjustments are triggered, and new CSS rules within media queries come into effect. As seen in the previous example, a breakpoint was established with a maximum width of 480px, affecting all devices below this width. Once the screen size surpasses 480px, the media query rules are invoked.
    

Alternatively, breakpoints can be defined using min-width declarations, e.g., (min-width: 480px), which influences devices with widths exceeding 480px, encompassing tablets, iPads, laptops, and larger screens.

An advanced targeting method combines both min-width and max-width rules. For instance, (min-width: 481px and max-width: 768px) encompasses devices with widths ranging between 481px and 768px. This excludes mobile devices below 480px while encompassing iPads and tablets within this range. Notably, laptops and larger devices are excluded because the 'max-width' is defined as 768px, exceeding typical laptop screen sizes.

Here's a reference guide for various common breakpoints in CSS media queries based on device width:

* 320px — 480px: Mobile devices.
    
* 481px — 768px: iPads, Tablets.
    
* 769px — 1024px: Small screens, laptops.
    
* 1025px — 1200px: Desktops, large screens.
    
* 1201px and above — Extra-large screens, TV.
    

```css
@media screen and (min-width: 320px) and (max-width: 480px) {
        img {
          max-width: 100px;
        }
}

@media screen and (min-width: 481px) and (max-width: 768px) {
        img {
          max-width: 300px;
        }
}

@media screen and (min-width: 769px) and (max-width: 1024px) {
        img {
          max-width: 500px;
        }
}
```

It's worth noting that breakpoints can vary, as there are no universally standardized values. Nonetheless, these breakpoints serve as widely accepted standards for web pages and applications designed for various devices.

## **Conclusion**

Responsive Design is a must in today’s web design and development field. Media queries are one of the most important parts of building responsive layouts, and I hope you found this article helpful in understanding how media queries work. For better understanding, visit [W3Schools](https://www.w3schools.com/css/css_rwd_intro.asp) for more information on everything you need to know and understand about media query and frontend development.

**RECOMMENDED RESOURCES**

Practice along with [freeCodeCamp](https://www.freecodecamp.org/learn/2022/responsive-web-design/).

[Master Responsive Web Design CSS Grid, Flexbox & Animation](https://www.udemy.com/share/1072T83@iWQXm9WJOqvzY74EdDmo1gefvZ5HHQXBvYBBecbdGQQR946kfkOqpp_T--BYs1mmmw==/) by Norbert B. Menyhart on Udemy.

Thanks for reading. I would love to connect with you. Connect with me on [X(Twitter)](https://twitter.com/EkunkeEbenezer?t=tW6464K0mmyhbk4XVtv50A&s=09) and [LinkedIn](https://www.linkedin.com/in/ebenezer-ekunke-65a1581a2). I'd appreciate your feedback, so please like and comment with your thoughts. If you found this article very helpful, do well to share it with others and subscribe to my newsletter below.

*In our next article, we are going to be talking about the layout systems for responsive design, starting with CSS Flexbox.* [**Click here**](https://nezer.hashnode.dev/mastering-responsive-web-design-for-seamless-user-experiences-css-flexbox-part-a-clnosorr6000409lccpc4bmbs) *to read it.*

See you on the next one!