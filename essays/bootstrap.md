---
layout: essay
type: essay
title: "Bootstrap 5: Convenience vs. Customization"
date: 2025-10-08
published: false
labels:
  - UI Frameworks
  - HTML, Bootstrap 5
  - Technical Essay
---

<img width="300px" class="rounded" src="../img/bootstrap.png">

## Convenience and the Hidden Cost of UI Frameworks
One of the reasons why people like to use UI frameworks like Bootstrap is because it can be more convenient in some circumstances because it comes with pre-designed components like buttons, icons, and navigation bars like so: 

```
// with Bootstrap 5
<button id="decrease" class="btn btn-secondary me-2">Click Me!</button>

// without UI framework
   button {	// manually setting up the button
      margin: 5px;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      background-color: #007bff;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
    }
<button id="decrease">Decrease</button>
```

This makes it easier on our side because you don’t have to worry about manually styling them unless you want to make them custom or different from the defaults. Which is where one of the cons of UI frameworks come into play where, customizing preset things to a specific way that you want can become annoying because you’d have to know what Bootstrap class is doing what and then altering it correctly. Another cone of UI frameworks is that they can become very cluttered and hard to understand how to alter code at a first glance like so:

```
// With Bootstrap 5
 <div class="card text-center shadow p-4" style="width: 20rem;">    /* this looks confusing and hard to tell what p-4 does and 
                                                                    how to change it so that it does what you want it to (in this case changing the padding on all four sides) */

    <h1 class="mb-4">Counter: <span id="count">0</span></h1>
    <div>
      <button id="decrease" class="btn btn-secondary me-2">Decrease</button>
      <button id="increase" class="btn btn-primary">Increase</button>
    </div>
  </div>

// UI Without framework
    button {
      margin: 5px;
      padding: 10px 20px;	// here it’s clear how much padding there is and easy to change
      font-size: 16px;
      border: none;
      border-radius: 5px;
      background-color: #007bff;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
    }
 <div class="container">
    <h1>Counter: <span id="count">0</span></h1>
    <button id="decrease">Decrease</button>
    <button id="increase">Increase</button>
  </div>
```
So as you can tell if you have multiple people working on a single website or even just maintaining a website can get stressful when using UI frameworks. That is unless you have a really solid grasp of that specific framework in order to make a change without absolutely breaking the website.

Another con to working with UI frameworks is that since it gets more complicated to make specific customizations to your website you’re less likely to make those customizations to make the website your own. Therefore most Bootstrap websites have a tendency to look the same because of the use of default settings making your website look boring or repetitive.

## Final Thoughts
All in all if you don’t mind that the various websites you build using UI frameworks may look very similar and have a good understanding of the classes then I think Bootstrap can be very useful. However if you want to have an easier time customizing your content to make them different and struggle with understanding the different classes in Bootstrap then I wouldn’t recommend it for you. Personally I was the latter case and really struggled with using Bootstrap especially since I didn’t have a solid understanding of the classes and defaults and would end up trying to change something and it wouldn’t do what I wanted it to.
