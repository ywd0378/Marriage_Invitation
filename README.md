<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <title>浪漫婚礼邀请 | 杨文达 & 孙智琴 结婚请帖</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --cream: #fef9f4;
            --warm-white: #fffef9;
            --rose-gold: #c4977a;
            --soft-pink: #f2d5c4;
            --deep-brown: #4a3424;
            --medium-brown: #7d5a3f;
            --light-brown: #b8916c;
            --champagne: #f7ede3;
            --blush: #fce4d6;
            --gold-accent: #d4a574;
            --text-dark: #3e2d1c;
            --shadow-soft: 0 4px 20px rgba(120, 80, 50, 0.07);
            --shadow-card: 0 8px 32px rgba(100, 60, 30, 0.06);
            --border-soft: #efe0d2;
            --radius-lg: 28px;
            --radius-md: 20px;
            --radius-sm: 60px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #fdf6ef;
            font-family: 'Montserrat', 'PingFang SC', 'Microsoft YaHei', 'Hiragino Sans GB', sans-serif;
            color: var(--text-dark);
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1.2rem;
            background-image:
                radial-gradient(ellipse at 20% 10%, rgba(220, 170, 140, 0.08) 0%, transparent 60%),
                radial-gradient(ellipse at 80% 90%, rgba(210, 155, 125, 0.06) 0%, transparent 55%),
                radial-gradient(ellipse at 50% 50%, rgba(240, 200, 170, 0.04) 0%, transparent 70%);
            background-attachment: fixed;
        }

        #petalsCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 9999;
        }

        .invitation-wrapper {
            width: 100%;
            max-width: 620px;
            background: var(--warm-white);
            box-shadow: var(--shadow-card), 0 0 0 1px rgba(210, 180, 155, 0.15);
            border-radius: var(--radius-lg);
            overflow: hidden;
            position: relative;
            z-index: 1;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: cardEntry 0.9s cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
        }

        @keyframes cardEntry {
            from { opacity: 0; transform: translateY(40px) scale(0.96); }
            to { opacity: 1; transform: translateY(0) scale(1); }
        }

        .invitation-wrapper:hover {
            box-shadow: 0 16px 48px rgba(100, 60, 30, 0.1), 0 0 0 1px rgba(200, 160, 130, 0.25);
            transform: translateY(-2px);
        }

        .hero {
            position: relative;
            background: linear-gradient(160deg, #f9e8d9 0%, #f5d8c0 25%, #fce8d5 50%, #f3d2b8 75%, #fae4cf 100%);
            height: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .hero-glow {
            position: absolute;
            border-radius: 50%;
            filter: blur(60px);
            opacity: 0.55;
            pointer-events: none;
            animation: glowBreathe 6s ease-in-out infinite;
        }
        .hero-glow.glow-1 { width: 200px; height: 200px; background: rgba(255,220,190,0.7); top: 10%; left: 15%; animation-delay: 0s; }
        .hero-glow.glow-2 { width: 160px; height: 160px; background: rgba(250,200,165,0.6); bottom: 15%; right: 12%; animation-delay: -3s; }
        .hero-glow.glow-3 { width: 120px; height: 120px; background: rgba(255,235,210,0.65); top: 50%; left: 55%; animation-delay: -1.5s; }

        @keyframes glowBreathe {
            0%,100%{transform:scale(1);opacity:0.5;}
            30%{transform:scale(1.25);opacity:0.7;}
            60%{transform:scale(0.9);opacity:0.4;}
        }

        .hero::before {
            content: "❁"; font-size: 150px; color: rgba(255,248,240,0.55);
            position: absolute; left: -25px; top: 15px; transform: rotate(-18deg);
            font-family: serif; animation: floatDecor 8s ease-in-out infinite; pointer-events: none;
        }
        .hero::after {
            content: "✿"; font-size: 130px; color: rgba(248,220,195,0.5);
            position: absolute; right: -18px; bottom: 5px; transform: rotate(12deg);
            animation: floatDecor 7s ease-in-out infinite reverse; pointer-events: none;
        }

        @keyframes floatDecor {
            0%,100%{transform:rotate(-18deg) translateY(0);}
            50%{transform:rotate(-14deg) translateY(-10px);}
        }

        .ring-container { position: relative; z-index: 3; display: flex; align-items: center; justify-content: center; }
        .ring-icon-outer {
            background: rgba(255,252,247,0.85); width: 140px; height: 140px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            box-shadow: 0 14px 28px rgba(100,55,25,0.12), 0 0 0 1px rgba(255,240,220,0.7);
            backdrop-filter: blur(4px); -webkit-backdrop-filter: blur(4px);
            border: 2px solid rgba(255,255,240,0.8);
            animation: ringPulse 3s ease-in-out infinite; transition: transform 0.3s ease;
        }
        .ring-icon-outer:hover { transform: scale(1.05); }
        @keyframes ringPulse {
            0%,100%{box-shadow:0 14px 28px rgba(100,55,25,0.12),0 0 0 1px rgba(255,240,220,0.7);}
            50%{box-shadow:0 18px 36px rgba(100,55,25,0.18),0 0 0 6px rgba(255,220,190,0.3);}
        }
        .ring-icon-outer i {
            font-size: 3.4rem; color: #c9a27c;
            filter: drop-shadow(0 4px 8px rgba(140,90,50,0.2));
            animation: ringShine 2.5s ease-in-out infinite;
        }
        @keyframes ringShine {
            0%,100%{filter:drop-shadow(0 4px 8px rgba(140,90,50,0.2));}
            50%{filter:drop-shadow(0 4px 16px rgba(200,140,80,0.5));}
        }

        .sparkle {
            position: absolute; pointer-events: none; z-index: 2; font-size: 1rem;
            color: #e8c8a0; animation: sparkleFloat 4s ease-in-out infinite; opacity: 0;
        }
        .sparkle:nth-child(1){top:18%;left:22%;animation-delay:0s;font-size:0.7rem;}
        .sparkle:nth-child(2){top:25%;right:20%;animation-delay:-1.2s;font-size:0.9rem;}
        .sparkle:nth-child(3){bottom:28%;left:28%;animation-delay:-2.5s;font-size:0.65rem;}
        .sparkle:nth-child(4){bottom:22%;right:25%;animation-delay:-3.6s;font-size:0.75rem;}
        .sparkle:nth-child(5){top:45%;left:10%;animation-delay:-0.8s;font-size:0.55rem;}
        .sparkle:nth-child(6){top:40%;right:8%;animation-delay:-2s;font-size:0.7rem;}

        @keyframes sparkleFloat {
            0%,100%{opacity:0;transform:translateY(0) scale(0.6);}
            30%{opacity:0.85;transform:translateY(-14px) scale(1.2);}
            60%{opacity:0.2;transform:translateY(-6px) scale(0.8);}
        }

        .content { padding: 2.2rem 2rem 2rem; position: relative; z-index: 1; }
        .invite-title { text-align: center; margin-bottom: 1.8rem; }
        .invite-title .pre-title {
            font-size:0.85rem; letter-spacing:4px; text-transform:uppercase;
            color:#be9a7c; margin-bottom:0.6rem; font-weight:500; display:block;
        }
        .couple-names {
            font-family:'Cormorant Garamond','Noto Serif SC','STSong','SimSun',serif;
            font-size:3.2rem; font-weight:600; color:#8b5a3c; letter-spacing:3px;
            margin:0.4rem 0; line-height:1.2; text-shadow:0 1px 2px rgba(0,0,0,0.04);
        }
        .ampersand {
            font-size:2.8rem; font-style:italic; font-weight:400; color:#d4a07a;
            margin:0 0.3rem; display:inline-block; animation:ampersandGlow 3s ease-in-out infinite;
        }
        @keyframes ampersandGlow {
            0%,100%{color:#d4a07a;text-shadow:0 0 0 transparent;}
            50%{color:#e8b890;text-shadow:0 0 18px rgba(210,150,110,0.4);}
        }
        .date-badge {
            background:#f9efe4; display:inline-block; padding:0.55rem 1.4rem;
            border-radius:var(--radius-sm); font-size:0.95rem; font-weight:500;
            margin-top:0.8rem; color:#a07250;
            box-shadow:inset 0 0 0 1px rgba(180,130,90,0.18), 0 2px 6px rgba(0,0,0,0.03);
            letter-spacing:0.5px;
        }
        .date-badge i { color:#c99770; margin-right:2px; }

        .divider {
            text-align:center; margin:1.6rem 0; color:#e2c8ae; font-size:1rem;
            letter-spacing:5px; display:flex; align-items:center; justify-content:center; gap:10px;
        }
        .divider::before,.divider::after {
            content:""; flex:1; height:1px;
            background:linear-gradient(to right, transparent, #e2c8ae, transparent);
            max-width:60px;
        }

        .core-info-card {
            background:#fefaf5; border-radius:var(--radius-md); padding:1.4rem 1.8rem;
            margin-bottom:1.5rem; box-shadow:var(--shadow-soft), 0 0 0 1px #f3e5d8;
            text-align:center; transition:box-shadow 0.3s ease;
        }
        .core-info-card:hover { box-shadow:0 6px 24px rgba(100,60,30,0.08), 0 0 0 1px #e8d4c0; }
        .core-date-time { display:flex; flex-direction:column; align-items:center; gap:0.3rem; margin-bottom:0.9rem; }
        .core-label { font-size:0.8rem; text-transform:uppercase; letter-spacing:2.5px; color:#b8926e; font-weight:500; }
        .core-label i { color:#c99a72; }
        .core-value {
            font-size:1.55rem; font-weight:600; color:#5a3c28;
            font-family:'Cormorant Garamond','Noto Serif SC',serif; letter-spacing:1px;
        }

        .address-section { margin-top:0.6rem; border-top:1px solid #f2e3d3; padding-top:0.9rem; }
        .address-line { font-size:1.05rem; font-weight:600; color:#6b4832; margin-bottom:0.3rem; letter-spacing:0.5px; }
        .address-detail { font-size:0.85rem; color:#a0846a; margin-bottom:10px; line-height:1.4; }

        .map-link-single, .btn-calendar {
            display:inline-flex; align-items:center; gap:6px;
            background:#fdf8f3; border:1px solid #ddc5ad; padding:7px 18px;
            border-radius:var(--radius-sm); font-size:0.82rem; color:#a8754f;
            margin-top:2px; cursor:pointer; transition:all 0.25s ease;
            text-decoration:none; font-weight:500; letter-spacing:0.3px; font-family:inherit;
        }
        .map-link-single i, .btn-calendar i { font-size:0.75rem; color:#c48b62; transition:transform 0.25s ease; }
        .map-link-single:hover, .btn-calendar:hover {
            background:#f9e8d7; border-color:#c48b62; color:#7d4f30;
            box-shadow:0 3px 12px rgba(160,100,55,0.12);
        }
        .map-link-single:hover i, .btn-calendar:hover i { transform:scale(1.2); }

        .action-buttons { display:flex; flex-wrap:wrap; gap:10px; justify-content:center; margin-top:10px; }

        .countdown {
            background:linear-gradient(135deg, #fff7f0 0%, #fff3ea 100%);
            border-radius:var(--radius-md); padding:1.3rem 1rem; text-align:center;
            margin:1.2rem 0 1rem; box-shadow:var(--shadow-soft), 0 0 0 1px #fbe8d7;
        }
        .countdown h4 {
            font-size:0.85rem; text-transform:uppercase; letter-spacing:2.5px;
            font-weight:500; color:#c9976e; margin-bottom:0.9rem;
            display:flex; align-items:center; justify-content:center; gap:8px;
        }
        .countdown h4 i { color:#d9a77e; font-size:0.75rem; animation:heartBeat 1.5s ease-in-out infinite; }
        @keyframes heartBeat {
            0%,100%{transform:scale(1);} 25%{transform:scale(1.2);} 50%{transform:scale(1);} 75%{transform:scale(1.15);}
        }
        .timer { display:flex; justify-content:center; gap:1rem; flex-wrap:wrap; }
        .time-block {
            background:#fffefb; border-radius:18px; padding:0.5rem 0.7rem; min-width:62px;
            box-shadow:0 2px 8px rgba(0,0,0,0.03); border:1px solid #f3e2d2;
            transition:transform 0.2s ease, box-shadow 0.2s ease;
        }
        .time-block:hover { transform:translateY(-3px); box-shadow:0 6px 16px rgba(140,80,40,0.1); }
        .time-number {
            font-size:1.7rem; font-weight:700; color:#8c593a; line-height:1;
            font-family:'Montserrat','PingFang SC',monospace; letter-spacing:1px;
            display:block; transition:color 0.3s;
        }
        .time-label { font-size:0.68rem; color:#b08966; text-transform:uppercase; letter-spacing:0.8px; font-weight:500; }

        /* 照片墙控制按钮 */
        .gallery-toggle-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            margin: 0 auto 1rem;
            background: transparent;
            border: 1px solid #ddc5ad;
            color: #a8754f;
            font-size: 0.82rem;
            padding: 7px 18px;
            border-radius: var(--radius-sm);
            cursor: pointer;
            letter-spacing: 1px;
            font-weight: 500;
            transition: all 0.3s ease;
            font-family: inherit;
        }
        .gallery-toggle-btn:hover {
            background: #f9e8d7;
            border-color: #c48b62;
            color: #7d4f30;
        }
        .gallery-toggle-btn i {
            transition: transform 0.3s ease;
        }
        .gallery-toggle-btn.expanded i {
            transform: rotate(180deg);
        }

        /* 照片墙容器 - 默认折叠 */
        .photo-gallery-wrapper {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.6s cubic-bezier(0.22, 0.61, 0.36, 1);
        }
        .photo-gallery-wrapper.expanded {
            max-height: 3000px;
        }

        .photo-gallery {
            padding: 0 0 1rem;
        }

        .photo-group {
            margin-bottom: 1.5rem;
        }
        .group-title {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            font-weight: 500;
            color: #c9976e;
            margin-bottom: 0.7rem;
            display: flex;
            align-items: center;
            gap: 6px;
            justify-content: center;
        }
        .group-title i { color: #d9a77e; font-size: 0.65rem; }
        .group-title .sparkle-icon { animation: sparkleFloat 3.5s ease-in-out infinite; font-size: 0.5rem; color: #d4a87a; }

        .photo-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .photo-item {
            position: relative;
            aspect-ratio: 1 / 1;
            border-radius: 14px;
            overflow: hidden;
            cursor: pointer;
            box-shadow: 0 4px 16px rgba(120,80,50,0.08), 0 0 0 1px rgba(210,170,140,0.2);
            transition: all 0.35s cubic-bezier(0.22,0.61,0.36,1);
            background: #fdf6ef;
            -webkit-tap-highlight-color: transparent;
        }
        .photo-item:hover { transform:translateY(-4px); box-shadow:0 10px 28px rgba(140,85,45,0.14),0 0 0 2px rgba(200,150,110,0.35); }
        .photo-item:active { transform:scale(0.97); transition:transform 0.15s ease; }
        .photo-item img { width:100%; height:100%; object-fit:cover; display:block; transition:transform 0.5s ease; }
        .photo-item:hover img { transform:scale(1.06); }
        .photo-overlay {
            position:absolute; inset:0; background:linear-gradient(180deg,transparent 55%,rgba(100,55,30,0.3) 100%);
            opacity:0; transition:opacity 0.35s ease; pointer-events:none;
            display:flex; align-items:flex-end; justify-content:center; padding-bottom:8px;
        }
        .photo-item:hover .photo-overlay { opacity:1; }
        .photo-overlay span { color:#fff; font-size:0.65rem; font-weight:500; letter-spacing:1px; text-shadow:0 1px 3px rgba(0,0,0,0.3); }

        .photo-placeholder {
            position:absolute; inset:0; display:flex; align-items:center; justify-content:center;
            background:linear-gradient(145deg,#f9ece0 0%,#f5e0ce 100%); z-index:-1;
        }
        .photo-placeholder i { font-size:1.8rem; color:#d4b896; opacity:0.6; }
        .photo-item::after {
            content:""; position:absolute; top:6px; right:6px; width:14px; height:14px;
            border-top:2px solid rgba(255,255,255,0.7); border-right:2px solid rgba(255,255,255,0.7);
            border-radius:0 4px 0 0; opacity:0; transition:opacity 0.35s ease; pointer-events:none; z-index:2;
        }
        .photo-item:hover::after { opacity:1; }
        .photo-item img.load-error { display:none; }
        .photo-item img.load-error+.photo-placeholder { z-index:1; }

        .gallery-footer-decoration {
            text-align: center;
            margin-top: 0.3rem;
            font-size: 0.6rem;
            letter-spacing: 3px;
            color: #d4b896;
            opacity: 0.8;
        }

        .simple-bless {
            text-align:center; font-size:0.88rem; color:#b08462; margin:1.3rem 0 0.5rem;
            font-style:italic; letter-spacing:0.5px; line-height:1.7;
        }
        .simple-bless i { color:#d4a87a; margin:0 4px; }

        .footer {
            background:#fbf5ed; text-align:center; padding:1.2rem; font-size:0.73rem;
            color:#b39174; border-top:1px solid #f2e4d5; letter-spacing:0.8px;
        }
        .footer .heart-icon { color:#d4a07a; animation:heartBeat 1.5s ease-in-out infinite; display:inline-block; margin:0 3px; }

        .music-toggle-btn {
            position:fixed; bottom:25px; right:25px; width:48px; height:48px;
            border-radius:50%; background:rgba(255,250,245,0.9); border:1px solid #e5ceb5;
            box-shadow:0 6px 18px rgba(140,90,45,0.12); color:#b1805b; font-size:1.2rem;
            display:flex; align-items:center; justify-content:center; cursor:pointer;
            z-index:10000; backdrop-filter:blur(6px); -webkit-backdrop-filter:blur(6px);
            transition:all 0.3s ease; outline:none;
        }
        .music-toggle-btn:hover {
            background:#fff8ef; border-color:#c89a70;
            box-shadow:0 8px 24px rgba(150,85,40,0.2); transform:scale(1.05);
        }
        .music-toggle-btn.playing {
            background:#fdf0e2; border-color:#d9a87c; color:#8c5a3a;
            animation:musicPulse 2s ease-in-out infinite;
        }
        @keyframes musicPulse {
            0%,100%{box-shadow:0 6px 18px rgba(140,90,45,0.12);}
            50%{box-shadow:0 6px 24px rgba(180,110,60,0.3);}
        }
        .music-toggle-btn i { transition:transform 0.3s ease; }
        .music-toggle-btn.playing i { animation:noteBounce 0.8s ease-in-out infinite; }
        @keyframes noteBounce {
            0%,100%{transform:translateY(0);} 50%{transform:translateY(-3px);}
        }

        .toast {
            position:fixed; bottom:85px; right:25px; transform:translateY(80px);
            background:#5a3c28; color:#fff; padding:10px 22px; border-radius:30px;
            font-size:0.8rem; z-index:10001; pointer-events:none; opacity:0;
            transition:all 0.4s cubic-bezier(0.22,0.61,0.36,1);
            letter-spacing:0.5px; box-shadow:0 8px 24px rgba(0,0,0,0.2); white-space:nowrap;
        }
        .toast.show { opacity:1; transform:translateY(0); }

        @media (max-width:600px) {
            body{padding:0.6rem;}
            .content{padding:1.6rem 1.3rem 1.5rem;}
            .couple-names{font-size:2.3rem; letter-spacing:2px;}
            .ampersand{font-size:2rem;}
            .core-value{font-size:1.25rem;}
            .time-number{font-size:1.35rem;}
            .time-block{min-width:50px; padding:0.4rem 0.5rem; border-radius:14px;}
            .address-line{font-size:0.95rem;}
            .hero{height:230px;}
            .ring-icon-outer{width:110px; height:110px;}
            .ring-icon-outer i{font-size:2.6rem;}
            .hero::before{font-size:100px; left:-20px; top:10px;}
            .hero::after{font-size:90px; right:-15px; bottom:0;}
            .music-toggle-btn{width:42px; height:42px; bottom:20px; right:20px; font-size:1rem;}
            .toast{bottom:75px; right:20px; font-size:0.7rem; padding:8px 18px;}
            .photo-grid{gap:8px;}
            .photo-item{border-radius:10px;}
            .photo-item::after{top:5px; right:5px; width:12px; height:12px; border-radius:0 3px 0 0;}
            .gallery-toggle-btn{font-size:0.75rem; padding:6px 14px;}
        }
    </style>
</head>
<body>
    <!-- 背景音乐：齐晨 - 咱们结婚吧 -->
    <audio id="bgm" loop preload="auto">
        <source src="https://github.com/ywd0378/Marriage_Invitation/raw/85aeb7571df5f3081e1df60a9a64909523dc8665/mp3/%E9%BD%90%E6%99%A8%20-%20%E5%92%B1%E4%BB%AC%E7%BB%93%E5%A9%9A%E5%90%A7.mp3" type="audio/mpeg">
        您的浏览器不支持音频播放。
    </audio>

    <button id="musicToggle" class="music-toggle-btn" title="播放背景音乐"><i class="fas fa-music"></i></button>
    <div class="toast" id="musicToast"></div>
    <canvas id="petalsCanvas" aria-hidden="true"></canvas>

    <div class="invitation-wrapper">
        <div class="hero">
            <div class="hero-glow glow-1"></div><div class="hero-glow glow-2"></div><div class="hero-glow glow-3"></div>
            <span class="sparkle">✦</span><span class="sparkle">✧</span><span class="sparkle">·</span>
            <span class="sparkle">✦</span><span class="sparkle">✧</span><span class="sparkle">·</span>
            <div class="ring-container"><div class="ring-icon-outer"><i class="fas fa-ring"></i></div></div>
        </div>
        <div class="content">
            <div class="invite-title">
                <span class="pre-title">携手共度 · 喜结良缘</span>
                <div class="couple-names">杨文达 <span class="ampersand">&</span> 孙智琴</div>
                <div class="date-badge"><i class="far fa-calendar-alt"></i> 2026年5月26日 · 良辰吉日</div>
            </div>
            <div class="divider"><i class="fas fa-feather-alt"></i> · Invitation · <i class="fas fa-feather-alt"></i></div>
            <div class="core-info-card">
                <div class="core-date-time">
                    <span class="core-label"><i class="far fa-clock"></i> 吉日良辰</span>
                    <span class="core-value">2026年5月26日（周二）</span>
                </div>
                <div class="address-section">
                    <div class="address-line">📍 通许县 · 西水沃</div>
                    <div class="address-detail">河南省开封市通许县西水沃</div>
                    <div class="action-buttons">
                        <a href="#" class="map-link-single" id="unifiedMapBtn"><i class="fas fa-map-marker-alt"></i> 查看地图 & 导航</a>
                        <button class="btn-calendar" id="addToCalendarBtn"><i class="far fa-calendar-plus"></i> 添加到日历</button>
                    </div>
                </div>
            </div>
            <div class="countdown">
                <h4><i class="far fa-heart"></i> 距离婚礼还有 <i class="far fa-heart"></i></h4>
                <div class="timer" id="timerContainer">
                    <div class="time-block"><span class="time-number" id="days">00</span><div class="time-label">天</div></div>
                    <div class="time-block"><span class="time-number" id="hours">00</span><div class="time-label">时</div></div>
                    <div class="time-block"><span class="time-number" id="minutes">00</span><div class="time-label">分</div></div>
                    <div class="time-block"><span class="time-number" id="seconds">00</span><div class="time-label">秒</div></div>
                </div>
            </div>

            <!-- 下拉照片墙触发按钮 -->
            <button id="galleryToggle" class="gallery-toggle-btn">
                <i class="fas fa-images"></i> 查看我们的甜蜜瞬间 <i class="fas fa-chevron-down"></i>
            </button>

            <!-- 可折叠的照片墙 -->
            <div class="photo-gallery-wrapper" id="photoGalleryWrapper">
                <div class="photo-gallery">
                    <!-- 第1组：初见 -->
                    <div class="photo-group">
                        <div class="group-title"><i class="fas fa-heart"></i> 初见 <span class="sparkle-icon">✦</span></div>
                        <div class="photo-grid" id="group1"></div>
                    </div>
                    <!-- 第2组：心动 -->
                    <div class="photo-group">
                        <div class="group-title"><i class="fas fa-heart"></i> 心动 <span class="sparkle-icon">✦</span></div>
                        <div class="photo-grid" id="group2"></div>
                    </div>
                    <!-- 第3组：约定 -->
                    <div class="photo-group">
                        <div class="group-title"><i class="fas fa-heart"></i> 约定 <span class="sparkle-icon">✦</span></div>
                        <div class="photo-grid" id="group3"></div>
                    </div>
                    <!-- 第4组：永恒 -->
                    <div class="photo-group">
                        <div class="group-title"><i class="fas fa-heart"></i> 永恒 <span class="sparkle-icon">✦</span></div>
                        <div class="photo-grid" id="group4"></div>
                    </div>
                    <div class="gallery-footer-decoration">✦ 每一个瞬间 · 都是爱的印记 ✦</div>
                </div>
            </div>

            <div class="simple-bless"><i class="fas fa-feather"></i> 诚邀您莅临，见证我们的幸福时刻 <i class="fas fa-feather"></i></div>
        </div>
        <div class="footer"><span class="heart-icon">♥</span> 与爱同行 · 杨文达 & 孙智琴 敬邀 <span class="heart-icon">♥</span></div>
    </div>

    <!-- 照片查看器（灯箱） -->
    <div id="photoViewer" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,0.9);z-index:10002;align-items:center;justify-content:center;cursor:pointer;" onclick="closePhotoViewer()">
        <img id="photoViewerImg" src="" alt="照片大图" style="max-width:92vw;max-height:88vh;border-radius:12px;box-shadow:0 20px 60px rgba(0,0,0,0.5);object-fit:contain;transition:transform 0.3s ease;">
        <button style="position:absolute;top:20px;right:25px;background:rgba(255,255,255,0.15);border:1px solid rgba(255,255,255,0.3);color:#fff;font-size:1.5rem;width:44px;height:44px;border-radius:50%;cursor:pointer;backdrop-filter:blur(4px);z-index:10003;" onclick="event.stopPropagation();closePhotoViewer();" title="关闭"><i class="fas fa-times"></i></button>
    </div>

    <script>
        (function() {
            // ==================== 背景音乐控制 ====================
            const bgm = document.getElementById('bgm');
            const musicToggle = document.getElementById('musicToggle');
            const musicToast = document.getElementById('musicToast');
            let musicPlaying = false;

            function showToast(msg) {
                if(!musicToast) return;
                musicToast.textContent = msg;
                musicToast.classList.add('show');
                clearTimeout(musicToast._timeout);
                musicToast._timeout = setTimeout(() => musicToast.classList.remove('show'), 2200);
            }

            function toggleMusic() {
                if(bgm.paused) {
                    bgm.play().then(() => {
                        musicPlaying = true;
                        musicToggle.classList.add('playing');
                        musicToggle.innerHTML = '<i class="fas fa-volume-up"></i>';
                        musicToggle.title = '暂停音乐';
                        showToast('🎵 咱们结婚吧 ~');
                    }).catch(() => showToast('⚠️ 音乐播放失败，请点击按钮重试'));
                } else {
                    bgm.pause();
                    musicPlaying = false;
                    musicToggle.classList.remove('playing');
                    musicToggle.innerHTML = '<i class="fas fa-music"></i>';
                    musicToggle.title = '播放背景音乐';
                    showToast('音乐已暂停');
                }
            }
            musicToggle?.addEventListener('click', toggleMusic);

            let autoplayAttempted = false;
            function attemptAutoplay() {
                if(autoplayAttempted || musicPlaying) return;
                autoplayAttempted = true;
                bgm.play().then(() => {
                    musicPlaying = true;
                    musicToggle.classList.add('playing');
                    musicToggle.innerHTML = '<i class="fas fa-volume-up"></i>';
                    musicToggle.title = '暂停音乐';
                }).catch(() => {});
            }
            document.addEventListener('click', attemptAutoplay, { once: true });
            document.addEventListener('touchstart', attemptAutoplay, { once: true });

            // ==================== 照片墙折叠/展开 ====================
            const galleryToggle = document.getElementById('galleryToggle');
            const galleryWrapper = document.getElementById('photoGalleryWrapper');
            let galleryExpanded = false;

            galleryToggle?.addEventListener('click', () => {
                galleryExpanded = !galleryExpanded;
                if (galleryExpanded) {
                    galleryWrapper.classList.add('expanded');
                    galleryToggle.classList.add('expanded');
                    galleryToggle.querySelector('.fa-chevron-down')?.classList.replace('fa-chevron-down', 'fa-chevron-up');
                } else {
                    galleryWrapper.classList.remove('expanded');
                    galleryToggle.classList.remove('expanded');
                    galleryToggle.querySelector('.fa-chevron-up')?.classList.replace('fa-chevron-up', 'fa-chevron-down');
                }
            });

            // ==================== 照片数据（16张真实照片，分4组） ====================
            // GitHub raw 直链：将 /blob/ 替换为 /raw/
            const groupPhotos = [
                // 第1组：初见
                [
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/1/19.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/1/27.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/1/28.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/1/3.jpg'
                ],
                // 第2组：心动
                [
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/2/20.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/2/21.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/2/22.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/2/5.jpg'
                ],
                // 第3组：约定
                [
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/3/14.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/3/15.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/3/23.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/3/24.jpg'
                ],
                // 第4组：永恒
                [
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/4/16.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/4/17.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/4/25.jpg',
                    'https://github.com/ywd0378/Marriage_Invitation/raw/main/photo/4/26.jpg'
                ]
            ];

            // 存储所有照片URL用于灯箱（扁平化）
            const allPhotos = groupPhotos.flat();

            // 生成照片HTML并插入对应组
            const groupContainers = [
                document.getElementById('group1'),
                document.getElementById('group2'),
                document.getElementById('group3'),
                document.getElementById('group4')
            ];

            groupPhotos.forEach((photos, groupIndex) => {
                const container = groupContainers[groupIndex];
                if (!container) return;
                let html = '';
                photos.forEach((src, idx) => {
                    const globalIndex = groupIndex * 4 + idx;
                    html += `
                        <div class="photo-item" title="点击查看大图" onclick="openPhotoViewer(${globalIndex})">
                            <img src="${src}" alt="甜蜜瞬间" loading="lazy" onerror="this.classList.add('load-error')">
                            <div class="photo-placeholder"><i class="fas fa-heart"></i></div>
                            <div class="photo-overlay"><span>❤</span></div>
                        </div>`;
                });
                container.innerHTML = html;
            });

            // ==================== 照片灯箱 ====================
            const photoViewer = document.getElementById('photoViewer');
            const photoViewerImg = document.getElementById('photoViewerImg');

            window.openPhotoViewer = function(index) {
                if (photoViewer && photoViewerImg && allPhotos[index]) {
                    photoViewerImg.src = allPhotos[index];
                    photoViewer.style.display = 'flex';
                    document.body.style.overflow = 'hidden';
                    photoViewerImg.style.transform = 'scale(0.9)';
                    requestAnimationFrame(() => { photoViewerImg.style.transform = 'scale(1)'; });
                }
            };

            window.closePhotoViewer = function() {
                if (photoViewer) {
                    photoViewer.style.display = 'none';
                    document.body.style.overflow = '';
                    if (photoViewerImg) {
                        photoViewerImg.src = '';
                        photoViewerImg.style.transform = 'scale(0.9)';
                    }
                }
            };

            document.addEventListener('keydown', (e) => {
                if (e.key === 'Escape' && photoViewer && photoViewer.style.display === 'flex') {
                    closePhotoViewer();
                }
            });

            // ==================== 花瓣飘落动画 ====================
            const canvas = document.getElementById('petalsCanvas');
            const ctx = canvas.getContext('2d');
            let petals = [], animationId, canvasWidth, canvasHeight;
            const petalColors = ['#f9d5c8','#fce4d6','#fad4c0','#fff0e8','#fde0d0','#f8cfba','#ffede0','#fbe0cc','#fef5ec','#fcdbc8','#f9e0d0','#fff5ed'];
            function resizeCanvas() { canvasWidth=window.innerWidth; canvasHeight=document.documentElement.scrollHeight; canvas.width=canvasWidth; canvas.height=canvasHeight; }
            function createPetal() { return { x:Math.random()*canvasWidth, y:-30-Math.random()*120, size:8+Math.random()*20, speedY:0.6+Math.random()*2.2, speedX:-0.5+Math.random()*1.0, rotation:Math.random()*Math.PI*2, rotationSpeed:(Math.random()-0.5)*0.03, opacity:0.4+Math.random()*0.5, color:petalColors[Math.floor(Math.random()*petalColors.length)], wobbleAmp:0.3+Math.random()*1.2, wobbleSpeed:0.01+Math.random()*0.03, wobbleOffset:Math.random()*Math.PI*2 }; }
            function drawPetal(p) { ctx.save(); ctx.translate(p.x,p.y); ctx.rotate(p.rotation); ctx.globalAlpha=p.opacity; ctx.fillStyle=p.color; ctx.beginPath(); ctx.ellipse(0,0,p.size*0.55,p.size,0,0,Math.PI*2); ctx.fill(); ctx.fillStyle='rgba(255,255,255,0.25)'; ctx.beginPath(); ctx.ellipse(p.size*0.55*0.25,-p.size*0.2,p.size*0.55*0.35,p.size*0.3,0.3,0,Math.PI*2); ctx.fill(); ctx.restore(); }
            function initPetals(count) { petals=[]; for(let i=0;i<count;i++){ let p=createPetal(); p.y=Math.random()*canvasHeight; petals.push(p); } }
            function animatePetals() { ctx.clearRect(0,0,canvasWidth,canvasHeight); for(let p of petals) { p.y+=p.speedY; p.x+=p.speedX+Math.sin(p.wobbleOffset+p.y*p.wobbleSpeed)*p.wobbleAmp; p.rotation+=p.rotationSpeed; p.wobbleOffset+=0.005; if(p.y>canvasHeight+40){p.y=-30-Math.random()*50; p.x=Math.random()*canvasWidth;} if(p.x<-40)p.x=canvasWidth+30; if(p.x>canvasWidth+40)p.x=-30; drawPetal(p); } animationId=requestAnimationFrame(animatePetals); }
            resizeCanvas(); initPetals(canvasWidth<500?35:55); animationId=requestAnimationFrame(animatePetals);
            window.addEventListener('resize',()=>{ clearTimeout(window._resizeTimer); window._resizeTimer=setTimeout(()=>{ resizeCanvas(); let c=canvasWidth<500?35:55; while(petals.length<c) petals.push(createPetal()); while(petals.length>c) petals.pop(); },200); });
            window.addEventListener('scroll',()=>{ clearTimeout(window._scrollTimer); window._scrollTimer=setTimeout(()=>{ let h=document.documentElement.scrollHeight; if(h!==canvasHeight){canvasHeight=h; canvas.height=h;} },150); },{passive:true});

            // ==================== 倒计时 ====================
            const wedding = new Date(2026,4,26,11,30,0);
            function updateCountdown() {
                const dist = wedding.getTime()-Date.now();
                const dEl=document.getElementById('days'),hEl=document.getElementById('hours'),mEl=document.getElementById('minutes'),sEl=document.getElementById('seconds');
                const title=document.querySelector('.countdown h4');
                if(dist<0){ if(dEl)dEl.innerText='00'; if(hEl)hEl.innerText='00'; if(mEl)mEl.innerText='00'; if(sEl)sEl.innerText='00'; if(title)title.innerHTML='<i class="far fa-smile"></i> 礼成 · 永结同心 <i class="far fa-smile"></i>'; return; }
                const d=Math.floor(dist/86400000),h=Math.floor((dist%86400000)/3600000),m=Math.floor((dist%3600000)/60000),s=Math.floor((dist%60000)/1000);
                if(dEl)dEl.innerText=d<10?'0'+d:d; if(hEl)hEl.innerText=h<10?'0'+h:h; if(mEl)mEl.innerText=m<10?'0'+m:m; if(sEl)sEl.innerText=s<10?'0'+s:s;
            }
            updateCountdown(); setInterval(updateCountdown,1000);

            document.getElementById('unifiedMapBtn')?.addEventListener('click',e=>{ e.preventDefault(); window.open('https://uri.amap.com/search?keyword='+encodeURIComponent('河南省开封市通许县西水沃')+'&callnative=1','_blank'); });
            document.getElementById('addToCalendarBtn')?.addEventListener('click',()=>{
                const s=new Date(2026,4,26,11,30,0),e=new Date(2026,4,26,15,0,0);
                const fmt=d=>{ const p=n=>String(n).padStart(2,'0'); return `${d.getFullYear()}${p(d.getMonth()+1)}${p(d.getDate())}T${p(d.getHours())}${p(d.getMinutes())}${p(d.getSeconds())}`; };
                const ics=['BEGIN:VCALENDAR','VERSION:2.0','PRODID:-//Wedding//CN','CALSCALE:GREGORIAN','METHOD:PUBLISH','BEGIN:VEVENT',`DTSTART:${fmt(s)}`,`DTEND:${fmt(e)}`,'SUMMARY:杨文达 & 孙智琴 婚礼','DESCRIPTION:杨文达与孙智琴的婚礼庆典\\n地点：河南省开封市通许县西水沃\\n诚挚邀请您莅临见证幸福时刻！','LOCATION:河南省开封市通许县西水沃','TRANSP:OPAQUE','BEGIN:VALARM','TRIGGER:-PT1D','ACTION:DISPLAY','DESCRIPTION:明天是杨文达 & 孙智琴的婚礼！','END:VALARM','END:VEVENT','END:VCALENDAR'].join('\r\n');
                const b=new Blob([ics],{type:'text/calendar;charset=utf-8'});
                const u=URL.createObjectURL(b); const a=document.createElement('a'); a.href=u; a.download='杨文达_孙智琴_婚礼邀请.ics';
                document.body.appendChild(a); a.click(); document.body.removeChild(a); URL.revokeObjectURL(u);
                showToast('✅ 日历已下载，请打开文件添加');
            });

            console.log('💐 杨文达 & 孙智琴 婚礼邀请函已就绪 | 音乐：咱们结婚吧 | 照片墙：16张/4组');
        })();
    </script>
</body>
</html>
