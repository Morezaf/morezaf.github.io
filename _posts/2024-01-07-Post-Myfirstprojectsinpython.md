---
layout: posts
title: Python Projects
---

## A short summary of my first projects in Python

Python is one of the most popular programming languages ​​today.

Since our programming learning was also accompanied by Python learning, we used various tools, including the Turtle library, in presenting the projects.

One of the ideas in the Turtle library to make beautiful designs is to use reversible functions.
These types of functions can be used to create famous fractals such as the triangular fractal.

But more interestingly, we used recursive functions to create designs derived from nature.
For example, these functions can be used to execute the sequential designs of the branches of a tree. In the same way, we decided to create first a tree and then a forest in addition to fractals.

Our projects were as follows:
- Triangle fractal
- Stellar fractal
- Tree
- Jungle

To design the tree, in addition to the trunk and branches, which were implemented with recursive functions, we needed other items such as leaves, flowers and blossoms, ground, etc., and we reached acceptable designs by using different geometric shapes.

In the code I put below, you can see how the reversible function works in the tree function, as well as other things:

I did the following to make the ground, flowers and leaves:
    
    import turtle
    def ground(a,s):
        turtle.fillcolor(s)
        turtle.begin_fill()
        for _ in range(4):
            turtle.right(90)
            turtle.forward(a)
        turtle.end_fill()

    def leaf(x,b,t,c):
        turtle.fillcolor(c)
        turtle.begin_fill()
        turtle.left(t)
        turtle.forward(x)
        turtle.right(b)
        turtle.forward(x)
        turtle.right(180-b)
        turtle.forward(x)
        turtle.right(b)
        turtle.forward(x)
        turtle.end_fill()
    
    def blossom(m,l):
        turtle.fillcolor("pink")
        turtle.begin_fill()
        for _ in range(m):
            turtle.forward(l)
            turtle.right(360/m)
        turtle.end_fill()

and finally, using recursive functions in the tree:
    
    def tree(d,r,k,m,l,x,b,t,c):
        if d < 10 or r < 10:
            return
        turtle.pencolor("brown4")
        turtle.pensize(k)
        turtle.forward(d)
        turtle.left(r)
        tree(d*0.7,r,k*0.6,m,l,x,b,t,c)
        turtle.right(2*r)
        tree(d*0.7,r,k*0.6,m,l,x,b,t,c)
        turtle.left(r)
        turtle.backward(d)
        if 10< d <13:
            leaf(x,b,t,"chartreuse4")
        if 10< d <13:
            leaf(x,b,t,c)
        if 10< d <13:
            blossom(m,l)

    turtle.hideturtle()
    turtle.tracer(0)
    turtle.Screen().bgcolor("darkslategray1")
    turtle.penup()
    turtle.setpos(0,-250)
    turtle.left(90)
    turtle.pendown()
    tree(150,30,20,20,2.2,22,30,30,"dark green")
    turtle.penup()
    turtle.setpos(1000,-250)
    turtle.right(90)
    turtle.pendown()
    ground(2000,"darkgreen")
    turtle.mainloop()

and our final output was like this:

![alt text](../assets/images/tree.jpg "my first project in python. hope you like it : )")

Next, according to what we learned and the abilities we found, we improved our designs and started to build a collection of trees in the form of a small forest.

But this time, using our creativity, we created trees that are more asymmetric than before and more natural:

![alt text](../assets/images/jungle.jpg "my second project in python.")