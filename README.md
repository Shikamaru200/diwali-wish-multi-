# diwali-wish-multi-
Digital Diwali Wishes 🪔

An interactive Diwali greeting (from N to S). It is a single file, index.html, with no build step.

The 7 pages
Welcome
Light the diyas
Decorate your Diwali corner
Share some mithai
Light up the sky (fireworks)
A little wish (the letter)
Happy Diwali! (finale)
Where to change things

Open index.html and search for Personalise here (about line 207). You will find this block:

js
const C={
  to:"S", from:"N", date:"8 November 2026",
  letter:[
    "Dear {to},",
    "May this Diwali bring countless reasons to smile, ...",
    "May your home glow with love, ...",
    "Wishing you and your family a very Happy Diwali! 🪔"
  ]
};
What you want to change	What to edit
Receiver's name (shown on page 1 and in "Dear ...")	to:"S"
Sender's name (letter signature and finale)	from:"N"
Date shown on page 1 and the finale	date:"8 November 2026"
Letter text	The lines inside letter:[ ... ]. Keep {to} where the receiver's name should appear. Each line is one paragraph; you can add or remove lines.
Change the text on other pages

Search for the exact words in index.html and edit them. They are plain HTML text:

Page headings and sub-lines: inside the <section> blocks (for example Let’s Make This Diwali A Little More Special).
Button labels: for example Enter The Celebration, Share Some Mithai, Celebrate Again.
Sweet caption: the caps=[...] list in the script.
Finale line: May your life always shine brighter than a thousand diyas.
Send a different name without editing the file

Add details to the link. Nothing in the code needs to change:

https://<username>.github.io/<repo>/?to=S&from=N&date=8%20November%202026

Use %20 for spaces. Change to= to make a different person's greeting from the same page.

Colours and fonts

All colours are at the top of the <style> block:

--gold, --amber, --cream set the accents and text.
#s0, #s1 ... #s7 set the background of each page.
The fonts are Fraunces (headings), Nunito (body) and Caveat (handwriting). You can swap them in the Google Fonts <link> and in the --serif, --sans and --hand variables.
Remove or reorder a page

Each page is a <section class="s" id="sN">. If you delete one, also check the enter[N] and leave[N] lines near the bottom of the script, because they use page numbers starting from 0. For example, enter[5] is the letter page and enter[6] is the finale.

Host it on GitHub Pages
Create a new repository on GitHub (public).
Upload index.html (and this README) to the root of the repo.
Go to Settings → Pages.
Under Build and deployment, choose Deploy from a branch, then branch main and folder / (root), and click Save.
After a minute or two your site is live at https://<username>.github.io/<repo-name>/.

Edit index.html on GitHub (pencil icon), commit, and the site updates in a minute or two.

Notes
Fonts load from Google Fonts, so the first load needs an internet connection. A fallback font is used otherwise.
Sound effects are off by default. Visitors can turn them on on the fireworks page.
The page respects the device's "reduce motion" setting, and visitors can also toggle it on the fireworks page.
Fireworks are digital only. No real crackers. 🧨🚫
