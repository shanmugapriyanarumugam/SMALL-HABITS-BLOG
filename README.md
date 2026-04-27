/* Mobile Optimization */
    @media (max-width: 768px) {
        /* Force everything to stay in bounds */
        html, body {
            max-width: 100vw;
            overflow-x: hidden;
        }
        
        .container {
            width: 100%;
            max-width: 100vw;
            box-shadow: none;
            overflow-x: hidden; /* Added strict overflow control here */
        }

        /* Prevent large text from breaking the layout */
        h1, h2, h3, .subtitle, p, a, div {
            overflow-wrap: break-word;
            word-wrap: break-word;
            hyphens: auto;
        }

        header { 
            padding: 3rem 1.5rem; 
        }
        
        h1 { 
            font-size: 2rem; 
        }

        main { 
            padding: 2rem 1.25rem; 
        }
        
        body { 
            font-size: 17px; 
            line-height: 1.6; 
        }

        /* Removed negative margins to prevent right-side spillage */
        .img-wrapper { 
            margin: 2rem 0; 
            width: 100%; 
            border-radius: 8px; /* Restored slight border radius */
        }

        blockquote { 
            margin: 2rem 0; 
            width: 100%; 
            padding: 1.5rem;
            font-size: 1.1rem;
            border-radius: 0 8px 8px 0;
        }

        .habit-steps li {
            padding: 1.25rem 1rem 1.25rem 3.5rem; 
        }
        
        .habit-steps li::before {
            left: 0.75rem;
            top: 1.25rem;
        }
    }
