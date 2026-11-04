---
title: The Presgrip Project
layout: post
categories: photography projects

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

    animation:
        presgrip-weave 1.3s infinite,
        presgrip-flicker .35s infinite;
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

        <div class="presgrip-title">
            <div class="presgrip-main">THE</div>
            <div class="presgrip-main">PRESGRIP</div>
            <div class="presgrip-main">PROJECT</div>
        </div>

        <div class="presgrip-grain"></div>

    </div>

</div>

<font size="4">The objective of <b>The Presgrip Project</b> is to collate as much information as possible about the <b>Presgrip</b> range of cine title products. 
</font>

<p style="padding-top:15px; line-height: 1.1">
<font size="2">
¹ If you'd like to contribute to this project, please raise a pull request on Github.
</font>
</p>

<!-- Place this tag where you want the button to render. -->
<p style="padding-top: 20px;">
<a class="github-button" href="https://github.com/martbetz/The-Presgrip-Project   " data-size="large" aria-label="View Repo">View Repo</a>
</p>
