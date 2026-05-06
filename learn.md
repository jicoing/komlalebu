<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="icon" type="image/png" href="favicon3.png">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Jayanjan Mukherjee - Cloud Developer, Meme Maker, Deep Thinker">
    <meta property="og:title" content="Jayanjan Mukherjee">
    <meta property="og:description" content="Cloud Developer & Meme Maker. Tweets about code, clouds, and chaos.">
    <title>Jayanjan Mukherjee — Cloud Developer & Meme Maker</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@300;400;700;900&family=Playfair+Display:wght@400;600;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        :root {
            --bg: #FAFAF8;
            --text: #1A1A1A;
            --text-secondary: #4A4A4A;
            --muted: #6B6B6B;
            --orange: #D4652F;
            --orange-light: #E67E4D;
            --accent: #C9511C;
            --green: #2E7D32;
            --border: #E0E0E0;
            --card-border: #333333;
            --card-bg: #FFFFFF;
            --tag-red: #C62828;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        html { scroll-behavior: smooth; }

        body {
            font-family: 'Merriweather', Georgia, serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.7;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        /* NAV */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 100;
            padding: 0.75rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #FFFFFF;
            border-bottom: 3px solid var(--card-border);
        }

        .nav-logo {
            font-family: 'Playfair Display', Georgia, serif;
            font-weight: 900;
            font-size: 1.4rem;
            color: var(--text);
            text-decoration: none;
            letter-spacing: -0.02em;
        }

        .nav-logo span {
            color: var(--orange);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.85rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: var(--orange);
        }

        /* TOP BAR */
        .top-bar {
            background: var(--card-border);
            color: #FFFFFF;
            padding: 0.4rem 2rem;
            font-size: 0.75rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 60px;
        }

        .top-bar-left {
            display: flex;
            gap: 1.5rem;
        }

        .top-bar-left span {
            font-weight: 600;
        }

        .breaking-tag {
            background: var(--tag-red);
            padding: 0.15rem 0.6rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .top-bar-right {
            font-weight: 400;
            opacity: 0.9;
        }

        /* HERO */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 5rem 1.5rem 4rem;
            text-align: center;
            background: linear-gradient(180deg, #FAFAF8 0%, #F0F0EE 100%);
            border-bottom: 1px solid var(--border);
        }

        .hero-content {
            max-width: 700px;
            margin: 0 auto;
        }

        .hero .date-line {
            font-size: 0.8rem;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: 0.1em;
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--text);
            margin-bottom: 1.5rem;
            box-shadow: 0 4px 20px rgba(0,0,0,0.15);
        }

        .hero h1 {
            font-family: 'Playfair Display', Georgia, serif;
            font-size: clamp(2.2rem, 6vw, 3.8rem);
            font-weight: 900;
            margin-bottom: 0.75rem;
            line-height: 1.15;
            letter-spacing: -0.02em;
        }

        .hero h1 span {
            color: var(--orange);
            display: block;
        }

        .hero .tagline {
            font-size: 1.15rem;
            color: var(--text-secondary);
            max-width: 550px;
            margin: 0 auto 2rem;
            font-weight: 300;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            padding-top: 1rem;
            border-top: 2px solid var(--card-border);
        }

        .btn {
            padding: 0.85rem 2rem;
            font-family: 'Merriweather', Georgia, serif;
            font-weight: 700;
            font-size: 0.9rem;
            text-decoration: none;
            transition: all 0.2s;
            cursor: pointer;
            border: none;
        }

        .btn-primary {
            background: var(--text);
            color: #FFFFFF;
        }

        .btn-primary:hover {
            background: var(--orange);
        }

        .btn-outline {
            border: 2px solid var(--text);
            color: var(--text);
            background: transparent;
        }

        .btn-outline:hover {
            background: var(--text);
            color: #FFFFFF;
        }

        /* SECTIONS */
        section {
            padding: 3.5rem 1.5rem;
        }

        .section-header {
            margin-bottom: 2.5rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid var(--card-border);
        }

        .section-label {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 0.15em;
            color: var(--orange);
            margin-bottom: 0.4rem;
            font-weight: 700;
        }

        .section-meta {
            font-size: 0.75rem;
            color: var(--muted);
            margin-top: 0.3rem;
        }

        h2 {
            font-family: 'Playfair Display', Georgia, serif;
            font-size: clamp(1.6rem, 4vw, 2.4rem);
            font-weight: 700;
            letter-spacing: -0.01em;
        }

        /* WHAT I CREATE - NEWS CARD STYLE */
        .pillars {
            background: #FFFFFF;
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
        }

        .pillars-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
        }

        .pillar-card {
            background: var(--card-bg);
            border: 2px solid var(--card-border);
            padding: 1.75rem;
            transition: all 0.3s;
        }

        .pillar-card:hover {
            transform: translateY(-3px);
            border-color: var(--orange);
        }

        .pillar-card .category {
            font-size: 0.65rem;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            color: var(--orange);
            font-weight: 700;
            margin-bottom: 0.75rem;
            display: block;
        }

        .pillar-icon {
            font-size: 2rem;
            margin-bottom: 0.75rem;
        }

        .pillar-card h3 {
            font-family: 'Playfair Display', Georgia, serif;
            font-size: 1.25rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            line-height: 1.3;
        }

        .pillar-card p {
            font-size: 0.9rem;
            color: var(--text-secondary);
            font-weight: 300;
        }

        /* VIDEOS - NEWS GRID */
        .videos-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
        }

        .video-card {
            background: var(--card-bg);
            border: 2px solid var(--border);
            transition: all 0.3s;
        }

        .video-card:hover {
            border-color: var(--card-border);
            transform: translateY(-2px);
        }

        .video-thumbnail {
            aspect-ratio: 16/9;
            background: #1A1A1A;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: #FFFFFF;
            border-bottom: 2px solid var(--card-border);
            position: relative;
        }

        .video-thumbnail .duration {
            position: absolute;
            bottom: 0.5rem;
            right: 0.5rem;
            background: rgba(0,0,0,0.8);
            color: #FFF;
            font-size: 0.7rem;
            padding: 0.2rem 0.4rem;
            font-weight: 600;
        }

        .video-info {
            padding: 1rem;
        }

        .video-info h3 {
            font-family: 'Playfair Display', Georgia, serif;
            font-size: 1.05rem;
            font-weight: 700;
            line-height: 1.35;
        }

        .video-info .video-date {
            font-size: 0.75rem;
            color: var(--muted);
            margin-top: 0.5rem;
        }

        /* LINKS - NEWSPAPER STYLE */
        .links {
            background: #F5F5F3;
            border-top: 1px solid var(--border);
        }

        .links-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1rem;
        }

        .link-card {
            background: #FFFFFF;
            border: 2px solid var(--card-border);
            padding: 1.5rem 1rem;
            text-align: center;
            text-decoration: none;
            color: var(--text);
            transition: all 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .link-card:hover {
            background: var(--text);
            color: #FFFFFF;
            border-color: var(--text);
        }

        .link-card i {
            font-size: 1.75rem;
            margin-bottom: 0.5rem;
        }

        .link-card span {
            font-size: 0.8rem;
            font-weight: 700;
            text-transform: uppercase;
        }

        /* SOCIALS */
        .socials {
            display: flex;
            justify-content: center;
            gap: 2rem;
            padding: 2rem 0;
            border-bottom: 1px solid var(--border);
        }

        .socials a {
            color: var(--text);
            font-size: 1.5rem;
            transition: color 0.2s;
        }

        .socials a:hover {
            color: var(--orange);
        }

        /* FOOTER */
        footer {
            text-align: center;
            padding: 2rem 1.5rem;
            background: var(--text);
            color: #FFFFFF;
        }

        footer .edition {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 0.15em;
            margin-bottom: 1rem;
            opacity: 0.6;
        }

        footer p {
            font-size: 0.85rem;
        }

        footer a {
            color: var(--orange-light);
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        /* WHATSAPP FLOAT */
        .wa-float {
            position: fixed;
            bottom: 1.5rem;
            right: 1.5rem;
            z-index: 99;
            width: 56px;
            height: 56px;
            background: var(--green);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            text-decoration: none;
            box-shadow: 0 4px 15px rgba(46, 125, 50, 0.4);
        }

        /* RESPONSIVE */
        @media (max-width: 900px) {
            .pillars-grid, .videos-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .links-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 600px) {
            nav {
                padding: 0.75rem 1rem;
            }
            .nav-links {
                display: none;
            }
            .top-bar {
                flex-direction: column;
                gap: 0.5rem;
                padding: 0.5rem 1rem;
            }
            .top-bar-left, .top-bar-right {
                justify-content: center;
            }
            .hero {
                padding: 4rem 1rem 3rem;
            }
            .profile-img {
                width: 120px;
                height: 120px;
            }
            .hero-buttons {
                flex-direction: column;
            }
            .btn {
                width: 100%;
                text-align: center;
            }
            .pillars-grid, .videos-grid, .links-grid {
                grid-template-columns: 1fr;
            }
            section {
                padding: 2.5rem 1rem;
            }
        }
    </style>
</head>
<body>

<!-- TOP BAR -->
<div class="top-bar">
    <div class="top-bar-left">
        <span class="breaking-tag">Latest</span>
        <span>Cloud & Memes Edition</span>
    </div>
    <div class="top-bar-right">
        <span id="current-date"></span>
    </div>
</div>

<!-- NAV -->
<nav>
    <a href="#" class="nav-logo">komla<span>.</span></a>
    <ul class="nav-links">
        <li><a href="#create">Create</a></li>
        <li><a href="#videos">Videos</a></li>
        <li><a href="#links">Join</a></li>
    </ul>
</nav>

<!-- HERO -->
<section class="hero">
    <div class="hero-content">
        <div class="date-line">Wednesday, May 6, 2026</div>
        <img src="coverpic1.JPG" alt="Jayanjan Mukherjee" class="profile-img">
        <h1>Cloud Dev & <span>Meme Maker</span></h1>
        <p class="tagline">Hi, I'm Jayanjan — an orange who loves building in the cloud and making memes about code, chaos, and everything in between.</p>
        <div class="hero-buttons">
            <a href="https://www.youtube.com/@jicoing" class="btn btn-primary" target="_blank">
                <i class="fab fa-youtube"></i> Subscribe on YouTube
            </a>
            <a href="#links" class="btn btn-outline">Coffee & Links</a>
        </div>
    </div>
</section>

<!-- WHAT I CREATE -->
<section class="pillars" id="create">
    <div class="container">
        <div class="section-header">
            <div class="section-label">Featured</div>
            <h2>Three Pillars of Content</h2>
            <div class="section-meta">Published May 6, 2026 · Cloud Development</div>
        </div>
        <div class="pillars-grid">
            <div class="pillar-card">
                <span class="category">Cloud</span>
                <div class="pillar-icon">☁️</div>
                <h3>Cloud Development</h3>
                <p>Building serverless apps, automating stuff, and sharing AWS tips that actually make sense.</p>
            </div>
            <div class="pillar-card">
                <span class="category">Entertainment</span>
                <div class="pillar-icon">🎬</div>
                <h3>Animated Memes</h3>
                <p>Wildly chaotic, uniquely animated memes about tech life and developer struggles.</p>
            </div>
            <div class="pillar-card">
                <span class="category">Opinion</span>
                <div class="pillar-icon">💭</div>
                <h3>Deep Thoughts</h3>
                <p>Occasional rants about software, life as a dev, and the absurdity of it all.</p>
            </div>
        </div>
    </div>
</section>

<!-- VIDEOS -->
<section id="videos">
    <div class="container">
        <div class="section-header">
            <div class="section-label">Video</div>
            <h2>Recent Uploads</h2>
            <div class="section-meta">Latest from the channel</div>
        </div>
        <div class="videos-grid">
            <a href="https://www.youtube.com/watch?v=example1" class="video-card" target="_blank">
                <div class="video-thumbnail">
                    <i class="fab fa-youtube"></i>
                    <span class="duration">12:34</span>
                </div>
                <div class="video-info">
                    <h3>How I Built This Website</h3>
                    <div class="video-date">May 3, 2026</div>
                </div>
            </a>
            <a href="https://www.youtube.com/watch?v=example2" class="video-card" target="_blank">
                <div class="video-thumbnail">
                    <i class="fab fa-youtube"></i>
                    <span class="duration">08:45</span>
                </div>
                <div class="video-info">
                    <h3>AWS Lambda vs My Brain</h3>
                    <div class="video-date">Apr 28, 2026</div>
                </div>
            </a>
            <a href="https://www.youtube.com/shorts/example3" class="video-card" target="_blank">
                <div class="video-thumbnail">
                    <i class="fab fa-youtube"></i>
                    <span class="duration">00:58</span>
                </div>
                <div class="video-info">
                    <h3>Debugging at 2am</h3>
                    <div class="video-date">Apr 22, 2026</div>
                </div>
            </a>
        </div>
    </div>
</section>

<!-- LINKS / JOIN -->
<section class="links" id="links">
    <div class="container">
        <div class="section-header">
            <div class="section-label">Support</div>
            <h2>Support the Orange</h2>
            <div class="section-meta">Help keep the memes coming</div>
        </div>
        <div class="links-grid">
            <a href="https://www.buymeacoffee.com/jicoing" class="link-card" target="_blank">
                <i class="fas fa-coffee"></i>
                <span>Buy Me Coffee</span>
            </a>
            <a href="https://www.youtube.com/@jicoing" class="link-card" target="_blank">
                <i class="fab fa-youtube"></i>
                <span>YouTube</span>
            </a>
            <a href="https://x.com/jicoing" class="link-card" target="_blank">
                <i class="fab fa-twitter"></i>
                <span>X / Twitter</span>
            </a>
            <a href="https://github.com/jicoing" class="link-card" target="_blank">
                <i class="fab fa-github"></i>
                <span>GitHub</span>
            </a>
        </div>
    </div>
</section>

<!-- SOCIALS -->
<div class="socials">
    <a href="https://www.youtube.com/@jicoing" target="_blank" title="YouTube"><i class="fab fa-youtube"></i></a>
    <a href="https://x.com/jicoing" target="_blank" title="X / Twitter"><i class="fab fa-twitter"></i></a>
    <a href="https://github.com/jicoing" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
    <a href="https://www.linkedin.com/in/jicoing" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
</div>

<!-- FOOTER -->
<footer>
    <div class="edition">komla Daily · Cloud & Tech Edition</div>
    <p>© 2025 Jayanjan Mukherjee</p>
    <p style="margin-top: 0.5rem;">
        <a href="https://github.com/jicoing">GitHub</a> · 
        <a href="https://x.com/jicoing">Twitter</a> · 
        <a href="projects.html">Projects</a>
    </p>
</footer>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.me/9836272250?text=Hi%20Jayanjan!" class="wa-float" target="_blank">
    <i class="fab fa-whatsapp"></i>
</a>

<script>
    document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' });
</script>

</body>
</html>