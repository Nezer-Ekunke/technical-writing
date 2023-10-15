---
title: "Mastering Responsive Web Design for Seamless User Experiences: CSS Flexbox (Part B)"
seoTitle: "HOW TO CREATE RESPONSIVE WEB LAYOUTS USING CSS FLEXBOX (Part B)"
seoDescription: "Learn how to create fully responsive 1-dimensional web layouts using the CSS Flexbox layout system"
datePublished: Sun Oct 15 2023 15:00:10 GMT+0000 (Coordinated Universal Time)
cuid: clnrlf95z000109ld01wx4rin
slug: mastering-responsive-web-design-for-seamless-user-experiences-css-flexbox-part-b
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696975648642/b606b3cb-8b29-4ccc-87b8-8295bbbcea85.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696975802053/6ad69f9b-78ef-4e96-8d49-704806efbc82.png
tags: flexbox, css, web-development, frontend-development, responsive-web-design

---

Welcome to Part B of the topic “**Mastering Responsive Web Design for Seamless User Experiences: CSS Flexbox.”** In our preceding article, we talked about Flexbox, with a primary focus on the Flexbox container and its associated properties. In this module, we're diving deeper into Flexbox to focus on flex items, which make up the Flex container.

We aim to show you how to structure and align flex items, as we did with flex containers. If you missed our previous discussion on flex containers or need more clarity, check out our earlier article via the link provided. This will give you a solid foundation to understand the topics in this current article.

## **Prerequisites**

* Before starting this, you must have a basic and solid familiarity with HTML.
    
* Must have previous knowledge of Flex containers and their properties.
    
* Must understand the CSS box model, how it works, and its application.
    
* A code editor (VS Code) is recommended.
    
* A web browser (Google Chrome or Mozilla Firefox).
    

## **Flex Items**

Flex items are children of the parent or flex container. They are the items that make up the flex container that we talked about earlier. Flex items also have properties, just like the flex container.

1. **Align self:** This property aligns individual flex items across the cross-axis inside the flex container. When this is set on a particular item, the value overrides the already existing align-item value. Take note that align-items targets all the items in a flex-container while align-self targets only one individual item.
    
    The properties of align-items are the same as align-self, but in this case, individual items are targeted. For instance, if I want to display item-3 as flex-start and item-4 as flex-end, this would be the code and the result.
    
    ```css
    .flexbox-container .item-3{
        align-self: flex-start;
    }
    
    .flexbox-container .item-4{
        align-self: flex-start;
    }
    ```
    
    ![align self demonstration](https://cdn.hashnode.com/res/hashnode/image/upload/v1696977129009/1cd3f183-3098-4dd5-a6ba-e89af0995789.png align="center")
    
    Notice that all other items are aligned as the default align-item property (stretch), but item-3 is self-aligned as flex-start across the cross-axis and item-4 as flex-end.
    
2. **Order:** This property determines the order in which items are placed. The default value is 0, and if set to a positive integer like 1, the item moves forward by 1 time; if set to 2, it moves forward by 2 times. But if set to a negative integer by -1, it moves backward 1 time, and if set to -2, it moves backward 2 times, and so on. Observe the illustration below.
    
    ```css
    .flexbox-container .item-3{
        order: 3;
    }
    ```
    
    ![order demonstration](https://cdn.hashnode.com/res/hashnode/image/upload/v1696977396856/371aa560-4df9-4179-9df2-69693b2ca8f8.png align="center")
    
    Item-3 was set to order 2, so it moved 2 places forward, making it the last item. Note that there are no units for the numbers specified.
    
3. **Flex grow and shrink:** This determines the extent to which a flex item grows or shrinks if necessary; take note that negative numbers are not required.
    
    ![Flex grow and shrink](https://cdn.hashnode.com/res/hashnode/image/upload/v1696977554684/c248f52a-bd53-4b56-aa1e-af9551fad68a.png align="center")
    
4. **Flex basis:** this value sets the size of an item. This can be set as auto or using figures with responsive units (recommended) in %, rem, etc. Also, px can be used.
    
    In the example below, the flex-basis is set to 200px for the number 3 item.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696977628545/97da1bb6-4190-4170-ad2c-8f76bf7a3fbd.png align="center")
    
    Source: [W3Schools](https://www.w3schools.com/css/css3_flexbox_items.asp#align-self)
    
5. **Flex property:** the flex property, just like the flex-flow property, is a shorthand combination of the flex-grow, flex-shrink, and flex-basis properties if you decide to target them all as one rather than being separate from them.
    
    ```css
    .flexbox-container .item-3{
        flex: 4 2 200px;
    }
    ```
    
    The first number represents flex-grow, the second represents flex-shrink, and the last represents flex-basis.
    

## Conclusion

In summary, mastering CSS Flexbox opens up new possibilities for web developers. It allows you to create adaptable and stylish designs that work well on various devices and screens. This documentation provides a solid understanding of Flexbox principles and methods, giving you the skills to enhance your web development expertise.

Whether you're designing a simple blog layout or a complex multi-column dashboard, Flexbox ensures your designs remain refined and functional across different digital platforms.

Another resource you can check out is this full-fledged Udemy course on [Mastering Responsive Web Design CSS Grid, Flexbox & Animations](https://www.udemy.com/course/master-responsive-web-design-css-grind-flexbox-animations/?kw=master+css+flexbox&src=sac) by Norbert B. Menyhart. It is one of my most recommended courses for a beginner to master the art of CSS layout systems, besides the official documentation.

*In our next article, we are going to explore the third topic in this series,* ***Mastering Responsive Web Design Layout for Seamless User Experiences***, which is the CSS Grid Layout. Stay tuned by subscribing to my newsletter to be notified when it is released.

Thanks for reading. I would love to connect with you. Connect with me on [**X(Twitter)**](https://twitter.com/EkunkeEbenezer?t=tW6464K0mmyhbk4XVtv50A&s=09) and [**LinkedIn**](https://www.linkedin.com/in/ebenezer-ekunke-65a1581a2). I'd appreciate your feedback, so please like and comment with your thoughts. If you found this article very helpful, do well to share it with others. See you at the next one!