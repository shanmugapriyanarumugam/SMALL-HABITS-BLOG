<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Power of Small Habits</title>
    
    <style>
        :root {
            --bg-color: #f0f4f8;
            --container-bg: #ffffff;
            --text-primary: #2d3748;
            --text-secondary: #4a5568;
            --accent-color: #319795; /* Teal */
            --accent-light: #e6fffa;
            --border-color: #e2e8f0;
            --font-heading: 'Georgia', serif;
            --font-body: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html, body {
            overflow-x: hidden; /* Prevent horizontal scroll from full-bleed elements */
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-primary);
            font-family: var(--font-body);
            line-height: 1.7;
            font-size: 18px;
            -webkit-font-smoothing: antialiased;
            -webkit-text-size-adjust: 100%; /* Prevent font resizing on orientation change */
        }

        /* Layout & Container */
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: var(--container-bg);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }

        /* Header Section */
        header {
            background: linear-gradient(135deg, #285e61 0%, #319795 100%);
            color: white;
            padding: 5rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        h1 {
            font-family: var(--font-heading);
            font-size: 2.8rem;
            margin-bottom: 1rem;
            line-height: 1.2;
            position: relative;
            z-index: 10;
            word-wrap: break-word; /* Prevent overflow on small screens */
        }

        .subtitle {
            font-size: 1.25rem;
            opacity: 0.95;
            font-weight: 300;
            margin-bottom: 1.5rem;
            position: relative;
            z-index: 10;
        }

        .meta {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            opacity: 0.8;
            border-top: 1px solid rgba(255,255,255,0.3);
            display: inline-block;
            padding-top: 1rem;
            position: relative;
            z-index: 10;
        }

        /* Main Content */
        main {
            padding: 4rem 3rem;
        }

        /* Typography */
        h2 {
            font-family: var(--font-heading);
            color: #2c3e50;
            font-size: 2rem;
            margin-top: 3rem;
            margin-bottom: 1.5rem;
            border-left: 5px solid var(--accent-color);
            padding-left: 1rem;
        }

        h3 {
            font-size: 1.4rem;
            margin-top: 2rem;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        p {
            margin-bottom: 1.8rem;
            color: var(--text-secondary);
        }

        strong {
            color: #285e61;
            font-weight: 700;
        }

        /* Images */
        .img-wrapper {
            width: 100%;
            margin: 3rem 0;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            position: relative;
            background-color: #f0f4f8; /* Placeholder color while loading */
        }

        img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }

        .img-wrapper:hover img {
            transform: scale(1.03);
        }

        .caption {
            text-align: center;
            font-size: 0.9rem;
            color: #718096;
            padding: 0.8rem;
            background: #f7fafc;
            border-top: 1px solid #edf2f7;
            font-style: italic;
        }

        /* Blockquote */
        blockquote {
            background-color: var(--accent-light);
            border-left: 6px solid var(--accent-color);
            padding: 2rem;
            margin: 3rem 0;
            font-family: var(--font-heading);
            font-size: 1.2rem;
            font-style: italic;
            color: #234e52;
            border-radius: 0 12px 12px 0;
            box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05);
        }

        blockquote small {
            display: block;
            margin-top: 1rem;
            font-size: 0.9rem;
            font-family: var(--font-body);
            font-style: normal;
            color: #319795;
            font-weight: bold;
        }

        /* Lists */
        .habit-steps {
            list-style: none;
            padding-left: 0;
            counter-reset: step-counter;
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.5rem;
        }

        .habit-steps li {
            background: white;
            border: 1px solid var(--border-color);
            padding: 1.5rem 1.5rem 1.5rem 4rem;
            border-radius: 10px;
            position: relative;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
            transition: transform 0.2s;
        }

        .habit-steps li:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            border-color: var(--accent-color);
        }

        .habit-steps li::before {
            content: counter(step-counter);
            counter-increment: step-counter;
            position: absolute;
            left: 1rem;
            top: 1.5rem;
            width: 2rem;
            height: 2rem;
            background-color: var(--accent-color);
            color: white;
            border-radius: 50%;
            text-align: center;
            line-height: 2rem;
            font-weight: bold;
            font-size: 1rem;
        }

        .step-title {
            display: block;
            font-weight: 800;
            font-size: 1.1rem;
            color: #2d3748;
            margin-bottom: 0.5rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 4rem 2rem;
            background-color: #1a202c;
            color: #a0aec0;
            font-size: 0.95rem;
        }

        footer p {
            color: #718096;
            margin-bottom: 0;
        }

        /* Mobile Optimization */
        @media (max-width: 768px) {
            .container {
                box-shadow: none;
            }
            header { 
                padding: 4rem 1.5rem; 
            }
            h1 { 
                font-size: 2.2rem; 
            }
            .subtitle {
                font-size: 1.1rem;
            }
            main { 
                padding: 2rem 1.25rem; 
            }
            body { 
                font-size: 17px; 
                line-height: 1.6; 
            }
            h2 {
                font-size: 1.6rem;
                margin-top: 2.5rem;
                border-left-width: 4px;
            }
            .img-wrapper { 
                margin: 2.5rem -1.25rem; 
                width: calc(100% + 2.5rem); 
                border-radius: 0; 
            }
            blockquote { 
                margin: 2.5rem -1.25rem; 
                width: calc(100% + 2.5rem); 
                border-radius: 0; 
                padding: 1.5rem;
                font-size: 1.1rem;
                border-left-width: 4px;
            }
            .habit-steps li {
                padding: 1.25rem 1rem 1.25rem 3.5rem; 
            }
            .habit-steps li::before {
                left: 0.75rem;
                top: 1.25rem;
            }
        }

        /* Small Phones optimization */
        @media (max-width: 380px) {
            h1 { font-size: 1.8rem; }
            header { padding: 3rem 1rem; }
            main { padding: 1.5rem 1rem; }
            .img-wrapper, blockquote {
                margin: 2rem -1rem;
                width: calc(100% + 2rem);
            }
        }
    </style>
</head>
<body>

    <div class="container">
        
        <header>
            <h1>The Power of Small Habits</h1>
            <div class="subtitle">Transform your life one step at a time.</div>
            <div class="meta">By Author Name</div>
        </header>

        <main>
            <h2>Why Habits Matter</h2>
            <p>Your life today is essentially the sum of your habits. What you repeatedly do ultimately forms the person you are, the things you believe, and the personality that you portray.</p>

            <blockquote>
                "Success is the product of daily habits—not once-in-a-lifetime transformations."
                <small>James Clear</small>
            </blockquote>

            <h2>How to Build a Habit</h2>
            <ul class="habit-steps">
                <li>
                    <span class="step-title">Make it Obvious</span>
                    Design your environment to make good habits easier.
                </li>
                <li>
                    <span class="step-title">Make it Attractive</span>
                    Pair an action you want to do with an action you need to do.
                </li>
                <li>
                    <span class="step-title">Make it Easy</span>
                    Reduce friction and master the decisive moment.
                </li>
            </ul>

            <div class="img-wrapper">
                <img src="https://via.placeholder.com/800x400" alt="Habit building graphic">
                <div class="caption">Consistency is key over time.</div>
            </div>

        </main>

        <footer>
            <p>&copy; 2024 Your Website. Keep growing.</p>
        </footer>

    </div>

</body>
</html>
