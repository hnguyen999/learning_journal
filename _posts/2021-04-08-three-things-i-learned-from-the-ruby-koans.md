---
layout: post
title: Three things I learned from The Ruby Koans
---

Here are (at least) three things I learned from [The Ruby Koans](http://rubykoans.com/):

In class on 4/8/21, I learned that you can commit to GitHub directly by navigating to the folders in my repository and commit below. 

1) I can do the same in Gitpod's terminal and the command is always git add -A; git commit -m. 

If I make commits in Gitpod, I will also need to push them to GitHub:
git add -A
git commit -m
git push

git b- name-of-branch
git checkout main
git checkout name-of-branch (to swap to that 1 branch)

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


3) map method CHANGES the varilable whereas each method only does the function within the block varilable and doesn't change the original variable
https://www.rubyguides.com/2018/10/ruby-map-method/

4) House-keeping:
html limitation: can post or get but cannot "delete" in an edit form. So rails made up for HTML's sucki-ness and we have data-method = "delete". This works for "patch" as well.

SECRUITY CSRF:
<input type="hidden" name="authenticity_token" value ="<%form_authenticity_token%>
https://gitpod.io/#snapshot/445c4fa3-279a-4334-a5c6-f5170c26a2da
                                                       
5) Short-hands:

x += y   # x = x + y
x /= y   # x = x / y
x ||= y  # x = x || y (but see disclaimer for OR below)


Both or and || evaluate to true if either operand is true. They evaluate their second operand only if the first is false.
As with and, the only difference between or and || is their precedence.
Just to make life interesting, and and or have the same precedence, while && has a higher precedence than ||.


