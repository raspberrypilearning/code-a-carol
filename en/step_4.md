## Code the introduction

The introduction is the melody associated with the words _"On the third day of Christmas, my true love sent to me"_.

<div id="audio-preview" class="pdf-hidden">

<audio controls preload>
  <source src="resources/intro.mp3" type="audio/mpeg">
Your browser does not support the <code>audio</code> element.
</audio>

</div>

Let's create a function to play this music in Sonic Pi.

+ Open up Sonic Pi and choose an empty buffer to write your code in.

+ Define a function called `:intro` (which will be blank inside for the moment).

[[[generic-sonicpi-function]]]

+ Inside the function, create two lists. One should be called notes and one should be called durations. You will use these lists to store the notes from the introduction.

```ruby
notes = []
durations = []
```

Here is the music, but don't worry if you can't read music as we have labelled each note too. "C4" means the note "C" in octave 4, which is how Sonic Pi refers to notes.

![Introduction](images/introduction.png)

+ Look at the music notes above. Add each of the note names to the notes list, separated by a comma. The first two notes are C4 so in Sonic Pi we would write this as ":c4".

```ruby
notes = [:c4, :c4]
```

You might have noticed that one of the notes is called B♭4 (B flat). You can make this note in Sonic Pi as ":bb4".

+ Next, add the durations of each note to the `durations` list.

| Note  | Duration |
+ ----- + -------- +
|![Crotchet](images/crotchet.png) | 1 |
|![Quaver](images/quaver.png) | 0.5 |
