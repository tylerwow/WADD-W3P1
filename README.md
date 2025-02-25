# Week 3 Practical 1 - Responsive layouts with media queries

In this practical you will implement a responsive layout using media queries.

Make a new copy of the York University Press website you created last practical. In this stage, you will add media queries to the CSS to make the site layout work for small and medium-sized devices. Screenshots of my media query layouts are shown at the bottom of this document.

### Exercise 1.1: Evaluate the current layout in the device simulator
Run the website in Chrome using the Live Preview extension and open the device simulator, which you can find in Developer Tools. Set the device simulator to responsive mode then view the site at different breakpoints by clicking the grey bars above the site. Scroll the full length of the site at each breakpoint and determine when and how the layout stops working on smaller screens. The breakpoint at which you start to see problems will depend on the details of your design. My layout starts to have problems at the tablet breakpoint (768px) and gets worse the smaller the breakpoint.

Some things to look out for:
- Having to scroll left and right to see some content
- Overlapping text
- Images that are too big for the screen
- Very narrow lines of text

### Exercise 1.2: Improve the existing code
Add the viewport meta tag to the `<head>` of the HTML file:
```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Use the device simulator in Chrome to explore how simply adding this tag has affected the layout on different devices.

### Exercise 3.3: Customise the layout for medium-sized devices
Remove the page background colour and margins around the content area for all devices smaller than 768px. To do this, add the following media query and override the appropriate style rules (one example of overriding styles is provided).
```
@media screen and (max-width:768px) {
    body {
        background-color: white;
    }
}
```
Here are some more changes to make for medium-sized devices:
- Make the date left aligned.
- Change the middle section of the page from a two-column layout to a single column. Make sure the `<main>` and `<aside>` take up the full width of their container.
- Now that the “Most Popular” section is full width on tablets, make the three sections it contains appear side by side.

Create further customizations if they will improve the layout on tablets.

### Exercise 3.4: Further customize the layout for small devices
For this exercise, we’ll define small devices as those under 425px wide. Add a media query with a `max-width` of 425px and make the following layout changes for small devices only:
- Remove the float on the main story image, centre align it and make sure it’s no bigger than the width of its container. You will need to use the `max-width` property.
- In the previous exercise, you converted the “Most Popular” section from a single column to a three-column layout for all devices less than 768px. This style should only apply to tablets. For devices with a maximum width of 425 pixels, the layout of the “Most Popular” section should be the same as it is for devices bigger than 768px.

Create further customizations if they will improve the layout on the smallest devices. Be sure to check how your site looks at the smallest breakpoint.

## Stage 2: (Optional) Make Your Portfolio Responsive
If you finish early, add go back to the portfolio you have worked on in previous practicals and check how it appears on small devices. Add media queries to adjust the layout as needed.

## York University Press medium (tablet) device layout
![The York University Press web page optimised for medium sized devices](https://github.com/IM-WADD/Week3Practical1/blob/main/assets/tablet.png)

## York University Press small (phone) device layout
![The York University Press web page optimised for small sized devices](https://github.com/IM-WADD/Week3Practical1/blob/main/assets/phone.png)
