## Decomposition

In programming, decomposition means breaking down a problem into smaller parts and solving each part in order to solve the whole problem.

Let's look at the beginning of the popular Christmas carol _Twelve Days of Christmas_:

```
On the first day of Christmas, my true love sent to me
A partridge in a pear tree.

On the second day of Christmas, my true love sent to me
Two turtledoves
And a partridge in a pear tree.

On the third day of Christmas, my true love sent to me
Three French hens,
Two turtledoves,
And a partridge in a pear tree.

etc...
```

You have probably noticed that there is a lot of repetition in the song. The following chunks of music are repeated:

- **Introduction** — _"On the first day of Christmas, my true love sent to me"_
- **Verse** — The tune is the same for _"Two turtledoves"_ and _"Three French hens"_
- **Partridge** — _"(And) a partridge in a pear tree"_

Each of these smaller chunks of the song can be written as a **function**. Then that function can be called whenever we need that melody to play. We will begin by writing some code to play the introduction.
