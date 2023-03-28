---
title: "Plotting beautiful spirographs with `matplotlib` and `spyrograph`"
date: 2023-03-27 10:51:00 -0500
categories: Python, tutorial
header:
  overlay_image: /images/rgb.gif
---

## Introduction
In this blog post, we'll be exploring the `plot` method of the `Hypotrochoid` class in the `spyrograph` library

This method allows users to create **beautiful visualizations** of **hypotrochoids** and **epitrochoids** using the popular `matplotlib` library

We will walk through the process of creating a **hypotrochoid** and then using the `plot` method to visualize it

## Prerequisite imports

Before we dive into **creating and plotting** a hypotrochoid, let's make sure we have `spyrograph` installed

{% highlight bash %}
pip3 install spyrograph matplotlib
{% endhighlight %}

## Creating a Hypotrochoid
To create a hypotrochoid, we need to **specify the parameters** `R` (**radius** of the fixed circle), `r` (**radius** of the rolling circle), `d` (**distance** from the rolling circle), and `thetas` (a list of **theta values**)

Here's an example of creating a hypotrochoid:

{% highlight python %}
from spyrograph import Hypotrochoid

R = 10
r = 6
d = 5
thetas = np.arange(0, 2 * np.pi, 0.01)

hypotrochoid = Hypotrochoid(R, r, d, thetas)
{% endhighlight %}

## Plotting the `Hypotrochoid` with the `plot` method

Now that we have our **hypotrochoid**, we can use the `plot` method to **visualize** it

This method will return a `matplotlib` **figure and axis** objects, which we can further customize if desired

{% highlight python %}
fig, ax = hypotrochoid.plot(
    color="blue",
    linewidth=1
)
plt.show()
{% endhighlight %}

In this example, we've specified the **color** of the hypotrochoid to be blue and the **line width** to be 1

You can **customize the appearance** of the plot by passing additional keyword arguments that are accepted by the `matplotlib.pyplot.plot` function

## Conclusion

The `plot` method in the `spyrograph` library makes it *incredibly* easy to create visually appealing plots of hypotrochoids and epitrochoids

With just a **few lines of code**, we can create stunning spirograph patterns that can be used for **artistic, educational, or scientific purposes**

Start **experimenting** with different parameter values and see what amazing designs you can create!
