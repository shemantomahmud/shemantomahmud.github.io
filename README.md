<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Premium Live TV Streaming Service">
    <link rel="shortcut icon" href="https://placehold.co/16x16/000000/ffffff?text=Premium+Live+TV+Streaming"/>
    <title>Premium Live TV Streaming</title>
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
        
            <div class="mt-2">
            © Copyright 2026 Developed By: <a href="https://github.com/shemantomahmud/" target="_blank">SHEMANTO MAHMUD</a>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // --- 1. M3U Data Injection ---
        const rawM3U = `#EXTM3U
#EXTINF:-1 group-title="BANGLA NEWS", JAMUNA TV
http://c1live.net:8080/JAMUNA-TV-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS", SOMOY TV
http://c1live.net:8080/SOMOY-TV-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS", EKATTOR TV
http://c1live.net:8080/EKATTOR-TV-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS", STAR NEWS
http://c1live.net:8080/CHANNEL-24-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS", DBC NEWS
http://c1live.net:8080/DBC-NEWS-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS",INDEPENDENT TV
http://c1live.net:8080/INDEPENDENT-TV/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS", NEWS 24
http://c1live.net:8080/NEWS-24-HD/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS",ATN NEWS
http://c1live.net:8080/ATN-NEWS/tracks-v1a1/mono.m3u8
#EXTINF:-1 group-title="BANGLA NEWS",CHANNEL 24
https://owrcovcrpy.gpcdn.net/bpk-tv/1703/output/index.m3u8
#EXTINF:-1 group-title="BANGLA NEWS",CHANNEL 1
https://owrcovcrpy.gpcdn.net/bpk-tv/1702/output/index.m3u8`;

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
