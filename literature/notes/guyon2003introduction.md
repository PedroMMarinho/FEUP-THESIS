# An Introduction to Variable and Feature Selection

- **Citekey:** `guyon2003introduction`
- **Authors:** Guyon, Isabelle; Elisseeff, André
- **Year:** 2003
- **Venue:** Journal of Machine Learning Research, 3, 1157-1182 (journal)
- **DOI:** no DOI — [https://www.jmlr.org/papers/v3/guyon03a.html](https://www.jmlr.org/papers/v3/guyon03a.html)
- **PDF:** `literature/papers/01-surveys-background/2003_Guyon_Intro-Variable-FS.pdf`
- **Theme:** `01-surveys-background`
- **Open access:** yes (gold, JMLR free access)
- **Read status:** read

> Fields below mirror the analysis columns in `literature/matrix.csv`.
> Keep both in sync when you finish reading.

## Task type

How can we do selection of features, what already exists and the various methods that were explored along the way.

## What exists

Methods we can use for feature selection: 
- Use filters, which basically are used to rank features using statistical criteria (good for a fast approach to see what variables can actually work), problems are that we cannot easily correlate features with one another to see if they work or not only by ranking them. Features that appear useless by themselves can be good joined with another. Features that also seem redundant might also improve the target capabilities instead of overfitting. Variables are trully redundant when they are perfectly correlated.
  
- Use wrappers, which basically is the usage of one or more subsets of features given their usefullness corresponding to a given predictor. Can be computationaly heavy depending on the strategies used to train and test the data. Two examples of doing wrapper type strategies, foward selection or backward elimination. Foward selection, basically uses subsets of variables expanding more and more over the following iterations. Backward elimination, starts to use all features at once and then starts by eliminating the least promising. 
For my thesis the wrapper search type used is GA, genetic algorithms. 

These wrappers are then "expanded" to embedded methods, this means that they select features during the training phase, losing the need to retrain the model every time. One example of an embedded method is by using a two-part objective funtion. 

Filters can be used with embedded methods, by using them at the subset creation/selection part.

- Feature Construction, can be good to reconstruct data that is not that good in terms of features, having the objective of reducing dimensionality while also improving performance.

## Relevance to my thesis

Good for contextualization of methods used for feature selection.
