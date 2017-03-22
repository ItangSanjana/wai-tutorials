---
title: Content Structure
status: draft
order: 6
wcag_success_criteria:
  - 1.3.1
wcag_techniques:
  - H40
  - G62
  - H48
  - H49
---
Mark-up website content semantically, so that the website is extensible, the content reusable and also conveys more meaning to assistive technologies.

## Articles

The HTML5 `<article>` element represents a complete or self-contained composition in a web page. Examples of articles include an item in a web shop or a news article on a news site.

{::nomarkdown}
<%= code_start %>
{:/nomarkdown}

~~~html
<article>
  <h2>Space Bear Classic</h2>
  …
</article>
<article>
  <h2>Space Bear Extreme</h2>
  …
</article>
~~~

{::nomarkdown}
<%= code_end %>
{:/nomarkdown}

## Sections

The HTML5 `<section>` element marks a general region of a web page or an article. It is used for thematic grouping of content.

{::nomarkdown}
<%= code_start %>
{:/nomarkdown}

~~~html
<section>
  <h2>Chapter 2</h2>
  …
</section>
~~~

{::nomarkdown}
<%= code_end %>
{:/nomarkdown}

## Paragraphs

Use the paragraph element (`<p>`) to mark-up paragraphs of text, such as this one. Consistent styling of paragraphs improves text readability. It also gives users more control when customizing their view.

## Lists

Use different types of lists to group information according to its nature to provide orientation for users.

* Unordered lists are used when the order of the items is not relevant. List items in unordered lists are marked with a bullet.
* Ordered lists are used for sequential information and are automatically enumerated by the browser.
* Description lists groups of related terms and descriptions and connects those programmatically.

Individual list items can contain a variety of HTML elements, including paragraphs, headings, form elements, and other (nested) lists.

### Unordered list

The unordered list consists of one `<ul>` element and multiple list item (`<li>`) elements:

{::nomarkdown}
<%=sample_start%>
<ul>
    <li>Corn</li>
    <li>Tomatoes</li>
    <li>Beans</li>
    <li>Onions</li>
    <li>Garlic</li>
    …
</ul>
<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<ul>
    <li>Corn</li>
    <li>Tomatoes</li>
    <li>Beans</li>
    <li>Onions</li>
    <li>Garlic</li>
    …
</ul>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

### Ordered list

The unordered list consists of one `<ol>` element and multiple list item (`<li>`) elements:

{::nomarkdown}
<%=sample_start%>
<ol>
    <li>Cook beans for 45 minutes.</li>
    <li>Cut vegetables in small cubes.</li>
    <li>Sauté onions and garlic.</li>
    <li>Deglaze using the tomatoes.</li>
    <li>Add corn and beans.</li>
    …
</ol>
<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<ol>
    <li>Cook beans for 45 minutes.</li>
    <li>Cut vegetables in small cubes.</li>
    <li>Sauté onions and garlic.</li>
    <li>Deglaze using the tomatoes.</li>
    <li>Add corn and beans.</li>
    …
</ol>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

### Nested lists

Every list can be nested into another list. In the following example, the order of preparation is not important, but the preparation itself should be done before using the ingredients. The information is still easy to digest, assistive technology can easily inform users about the number of steps.

{::nomarkdown}
<%=sample_start%>

<ol>
    <li>
        Prepare ingredients
        <ul>
            <li>Cook beans for 45 minutes.</li>
            <li>Cut vegetables in small cubes.</li>
        </ul>
    </li>
    <li>Sauté onions and garlic.</li>
    <li>Deglaze using the tomatoes.</li>
    <li>Add corn and beans.</li>
    …
</ol>

<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<ol>
    <li>
        Prepare ingredients
        <ul>
            <li>Cook beans for 45 minutes.</li>
            <li>Cut vegetables in small cubes.</li>
        </ul>
    </li>
    <li>Sauté onions and garlic.</li>
    <li>Deglaze using the tomatoes.</li>
    <li>Add corn and beans.</li>
    …
</ol>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

### Description lists
{:.newex}

A description list consists of one or more term and description groupings. Each grouping associates one or more terms (the contents of `<dt>` elements) with one or more descriptions (the contents of `<dd>` elements).

A grouping begins either on the first item of the list or whenever a `<dt>` element follows an `<dd>` element.

#### One term, multiple descriptions
{:.ex}

In the following example, John and Luke are described as authors and Frank is described as editor.

{::nomarkdown}
<%=sample_start%>
<dl>
  <dt>Authors</dt>
  <dd>John</dd>
  <dd>Luke</dd>
  <dt>Editor</dt>
  <dd>Frank</dd>
</dl>
<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<dl>
  <dt>Authors</dt>
  <dd>John</dd>
  <dd>Luke</dd>
  <dt>Editor</dt>
  <dd>Frank</dd>
</dl>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

#### Multiple terms, one description
{:.ex}

In the next example, two different spellings of a word are defined using description lists. In such cases, use the `dfn` element to mark up the defined term.

{::nomarkdown}
<%=sample_start%>
<dl>
   <dt lang="en-US"><dfn>color</dfn></dt>
   <dt lang="en-GB"><dfn>colour</dfn></dt>
   <dd>A sensation which (in humans) derives from the ability of the fine structure of the eye to distinguish three differently filtered analyses of a view.</dd>
</dl>
<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<dl>
   <dt lang="en-US"><dfn>color</dfn></dt>
   <dt lang="en-GB"><dfn>colour</dfn></dt>
   <dd>A sensation which (in humans) derives from the ability of the fine structure of the eye to distinguish three differently filtered analyses of a view.</dd>
</dl>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

#### Multiple terms, multiple descriptions
{:.ex}

In this example, John and Luke authors and also editors:

{::nomarkdown}
<%=sample_start%>
<dl>
  <dt>Authors</dt>
  <dt>Editors</dt>
  <dd>John</dd>
  <dd>Luke</dd>
</dl>
<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<dl>
  <dt>Authors</dt>
  <dt>Editors</dt>
  <dd>John</dd>
  <dd>Luke</dd>
</dl>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

## Quotes
{:.newex}

Identifying a quotation as such helps clarify that the content is attributed to another author. Quotes can be marked up as inline or as blocks of text.

### Blockquote
{:.ex}

Use the `<blockquote>` element for longer and more complex quotes. It can contain paragraphs, headings, and other text structure elements. Those should reflect the structure of the cited document. The `<cite>` element is used to refer to the source of the quote.

{::nomarkdown}
<%=sample_start%>

<p>The following is an excerpt from the <cite>The Story of my Life</cite> by Helen Keller</p>
<blockquote>
    <p>Even in the days before my teacher came, I used to feel along the square stiff boxwood hedges, and, guided by the sense of smell, would find the first violets and lilies. There, too, after a fit of temper, I went to find comfort and to hide my hot face  in the cool leaves and grass.</p>
</blockquote>

<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<p>The following is an excerpt from the <cite>The Story of my Life</cite> by Helen Keller</p>
<blockquote>
    <p>Even in the days before my teacher came, I used to feel along the square stiff boxwood hedges, and, guided by the sense of smell, would find the first violets and lilies. There, too, after a fit of temper, I went to find comfort and to hide my hot face  in the cool leaves and grass.</p>
</blockquote>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

### Inline quote
{:.ex}

For shorter quotes, that are usually embedded in another sentence, use the `<q>` element.

{::nomarkdown}
<%=sample_start%>

<p>Helen Keller said, <q>Self-pity is our worst enemy and if we yield to it, we can never do anything good in the world.</q></p>

<%=sample_end%>
{:/nomarkdown}

{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<p>Helen Keller said, <q>Self-pity is our worst enemy and if we yield to it, we can never do anything good in the world.</q></p>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

## Figures

Figures are blocks with additional information to the main content of the page – sometimes referenced from the main text. They typically contain  lists, images, tables, but can also contain other content. For example an annual report could reference to a diagram containing the sales volumes of a product.

Each figure is wrapped in a `<figure>` element and labeled using a nested `<figcaption>` element.


{::nomarkdown}
<%=code_start%>
{:/nomarkdown}

~~~html
<p>The sales volume of our SpaceBear product was steadily the first three quarters but had a huge success in quarter four with the introduction of SuperBear in time for the holiday season. See graphic G3 for details.</p>

<figure role="group" aria-labelledby="fig-t3-capt">
    <figcaption id="fig-t3-capt">G3: SpaceBear sales volume</figcaption>
    <img src="…"
         alt="SpaceBear sales diagram, showing the huge success in Q4"
         longdesc="…">
    <a href="…">Long Description</a>
</figure>
~~~

{::nomarkdown}
<%=code_end%>
{:/nomarkdown}

{::nomarkdown}
<%=notes_start%>
{:/nomarkdown}

* **Note:** At the time of writing, WAI-ARIA attributes `role="group"` and `aria-labelledby` are used to provide the information to assistive technologies in a consistent way.

* **Note:** For more information on how to mark up diagrams, see [complex images](/images/complex.html).

{::nomarkdown}
<%=notes_end%>
{:/nomarkdown}


## Images and illustrations

Images and illustrations are useful to create visual engagement for many users. They may also clarify text for people with reading disabilities. Where images or illustrations are used, proper alternative texts need to be added. See the [Images Tutorial](/images/index.html) for guidance on alternative texts.

## Tables

Data tables provide a useful way to display the data so that the structure of the table can be communicated to everyone. Proper table layout allows people to understand meaningful data relationships without seeing the grid. For more details, see the [Tables Tutorial](/tables/index.html).
