# Netflix Landing Page 
Clone of the Netflix website as a light HTML CSS and JS : http://127.0.0.1:5500/index.html

## What it is

A basic warmup. Simple, practice oriented, clone of the Netflix Homepage. Built with:

HTML
CSS
Vanilla JS - ES6
Awesomeness font

## Learning Points
1.CSS GRID \
2.STYLING TABLES \
3.TABS WITH JAVASCRIPT \
4.POSITIONING 

## SOME NEW WAY
Usually, people tend to run to CSS Frameworks to develop and style tabs and switching tabs. But here's a pretty simple, basic way of creating switchable tab content using Vanilla JS:

```
const tabItems = document.querySelectorAll(".tab-item");
const tabContentItems = document.querySelectorAll(".tab-content-item");

// Select tab content
function selectItem(e) {
  removeBorder();
  removeShow();
  // Add border to current tab
  this.classList.add("tab-border");
  // Grab content item from DOM
  const tabContentItem = document.querySelector(`#${this.id}-content`);
  // Add show class
  tabContentItem.classList.add("show");
}
function removeBorder() {
  tabItems.forEach(item => item.classList.remove("tab-border"));
}
function removeShow() {
  tabContentItems.forEach(item => item.classList.remove("show"));
}
// Listen for tab click
tabItems.forEach(item => item.addEventListener("click", selectItem));
```
