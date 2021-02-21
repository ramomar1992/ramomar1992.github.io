# CSS Images and Practical 

## CSS Images and

### Images Sizes and Alignment

We can resize images using the height and width properties. When doing so, we help the page load faster and smoother. Instead of specifying images sized individually, you can create three categories: small, medium, large, and then you can apply it to your images in the class name, so you only need to write CSS the code once.

#### Images Alignment

To align images, you can also do that in two way:

1. Add the float property to the sizing code that uses the class selector.
2. Use new class names such as left and right and use the float properties inside the new class selector for the new class name.

#### Centering Images

Images are inline elements by default; therefore, you need to change their state to block so you can align them in two ways:

1. You can use the `text-align` property and make it center on the containing element.
2. You can use the `margin` property and set left, and right offsets auto.

### Background Images

The background-image property allows you to place an image behind any HTML element. By default, a background image will repeat to fill the entire box.

#### Background Image Repeat and Attachment

Since the background image can be small and repeat to spread around the whole containing element, you can specify the repeat property. It may have four values:

1. repeat: this is the default, and the image will be repeated across the whole element.
2. repeat-x: this will repeat only along the x-axis or horizontally.
3. repeat-y: this will repeat only along the y-axis or vertically.
4. no-repeat: the image will show only once.

We can specify the attachment property, so the background has different behaviors:

1. fixed: the image stays in the same position.
2. scroll: the background image will move up and down while the user scrolls the page.

#### Background positioning

When an image is not being repeated, you can use the background-position property to specify where the background image should be placed in the browser window. This property usually has a pair of values. The first represents the horizontal position, and the second represents the vertical.

*Note*: If you only specify one value, the second value will default to center. You can also use a pair of pixels or percentages. These represent the distance from the top left corner of the browser window (or containing box).

#### Shorthand background

The properties must be specified in this order:

1. background-color
2. background-image
3. background-repeat
4. background-attachment
5. background-position

CSS3 will also support the use of multiple background images by repeating the background shorthand.

#### Image Rollover and Sprits

When we use different images to style a single element in different states, this is called Rollover. When we use one image and change its position to indicate different states of the element, it's called Sprite. The advantage of using sprites is that the web browser only needs to request one image rather than many images, making the web page load faster.

```CSS

a.button {
height: 36px;
background-image: url("images/button-sprite.jpg");
text-indent: -9999px;
display: inline-block;}
a#add-to-basket {
width: 174px;
background-position: 0px 0px;}
a#framing-options {
width: 210px;
background-position: -175px 0px;}
a#add-to-basket:hover {
background-position: 0px -40px;}
a#framing-options:hover {
background-position: -175px -40px;}
a#add-to-basket:active {
background-position: 0px -80px;}
a#framing-options:active {
background-position: -175px -80px;}

```

#### Backgorund Gradients

It is allowed to add color in gradient to any element. It represents the hues of colors from one side of the image to another. We specify different colors, and the gradient will be the range of colors that comes between them. 

```CSS

#gradient {
/* fallback color */
background-color: #66cccc;
/* fallback image */
background-image: url(images/fallback-image.png);
/* Firefox 3.6+ */
background-image: -moz-linear-gradient(#336666,
#66cccc);
/* Safari 4+, Chrome 1+ */
background-image: -webkit-gradient(linear, 0% 0%,
0% 100%, from(#66cccc), to(#336666));
/* Safari 5.1+, Chrome 10+ */
background-image: -webkit-linear-gradient(#336666,
#66cccc);
/* Opera 11.10+ */
background-image: -o-linear-gradient(#336666,
#66cccc);
height: 150px;
width: 300px;}

```

#### Contrast

If you want to add text to the background image element, you have to care about the contrast between the image and the text. Because images usually have high contrast, we need to modify their color before using them as background images.

![Image contrast](../images/contrast.png)

## Practical information

### SEO - Search Engine Optimization

In this section we will cover what should you do to incease chances that your web page will appear to the top of search engine results when a user searches for a topic that your website covers.

### On-Page Techniques

On-page techniques rely on text content on your page and how it would be relevant to the search keywords that users input in serach engines. There are seven places where you can place these keywords in order for the engines to rate your website as relevant:

1. The page title
2. The web address of your site
3. Headings
4. Texts
5. Link text
6. Image alt text
7. Page description

#### How to determine the keywords your going to include in your pages

Determining which keywords to use on your site can be one of the hardest tasks when you start to think about SEO. Here are six steps that will help you identify the right keywords and phrases for your site:

1. Brainstorming: you can list all topics keyword your website covers and you may ask people what would they enter on the search engine to get to your site's topics.
2. Organize: sort keywords into different categories.
3. Research: there are several tool that can help provide you with new keywords to include.
4. Compare: you may compare the keywords you came up with with other website that use the same keywords and look for how many times a certain keywords has been used to reach for these sites.
5. Refine: you need to pick which keywords you will focus on. These should always be the ones that are most relevant to each section of your site. If there is a phrase that is very relevant but you find there is a lot of competition, you should still use it. To improve the chances of your site being found you can look at whether there are other words that could be incorporated into a phrase.
6. Map: it is picking which keywords should go on which page ot group of pages.

## Analytics

When you post your site on the web, and the visitors begin to reach it, you need to analyze them on many aspects. There are several tools you can use to do your analysis, and one of the best tools is GOOGLE ANALYTICS. You first need to sign up for an account to use this service, and then Google will give you a tracking code that links to your website and record web traffic to your site.

There are many features that the service offers. Following is some of them: 

* ### How many people are coming to your site: 

It records many types of information such as:

1. Visits
2. Unique visits
3. Pageviews
4. Pages per visit
5. Average time on site

* ### What are your visitors looking at:

This allows you to learn more about what the visitors come to your site for. It records:

1. Pages your visitors looking at
2. Landing pages
3. Top exit Pages
4. Bounce rate

* ###  Where are your visitors come from

It is like trafficking where your visitors come from. This can be very handy since you can get in touch with those sites' owners and sites with the same topics so that you can cooperate with them. It provides you with this information: 

1. Referrers sites and number of people come from them
2. Direct input or direct access from sources other than the web
3. Search terms that users used to get to your site from the search engines
4. Many more advanced features that give you huge control over your website traffics

## Domain Names and Hosting