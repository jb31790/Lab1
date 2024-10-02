# Lab 1
**Author: JB**

**Date: 2024-10-02**

## Introduction
This is an explanation of my work with ***"Lab 1"***. For details surrounding the objective/goal with this lab, see the [readme-file](./README.md).

### Objective
In short, the objective of this lab was to create a website with html and css, meeting a variety of criteria.

## Approach
My initial approach to this lab was to read through the requirements to pass the lab, and then write up a plan of how I'd create my website. After writing my plan, which can be found in the [readme-file](./README.md), I created a todo-list out of this plan, so that I would have something that I could actually act upon.

## Template
When creating websites I usually try to start of by making a base html "template" of my website. This template includes just about everything outside of the `<main>` section. So I make a sensible header, navbar, footer, etc. One thing thats important to note however is that I start of by making it purely in html, so no css. This is done to make sure that the website is somewhat sensible without css. This is required for lots or reasons, SEO (Search Engine Optimization), accessability support, and support for alternative browsers (w3m, lynx, etc.) just to name a few.

After I've created this html-template I start styling this with css.

## Smart CSS

There are a few things I've learned when it comes to css that has helped me a lot:
- CSS-variables
- CSS "debug-mode"
- Use `em` as much as possible

I'll quickly go through these points, but feel free to skip them if you already know about/use them!

### CSS-variables
In CSS you can create variables to reuse frequently used values, such as colors, fonts, paddings/margins, etc.

My standard snippet that I always use looks like this:
```css
:root {
	--main-fg: #eee;
	--main-bg: #233;
	--main-accent: #B44833;
	--muted-gray: #666;
	--font-monospace: "Space Mono", monospace;

    /* More about this later */
	--debug-mode: 0;
	--debug-outline: calc(2px * var(--debug-mode)) solid red;
}
```

***Of course I change out the colors and font depending on my websites theme!***

### CSS "debug-mode"
As you can see in the example above, I always set some global css-variables, that I later reuse in this way:
```css
h1 {
    outline: var(--debug-outline)
    ...
}
```

I set this attribute on most of my elements, and when I later quickly want to see the actuall size of the elements I just flip the `--debug-mode` to `1`, and all of my elements get outlined in red. Yes, I know there are browser dev-tools and all that, but I thing flipping a single value is way quicker and easier.

### `em`
"em" is a very useful unit to use in css. Simply put, it represents the font size. If you use the em-unit everywhere it means that you can scale it simply by changing the font size. This makes it easier to make responsive pages, and it also makes sure that things are sized correctly if you zoom in in your browser.

## Creating Pages
When I've got an html "template", correctly styled with css, I can start adding in content.

*Aaaand, voila, a finished website!!*


# Challenges
I know this may sound a bit cocky, but I honestly haven't really stumbled upon any challenges with this assignment. I've created quite a few html/css webpages before and already solved most problems already. Sure, responsiveness is always a bit tricky to get working, but thats pretty easily solveable using the em-unit and scaling the font on different screen-sizes. I've gotta admit that making this page responsive was a bit tricky since I didn't exactly follow every best practice while making this site. I had to speedrun this thing, so I planned and made this website all in one sitting. This means that I made lots of small mistakes that I would've fixed if I had more time.


# Conclusion
To sum everything up I think I had a good plan and executed it quite well, concidering the limited time I gave myself. Yes, the style of the site is a bit wonky, I'm no good at design. Yes, the responsiveness of the site may be questionable, but it at least looks good on both my PCs monitor and on my phone. Is this the best, most wonderful website in the world? Absolutely not! But I've gotta say I'm actually quite proud of being able to go from having no plan, no code, not even a git-repo, to having hopefully met most of the requirements and achieving the objective in less than 7 hours of work (excl. breaks for lunch and dinner).
