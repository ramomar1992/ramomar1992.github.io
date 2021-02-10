
# HTML Images, CSS Color and Text

## HTML Images

There are many instances that you want to add images to your web page. You perhaps want to show a product, diagram, illustration or just to give extra information about a certein topic. A good image can convey the meaning better than words. Therefore, you have to consider including images to your web page whenever there is a chance that the image will be in a better place than never. 

What should be:

* Relevent to the content
* Delever information
* Easy to recognise
* Confirm with the page's color pallet

### How to organize image files  

If you are building a website from scratch consider creating a separate folder for images to keep your site's files clean and organized. If you, also, have large website with large image content, consider putting them into subdirectories with each directory has images of similer type.

### How to add image to the page

To create an image you can add the \<img> tag. It is a self-closing tag and it does not need a closing tag. Inside the tage you have to provide three main attributes; `src`, `alt`, and `title`. The `src`attribute is where you will add the address of the image; it can be relative or absolute depending on the source of the image. The `alt`attribut is a text contain accurate description to the image. The `title`is extra information that can be provided, so when the user hovers over the image it will show a tootip to the user.

```html
<!-- This code is taken from Duckett HTML book -->

<img src="images/quokka.jpg" alt="A family of
quokka" title="The quokka is an Australian
marsupial that is similar in size to the
domestic cat." />

```

**Note:** You can add the height and width attributes but you would better user CSS to adjust the size of the image.

```html
<!-- This code is taken from Duckett HTML book -->

<img src="images/quokka.jpg" alt="A family of
quokka" width="600" height="450" />

```

### Where to add the image

You can add the image above a paragraph; so text will be in a new line under the image, at the beginning of a paragraph; then the first line of a paragraph will be floating aroung the paragraph, or in the middle of a paragraph; then the whole text will be floating around it. 

```html
<!-- This code is taken from Duckett HTML book -->

<img src="images/bird.gif" alt="Bird" width="100"
height="100" />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic. Many species undertake
long distance annual migrations, and many more
perform shorter irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" />There are around 10,000 living
species of birds that inhabit different
ecosystems from the Arctic to the Antarctic. Many
species undertake long distance annual
migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic.<img
src="images/bird.gif" alt="Bird" width="100"
height="100" />Many species undertake long
distance annual migrations, and many more perform
shorter irregular journeys.</p>

```

**Note**: Programmers in the past used to specify a special `align`attribute to either left or right align the image according to the text position. However, you should do that using CSS.

```html
<!-- This code is taken from Duckett HTML book -->

<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="left" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="right" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>

```

You can also align it vertically, and that will determine where the top line should be placed in accordence to the iamage. But, you,also, should not use it in HTML, instead do it with CSS.

```html
<!-- This code is taken from Duckett HTML book -->

<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="top" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="middle" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" align="bottom" />There are around
10,000 living species of birds that inhabit
different ecosystems from the Arctic to the
Antarctic. Many species undertake long distance
annual migrations, and many more perform shorter
irregular journeys.</p>

```

### General rules to care aobut when adding images to your website

#### Image szie:

Your images should be saved in the same size you want them to appear on your web page. IF you have a bigger picture you need to use on of image editing softweres and edit it to the exact size you need.

#### Resolution 

If you want the image to load properly and quickly, you have to cosider saving the image in the right resolution the web allows it to be. If the resolution of the image is high then it will have a larger size, so the image will load slowly in the page. In the same manner, if you have low resulution image it will not appear nice on the page and you will notice its clearlessness.

**note**: The best resolution for the web is 72 pixles per inche ot 72ppi.

#### Image format

The format of the image is crucial when you choose image with highly color content.

- if your image contain a lot of colors, you need to save it as jpg 
- if there is only few colors in the image save it as png
- if the image is a vector image sace it in SVG
- if you want it to contain animation save it as GIF ot Animated-GIF
- if you want to add images with high transperency save it as png or trans-gif

### Figure and Figure caption

Because images come with captions, in HTML5, there is a new element called figure element \<figure>. This element can contain the image and inside it you can add the \<figcaption> element, where you can type your caption to tell more informaiotn that appears in small font size under the image. 

**Nore**: You can have more than one image inside one \<figure> element as long as the share the same caption.