
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 9.2 - Responsive Typography & Images</title>

    <style>
        /* 1. Basic Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            font-size: 1rem;
            line-height: 1.7;
            color: #263238;
            background-color: #f4f7fb;
        }

        /* 2. Responsive Header */
        header {
            background-color: #172554;
            color: white;
            padding: 1.25rem 5%;
            text-align: center;
        }

        header h1 {
            font-size: clamp(1.5rem, 4vw, 2.5rem);
        }

        header p {
            font-size: 1rem;
            color: #dbeafe;
        }

        /* 3. Navigation */
        nav {
            background-color: #1e40af;
            padding: 0.75rem;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 0.8rem;
            font-size: 1em;
        }

        nav a:hover {
            color: #bfdbfe;
        }

        /* 4. Main Content Container */
        .container {
            width: 90%;
            max-width: 1100px;
            margin: 2rem auto;
        }

        /* 5. Article Section */
        .article {
            background-color: white;
            padding: clamp(1rem, 4vw, 2.5rem);
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
        }

        .article h2 {
            font-size: clamp(1.5rem, 3vw, 2.2rem);
            line-height: 1.3;
            margin-bottom: 1rem;
            color: #172554;
        }

        .article h3 {
            font-size: clamp(1.2rem, 2.5vw, 1.5rem);
            margin: 1.5rem 0 0.5rem;
            color: #1d4ed8;
        }

        .article p {
            font-size: clamp(0.95rem, 1.5vw, 1.1rem);
            margin-bottom: 1rem;
            overflow-wrap: break-word;
        }

        /* 6. Responsive Images */
        .article img {
            display: block;
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin: 1.5rem auto;
        }

        .hero-image {
            width: 100%;
        }

        .caption {
            font-size: 0.85rem;
            color: #64748b;
            text-align: center;
            margin-top: -1rem;
        }

        /* 7. Two Responsive Cards */
        .features {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .card {
            background-color: #eff6ff;
            padding: 1.25rem;
            border-radius: 10px;
            min-width: 0;
        }

        .card img {
            width: 100%;
            height: auto;
        }

        .card h3 {
            margin-top: 0.5rem;
        }

        /* 8. Footer */
        footer {
            background-color: #172554;
            color: white;
            text-align: center;
            padding: 1.5rem 1rem;
            margin-top: 2rem;
        }

        /* 9. Mobile Responsive Design */
        @media (max-width: 600px) {
            .container {
                width: 94%;
                margin: 1rem auto;
            }

            nav a {
                display: inline-block;
                margin: 0.25rem 0.5rem;
                font-size: 0.9rem;
            }

            .features {
                grid-template-columns: 1fr;
                gap: 1rem;
            }

            .article {
                border-radius: 8px;
            }

            .article img {
                margin: 1rem auto;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>My Responsive Blog</h1>
        <p>Learning Web Development, One Step at a Time</p>
    </header>

    <nav>
        <a href="#home">Home</a>
        <a href="#article">Articles</a>
        <a href="#features">Explore</a>
        <a href="#contact">Contact</a>
    </nav>

    <main class="container" id="home">

        <article class="article" id="article">

            <h2>Responsive Web Design: A Beginner's Guide</h2>

            <p>
                Responsive web design is an approach that makes websites
                look good on mobile phones, tablets, laptops, and desktop
                computers. It improves readability and provides a better
                user experience on every screen size.
            </p>

            <img
                class="hero-image"
                src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1200&q=80"
                alt="Laptop and workspace for web development"
            >

            <p class="caption">
                A modern workspace for learning web development.
            </p>

            <h3>Why Is Responsive Design Important?</h3>

            <p>
                People access websites using different devices.
                A responsive website adjusts its layout and text size
                according to the available screen width. This prevents
                horizontal scrolling and keeps content easy to read.
            </p>

            <h3>Responsive Typography</h3>

            <p>
                CSS properties such as rem, em, and clamp() help developers
                create flexible typography. The clamp() function allows
                font sizes to grow or shrink within defined limits.
                As a result, headings remain readable on both small
                and large screens.
            </p>

            <h3>Responsive Images</h3>

            <p>
                Images should maintain their original proportions when
                the screen size changes. Using max-width: 100% and
                height: auto prevents images from overflowing or
                becoming stretched.
            </p>

            <div class="features" id="features">

                <section class="card">
                    <img
                        src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?auto=format&fit=crop&w=700&q=80"
                        alt="Person working on a laptop"
                        loading="lazy"
                    >

                    <h3>Flexible Layout</h3>

                    <p>
                        Flexible layouts adjust the content to fit
                        different screen sizes using CSS Grid and
                        responsive widths.
                    </p>
                </section>

                <section class="card">
                    <img
                        src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?auto=format&fit=crop&w=700&q=80"
                        alt="Team collaborating on technology"
                        loading="lazy"
                    >

                    <h3>Better Experience</h3>

                    <p>
                        Readable text, properly sized images, and
                        consistent spacing make websites easier
                        to use on every device.
                    </p>
                </section>

            </div>

            <h3>Conclusion</h3>

            <p>
                Responsive typography and images are essential parts
                of modern web development. By using flexible font sizes,
                suitable content widths, responsive images, and media
                queries, developers can create websites that work
                across mobile and desktop screens.
            </p>

        </article>

    </main>

    <footer id="contact">
        <p>&copy; 2026 My Responsive Blog | Assignment 9.2</p>
        <p>Created using HTML and CSS</p>
    </footer>

</body>
</html>
