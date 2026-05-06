# Responsive Optimized Full Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Responsive Modern Website</title>

<style>

:root{
    --bg-color:#f5f7fa;
    --container-bg:#ffffff;
    --text-primary:#1f2937;
    --text-secondary:#4b5563;
    --accent-color:#319795;
    --accent-light:#e6fffa;
    --border-color:#e5e7eb;

    --font-body:Arial,sans-serif;
    --font-heading:Georgia,serif;
}

/* =========================
   RESET
========================= */

*,
*::before,
*::after{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
    overflow-x:hidden;
}

body{
    background:var(--bg-color);
    color:var(--text-primary);

    font-family:var(--font-body);
    font-size:18px;
    line-height:1.7;

    overflow-x:hidden;

    -webkit-font-smoothing:antialiased;
    -webkit-text-size-adjust:100%;
}

/* =========================
   CONTAINER
========================= */

.container{
    width:100%;
    max-width:900px;

    margin:auto;

    background:var(--container-bg);

    box-shadow:
    0 10px 20px rgba(0,0,0,0.08);

    overflow:hidden;
}

/* =========================
   HEADER
========================= */

header{
    background:linear-gradient(
        135deg,
        #285e61,
        #319795
    );

    color:white;

    text-align:center;

    padding:80px 20px;

    position:relative;
    overflow:hidden;
}

h1{
    font-family:var(--font-heading);

    font-size:clamp(2rem,5vw,3.5rem);

    margin-bottom:15px;

    line-height:1.2;

    word-break:break-word;
}

.subtitle{
    font-size:clamp(1rem,2vw,1.3rem);

    opacity:0.9;

    margin-bottom:20px;

    font-weight:300;
}

.meta{
    display:inline-block;

    border-top:1px solid rgba(255,255,255,0.4);

    padding-top:12px;

    font-size:14px;

    letter-spacing:2px;

    text-transform:uppercase;
}

/* =========================
   MAIN CONTENT
========================= */

main{
    padding:50px 40px;
}

/* =========================
   TYPOGRAPHY
========================= */

h2{
    font-family:var(--font-heading);

    font-size:clamp(1.5rem,3vw,2.2rem);

    margin-bottom:20px;
    margin-top:40px;

    border-left:5px solid var(--accent-color);

    padding-left:15px;

    color:#2c3e50;
}

h3{
    margin-top:25px;
    margin-bottom:10px;

    font-size:1.4rem;

    color:var(--text-primary);
}

p{
    margin-bottom:20px;

    color:var(--text-secondary);
}

strong{
    color:#285e61;
    font-weight:700;
}

/* =========================
   IMAGE SECTION
========================= */

.img-wrapper{
    width:100%;

    overflow:hidden;

    border-radius:14px;

    margin:35px 0;

    background:#eee;

    box-shadow:
    0 10px 20px rgba(0,0,0,0.08);
}

.img-wrapper img{
    width:100%;
    height:auto;

    display:block;

    transition:0.4s ease;
}

.img-wrapper:hover img{
    transform:scale(1.03);
}

.caption{
    text-align:center;

    padding:12px;

    font-size:14px;

    background:#f9fafb;

    color:#6b7280;

    font-style:italic;
}

/* =========================
   BLOCKQUOTE
========================= */

blockquote{
    background:var(--accent-light);

    border-left:6px solid var(--accent-color);

    padding:30px;

    margin:40px 0;

    border-radius:10px;

    font-size:1.2rem;

    font-style:italic;

    color:#234e52;

    box-shadow:0 4px 6px rgba(0,0,0,0.05);
}

blockquote small{
    display:block;

    margin-top:15px;

    font-size:14px;

    font-style:normal;

    color:#319795;

    font-weight:bold;
}

/* =========================
   LIST SECTION
========================= */

.habit-steps{
    list-style:none;

    display:grid;

    gap:20px;

    margin-top:20px;

    counter-reset:step;
}

.habit-steps li{
    position:relative;

    background:white;

    border:1px solid var(--border-color);

    border-radius:12px;

    padding:25px 20px 25px 70px;

    transition:0.3s ease;
}

.habit-steps li:hover{
    transform:translateY(-3px);

    box-shadow:
    0 8px 15px rgba(0,0,0,0.05);

    border-color:var(--accent-color);
}

.habit-steps li::before{
    content:counter(step);

    counter-increment:step;

    position:absolute;

    left:20px;
    top:22px;

    width:35px;
    height:35px;

    border-radius:50%;

    background:var(--accent-color);

    color:white;

    display:flex;
    align-items:center;
    justify-content:center;

    font-weight:bold;
}

.step-title{
    display:block;

    margin-bottom:8px;

    font-size:1.1rem;

    font-weight:bold;

    color:#2d3748;
}

/* =========================
   FOOTER
========================= */

footer{
    background:#111827;

    color:#9ca3af;

    text-align:center;

    padding:40px 20px;
}

footer p{
    margin:0;
}

/* =========================
   TABLET RESPONSIVE
========================= */

@media(max-width:768px){

    body{
        font-size:16px;
        line-height:1.6;
    }

    .container{
        box-shadow:none;
    }

    main{
        padding:35px 20px;
    }

    header{
        padding:60px 20px;
    }

    blockquote{
        padding:20px;

        font-size:1rem;
    }

    .habit-steps li{
        padding:
        20px
        15px
        20px
        60px;
    }

}

/* =========================
   MOBILE RESPONSIVE
========================= */

@media(max-width:480px){

    header{
        padding:50px 15px;
    }

    main{
        padding:25px 15px;
    }

    h2{
        padding-left:10px;

        border-left-width:4px;
    }

    .img-wrapper{
        border-radius:10px;
    }

    blockquote{
        margin:25px 0;

        border-left-width:4px;
    }

    .habit-steps li{
        padding:
        18px
        12px
        18px
        55px;
    }

    .habit-steps li::before{
        width:30px;
        height:30px;

        left:15px;
    }

}

</style>
</head>

<body>

<div class="container">

<header>
    <h1>Build Better Habits</h1>

    <p class="subtitle">
        Small daily improvements create long-term success.
    </p>

    <div class="meta">
        Responsive Mobile + Desktop Design
    </div>
</header>

<main>

    <h2>Introduction</h2>

    <p>
        This modern responsive layout is fully optimized for
        mobile phones, tablets, laptops, and desktop screens.
        The design automatically adjusts spacing, typography,
        and images for better readability and smoother performance.
    </p>

    <div class="img-wrapper">
        <img src="https://picsum.photos/900/500" alt="Responsive Website Image">

        <div class="caption">
            Modern responsive design optimized for all devices.
        </div>
    </div>

    <blockquote>
        Consistency is more important than perfection.

        <small>
            — Daily Habit Principle
        </small>
    </blockquote>

    <h2>How To Build Better Habits</h2>

    <p>
        Building better habits requires consistency, patience,
        and a simple step-by-step process.
    </p>

    <ul class="habit-steps">

        <li>
            <span class="step-title">
                Start Small
            </span>

            Focus on tiny improvements every single day.
        </li>

        <li>
            <span class="step-title">
                Stay Consistent
            </span>

            Repeating small actions daily creates long-term growth.
        </li>

        <li>
            <span class="step-title">
                Track Progress
            </span>

            Measure improvements regularly to stay motivated.
        </li>

        <li>
            <span class="step-title">
                Avoid Distractions
            </span>

            Create an environment that supports productivity.
        </li>

    </ul>

    <h2>Conclusion</h2>

    <p>
        This rewritten version combines your original styling,
        responsive mobile optimization, cleaner structure,
        and modern UI improvements into one complete code.
    </p>

</main>

<footer>
    <p>
        Responsive Website © 2026
    </p>
</footer>

</div>

</body>
</html>
```
