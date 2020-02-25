# [Nothing is Something](https://www.youtube.com/watch?v=OMPfEXIlTVE) [00:35:52] by **Sandi Metz** (2015)

## What does it teaches ?
She explore one possibility to avoid IFs statements and get a more flexible software.
Explains how to apply strategy pattern to combine behaviour.  
In the example she combines different formatting strategies with different sorting algorithms.

She also shows the limitations of using inheritance to provide combinations of behaviours.  

She explores a technique to realize what varies.
She compares the different branches of the conditional and realizes that one does not sort and the otherone does sort.
She decides to interpret the NoSort as a special type of sorting strategy. (Nothing is something)
After that she decided to build 2 sort strategies (DefaultOrder and RandomOrder)
DefaultOrder doesn't do anything.

### Technique Recipie
* Compare conditional's branches
* Identify what is different
* Give it a name
* For each branch
* Extract the identified behaviour into a strategy

The result is flexible(configurable) software.
You can compose MainBehaviour --> (RandomOrder + HtmlFormat) or (DefaultOrder + JsonFormat) by instantiating and linking objects.



