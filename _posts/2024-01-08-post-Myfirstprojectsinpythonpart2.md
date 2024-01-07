---
layout: posts
title: Python Projects Part II
---

## A short summary of my first projects in Python

Fractals are another well-known type of recursive application that is more general.

In this type, we have a series of repeated shapes from small to large that grow in a certain proportion and create a beautiful design.

In the following, we will see the code and image of two examples of these fractals.

* [for more information](https://towardsdatascience.com/creating-fractals-in-python-a502e5fc2094)

Triangle fractal:

    import turtle

    def triangle(d):
        if d < 10:
            return
        for _ in range(3):
            triangle(d/2)
            turtle.forward(d)
            turtle.left(120)

    turtle.hideturtle()
    turtle.penup()
    turtle.backward(200)
    turtle.right(90)
    turtle.forward(100)
    turtle.left(90)
    turtle.pendown()
    turtle.Screen().bgcolor("aquamarine2")
    turtle.pencolor("darkslategray")
    turtle.tracer(0)
    triangle(400)
    turtle.mainloop()

![alt text](../assets/images/Screenshot%20(17).png "Triangle fractal")

Stellar fractal:

    import turtle

    def star(n,d):
        if d < 5:
            return
        for _ in range(n):
            turtle.forward(d)
            star(n , d/3)
            turtle.right(180 - 180/n)
        
    turtle.penup()
    turtle.setpos(-150,30)
    turtle.pendown()
    turtle.speed(0)
    turtle.Screen().bgcolor("black")
    turtle.pensize(3)
    turtle.pencolor("gold")
    star(5,300)
    turtle.mainloop()

![alt text](../assets/images/Screenshot%20(15).png "Stellar fractal")