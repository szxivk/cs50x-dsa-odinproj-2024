# HTML Foundations

- HTML and CSS:
- HTML is the raw data that a webpage is built out of. All the text, links, cards, lists, and buttons are created in HTML. CSS is what adds style to those plain elements. HTML puts information on a webpage, and CSS positions that information, gives it color, changes the font, and makes it look great!
-  they are only concerned with presenting information. They are not used to program any logic. JavaScript is a programming language and it’s used to make webpages do things.
- HTML markups are enhanced by CSS and JavaScript, which is why it’s recommended that you learn this programming language first. it allows you as a website owner to create the basic structure of you website
- While CSS is a static programming language, it can be used to make your website appear visually pleasing and modern.
- Along with the presentation of HTML, CSS can also be used to alter the layout and formatting of your website.
- While HTML provides the structure for a website and CSS allows you to control the presentation of a site, the JavaScript programming language gives you the tools that you need to alter the behavior of different elements that are found on a website page.


## Elements and Tags

- HTML (HyperText Markup Language) defines the structure and content of the webpages (which are basically like documents). its made up of tags.
- Almost all elements on an HTML page are just pieces of content wrapped in opening and closing HTML tags.
- eg,. a full paragragph element looks like following:
  ```html
  <p>some text content</p>
  ```
  - Opening tags `<keyword>` tell the browser that this is the start of an HTML element. `<p>` in above example.
  - Closing tags tell the browser where an element ends. They are almost the same as opening tags; the only difference is that they have a forward slash before the keyword. `</keyword>`. `</p>` in above example.
  - `some text content` represents content wrapped within the opening and closing tags.
  - The opening and closing tags tell the browser what content the element contains. The browser can then use that information to determine how it should interpret and format the content.
- [Predefined tags in HTML](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).
- It is important to use the correct tags for content. Using the correct tags can have a big impact on two aspects of your sites:
  - how they are ranked in search engines; and
  - how accessible they are to users who rely on assistive technologies, like screen readers, to use the internet.
- Using the correct elements for content is called **semantic HTML**.

#### Void Elements

- Some HTML elements do not have a closing tag.
- like: `<br>` or `<img>`.
- No closing tag means they can’t wrap content like other tags do. therefore, they are void of any content, there is nothing inside of them.

**NOTE**: You might also see these referred to as self-closing tags. But those are just void elements with a forward slash(/) at the end like: `<br /> `or `<img />`, but the latest version of the HTML specification discourages their use and considers them invalid.

#### HTML Boilerplate

- All HTML documents have the same basic structure or boilerplate that needs to be in place before anything useful can be done

**NOTE**: We should always name the HTML file that will contain the homepage of our website index.html. This is because web servers will by default look for an index.html page when users land on our websites – and not having one will cause big problems.

**TIP**: VSCode has a built-in shortcut you can use for generating all the boilerplate in one go. Please note that this shortcut only works while editing a file with the .html extension or a text file with the HTML language already selected. To trigger the shortcut, delete everything in the index.html file and just enter ! on the first line. This will bring up a couple of options. Press the Enter key to choose the first one, and voila, you should have all the boilerplate populated for you.

- boilerplate will look as follows:
```html
<!DOCTYPE html> <!--HTML page starts with a doctype declaration. this is how we write comment in HTML-->

<html lang="en"> <!--This is what’s known as the root element of the document-->
    <!--lang above represents an HTML attribute-->
    <head>
        <meta charset="UTF-8">
        <title>My First Webpage</title>
    </head>

    <body>

    </body>
</html>
```
- The `<head>` element is where we put important meta-information about our webpages, and stuff required for our webpages to render correctly in the browser. Inside the `<head>`, we should not use any element that displays content on the webpage.
-  The `<body>` element is where all the content that will be displayed to users will go - the text, images, lists, links, and so on.

#### Paragraphs

-  A paragraph element is defined by wrapping text content with a `<p>` tag.
-  If we want to create paragraphs in HTML, we need to use the paragraph element, which will add a new line after each of our paragraphs.
-  Otherwise when the browser encounters new lines in your HTML, it will compress them down into one single space (**only first space counts**). The result of this compression is that all of the text is clumped together into one long line.

#### Headings

- There are 6 different levels of headings starting from `<h1>` to `<h6>`
- Headings are defined much like paragraphs. For example, to create an h1 heading, we wrap our heading text in an `<h1>` tag.

#### Strong Element

- The `<strong>` element makes text bold. It also semantically marks text as important; this affects tools, like screen readers, that users with visual impairments will rely on to use your website.
- To define a strong element, we wrap text content in a `<strong>` tag.
  ```html
  <body>
    <p>Lorem ipsum <strong>dolor sit</strong> amet, consectetur adipiscing elit.</p>
  </body>
  ```

#### Em Element

- The `<em>` element makes text italic. It also semantically places emphasis on the text, which again may affect things like screen readers. To define an emphasised element, wrap the text content in an `<em>`tag.

#### Nesting and indentation

- When we **nest** elements within other elements, we create a parent and child relationship between them. The nested elements are the children and the element they are nested within is the parent.
- In the following example, the body element is the parent and the paragraphs are the child:
  ```html
<html>
  <head>
  </head>
  <body>
    <p>Lorem ipsum dolor sit amet.</p>
    <p>Ut enim ad minim veniam.</p>
  </body>
 </html>
  ```
-  HTML parent elements can have many children. Elements at the same level of nesting are considered to be siblings.
-  We use **indentation** to make the level of nesting clear and readable for ourselves and other developers who will work with our HTML in the future.
-  
**REMEMBER**: In order to write an HTML comment, we just enclose the comment with `<!-- and -->` tags. and the vscode shortcut in Windows and Linux Usersis: Ctrl + /

#### Lists

- Unordered lists:  created using the `<ul>` element, and each item within the list is created using the list item element `<li>`.
  - Each list item in an unordered list begins with a bullet point.
- Ordered lists: created using the `<ol>` element. Each individual item in them is again created using the list item element `<li>`. 
  - However, each list item in an ordered list begins with a number instead.

#### Links

- Links are one of the key features of HTML. They allow us to link to other HTML pages on the web. In fact, this is why it’s called **the web**.
- To create a link in HTML, we use the anchor element. An anchor element is defined by wrapping the text or another HTML element we want to be a link with an `<a>` tag.
- But, we need to add an href (hypertext reference) attribute to the opening anchor tag. The value of the href attribute is the destination we want our link to go to.
**NOTE**: An HTML attribute gives additional information to an HTML element and always goes in the element’s opening tag. 
  ```html
  <a href="https://www.theodinproject.com/about">About The Odin Project</a>
  ```
**NOTE**: you can use anchor tags to link to any kind of resource on the internet, not just other HTML documents. You can link to videos, pdf files, images, and so on,
but for the most part, you will be linking to other HTML documents.

- Below is how you code safer links which open in a new tab:
```html
<a href="https://www.theodinproject.com/about" target="_blank" rel="noopener noreferrer">About The Odin Project</a>
```

- The `target` attribute: While `href` specifies the destination link, target specifies where the linked resource will be opened.
If it is not present, then, by default, it will take on the `_self` value which opens the link in the current tab.
To open the link in a new tab or window (depends on browser settings) you can set it to `_blank`.

- The `rel` attribute: is used to describe the relation between the current page and the linked document.

- The `noopener` and `noreferrer` values are ways to protect the page you're coming from and make the interaction between pages safer.
  - these are used to:
    1. Prevent security risks (by stopping the new page from messing with the original page).
    2. Enhance privacy (by hiding the source page from the new page).

-  It is recommended to always pair a `target="_blank"` with a `rel="noopener noreferrer"`.


- Links to pages on other websites on the internet are called **absolute links**.
  - made up of the following parts: `protocol://domain/path`

- Links to other pages within our own website are called **relative links**.
  - Relative links only include the file path to the other page, relative to the page you are creating the link on (see example in code_along/odin-links-and-images).

#### Images

- To display an image in HTML we use the `<img>` element. Unlike the other elements we have encountered, the `<img>` element is a void element.
As we have seen earlier in the course, void elements do not need a closing tag because they are naturally empty and do not contain any content.
- Instead of wrapping content with an opening and closing tag, it embeds an image into the page using a `src` attribute which tells the browser where the image file is located. The `src` attribute works much like the `href` attribute for anchor tags. It can embed an image using both *absolute* and *relative* paths.
- Besides the `src` attribute, every image element must also have an `alt` (alternative text) attribute.
- The `alt` attribute is used to describe an image. It will be used in place of the image if it cannot be loaded. It is also used with screen readers to describe what the image is to visually impaired users.
- Specifying `height` and `width` attributes in image tags helps the browser layout the page without causing the page to jump and flash.
**NOTE**: It is a good habit to always specify these attributes on every image, even when the image is the correct size or you are using CSS to modify it.
- check examples in odin-proj/webdev-foundations/code-along/odin-links-and-images

#### Commit messages
- [an amazing article.](https://cbea.ms/git-commit/)
