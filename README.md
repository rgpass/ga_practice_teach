# Hashes

**Objective:** Identify what a hash is and why you would use it instead of an array.

* Discussion: What is a hash?
* Discussion: Why use a hash vs array?
* Demo: How to create a hash
* Demo: Access items in a hash (vs an array)

## Quick Review
:symbol vs "String"

* Symbols are immutable
* Symbols are faster
* Symbols are references -- each symbol has one value


## What We'll Cover

### What is a hash?
In programming terms, a hash is a collection of unique keys and values.

### Why use a hash vs array?
I like to use simple terms rather than programming talk. You guys learned about arrays earlier. A grocery list is a good example of an array.

```
list = ["Avocados", "Tomatoes", "Red onion", "Jalapenos", "Chips"]
```

However, real-world objects (and programming objects) aren't best described with lists like this. For instance, you wouldn't describe me like this:

```
gerry = ["brown", 2, "brown", "weird"]
```

Remember, Ruby is made to be an easy-to-read language, it's designed with the developer in mind.

```
gerrys_looks = gerry[3]  # Huh? Oh... ouch. :(
```

Let's try this again.

```
gerry = { :hair_color => "brown", :eye_count => 2, eye_color: "brown", looks: "weird" }

gerrys_looks = gerry[:looks]
```

Alright, so back to programming speak. The keys are:

```
gerry.keys # => [:hair_color, :eye_count, :eye_color, :looks]
```

and the values are:

```
gerry.values # => ["brown", 2, "brown", "weird"]
```

These make up key-value pairs. An example of one key-value pair is:

```
hair_color: "brown"
```


### How to create a hash
There are two ways to make a hash:

```
first_way = {}
second_way = Hash.new
```

Both allow you to add traits in new lines.

```
first_way[:best_movie_ever] = "Top Gun"
second_way[:best_comedy] = "Anchorman"
```

However, typically you use a less-verbose version of ```first_way``` to create a hash.

```
best_way = { best_movie_ever: "Top Gun", best_comedy: "Anchorman" }
```


### Access items in a hash (vs an array)
* Wait, what if my keys aren't unique?