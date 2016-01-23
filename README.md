## Whats in this library?

A pair of fold-like datatypes that consume
[Producers](http://hackage.haskell.org/package/pipes-4.1.7/docs/Pipes.html#t:Producer)
from [pipes](http://hackage.haskell.org/package/pipes) and can be constructed
in a variety of ways, in particular from the more versatile folds in Gabriel
Gonzalez's [foldl](http://hackage.haskell.org/package/foldl) package.

The **Fold1** consumes a single **Producer**, while the **Fold2** datatype
consumes two **Producer**s concurrently.

## Why was this library created?

I wanted a fold-like datatype for IO-based Producers that let me perform
"bracketing" operations (the folds in foldl are push-based and do not allow
that). 

I also wanted to be able to fold two Producers concurrently (for example, take
the piped stdout & stderr streams of an external process and merge the lines
into a single file as they are produced).

Finally, I wanted the fold-like datatype to have a "failure value" baked in.

If you don't need any of that, you are better off using **pipes** and/or
**foldl** by themselves. 

## Where can I find working examples for this library?

There are none yet.
