# SFECSS
Short Functional Elements CSS

The CSS method consists of semantic and functional names and elements.
Notes, comments and logs are placed in the SCSS-file, and not in the mark-up.
By using shorthand names the markup is reduced.


##  Legal names

Legal markup elements are: 

* Div (class "div")
* Span(class "span")
* P (class "p")
* A (class "a")


Legal semantic names for primary elements are:
See W3 HTML5 Guide for their semantic use

* Article (class "article" or "artc")
* Aside (class "aside" or "asd")
* Details ("details" or "dtl")
* Figure ("figure" or "fgr")
* Footer (class "footer" or "ftr")
* Header (class "header" or "hrd")
* Main (class "main")
* Nav (class "nav")
* Section (class "section" or "sect")


Legal functional names for primary elements are:

* Area ("area" or "ar")
* Bin ("bin")
* Box ("box")
* Composition ("composition" or "compo")
* Deco ("deco" or "dc")
* Document ("document" or "docm")
* Hero ("hero" or "hro")
* Layout ("layout" or "layt")
* Page ("page" or "pg")
* Container ("container" or "con")
* Content ("content" or "cont")
* Root ("root")
* Scene ("scene" or "scn")
* Search ("search" or "srch")
* Sector ("sector" or "sct")
* View ("view" or "vw")
* Zone ("zone" or "zn")
* Wrapper ("wrapper" or "wrpr")




Legal names for sub elements are:

* Branch ("branch" or "brnc")
* Cast ("cast" or "cst")
* Component ("component" or "cmp")
* Division ("division" or "divs")
* Element ("element" or "elm")
* Form ("form" or "frm")
* Group ("group" or "grp")
* Item ("item" or "itm")
* List ("list" or "lt")
* Loop ("loop" or "lp")
* Part ("part" or "prt")
* Segment ("segment" or "sgmt")
* Subarea ("subarea" or "subar")
* Subdivision ("subdivision" or "subd")
* Subheader ("subheader" or "subhrd")
* Subitem ("subitem" or "subit")
* Subsegment ("subsegment" or "subsg")
* Subcomponent ("subcomponent" or "subcomp")
* Subsector ("subsector" or "subsct")
* Summary ("summary" or "smry")



Legal names for utility classes are:

* tl (text-alignment left)
* fl (float left)
* upc (uppercase)
* ht (header type)
* ft (font-type)
* color (or "clr")
* link-color(or "lclr")
* anim (css animation class)



## Usage

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

Some elements are sub elements and they are named as such.
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

In the SCSS, we document the usage of the content component, this way the documentation and logics are removed from the mark-up.

```
/**
* Content container used on
* frontpage
* productlist
* recommended products in basket
**/
.container-1 {
.segment-1 {
}
.segment-2 {
}
}
```

We know the "segment" is a sub element, so there must be a legal name for the head element

```
<div class="container-1">
<p class="segment-1">text</p>
</div>
```

Or just enclose the whole css area, without numbering the sub elements. We can always find way to the primary element, since there are many sub element names.

```
/**
* Content container used on
* frontpage
* productlist
* recommended products in basket
**/
.main-2 {
.segment {
}
.detail {
}
}
}
```

Advanced setup
```
<div class="container-1">
<div class="segment">
<div class="subsegment-1"></div>
<div class="subsegment-2">
<span class="subitem"></span>
</div>
</div>
</div>
```

Advanced setup shortened
```
<div class="cont-1">
<div class="subhrd ht-1 fl">This is a title</div>
<div class="sgmt">
<div class="subsct-1 ft-1">Also a title</div>
<div class="subsct-2">
<span class="subit ft-2">Description</span>
</div>
</div>
</div>
```

