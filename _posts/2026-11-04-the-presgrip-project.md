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
The objective of <strong>The Presgrip Project</strong> is to collate as much information as possible about the
<strong>Presgrip</strong> range of cine title products. Please reference the project
<a href="https://github.com/martbetz/The-Presgrip-Project/blob/main/FAQs.md">FAQs</a>.
</p>

<hr>

<div class="notice">
  <p>
This project is an exercise in ongoing factual research and data collection; as such, the following information should only be considered as accurate as the latest evidence suggests.<br><br>
  </p>
  <p>
Where possible, links are provided to original sources; where original sources are no longer available (whether in full or in part), detailed summaries of the original sources remain cited.<br><br>
  </p>
  <p>
This project is solely intended for reference and is a continual work-in-progress. Please raise an issue for any proposed corrections and a pull request for any proposed contributions.
</div>
</p>

<hr>

<h3>Supply &amp; Manufacture</h3>

<p>
<strong>Presgrip Cine Title Sets</strong> were manufactured and marketed, primarily during the 1950s and 1960s, by
<strong>Presgrip Sign Co</strong> (🇬🇧 GBR).
</p>

<p>
There were a total of nine different sets available.
(<a href="https://d2x313g9lpht1q.cloudfront.net/original/3X/6/4/640e409d7310a4fc8579e0982e92274200045b88.png">1</a>)
</p>

<p>
Associated addresses for Presgrip Sign Co are
<a href="https://streetscan.co.uk/postcode/so23-0ld">Winall Valley Road</a> and
<a href="geo:51.0629327,-1.3081366?q=51.0629327,-1.3081366&z=17">55a Eastgate Street</a>
in Hampshire, England.
(<a href="https://d2x313g9lpht1q.cloudfront.net/original/3X/6/4/640e409d7310a4fc8579e0982e92274200045b88.png">2</a>)
</p>

<p>
The company was associated with directors CE Tanner and TB Tanner, along with Kennet Price Markers Ltd as the ultimate proprietor.
(<a href="https://archivescatalogue.hants.gov.uk/records/A24057?hl=en-GB">3</a>)
</p>

<p>
Presgrip Sign Co was an exhibitor at the 1955 British Industries Fair (located at Stand F33).
(<a href="https://www.gracesguide.co.uk/1955_British_Industries_Fair:_Company_P">4</a>)
</p>

<h3>Presgrip Cine Title Sets</h3>

<p>
During the boom of amateur filmmaking in the mid-20th century (the 1950s and 60s), the company adapted their core product,
removable and reusable letters, to create the Presgrip Cine Title Sets for 8mm and 16mm cine film; these sets enabled amateur filmmakers
to easily create professional-looking titles and captions for home movies.
</p>

<p>
Presgrip offered several different versions of their Cine Title Sets, catering to various budgets and needs of the amateur filmmaker.
The contents typically revolved around a core set of reusable components designed for easy filming.
</p>

<ul>
    <li><strong>Letters and numbers:</strong> Usually white plastic characters supplied in large quantities, including a full alphabet and punctuation marks.</li>
    <li><strong>The board/screen:</strong> A title board or screen featuring a ribbed or slotted surface to keep letters aligned.</li>
    <li><strong>Backgrounds:</strong> Interchangeable red, blue, and green backgrounds to provide contrast when filming.</li>
    <li><strong>Celluloid filters:</strong> Colored plastic filters used to create tinting and special colour effects.</li>
    <li><strong>Instructions and layout guides:</strong> Manuals and centering guides to ensure titles appeared correctly framed.</li>
</ul>

<h3>Product Price List</h3>

<table>
    <thead>
        <tr>
            <th>Description</th>
            <th>Price Each</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>Outfit 'B' - standard complete set</td><td>£4 0s 0d (four pounds)</td></tr>
        <tr><td>Outfit 'MAJOR' - larger, more comprehensive set</td><td>£5 12s 6d (five pounds, twelve shillings, and sixpence)</td></tr>
        <tr><td>Felt board - 15" × 12"</td><td>£1 10s 0d (one pound, ten shillings)</td></tr>
        <tr><td>Title easel - for holding the titling board</td><td>£1 15s 0d (one pound, fifteen shillings)</td></tr>
        <tr><td>"100" set of extra white letters/figures</td><td>12s 6d (twelve shillings, sixpence)</td></tr>
        <tr><td>"100" set of extra yellow letters/figures</td><td>15s 0d (fifteen shillings)</td></tr>
    </tbody>
</table>

<h3>Spares Price List</h3>

<h4>Letters (Upper Case)</h4>

<div class="char-list">
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z ? ! ( ) &amp;
</div>

<table>
    <thead>
        <tr>
            <th>Size</th>
            <th>Price Each</th>
            <th>Price Per Dozen</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>3/4"</td><td>3d (threepence)</td><td>2s 9d (two shillings, ninepence)</td></tr>
        <tr><td>9/16"</td><td>3d (threepence)</td><td>2s 6d (two shillings, sixpence)</td></tr>
        <tr><td>3/8"</td><td>2½d (two and halfpence)</td><td>2s 3d (two shillings, threepence)</td></tr>
        <tr><td>Script</td><td>3d (threepence)</td><td>2s 6d (two shillings, sixpence)</td></tr>
    </tbody>
</table>

<h4>Letters (Lower Case)</h4>

<div class="char-list">
a b c d e f g h i j k l m n o p q r s t u v w x y z ? !
</div>

<table>
    <thead>
        <tr>
            <th>Size</th>
            <th>Price Each</th>
            <th>Price Per Dozen</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>9/16"</td><td>3d (threepence)</td><td>2s 6d (two shillings, sixpence)</td></tr>
        <tr><td>3/8"</td><td>2½d (two and halfpence)</td><td>2s 3d (two shillings, threepence)</td></tr>
        <tr><td>Script</td><td>3d (threepence)</td><td>2s 6d (two shillings, sixpence)</td></tr>
    </tbody>
</table>

<h4>Numerals</h4>

<div class="char-list">
1 2 3 4 5 6 7 8 9 £ / /- $
</div>

<table>
    <thead>
        <tr>
            <th>Size</th>
            <th>Price Each</th>
            <th>Price Per Dozen</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>1"</td><td>3½d (three and halfpence)</td><td>3s 6d (three shillings, sixpence)</td></tr>
        <tr><td>12/16"</td><td>3d (threepence)</td><td>3s (three shillings)</td></tr>
        <tr><td>9/16"</td><td>3d (threepence)</td><td>2s 6d (two shillings, sixpence)</td></tr>
        <tr><td>3/8"</td><td>3½d (three and halfpence)</td><td>2s 3d (two shillings, threepence)</td></tr>
        <tr><td>Script (except £ / /- d $)</td><td>3d (threepence)</td><td>2s 6d (two shillings, sixpence)</td></tr>
    </tbody>
</table>

<h4>Titler</h4>

<table>
    <thead>
        <tr>
            <th>Description</th>
            <th>Price Each</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>Raising and lowering attachment</td><td>£10 10s 0d (ten pounds, ten shillings)</td></tr>
        <tr><td>Lamp reflector</td><td>45s 0d (forty-five shillings)</td></tr>
        <tr><td>Animation table</td><td>17s 6d (seventeen shillings, sixpence)</td></tr>
        <tr><td>13 7/8" × 13 7/8" Perspex screen</td><td>17s 6d (seventeen shillings, sixpence)</td></tr>
        <tr><td>13 7/8" × 12" Perspex screen</td><td>15s 0d (fifteen shillings)</td></tr>
    </tbody>
</table>

<h4>Misc</h4>

<table>
    <thead>
        <tr>
            <th>Description</th>
            <th>Price Each</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>12" × 9" transparent screen</td><td>6s 0d (six shillings)</td></tr>
        <tr><td>Centering rule</td><td>2s 3d (two shillings, threepence)</td></tr>
        <tr><td>12" × 9" background leatherette sheet (red, blue, green, black)</td><td>9d (ninepence)</td></tr>
        <tr><td>12" × 9" layout card</td><td>9d (ninepence)</td></tr>
        <tr><td>12" × 9" script layout card</td><td>9d (ninepence)</td></tr>
        <tr><td>Cardboard box with one plastic tray</td><td>6s 6d (six shillings, sixpence)</td></tr>
        <tr><td>Wooden box with two plastic trays</td><td>40s 0d (forty shillings)</td></tr>
        <tr><td>Wooden box with one plastic tray</td><td>35s 0d (thirty-five shillings)</td></tr>
    </tbody>
</table>

</body>
</html>
