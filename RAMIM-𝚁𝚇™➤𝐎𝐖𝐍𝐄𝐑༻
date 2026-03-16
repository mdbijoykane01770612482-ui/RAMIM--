<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
    <title>RAMIM-𝚁𝚇™➤𝐎𝐖𝐍𝐄𝐑༻ AI</title>
    <style>
        :root {
            --primary-glow: #00E5FF;
            --secondary-glow: #B400FF;
            --accent-glow: #FF0055;
            --text-highlight: #FFFFFF;
            --win-green: #00FF88;
            --loss-red: #FF1744;
            --glass-bg: rgba(8, 5, 18, 0.85);
        }

        * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
        body { height: 100vh; overflow: hidden; background: #030105; font-family: 'Poppins', sans-serif; }
        iframe { position: absolute; inset: 0; width: 100%; height: 100%; border: none; z-index: 1; }

        /* Draggable Container */
        #core {
            position: fixed;
            right: 20px;
            top: 100px;
            width: 280px;
            z-index: 99999;
            filter: drop-shadow(0 15px 30px rgba(0,0,0,0.9));
            touch-action: none; 
        }

        #timerPill {
            position: absolute;
            top: -22px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(135deg, #0a0514, #150a26);
            color: var(--primary-glow);
            border: 1px solid var(--primary-glow);
            padding: 6px 24px;
            border-radius: 50px;
            font-weight: 900;
            font-size: 17px;
            box-shadow: 0 0 15px rgba(0, 229, 255, 0.4);
            z-index: 101;
            display: flex;
            align-items: center;
        }

        .timer-icon { margin-right: 6px; font-size: 14px; animation: pulseBeat 1s infinite; }
        @keyframes pulseBeat { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.2); } }

        #panel { display: none; }

        #login {
            position: relative;
            padding: 30px 20px;
            border-radius: 20px;
            background: var(--glass-bg);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            overflow: hidden;
        }

        #login::before {
            content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%;
            background: conic-gradient(transparent, var(--primary-glow), transparent 30%, var(--secondary-glow), transparent 60%, var(--accent-glow));
            animation: rotateBorder 4s linear infinite; z-index: -1;
        }
        #login::after { content: ''; position: absolute; inset: 2px; background: var(--glass-bg); border-radius: 18px; z-index: -1; }
        @keyframes rotateBorder { 100% { transform: rotate(360deg); } }

        .brand-title {
            background: linear-gradient(to right, var(--primary-glow), var(--text-highlight), var(--primary-glow));
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            font-size: 22px; font-weight: 900; letter-spacing: 2px; margin-bottom: 5px;
        }

        .subtitle { color: var(--accent-glow); font-size: 11px; font-weight: 700; letter-spacing: 2px; margin-bottom: 25px; text-transform: uppercase; }
        
        .inp { 
            width: 100%; height: 48px; background: rgba(0, 0, 0, 0.6); 
            border: 1px solid var(--primary-glow); border-radius: 12px; 
            color: #fff; text-align: center; margin-bottom: 18px; 
            outline: none; touch-action: auto !important;
        }
        
        .btn { width: 100%; height: 48px; border: none; border-radius: 12px; background: linear-gradient(45deg, var(--secondary-glow), var(--accent-glow)); color: #fff; font-weight: 900; cursor: pointer; }

        .admin-link {
            display: inline-block;
            margin-top: 15px;
            color: #fff;
            text-decoration: none;
            font-size: 11px;
            background: rgba(255, 255, 255, 0.05);
            padding: 5px 15px;
            border-radius: 50px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: 0.3s;
            touch-action: auto !important;
        }

        /* Device Locked Alert */
        #custom-alert {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 90%;
            max-width: 400px;
            background: #000;
            border: 2px solid #ff0000;
            border-radius: 15px;
            padding: 30px 20px;
            text-align: center;
            z-index: 200000;
            display: none;
            box-shadow: 0 0 30px rgba(255, 0, 0, 0.4);
        }

        .alert-title { color: #ff0000; font-size: 28px; font-weight: 900; margin-bottom: 15px; }
        .alert-msg { color: #fff; font-size: 16px; font-weight: 500; line-height: 1.5; }

        /* Prediction Interface */
        .stage { position: relative; height: 250px; width: 100%; display: flex; align-items: center; justify-content: center; }
        .orbit-container { position: absolute; width: 220px; height: 220px; animation: spinRings 8s linear infinite; border-radius: 50%; border: 2px dashed rgba(255, 255, 255, 0.15); }
        @keyframes spinRings { to { transform: rotate(360deg); } }
        
        .comet { 
            position: absolute; width: 14px; height: 14px; border-radius: 50%; background: #fff; 
            box-shadow: 0 0 20px currentColor; animation: rgbShift 4s linear infinite;
        }
        @keyframes rgbShift {
            0%, 100% { color: var(--primary-glow); box-shadow: 0 0 15px var(--primary-glow); }
            33% { color: var(--secondary-glow); box-shadow: 0 0 15px var(--secondary-glow); }
            66% { color: var(--accent-glow); box-shadow: 0 0 15px var(--accent-glow); }
        }

        .hexContainer { position: relative; width: 170px; height: 170px; display: flex; align-items: center; justify-content: center; }
        .hexSVG { position: absolute; inset: 0; width: 100%; height: 100%; animation: breathe 2.5s infinite alternate ease-in-out; }
        @keyframes breathe { 0% { transform: scale(0.98); } 100% { transform: scale(1.02); } }

        .content { position: relative; z-index: 10; text-align: center; width: 125px; height: 125px; display: flex; flex-direction: column; align-items: center; justify-content: center; }
        .bs { font-size: 36px; font-weight: 900; line-height: 1.1; margin: 5px 0; }
        .big { color: #fff; text-shadow: 0 0 15px var(--win-green); }
        .small { color: #fff; text-shadow: 0 0 15px var(--loss-red); }
        .period-txt { font-size: 13px; font-weight: 900; color: var(--primary-glow); border: 1px solid var(--primary-glow); padding: 3px 12px; border-radius: 6px; background: rgba(0,0,0,0.5); }
    </style>
</head>
<body>

<iframe src="https://hgnice.bet/#/register?invitationCode=84826526579"></iframe>

<div id="custom-alert">
    <div class="alert-title">⚠️ DEVICE LOCKED ⚠️</div>
    <div class="alert-msg"> 😆 বোকাচোদা আমাদের রেফারে একাউন্ট নাই তোর  সাহারিয়া  ভাইয়ের সাথে যোগাযোগ কর 👇@sahariya_XR👇 </div>
</div>

<div id="core">
    <div id="timerPill">
        <span class="timer-icon">⏳</span>
        <span id="timeVal">00</span>
    </div>

    <div id="login">
        <div class="brand-title">👑RX TEAM👑</div>
        <div class="subtitle">RAMIM-𝚁𝚇™➤𝐎𝐖𝐍𝐄𝐑༻</div>
        <input id="key" class="inp" type="password" placeholder="ENTER KEY">
        <button id="unlockBtn" class="btn">CONNECT SERVER</button>
        <a href="t.me/sahariya_XR" target="_blank" class="admin-link">OWNER:sahariya_XR</a>
    </div>

    <div id="panel">
        <div class="stage">
            <div class="orbit-container">
                <div class="comet" style="top: -7px; left: 50%; transform: translateX(-50%);"></div>
                <div class="comet" style="bottom: -7px; left: 50%; transform: translateX(-50%);"></div>
                <div class="comet" style="left: -7px; top: 50%; transform: translateY(-50%);"></div>
                <div class="comet" style="right: -7px; top: 50%; transform: translateY(-50%);"></div>
            </div>
            <div class="hexContainer">
                <svg class="hexSVG" viewBox="0 0 100 100">
                    <polygon points="50,2 95,25 95,75 50,98 5,75 5,25" fill="rgba(8,5,20,0.85)" stroke="url(#cyberGrad)" stroke-width="2"></polygon>
                    <defs>
                        <linearGradient id="cyberGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                            <stop offset="0%" style="stop-color:var(--primary-glow)"></stop>
                            <stop offset="100%" style="stop-color:var(--accent-glow)"></stop>
                        </linearGradient>
                    </defs>
                </svg>
                <div class="content">
                    <div style="font-size: 10px; color: #aaa;">ANALYSIS</div>
                    <div id="bs" class="bs">WAITING</div>
                    <div class="period-txt" id="p">00:00:00</div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    let isLive = false, lastID = "";
    const api = "https://draw.ar-lottery01.com/WinGo/WinGo_30S/GetHistoryIssuePage.json?pageNo=1&pageSize=10";

    async function updateMarket() {
        if(!isLive) return;
        try {
            const res = await fetch(api);
            const data = await res.json();
            const top = data.data.list[0];
            
            // রিয়েল টাইম ক্লক আপডেট
            const now = new Date();
            const timeStr = now.getHours().toString().padStart(2, '0') + ":" + 
                            now.getMinutes().toString().padStart(2, '0') + ":" + 
                            now.getSeconds().toString().padStart(2, '0');
            document.getElementById('p').innerText = timeStr;

            // পিরিয়ড চেঞ্জ হলে শুধু প্রেডিকশন আপডেট হবে
            if (lastID !== top.issueNumber) {
                const currentBS = parseInt(top.number) >= 5 ? "BIG" : "SMALL";
                const el = document.getElementById('bs');
                el.innerText = currentBS;
                el.className = "bs " + currentBS.toLowerCase();
                lastID = top.issueNumber;
            }
        } catch (e) {}
    }

    document.getElementById('unlockBtn').onclick = () => {
        if(document.getElementById('key').value === "VIPRX") {
            document.getElementById('login').style.display = 'none';
            document.getElementById('panel').style.display = 'block';
            isLive = true; 
            setInterval(() => {
                const now = new Date();
                const rem = 30 - (now.getSeconds() % 30);
                document.getElementById('timeVal').innerText = (rem < 10 ? "0" : "") + rem;
                updateMarket();
            }, 1000);
        } else {
            document.getElementById('custom-alert').style.display = 'block';
            setTimeout(() => document.getElementById('custom-alert').style.display = 'none', 4000);
        }
    };

    // ড্র্যাগিং সিস্টেম
    const core = document.getElementById('core');
    let ox, oy, isDrag = false;

    const start = (e) => {
        if (['INPUT', 'BUTTON', 'A'].includes(e.target.tagName)) return;
        isDrag = true;
        const x = e.touches ? e.touches[0].clientX : e.clientX;
        const y = e.touches ? e.touches[0].clientY : e.clientY;
        ox = x - core.offsetLeft; oy = y - core.offsetTop;
    };

    const move = (e) => {
        if (!isDrag) return;
        const x = e.touches ? e.touches[0].clientX : e.clientX;
        const y = e.touches ? e.touches[0].clientY : e.clientY;
        core.style.left = (x - ox) + 'px'; core.style.top = (y - oy) + 'px'; core.style.right = 'auto';
    };

    core.addEventListener('mousedown', start);
    core.addEventListener('touchstart', start, { passive: true });
    document.addEventListener('mousemove', move);
    document.addEventListener('touchmove', move, { passive: false });
    document.addEventListener('mouseup', () => isDrag = false);
    document.addEventListener('touchend', () => isDrag = false);
</script>

</body>
</html>
