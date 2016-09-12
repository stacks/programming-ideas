# Stacks project programming ideas

Some ideas regarding programming for the Stacks project. In no particular order.

## Responsive layout
Even though the Stacks project needs to display a lot of information, it should be possible to have at least a somewhat functional mobile website. Preferably this is achieved using a responsive layout, as much as possible using pure CSS. How do other information-heavy websites tackle this?

## MathJax preprocessing
Using [mathjax/MathJax-node](https://github.com/mathjax/MathJax-node) it is possible to render LaTeX to SVG or MathML on the server, and send this to the browser. Unfortunately it is the HTML-CSS output that looks best, and which we are using right now. So maybe this is not a good option?

## Local version of the Stacks project and improved deployment script
Right now, it takes about 15 steps to set up the Stacks project on your own computer. It is convenient to have a local version of the Stacks project when you are on the go, so this should be easier. Also, some of the scripts are now taken from a CDN, which of course doesn't work when offline.

## Twitter bots
Just for fun we could have a Twitter bot for a "slogan of the day" and "tag of the day". 

## Website code optimisations
First we should benchmark some heavy pages, and see whether there are any bottlenecks. The code isn't written optimally, so maybe there are some fixes (without completely overhauling the system) that improve the processing speed.

## Stacks project comparison tables
In [stacks/stacks-table](https://github.com/stacks/stacks-table) I started a comparison table for properties in the Stacks project. We should finish this.

## Stacks project scatter graph
In [stacks/stacks-scatter](https://github.com/stacks/stacks-scatter) I started a scatter plot of the growth of the Stacks project. We should finish this, and optimise the code because right now it is _slow_ (but maybe there is no way around this).

## Speed up the graph generation script
If you have ever run this yourself, you'll know that it is slow. It does some non-trivial things, but maybe there is no reason for it to be this slow.

## ``Relative'' page counts
Instead of treating the Stacks project as a linear book, you could treat it as a book for each separate result. Then one would not say that the definition of an algebraic stack is on page 3000+, but probably much earlier. Of course, we have the number of tags in the statistics. The problem is also that for definitions there is no good dependency thingie.

## Improve the history functionality
The way this is set up is very weird, and it deserves an overhaul.

## Make updating the website independent of `make tags`
We should check whether it is possible to create a version of the update process that does not involve building all the pdf's. Right now that is the bottleneck in the update process (together with the graph generation). We could move building the pdf's to a cronjob, whilst ensuring near instanteneous updates for the text on the website. The page numbers would be off for at most 24 hours.

## Fix the bugs listed on the various project
See the title.

## Consider the ideas listed on the various project
Again, see the title. There are some that would fit on this list probably.

## Compatibility issues
Right now the code is written with PHP5 and Python 2(.7) in mind. We should check whether there are any incompatibilities with PHP7 and Python 3(.4+).
