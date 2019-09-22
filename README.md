# SFECSS
Short Functional Elements CSS

The CSS method consists of semantic and functional names and elements.
Notes, comments and logs are placed in the SCSS-file, and not in the mark-up.
By using shorthand names the markup is reduced.


Legal semantic names for elements are:

* Header (class "header" or "hrd")
* Footer (class "footer" or "ftr")
* Main (class "main")
* Nav (class "nav")
* Article (class "article" or "artc")
* Section (class "section" or "sect")
* Aside (class "aside" or "asd")


Legal markup elements are: 

* Div (class "div")
* Span(class "span")
* P (class "p")
* A (class "a")


Legal functional names for elements are:

* Area ("area" or "ar")
* Layout ("Layout" or "layt")
* Page ("page" or "pg")
* Deco ("deco" or "dc")
* Container ("container" or "con")
* Content ("content" or "cont")
* Component ("component" or "cmp")
* Element ("element" or "elm")
* Item ("item" or "itm")
* Group ("group" or "grp")Loop ("loop" or "lp")
* List ("list" or "lt")Form ("form" or "frm")
* Search ("search" or "srch")
* Sector ("sector" or "sct")
* Shorttext ("shorttext" or "shrtx")
* Text ("Text" or "txt")
* View ("View" or "vw")


Legal names for sub elements are:

* Subdivision ("subdivision" or "subd")
* Segment ("segment" or "sgmt")
* Item ("item" or "itm")
* Content ("content" or "cont")
* Container ("container" or "con")
* Division ("division" or "div")


Legal names for utility classes are:

* t-l (text-alignment left)
* f-l (float left)
* u-cl (uppercase)
* ht (header type)
* ft (font-type)
* color (or "clr")
* link-color(or "lclr")
* anim (css animation class)



##Usage

Before
```
<div class="frontpage__list_item">
<p class="frontpage_list_smalltext">text</p>
</div>
```

The div might change later to something else, be moved or could be reused for another purpose.
So the "frontpage__list_item" might suddenly be product list, category or something else.

We are not interested in position or sizes that might change later, so we rename by using SFECSS names.
Since the content is the first content block on the webpage, we name it "content-1".
The sub element can be name "segment-1" as it is the first sub segment in the "content-1"

```
<div class="content-1">
<p class="segment-1">text</p>
</div>
```

We can then reduce the markup by using SFECSS short names:

```
<div class="cont-1">
<p class="sgmt-1">text</p>
</div>
```
