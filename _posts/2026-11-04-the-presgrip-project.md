---
title: The Presgrip Project
layout: post
categories: photography projects
excerpt_separator: "<!-- more -->"

actions:
  - label: "VIEW REPO"
    icon: github
    url: "https://github.com/martbetz/The-Promura-Project"
  - label: "CONTRIBUTE"
    icon: email
    url: "mailto:martbetz@yopmail.com?subject=The%Promura%Project"
---

<style>

.presgrip-frame{
    position:relative;

    width:min(400px, calc(100vw - 32px));
    aspect-ratio:4/3;

    margin:20px auto 30px auto;

    background:#050505;

    border:8px solid #050505;
    box-sizing:border-box;

    overflow:hidden;
}

.presgrip-screen{
    position:absolute;
    inset:0;

    background:#4b0d0d;

    animation: presgrip-flicker .35s infinite;
}

/* Inner viewport to handle the wobble without moving the outer frame */
.presgrip-viewport {
    position: absolute;
    inset: -6px; /* Slightly oversized to hide edge jitter */
    overflow: hidden;
    animation: presgrip-weave 1.3s infinite;
}

.presgrip-screen::before{
    content:"";
    position:absolute;
    inset:0;

    background:
    linear-gradient(
        rgba(255,220,150,.04),
        rgba(255,220,150,.02)
    );

    mix-blend-mode:screen;
}

.presgrip-screen::after{
    content:"";
    position:absolute;
    inset:0;

    background:
    radial-gradient(
        ellipse at center,
        transparent 55%,
        rgba(0,0,0,.15) 75%,
        rgba(0,0,0,.45) 100%
    );

    pointer-events:none;
    z-index: 2; /* Keeps the vignette locked to the stable edges */
}

.presgrip-title{
    position:absolute;
    inset:0;

    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;

    text-align:center;

    color:#efe6c8;

    font-family:
        "Arial Narrow",
        "Helvetica Neue",
        Arial,
        sans-serif;

    text-transform:uppercase;

    filter:blur(.25px);
}

.presgrip-main{
    font-size:32px;
    font-weight:500;
    letter-spacing:.22em;
    line-height:1.15;

    text-shadow:
        0 0 1px rgba(255,255,220,.4);

    transform:rotate(-0.15deg);
}

.presgrip-grain{
    position:absolute;
    inset:-20px;

    opacity:.14;

    background-image:
    repeating-radial-gradient(
        circle,
        rgba(255,255,255,.15) 0,
        rgba(255,255,255,.15) .5px,
        transparent 1.5px,
        transparent 4px
    );

    animation:presgrip-grain .25s infinite;
}

@keyframes presgrip-weave{

    0%{
        transform:translate(0px,0px) rotate(0deg);
    }

    17%{
        transform:translate(-0.4px,0.3px) rotate(-0.03deg);
    }

    31%{
        transform:translate(0.2px,-0.5px) rotate(0.02deg);
    }

    52%{
        transform:translate(-0.3px,-0.1px) rotate(-0.02deg);
    }

    68%{
        transform:translate(0.5px,0.2px) rotate(0.03deg);
    }

    84%{
        transform:translate(-0.1px,0.4px) rotate(-0.01deg);
    }

    100%{
        transform:translate(0px,0px) rotate(0deg);
    }
}

@keyframes presgrip-flicker{

    0%   { filter:brightness(1.00); }
    10%  { filter:brightness(1.05); }
    15%  { filter:brightness(.97); }
    22%  { filter:brightness(1.03); }
    31%  { filter:brightness(.95); }
    46%  { filter:brightness(1.06); }
    58%  { filter:brightness(.98); }
    65%  { filter:brightness(1.04); }
    79%  { filter:brightness(.96); }
    89%  { filter:brightness(1.07); }
    100% { filter:brightness(1.00); }
}

@keyframes presgrip-grain{

    0%{
        transform:translate(0,0);
    }

    25%{
        transform:translate(3px,-2px);
    }

    50%{
        transform:translate(-2px,2px);
    }

    75%{
        transform:translate(2px,-1px);
    }

    100%{
        transform:translate(0,0);
    }
}

html,
body{
    overflow-x:hidden;
}

</style>

<div class="presgrip-frame">

    <div class="presgrip-screen">
        <div class="presgrip-viewport">
            <div class="presgrip-title">
                <div class="presgrip-main">THE</div>
                <div class="presgrip-main">PRESGRIP</div>
                <div class="presgrip-main">PROJECT</div>
            </div>

            <div class="presgrip-grain"></div>
        </div>
    </div>

</div>

<!-- more -->

<p>
   The objective of <b>The Presgrip Project</b> is to collate as much information as possible about the <b>Presgrip</b> range of cine title products. Please reference the project <a href="https://github.com/martbetz/The-Presgrip-Project/blob/main/FAQs.md">FAQs</a>.

---

<b>This project is an excersise in ongoing factual research and data collection; as such, the following information should only be considered as accurate as the latest evidence suggests. 

Where possible, links are provided to original sources; where original sources are no longer available (whether in full or in part), detailed summaries of the original sources remain sited.

This project is soley intended for reference and is a continual work-in-progress. Please raise an issue for any proposed corrections and a pull request for any proposed contributions.</b>

---

<h3><center>Supply & Manufacture</center></h3>

<p>
   <b>Presgrip Cine Title Sets</b> were manufactured and marketed, primarily during the 1950s and 1960s, by <b>Presgrip Sign Co</b> (🇬🇧 GBR). 
</p>

  <p>
   There were a total of nine different sets available. (<a href="https://d2x313g9lpht1q.cloudfront.net/original/3X/6/4/640e409d7310a4fc8579e0982e92274200045b88.png">1</a>) 
  </p>
   
<p>
Associated addresses for Presgrip Sign Co are <a href="https://streetscan.co.uk/postcode/so23-0ld">Winall Valley Road</a> and <a href="geo:51.0629327,-1.3081366?q=51.0629327,-1.3081366&z=17">55a Eastgate Street</a> in Hamphire, England. (<a href="https://d2x313g9lpht1q.cloudfront.net/original/3X/6/4/640e409d7310a4fc8579e0982e92274200045b88.png">2</a>) 
   
<p>
The company was associated with directors CE Tanner and TB Tanner, along with Kennet Price Markers Ltd as the ultimate proprietor. (<a href="https://archivescatalogue.hants.gov.uk/records/A24057?hl=en-GB">3</a>)
   </p>

<p>
Presgrip Sign Co was an exhibitor at the 1955 British Industries Fair (located at Stand F33). (<a href="https://www.gracesguide.co.uk/1955_British_Industries_Fair:_Company_P">4</a>)
​


<h3><center>Presgrip Cine Title Sets</center></h3>

<p>
During the boom of amateur filmmaking in the mid-20th century (the 1950s and 60s), the company adapted their core product&nbsp;— removable and reusable letters&nbsp;— to create the Presgrip Cini Title Sets for 8mm and 16mm cine film; these sets enabled amateur film-makers to easily create professional-looking titles and captions for home movies.

</p>
   
<p>
Presgrip offered several different versions of their Cine Title Sets, catering to various budgets and needs of the amateur filmmaker, the contents of which typically revolved around a core set of reusable components designed for easy filming. The main feature of any Presgrip set was the lettering system itself:

- ​letters and numbers: these were usually white plastic characters that came in large quantities (a full alphabet and often common punctuation marks) and were mounted on sheets or in a segmented tray for organization

- ​the board/screen: a title board or screen where the letters would be mounted which often featured a ribbed or slotted surface to keep the letters neatly aligned

- ​backgrounds: to add variety, sets often included different colored backgrounds (mainly red, blue, and green) that could be swapped out on the board; these allowed for contrasting colors to make the white letters pop on film

- ​"celluloid" filters: some of the more complete sets included a set of colored celluloid or plastic filters; these could be placed over the title to add color effects or tints to the title sequence when filmed

- ​instructions and layout guides: The original kits always came with an instruction manual and sometimes a layout-reference card to help the filmmaker center their titles correctly within the camera's frame (especially important for older 8mm and 16mm formats)
</p>

<center>

<p style="margin-top: 40px;">

<h3>Product Price List</h3>

</p>

<p style="margin-top: 20px;">

|DESCRIPTION|PRICE EACH|
|------|----|
|Outfit 'B' - standard complete set |£4 0s 0d (four pounds)|
|Outfit 'MAJOR' - larger, more comprehensive set |£5 12s 6d (five pounds, twelve shillings, and sixpence)|
|felt board - 15" x 12"| £1 10s 0d (one pound, ten shillings)|
|title easel - for holding the titling board |£1 15s 0d (one pound, fifteen shillings)|
|"100" set of extra white letters/figures |12s 6d (twelve shillings, sixpence)|
|"100" set of extra yellow letters/figures|15s 0d (fifteen shillings)|

</p>

<p style="margin-top: 40px;">

<h3>Spares Price List</h3>

<h4>Letters (Upper Case)</h4>

</p>

<p style="margin-top: -15px;">
   
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z ? ! ( ) &

</p>

<p style="margin-top: 20px;">

|SIZE|PRICE EACH|PRICE PER DOZEN|
|------|----|----|
|3/4"|3d (threepence)|2s 9d (two shillings, ninepence)|
|9/16"|3d (threepence)|2s 6d (two shillings, sixpence)|
|3/8"|2½d (two and halfpence)|2s 3d (two shillings, threepence)|
|script|3d (threepence)|2s 6d (two shillings, sixpence)|

</p>

<h4><center>Letters (Lower Case)</center></h4>

<p style="margin-top: -15px;">

a b c d e f g h i j k l m n o p q r s t u v w x y z ? !

</p>

<p style="margin-top: 20px;">

|SIZE|PRICE EACH|PRICE PER DOZEN|
|------|----|----|
|9/16"|3d (threepence)|2s 6d (two shillings, sixpence)|
|3/8"|2½d (two and halfpence)|2s 3d (two shillings, threepence)|
|script|3d (threepence)|2s 6d (two shillings, sixpence)|

</p>

<h4>Numerals</h4>

<p style="margin-top: -15px;">


1 2 3 4 5 6 7 8 9 £ / /- $

</p>

<p style="margin-top: 20px;">

|SIZE|PRICE EACH|PRICE PER DOZEN|
|------|----|----|
|1"|3½d (three and halfpence)|3s 6d (three shillings, sixpence)|
|12/16"|3d (threepence)|3s (three shillings)|
|9/16"|3d (threepence)|2s 6d (two shillings, sixpence)|
|3/8"|3½d (three and halfpence)|2s 3d (two shillings, threepence)|
|script (except £ / /- d $)|3d (threepence)|2s 6d (two shillings, sixpence)|

</p>



<h4>Titler</h4>

<p style="margin-top: 20px;">

|DESCRIPTION|PRICE EACH|
|------|----|
|raising and lowering attachment|£10 10s 0d (ten pounds, ten shillings)|
|lamp reflector|45s 0d (forty-five shillings)|
|animation table|17s 6d (seventeen shilings, sixpence)|
|13 7/8" x 13 7/8" perspex screen|17s 6d (seventeen shilings, sixpence)|
|13 7/8" x 12" perspex screen|15s 0d (fifteen shillings)|

</p>

<h4>Misc</h4>

<p style="margin-top: 20px;">

|DESCRIPTION|PRICE EACH|
|------|----|
|12" x 9" transparent screen|6s 0d (six shillings shillings)|
|centering rule|2s 3d (two shillings, theepence)|
|12" x 9" background letherette sheet (red, blue, green, black)|9d (ninepence)|
|12" x 9" layout card| 9d (ninepence)|
|12" x 9" script layout card| 9d (ninepence)|
|cardboard box with one plastic tray|6s 6d (six shillings, sixpence|
|wooden box with two plastic trays|40s 0d (forty shillings)|
|wooden box with one plastic tray|35s 0d (35 shillings)|

</center>

</p>
