# Introduction

It's difficult to even touch the surface of D3 in an hour's worth of time, and even more difficult with the introduction of HTML, CSS, and SVG (which I assume some of you are familiar or even fluent in, and others not so much). With all that in mind, I've designed this brown-bag with one goal in mind: to provide everyone here with a high-level familiarity of d3's capabilities.

I have not designed this for you to follow along. Rather, I've hosted this tutorial online so that you can go back to it and work through the examples if you so desire. Or move beyond and create your own first d3 visualization. Either way, your choice.

# Overview

So, let's start with a question, What is (and what isn't) D3.js? Data-Driven Documents, or D3 for short, is a Javascript library for creating data visualizations in the browser.

* It IS a declarative framework (meaning, we're telling D3 what to accomplish and letting it figure out how to accomplish it) for binding arbitrary data to a Document Object Model (DOM). Here's a what the DOM looks like: when the browser displays an HTML page, it creates an interactive object graph from the tag hierarchy.

* It is built atop of web standards such as HTML, CSS, and SVG. D3 eschews custom, propriety graphical marks and instead piggybacks off of what is already there and provides a way of interacting with these widely implemented web standards. D3's here for the long haul.

* And finally, D3 IS NOT a charting library. Sure, it can be used to produce bar charts and scatterplots, but its goal is not to deliver a readymade way of producing these kinds of visualizations.

What this means is simple: as we gain expressibility, we lose efficiency. On this scale, we see visualization tools such as Tableau and Excel on the left: they provide molds for us to fit data into and this affords us efficiency. On the other hand, D3 would be plotted on the right-hand side with its predecessor, Protovis, and the ever expressive Processing language. I should state here that this chart maps well to the various use cases of these tools and languages. Business analysts are more likely to use Tableau because of its efficiency, whereas data storytellers (for example, the New York Times) are more likely to employ d3 for its expressibility.

# Data Joins

Person:Chair::Data:DOM element analogy

the update pattern is the epitome of d3 as a declarative framework: tell it what you want.


* ` svg.selectAll(‘circle’) ` returns a new empty selection.
* this selection is joined to an array of data, resulting in 3 new selections that represent the three possible states: enter, update, and exit.
  In this case, since the selection was empty, the update and exit selections are empty, while the enter selection contains a placeholder for each new datum.
