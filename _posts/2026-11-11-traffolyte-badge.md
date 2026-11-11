---
title: Traffolyte Magic!
layout: post
categories: miscellaneous
---

It's been a great many years since I wandered through that convention hall, but those little oblong red-and-white badges are something I'll never forget — for me, they've always held an attraction of curious magical charm.

Everybody had one, and I wanted one too — but sadly I wasn't a radio ham, and I didn't have a cool callsign to show off.

Today, I'm going to get one&nbso;— and while I <i>still</i> don't have a cool callsign to show off, I <i>do</i> have a neat little website (even if I say so myself).

So here's my soon-to-be Traffolyte pin badge&nbsp;— what you reckon, Bob?

​<style>
.traffolyte-wrap{
display:flex;
justify-content:center;
margin:2rem 0;
perspective:1000px;
}

.traffolyte-container{
transform-style:preserve-3d;
cursor:pointer;
}

.traffolyte-badge{
width:260px;
height:84px;
position:relative;
overflow:hidden;

--red-top:#b4191f;
--red-mid:#a21217;
--red-bottom:#890d11;
--engraving:#fcfbf8;

--gloss-x:0px;
--gloss-y:0px;
--gloss-opacity:.22;

background:
linear-gradient(
180deg,
var(--red-top) 0%,
var(--red-mid) 35%,
#971116 70%,
var(--red-bottom) 100%
);

border-radius:1px;

border-top:1px solid rgba(255,255,255,.15);
border-left:1px solid rgba(255,255,255,.06);
border-right:1px solid rgba(0,0,0,.20);
border-bottom:1px solid rgba(0,0,0,.32);

box-shadow:
0 4px 16px rgba(0,0,0,.22),
inset 0 1px 1px rgba(255,255,255,.3);

transition:
transform .1s ease-out,
box-shadow .1s ease,
opacity .1s ease-out;
}

.traffolyte-badge::before{
content:"";
position:absolute;
inset:0;

background:
repeating-linear-gradient(
90deg,
rgba(255,255,255,.01) 0,
rgba(255,255,255,.01) 1px,
transparent 1px,
transparent 4px
);
}

.traffolyte-badge::after{
content:"";
position:absolute;
inset:-100%;
z-index:10;

opacity:var(--gloss-opacity);

background:
linear-gradient(
135deg,
transparent 35%,
rgba(255,255,255,.02) 42%,
rgba(255,255,255,.22) 48.5%,
rgba(255,255,255,.30) 50%,
rgba(255,255,255,.22) 51.5%,
rgba(255,255,255,.05) 58%,
transparent 65%
);

transform:translate(var(--gloss-x),var(--gloss-y));
pointer-events:none;
}

.traffolyte-text{
position:absolute;
inset:0;
z-index:1;

display:flex;
flex-direction:column;
justify-content:center;
align-items:center;

transform:translateY(-1px);
}

.traffolyte-callsign{
position:relative;

font-family:Bahnschrift,"DIN 1451 Mittelschrift",Arial,sans-serif;
font-size:30px;
font-weight:300;
line-height:1;
letter-spacing:2px;

color:var(--engraving);
}

.traffolyte-callsign::before{
content:attr(data-text);

position:absolute;
inset:0;

color:rgba(0,0,0,.28);
transform:translateY(-0.5px);
z-index:-1;
}

.traffolyte-name{
position:relative;

margin-top:6px;

font-family:Bahnschrift,"DIN 1451 Mittelschrift",Arial,sans-serif;
font-size:19.8px;
font-weight:240;
line-height:1;
letter-spacing:1px;

color:var(--engraving);
}

.traffolyte-name::before{
content:attr(data-text);

position:absolute;
inset:0;

color:rgba(0,0,0,.28);
transform:translateY(-0.5px);
z-index:-1;
}
</style>

<div class="traffolyte-wrap">
<div class="traffolyte-container" id="traffolyteContainer">
<div class="traffolyte-badge" id="traffolyteBadge">

<div class="traffolyte-text">

<div
class="traffolyte-callsign"
data-text="MART BETZ">
MART BETZ
</div>

<div
class="traffolyte-name"
data-text="martbetz.github.io">
martbetz.github.io
</div>

</div>

</div>
</div>
</div>

<script>
(function(){

const container = document.getElementById('traffolyteContainer');
const badge = document.getElementById('traffolyteBadge');

if(!container || !badge) return;

container.addEventListener('mousemove', (e) => {

const rect = container.getBoundingClientRect();

const x = e.clientX - rect.left;
const y = e.clientY - rect.top;

const xc = rect.width / 2;
const yc = rect.height / 2;

const dx = (x - xc) / xc;
const dy = (y - yc) / yc;

const rotateX = -dy * 15;
const rotateY = dx * 15;

badge.style.setProperty('--gloss-x', (dx * 60) + 'px');
badge.style.setProperty('--gloss-y', (dy * 60) + 'px');

const d = Math.min(Math.sqrt(dx * dx + dy * dy), 1);

badge.style.setProperty(
'--gloss-opacity',
0.22 + (d * 0.78)
);

badge.style.transform =
rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale3d(1.02,1.02,1.02);

badge.style.boxShadow =
${-rotateY}px ${rotateX + 4}px 20px rgba(0,0,0,0.3), inset 0 1px 1px rgba(255,255,255,0.4);
});

container.addEventListener('mouseleave', () => {

badge.style.transform =
'rotateX(0deg) rotateY(0deg) scale3d(1,1,1)';

badge.style.boxShadow =
'0 4px 16px rgba(0,0,0,.22), inset 0 1px 1px rgba(255,255,255,.3)';

badge.style.setProperty('--gloss-x', '0px');
badge.style.setProperty('--gloss-y', '0px');
badge.style.setProperty('--gloss-opacity', '.22');
});

})();
</script>
​
​Traffolyte was invented in Manchester in 1927 by the Metropolitan-Vickers Electrical Company. Originally manufactured as a phenolic plastic sheet material for heavy electrical insulation, its unique multi-layered construction made it an instant classic for industrial signage and switchboard labels (and, of course, radio ham badges).
​
Traffolyte consists of distinct layered colors, most famously a bright red outer cap over a solid white inner core. Rather than printing ink on top of the surface, a rotary router or mechanical pantograph physically cuts through the top red veneer; this exposes the stark white layer underneath, forming lovely high-contrast lettering that endures the test of time. The result is a clean, slightly recessed stroke with a subtle depth that modern flat-printing simply just can't match.

​As soon as I find somewhere suitable, I'll be getting my badge made up&nbsp;— <i>and I really can't wait!



​
