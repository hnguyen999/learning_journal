---
layout: post
title: Three things I learned from The Ruby Koans
---

Here are (at least) three things I learned from [The Ruby Koans](http://rubykoans.com/):

In class on 4/8/21, I learned that you can commit to GitHub directly by navigating to the folders in my repository and commit below. 

1) I can do the same in Gitpod's terminal and the command is always git add -A; git commit -m. 

If I make commits in Gitpod, I will also need to push them to GitHub:
git add -A; git commit -m
git push

2) shovel operator modifies original string (Ruby methods generally do not modify the original string)

def test_the_shovel_operator_modifies_the_original_string
    original_string = "Hello, "
    hi = original_string
    there = "World"
    hi << there
    assert_equal  "Hello, World", original_string

    # THINK ABOUT IT:
    #
    # Ruby programmers tend to favor the shovel operator (<<) over the
    # plus equals operator (+=) when building up strings.  Why?
  end

Usually methods that end in “!” mean that the method will modify the object that the method was called on
So a = "hello"
a.reverse = "olleh"
a remains "hello"

Unless: a.reverse!
then now it sticks! 

