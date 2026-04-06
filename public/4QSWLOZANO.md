# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="Imanuel C. Crisostomo, Nikolai G. Salvador" />
  <meta name="revised" content="<date today>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5; position: fixed; bottom: 0; width: 100%;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px; position: relative; top: 20px; left: 20px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px; position: absolute; top: 66px; left: 200px;
      z-index: 1;
    }
    .notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
    }
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
  <div class="notice">Notice!</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

 When the sidebar's positioning was changed to relative, the distance between the sidebar and the top left, right, or bottom of its current position becomes equal.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

Unlike relative positioning, a fixed positioning makes the footer follow the screen when you scroll up and down on the page.This is because fixed positioning makes it *fixed* no matter whether you scroll up or down on the page, differing from the relative positioning.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

Absolute positioning changes the distance of the main content from the center, by the same amount of pixels that you apply in each direction, either top, right, left, or bottom. Compared to fixed, which is dependent on the screen, setting it to absolute positioning keeps it in its place relative to the center of the page, rather than the user's screen.

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?

The notice appears above the main content, because it has a greater z-index, which means it becomes the upper layer that overlaps with the main content. If you swap the z-index values then the main content is the one that overlaps the notice because of the higher z index.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    * What do you observe on about the effect of z-index on .notice and .content boxes?

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    Static - Relative to nothing, base positioning of an element.
    Relative - It moves from the current position away from the four directions, equal to the amount of pixels set.
    Absolute - It moves from the center towards each of the cardinal directions, equal to the amount of pixels set.
    Fixed - Depends on the user's screen.

    b. How does absolute positioning depend on its parent element?

    Depends on the parent element as it turns into the center.

    c. How do you differentiate sticky from fixed (you can research on sticky)?

    Sticky is the combination of fixed and relative, stays set in its position to the cardinal directions until the user scrolls past a certain point, which makes it stick to one position on the user's screen.

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.

    I would make sure that things like notices or notifications have a higher z-index and are sticky. I would keep my headers and footers fixed.

    I would make sure that things like notices/notifications are of higher z-index and are sticky, which keeps headers, footers, etc. fixed and organized.