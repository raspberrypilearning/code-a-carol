## Decomposition

In programming, decomposition is breaking down a problem into smaller parts and solving each part in order to solve the whole problem.

Let's look at the first part of the popular Christmas song _Twelve days of Christmas_:

```
On the first day of Christmas, my true love sent to me
A partridge in a pear tree.

On the second day of Christmas, my true love sent to me
Two turtledoves
And a partridge in a pear tree.

On the third day of Christmas, my true love sent to me
Three French hens,
Two turtledoves
And a partridge in a pear tree.

etc...
```

You have probably noticed that there is a lot of repetition in the song. The following chunks of music are repeated:

- **Introduction** — _On the first day of Christmas, my true love sent to me_
- **Verse** — The tune is the same for _Two turtledoves_ and _Three French hens_
- **Partridge** — _(And) a partridge in a pear tree_

Each of these smaller chunks of the song can be written as a **function**. Then that function can be called whenever we need that melody to play. We will begin by writing some code to play the introduction.
