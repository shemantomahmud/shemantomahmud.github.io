<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <title>Premium Live TV Streaming | Watch HD Channels Online</title>
    <meta name="description" content="Experience high-quality Premium Live TV Streaming. Watch your favorite sports, news, and entertainment channels seamlessly in HD anywhere, anytime.">
    <meta name="keywords" content="Live TV, HD Streaming, IPTV, Premium TV, Watch TV Online, Sports Streaming, Bdix Live TV, Web Player">
    <meta name="author" content="Sohag1192">
    <meta name="robots" content="index, follow">
    
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://yourwebsite.com/">
    <meta property="og:title" content="Premium Live TV Streaming | Watch HD Channels Online">
    <meta property="og:description" content="Experience high-quality Premium Live TV Streaming. Watch your favorite sports, news, and entertainment channels seamlessly in HD.">
    <meta property="og:image" content="https://placehold.co/1200x630/e50914/ffffff?text=Premium+Live+TV">
    
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://yourwebsite.com/">
    <meta property="twitter:title" content="Premium Live TV Streaming | Watch HD Channels Online">
    <meta property="twitter:description" content="Experience high-quality Premium Live TV Streaming. Watch your favorite sports, news, and entertainment channels seamlessly in HD.">
    <meta property="twitter:image" content="https://placehold.co/1200x630/e50914/ffffff?text=Premium+Live+TV">
    <link rel="shortcut icon" href="https://placehold.co/16x16/000000/ffffff?text=TV"/>
    <link rel="icon" href="favicon.png">

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://vjs.zencdn.net/7.20.3/video-js.css" rel="stylesheet">

    <style>
        :root{
            --primary: #e50914; /* Netflix Red */
            --primary-hover: #ff0f1e;
            --dark: #0a0a0a;
            --light: #f5f5f5;
            --semi-transparent: rgba(20, 20, 20, 0.75);
            --dark-transparent: rgba(10, 10, 10, 0.85);
            --card-bg: rgba(255, 255, 255, 0.04);
            --muted: #a3a3a3;
            --border-glass: rgba(255, 255, 255, 0.08);
        }

        html, body {
            height: 100%;
            scroll-behavior: smooth;
        }

        body {
            /* Premium cinematic gradient background */
            background: radial-gradient(circle at top, #2b0b12 0%, #0a0a0a 40%, #000000 100%);
            color: var(--light);
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            min-height: 100vh;
            margin: 0;
            padding-top: 76px; /* Space for navbar */
        }

        /* ---------- CUSTOM SCROLLBAR ---------- */
        ::-webkit-scrollbar { width: 8px; height: 6px; }
        ::-webkit-scrollbar-thumb { background: var(--border-glass); border-radius: 10px; }
        ::-webkit-scrollbar-thumb:hover { background: var(--primary); }
        ::-webkit-scrollbar-track { background: transparent; }

        /* ---------- NAVBAR ---------- */
        .navbar-custom {
            background-color: var(--dark-transparent);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-glass);
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.5);
            padding: 12px 0;
        }
        
        .navbar-custom .navbar-brand {
            color: var(--light);
            font-weight: 700;
            letter-spacing: 0.5px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            font-size: 16px;
            padding: 8px 14px;
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .navbar-custom .navbar-brand i { color: var(--primary); }
        .navbar-custom .navbar-brand:hover { background: var(--card-bg); text-shadow: 0 0 8px rgba(229,9,20,0.4); }

        .navbar-custom .nav-link {
            color: var(--muted) !important;
            font-weight: 500;
            padding: 8px 14px;
            margin: 0 2px;
            transition: all 0.3s ease;
            border-radius: 6px;
        }
        
        .navbar-custom .nav-link:hover {
            color: var(--light) !important;
            background: var(--card-bg);
            transform: translateY(-1px);
        }

        .navbar-custom .navbar-collapse {
            background: transparent;
        }

        @media (max-width: 991px) {
            .navbar-custom .navbar-collapse {
                background: #111;
                border-radius: 8px;
                padding: 10px;
                margin-top: 10px;
                border: 1px solid var(--border-glass);
            }
        }

        /* ---------- PLAYER ---------- */
        .player-sticky {
            position: sticky;
            top: 96px; 
            z-index: 100;
            align-self: start;
        }

        .player-container {
            width: 100%;
            background: #000;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0,0,0,0.6);
            border: 1px solid var(--border-glass);
        }

        .video-js {
            width: 100% !important;
            height: 65vh !important;
            object-fit: contain;
        }

        /* ---------- NOW PLAYING ---------- */
        .now-playing {
            display: inline-block;
            background: linear-gradient(135deg, var(--primary) 0%, #a0060e 100%);
            color: white;
            padding: 10px 20px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(229, 9, 20, 0.4);
            letter-spacing: 0.5px;
        }

        /* ---------- CHANNEL LIST PANEL ---------- */
        .channel-list {
            background-color: var(--semi-transparent);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-radius: 16px;
            padding: 22px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
            border: 1px solid var(--border-glass);
            height: calc(100vh - 130px);
            overflow-y: auto;
            overflow-x: hidden;
        }

        .channel-list h5 {
            color: var(--light);
            font-weight: 700;
            letter-spacing: 0.5px;
        }

        /* ---------- SEARCH BOX ---------- */
        .channel-search input {
            width: 100%;
            padding: 12px 16px;
            border-radius: 10px;
            border: 1px solid var(--border-glass);
            background: rgba(0,0,0,0.5);
            color: var(--light);
            transition: 0.3s;
            margin-bottom: 20px;
        }
        .channel-search input:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 10px rgba(229,9,20,0.2);
            background: rgba(0,0,0,0.8);
        }

        /* ---------- CHANNEL GRID & CARDS ---------- */
        #vidlink {
            display: grid;
            grid-template-columns: repeat(1, 1fr);
            gap: 16px;
            padding: 0 4px 10px 4px;
            margin: 0;
            list-style: none;
        }

        @media (min-width: 992px) { #vidlink { grid-template-columns: repeat(2, 1fr); } }
        @media (min-width: 1400px) { #vidlink { grid-template-columns: repeat(3, 1fr); } }

        #vidlink .channel {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            background: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.25s cubic-bezier(0.25, 0.8, 0.25, 1);
            border: 1px solid transparent;
            padding: 12px;
            cursor: pointer;
        }
        
        #vidlink .channel:hover {
            transform: translateY(-4px) scale(1.02);
            background: rgba(255,255,255,0.08);
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
            border-color: rgba(255,255,255,0.2);
        }

        #vidlink .thumb {
            width: 100%;
            max-width: 110px;
            aspect-ratio: 1/1;
            display: block;
            border-radius: 8px;
            object-fit: contain;
            background: rgba(0,0,0,0.3);
            padding: 8px;
            transition: 0.3s;
        }

        .channel-label {
            width: 100%;
            text-align: center;
            color: var(--muted);
            font-weight: 600;
            font-size: 13px;
            padding: 6px;
            border-radius: 6px;
            transition: 0.3s;
        }

        /* ---------- ACTIVE STATE ---------- */
        .channel.selected {
            border: 1px solid var(--primary) !important;
            background: linear-gradient(to bottom, rgba(229,9,20,0.1), rgba(0,0,0,0.5)) !important;
            box-shadow: 0 8px 25px rgba(229,9,20,0.2) !important;
        }
        .channel.selected .channel-label {
            color: var(--light);
            background: var(--primary);
        }

        /* ---------- MOBILE RESPONSIVENESS ---------- */
        @media (max-width: 991px) {
            .video-js { height: 40vh !important; }
            .player-sticky { margin-bottom: 0px; top: 76px; }
            body { padding-top: 76px; }

            .channel-list {
                height: auto;
                padding: 15px 0;
                background: transparent;
                box-shadow: none;
                border: none;
            }
            .channel-list h5, .channel-list p.small { padding: 0 15px; }

            #vidlink {
                display: flex;
                flex-direction: row;
                overflow-x: auto;
                scroll-snap-type: x mandatory;
                gap: 12px;
                padding: 5px 15px 15px 15px;
            }
            #vidlink > li {
                flex: 0 0 100px;
                scroll-snap-align: start;
            }
            .channel-label { display: none !important; }
        }

        /* ---------- FOOTER ---------- */
        .copyright-footer {
            background-color: var(--dark-transparent);
            backdrop-filter: blur(10px);
            color: var(--muted);
            text-align: center;
            padding: 20px;
            margin-top: 30px;
            font-size: 14px;
            border-top: 1px solid var(--border-glass);
            border-radius: 12px;
        }
        .copyright-footer a { color: var(--light); text-decoration: none; transition: 0.2s; }
        .copyright-footer a:hover { color: var(--primary); }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark navbar-custom fixed-top">
        <div class="container-fluid">
            <a class="navbar-brand" href="/"><i class="fas fa-play"></i> PREMIUM TV</a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mainNav"
                    aria-controls="mainNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="mainNav">
                <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                    <li class="nav-item"><a class="nav-link" href="http://172.16.50.4"><i class="fas fa-tv me-1"></i> FTP 1</a></li>
                    <li class="nav-item"><a class="nav-link" href="http://10.16.100.244"><i class="fas fa-mobile-screen me-1"></i> FTP 2</a></li>
                    <li class="nav-item"><a class="nav-link" href="http://172.50.50.20/"><i class="fas fa-server me-1"></i> FTP 3</a></li>
                    <li class="nav-item"><a class="nav-link" href="http://100.100.100.6"><i class="fas fa-server me-1"></i> FTP 4</a></li>
                    <li class="nav-item"><a class="nav-link" href="http://100.100.100.6:8096/"><i class="fas fa-film me-1"></i> FTP 5</a></li>
                    <li class="nav-item"><a class="nav-link" href="http://10.30.30.30/"><i class="fas fa-satellite-dish me-1"></i> IPTV 1</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container-fluid px-3 px-lg-4">
        <div class="row justify-content-center g-4">

            <div class="col-12 col-lg-8 mt-4 player-sticky">
                <div class="player-container">
                    <video id="Sohag_Player"
                            class="video-js vjs-default-skin vjs-big-play-centered vjs-fill"
                            controls
                            preload="auto"
                            data-setup='{}'>
                        <source src="http://172.16.234.30:9090/hls/channel_1.m3u8" type="application/x-mpegURL" />
                    </video>
                </div>

                <div id="nowPlayingWrapper" class="mt-4 d-none d-lg-flex justify-content-between align-items-center">
                    <span id="nowPlaying" class="now-playing">
                        <i class="fas fa-circle-play me-2"></i>Now Playing: Channel 1
                    </span>
                </div>
            </div>

            <div class="col-12 col-lg-4 mt-lg-4 mt-2">
                <div class="channel-list">
                    <div class="d-flex justify-content-between align-items-center mb-1">
                        <h5><i class="fas fa-broadcast-tower me-2 text-danger"></i>Channels</h5>
                    </div>
                    <p class="small text-muted mb-3">Click any channel to start streaming</p>

                    <div class="channel-search d-none d-lg-block">
                        <input id="channelFilter" type="text" placeholder="Search channels..." oninput="filterChannels()" />
                    </div>

                    <ul id="vidlink" class="thumbnail-slider">
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:9090/hls/channel_1.m3u8','Channel 1', this)" title="Channel 1">
                                <img class="thumb" src="assets/images/1.jpg" alt="Channel 1" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH1'">
                                <div class="channel-label">Channel 1</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:9090/hls2/ch2.m3u8','Channel 2', this)" title="Channel 2">
                                <img class="thumb" src="assets/images/2.jpg" alt="Channel 2" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH2'">
                                <div class="channel-label">Channel 2</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:9090/hls3/ch3.m3u8','Channel 3', this)" title="Channel 3">
                                <img class="thumb" src="assets/images/3.jpg" alt="Channel 3" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH3'">
                                <div class="channel-label">Channel 3</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:9090/hls4/ch4.m3u8','Channel 4', this)" title="Channel 4">
                                <img class="thumb" src="assets/images/4.jpg" alt="Channel 4" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH4'">
                                <div class="channel-label">Channel 4</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:9090/hls5/ch5.m3u8','Channel 5', this)" title="Channel 5">
                                <img class="thumb" src="assets/images/5.jpg" alt="Channel 5" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH5'">
                                <div class="channel-label">Channel 5</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:9090/hls6/ch6.m3u8','Channel 6', this)" title="Channel 6">
                                <img class="thumb" src="assets/images/6.jpg" alt="Channel 6" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH6'">
                                <div class="channel-label">Channel 6</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:9090/hls7/ch7.m3u8','Channel 7', this)" title="Channel 7">
                                <img class="thumb" src="assets/images/7.jpg" alt="Channel 7" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH7'">
                                <div class="channel-label">Channel 7</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:8080/ch4/index.m3u8','Channel 8', this)" title="Channel 8">
                                <img class="thumb" src="assets/images/8.jpg" alt="Channel 8" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH8'">
                                <div class="channel-label">Channel 8</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:8080/ch9/index.m3u8','Channel 9', this)" title="Channel 9">
                                <img class="thumb" src="assets/images/9.jpg" alt="Channel 9" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH9'">
                                <div class="channel-label">Channel 9</div>
                            </div>
                        </li>
                        <li class="Sports">
                            <div class="channel" onclick="switchChannel('http://172.16.234.30:8080/ch11/index.m3u8','Channel 10', this)" title="Channel 10">
                                <img class="thumb" src="assets/images/10.jpg" alt="Channel 10" onerror="this.src='https://placehold.co/100x100/111/fff?text=CH10'">
                                <div class="channel-label">Channel 10</div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>

        </div>
    </div>

    <div class="container p-3 mb-3">
        <div class="copyright-footer">
            &copy; 2025 Bdix Live TV. All Rights Reserved.<br>
            <span class="mt-1 d-block">
                Developed by <a href="https://github.com/sohag1192" target="_blank" style="font-weight: 600;">Sohag1192</a>
            </span>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://vjs.zencdn.net/7.20.3/video.min.js"></script>

    <script>
        // Initialize Video.js player
        const player = videojs('Sohag_Player');

        // Keep a reference to the currently selected channel element (for highlight)
        let currentSelectedChannel = null;

        function switchChannel(url, name, element) {
            if (!url) return;

            // update player src and play
            player.src({ src: url, type: 'application/x-mpegURL' });
            player.play().catch((e) => {
                console.debug('Autoplay blocked or failed:', e);
            });

            // update Now Playing label (only visible on desktop)
            const now = document.getElementById('nowPlaying');
            if (now) now.innerHTML = `<i class="fas fa-circle-play me-2"></i>Now Playing: ${name}`;

            // highlight selected tile
            try {
                if (currentSelectedChannel) currentSelectedChannel.classList.remove('selected');
                const channelEl = element && element.classList && element.classList.contains('channel') ? element : element.closest('.channel');
                if (channelEl) {
                    channelEl.classList.add('selected');
                    currentSelectedChannel = channelEl;
                }
            } catch (ex) {
                console.warn('Highlighting channel failed', ex);
            }

            // scroll the channel tile into view (works for mobile horizontal)
            if (element) {
                const parentPanel = element.closest('.channel-list');
                if (parentPanel) {
                    element.scrollIntoView({ behavior: 'smooth', block: 'nearest', inline: 'center' });
                }
            }
        }

        // Filter/search functionality
        function filterChannels() {
            const searchContainer = document.querySelector('.channel-search');
            if (!searchContainer) return;
            if (window.getComputedStyle(searchContainer).display === 'none') return;

            const q = document.getElementById('channelFilter').value.trim().toLowerCase();
            const items = document.querySelectorAll('#vidlink .channel');
            items.forEach(ch => {
                const label = (ch.querySelector('.channel-label')?.textContent || '').toLowerCase();
                const title = (ch.getAttribute('title') || '').toLowerCase();
                const alt = (ch.querySelector('.thumb')?.alt || '').toLowerCase();
                if (!q || label.includes(q) || title.includes(q) || alt.includes(q)) {
                    ch.parentElement.style.display = ''; 
                } else {
                    ch.parentElement.style.display = 'none';
                }
            });
        }

        // Initialize: mark the first channel as selected on load
        document.addEventListener('DOMContentLoaded', function() {
            const first = document.querySelector('#vidlink .channel');
            if (first) {
                first.classList.add('selected');
                currentSelectedChannel = first;
            }
        });

        // Keyboard navigation (left/right up/down)
        document.addEventListener('keydown', function(e) {
            if (!currentSelectedChannel) return;
            const all = Array.from(document.querySelectorAll('#vidlink .channel')).filter(n => n.parentElement.style.display !== 'none');
            const idx = all.indexOf(currentSelectedChannel);
            if (idx === -1) return;

            let targetIdx = -1;

            if (window.innerWidth < 992) {
                if (e.key === 'ArrowRight') targetIdx = idx + 1;
                else if (e.key === 'ArrowLeft') targetIdx = idx - 1;
            } else {
                if (e.key === 'ArrowDown') targetIdx = idx + 1;
                else if (e.key === 'ArrowUp') targetIdx = idx - 1;
            }

            if (targetIdx >= 0 && targetIdx < all.length) {
                all[targetIdx].click();
                e.preventDefault();
            }
        });
    </script>
</body>
</html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Shemanto Live TV Server">
    <link rel="shortcut icon" href="https://share.google/EHq3qDbqyCDV0vtgd"/>
    <title>Shemanto Live TV Server</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/hls.js@latest"></script>
    <style>
        :root {
            --primary-dark: #121212;
            --secondary-dark: #1E1E1E;
            --accent-dark: #BB86FC;
            --text-dark: #E1E1E1;
            
            --primary-light: #FFFFFF;
            --secondary-light: #F5F5F5;
            --accent-light: #6200EE;
            --text-light: #333333;
            
            --current-primary: var(--primary-dark);
            --current-secondary: var(--secondary-dark);
            --current-accent: var(--accent-dark);
            --current-text: var(--text-dark);
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            margin: 0;
            padding: 0;
            color: var(--current-text);
            background-color: var(--current-primary);
            transition: all 0.5s ease;
            min-height: 100vh;
        }

        /* Animated Background */
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Theme Toggle */
        .theme-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
            background: rgba(0,0,0,0.3);
            border-radius: 50px;
            padding: 5px;
            cursor: pointer;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
        }

        .theme-toggle:hover {
            transform: scale(1.1);
        }

        .theme-toggle i {
            font-size: 1.5rem;
            padding: 10px;
            color: var(--current-text);
        }

        /* Main Container */
        .main-container {
            max-width: 1600px;
            margin: 0 auto;
            padding: 30px;
            padding-top: 80px;
        }

        /* Player Section */
        .player-section {
            background-color: var(--current-secondary);
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            overflow: hidden;
            transition: all 0.3s ease;
            position: relative;
        }

        .player-section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.3);
        }

        /* Responsive Embed */
        .embed-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            background: #000;
        }

        .embed-container video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
            background-color: #000;
        }

        /* Player Info */
        .player-info {
            padding: 15px 20px;
            background: linear-gradient(transparent, rgba(0,0,0,0.9));
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            z-index: 10;
            pointer-events: none;
        }

        .channel-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 5px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.8);
            color: #fff;
        }

        .program-info {
            font-size: 0.9rem;
            opacity: 0.9;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.8);
            color: #ccc;
        }

        /* Channel List */
        .channel-list {
            background-color: var(--current-secondary);
            border-radius: 16px;
            padding: 20px;
            height: 100%;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .channel-list-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .channel-list-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin: 0;
        }

        .channel-count {
            background-color: var(--current-accent);
            color: var(--current-primary);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .channel-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 15px;
            overflow-y: auto;
            max-height: 70vh;
            padding-right: 5px;
        }
        
        /* Navbar Style Header */
        .top-nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            background: rgba(0,0,0,0.5);
            backdrop-filter: blur(10px);
        }

        .tv-link {
            color: #fff;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.2rem;
            transition: color 0.3s;
        }

        .tv-link:hover {
            color: var(--current-accent);
        }

        /* Updated Channel Item & Image Views */
        .channel-item {
            background-color: rgba(255,255,255,0.03);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            cursor: pointer;
            border: 2px solid transparent;
            display: flex;
            flex-direction: column;
        }

        .channel-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
            border-color: var(--current-accent);
            background-color: rgba(255,255,255,0.06);
        }

        .channel-item.active {
            border-color: var(--current-accent);
            box-shadow: 0 0 0 3px rgba(187, 134, 252, 0.3);
            background-color: rgba(187, 134, 252, 0.1);
        }

        .channel-thumbnail-wrapper {
            width: 100%;
            aspect-ratio: 16/9;
            background-color: #0a0a0a;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 12px;
            overflow: hidden;
        }

        .channel-thumbnail {
            width: 100%;
            height: 100%;
            object-fit: contain;
            transition: transform 0.3s ease;
        }

        .channel-item:hover .channel-thumbnail {
            transform: scale(1.1);
        }

        .channel-name {
            padding: 10px 8px;
            font-size: 0.9rem;
            font-weight: 500;
            text-align: center;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            border-top: 1px solid rgba(255,255,255,0.05);
        }

        /* Light Theme Adjustments */
        body.light-theme {
            --current-primary: var(--primary-light);
            --current-secondary: var(--secondary-light);
            --current-accent: var(--accent-light);
            --current-text: var(--text-light);
        }

        body.light-theme .channel-list {
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        body.light-theme .channel-item {
            background-color: #ffffff;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        body.light-theme .channel-thumbnail-wrapper {
            background-color: #f8f9fa;
        }

        body.light-theme .channel-name {
            border-top: 1px solid rgba(0,0,0,0.05);
        }

        body.light-theme .player-info {
            background: linear-gradient(transparent, rgba(0,0,0,0.6));
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            font-size: 0.9rem;
            opacity: 0.7;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        .footer a {
            color: var(--current-accent);
            text-decoration: none;
        }

        .footer a:hover {
            text-decoration: underline;
        }

        /* Responsive Adjustments */
        @media (max-width: 992px) {
            .channel-grid {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            }
        }

        @media (max-width: 768px) {
            .main-container {
                padding: 15px;
                padding-top: 70px;
            }
            
            .channel-grid {
                grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
                gap: 10px;
            }
            
            .channel-name {
                font-size: 0.75rem;
                padding: 6px 4px;
            }
            
            .channel-list-title {
                font-size: 1.2rem;
            }
        }

        /* Custom scrollbar */
        .channel-grid::-webkit-scrollbar {
            width: 6px;
        }

        .channel-grid::-webkit-scrollbar-track {
            background: rgba(255,255,255,0.05);
            border-radius: 10px;
        }

        .channel-grid::-webkit-scrollbar-thumb {
            background: var(--current-accent);
            border-radius: 10px;
        }

        .channel-grid::-webkit-scrollbar-thumb:hover {
            background: rgba(187, 134, 252, 0.8);
        }
    </style>
</head>
<body>
    <div class="background"></div>

    <header class="top-nav">
        <a href="/" class="tv-link"><i class="fas fa-tv me-2"></i>TV Version</a>
        <div class="theme-toggle" id="themeToggle">
            <i class="fas fa-moon"></i>
        </div>
    </header>

    <div class="main-container">
        <div class="row g-4">
            <div class="col-lg-9 col-md-8">
                <div class="player-section">
                    <div class="embed-container">
                        <video id="video-player" controls autoplay></video>
                        <div class="player-info">
                            <div class="channel-title">Loading...</div>
                            <div class="program-info">Please select a channel</div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="col-lg-3 col-md-4">
                <div class="channel-list">
                    <div class="channel-list-header">
                        <h2 class="channel-list-title">Channels</h2>
                        <div class="channel-count" id="channelCount">0</div>
                    </div>
                    <div class="channel-grid" id="channelGrid"></div>
                </div>
            </div>
        </div>
    </div>

    <div class="footer">
        <div>
            <img src="https://hitscounter.dev/api/hit?url=https%3A%2F%2Fgithub.com%2Fsohag1192%2FLive-Tv-Server&label=&icon=github&color=%23198754&message=&style=flat&tz=UTC" alt="GitHub hits">
        </div>
        <div class="mt-2">
            Â© Copyright 2013 Md Sohag Rana, Developed By: <a href="https://t.me/MdSohagRana" target="_blank">Md Sohag Rana</a>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // --- 1. M3U Data Injection ---
        const rawM3U = `#EXTM3U
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/jamunatv-logo.png" group-title="BANGLA NEWS", JAMUNA-TV-HD
http://c1live.net:8080/JAMUNA-TV-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/somoytv.png" group-title="BANGLA NEWS", SOMOY-TV-HD
http://c1live.net:8080/SOMOY-TV-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/ekattortv.png" group-title="BANGLA NEWS", EKATTOR-TV-HD
http://c1live.net:8080/EKATTOR-TV-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/channel24.png" group-title="BANGLA NEWS", CHANNEL-24-HD
http://c1live.net:8080/CHANNEL-24-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/dbcnews.png" group-title="BANGLA NEWS", DBC-NEWS-HD
http://c1live.net:8080/DBC-NEWS-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/independent.png" group-title="BANGLA NEWS",INDEPENDENT-TV
http://c1live.net:8080/INDEPENDENT-TV/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/jamunatv-logo.png" group-title="BANGLA NEWS",EKHON-TV-HD
http://c1live.net:8080/EKHON-TV-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/news24.png" group-title="BANGLA NEWS", NEWS-24-HD
http://c1live.net:8080/NEWS-24-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 tvg-logo="http://c1live.net/img/channels/atnnews.png group-title="BANGLA NEWS",ATN-NEWS
http://c1live.net:8080/ATN-NEWS/tracks-v1a1/mono.m3u8

        // --- 2. Parse M3U ---
        function parseM3U(data) {
            const lines = data.split('\n');
            const channels = [];
            let currentChannel = {};

            for (let line of lines) {
                line = line.trim();
                if (line.startsWith('#EXTINF:')) {
                    const logoMatch = line.match(/tvg-logo="([^"]+)"/);
                    currentChannel.logo = logoMatch ? logoMatch[1] : 'https://placehold.co/420x300/1a1a1a/ffffff?text=LIVE%20TV';

                    const groupMatch = line.match(/group-title="([^"]+)"/);
                    currentChannel.group = groupMatch ? groupMatch[1] : 'Live TV';

                    const parts = line.split(',');
                    currentChannel.name = parts[parts.length - 1];
                } else if (line.startsWith('http')) {
                    currentChannel.url = line;
                    channels.push(currentChannel);
                    currentChannel = {}; 
                }
            }
            return channels;
        }

        const channelData = parseM3U(rawM3U);

        // --- 3. Render Channels to DOM ---
        const channelGrid = document.getElementById('channelGrid');
        document.getElementById('channelCount').textContent = channelData.length + " Channels";

        channelData.forEach((ch, index) => {
            const item = document.createElement('div');
            item.className = 'channel-item';
            
            // Thumbnail handling (fallback if image fails to load)
            const fallbackImg = `https://placehold.co/420x300/1a1a1a/ffffff?text=${encodeURIComponent(ch.name)}`;
            
            // Updated HTML structure for the new image view
            item.innerHTML = `
                <div class="channel-thumbnail-wrapper">
                    <img src="${ch.logo}" class="channel-thumbnail" alt="${ch.name}" onerror="this.src='${fallbackImg}'">
                </div>
                <div class="channel-name">${ch.name}</div>
            `;
            
            item.addEventListener('click', function(e) {
                changeChannel(ch.url, ch.name, ch.group, this);
            });

            channelGrid.appendChild(item);
        });

        // Global variable to hold HLS instance
        let hlsInstance = null;

        // --- 4. Video Player & Channel Change Logic ---
        function changeChannel(url, channelName, programInfo, element) {
            const video = document.getElementById('video-player');
            
            if (hlsInstance) {
                hlsInstance.destroy();
            }

            if (Hls.isSupported()) {
                hlsInstance = new Hls();
                hlsInstance.loadSource(url);
                hlsInstance.attachMedia(video);
                hlsInstance.on(Hls.Events.MANIFEST_PARSED, function() {
                    video.play().catch(e => console.log("Auto-play prevented", e));
                });
            } 
            else if (video.canPlayType('application/vnd.apple.mpegurl')) {
                video.src = url;
                video.addEventListener('loadedmetadata', function() {
                    video.play();
                });
            }

            // Update UI
            document.querySelector('.channel-title').textContent = channelName;
            document.querySelector('.program-info').textContent = "Group: " + programInfo;
            
            const items = document.querySelectorAll('.channel-item');
            items.forEach(item => item.classList.remove('active'));
            if (element) {
                element.classList.add('active');
                element.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
            }
        }

        // --- 5. Theme & Initialization ---
        const themeToggle = document.getElementById('themeToggle');
        const body = document.body;
        
        const savedTheme = localStorage.getItem('theme') || 
                          (window.matchMedia('(prefers-color-scheme: light)').matches ? 'light' : 'dark');
        
        if (savedTheme === 'light') {
            body.classList.add('light-theme');
            themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
        }
        
        themeToggle.addEventListener('click', () => {
            body.classList.toggle('light-theme');
            const isLight = body.classList.contains('light-theme');
            
            localStorage.setItem('theme', isLight ? 'light' : 'dark');
            themeToggle.innerHTML = isLight ? '<i class="fas fa-sun"></i>' : '<i class="fas fa-moon"></i>';
        });

        // Keyboard Shortcuts
        document.addEventListener('keydown', function(e) {
            const items = document.querySelectorAll('.channel-item');
            if(items.length === 0) return;

            const currentActive = document.querySelector('.channel-item.active');
            let currentIndex = currentActive ? Array.from(items).indexOf(currentActive) : 0;
            
            if (e.key === 'ArrowUp' || e.key === 'ArrowLeft') {
                e.preventDefault();
                currentIndex = (currentIndex - 1 + items.length) % items.length;
            } else if (e.key === 'ArrowDown' || e.key === 'ArrowRight') {
                e.preventDefault();
                currentIndex = (currentIndex + 1) % items.length;
            } else if (e.key >= '1' && e.key <= '9') {
                currentIndex = parseInt(e.key) - 1;
                if (currentIndex >= items.length) currentIndex = items.length - 1;
            } else {
                return;
            }
            
            items[currentIndex].click();
        });

        // Initialize with first channel active on load
        document.addEventListener('DOMContentLoaded', function() {
            if (channelData.length > 0) {
                document.querySelector('.channel-item').click();
            }
        });
    </script>
</body>
</html>
