# bio
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>OOO｜個人網路名片</title>

<style>
    *{
        margin:0;
        padding:0;
        box-sizing:border-box;
        font-family: "Segoe UI", sans-serif;
    }

    body{
        background: linear-gradient(135deg,#0f172a,#020617);
        color:white;
        min-height:100vh;
        display:flex;
        justify-content:center;
        align-items:center;
        overflow:hidden;
    }

    /* 背景科技感光圈 */
    body::before,
    body::after{
        content:"";
        position:absolute;
        width:500px;
        height:500px;
        border-radius:50%;
        filter:blur(120px);
        opacity:0.3;
        z-index:0;
    }

    body::before{
        background:#00c6ff;
        top:-150px;
        left:-150px;
    }

    body::after{
        background:#7c3aed;
        bottom:-150px;
        right:-150px;
    }

    .card{
        position:relative;
        z-index:1;
        width:90%;
        max-width:900px;
        background:rgba(255,255,255,0.08);
        border:1px solid rgba(255,255,255,0.15);
        backdrop-filter: blur(15px);
        border-radius:28px;
        padding:50px;
        box-shadow:0 0 30px rgba(0,0,0,0.4);
        animation:fadeIn 1.2s ease;
    }

    .top{
        display:flex;
        align-items:center;
        gap:30px;
        flex-wrap:wrap;
    }

    .avatar{
        width:140px;
        height:140px;
        border-radius:50%;
        background:linear-gradient(135deg,#00d4ff,#7c3aed);
        display:flex;
        justify-content:center;
        align-items:center;
        font-size:55px;
        font-weight:bold;
        box-shadow:0 0 25px rgba(0,212,255,0.5);
    }

    .info h1{
        font-size:3rem;
        margin-bottom:10px;
        letter-spacing:2px;
    }

    .info p{
        color:#cbd5e1;
        margin:8px 0;
        font-size:1rem;
    }

    .info a{
        color:#38bdf8;
        text-decoration:none;
    }

    .info a:hover{
        text-decoration:underline;
    }

    .section{
        margin-top:40px;
    }

    .section h2{
        font-size:1.4rem;
        margin-bottom:18px;
        color:#38bdf8;
        border-left:4px solid #38bdf8;
        padding-left:12px;
    }

    .skills{
        display:flex;
        gap:15px;
        flex-wrap:wrap;
    }

    .skill{
        background:rgba(255,255,255,0.08);
        border:1px solid rgba(255,255,255,0.15);
        padding:12px 20px;
        border-radius:999px;
        transition:0.3s;
    }

    .skill:hover{
        transform:translateY(-4px);
        background:rgba(56,189,248,0.15);
        box-shadow:0 0 15px rgba(56,189,248,0.3);
    }

    .cert-list{
        display:grid;
        grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
        gap:18px;
    }

    .cert{
        background:rgba(255,255,255,0.06);
        border:1px solid rgba(255,255,255,0.12);
        padding:20px;
        border-radius:18px;
        transition:0.3s;
    }

    .cert:hover{
        transform:scale(1.03);
        border-color:#38bdf8;
    }

    footer{
        margin-top:40px;
        text-align:center;
        color:#94a3b8;
        font-size:0.9rem;
    }

    @keyframes fadeIn{
        from{
            opacity:0;
            transform:translateY(30px);
        }
        to{
            opacity:1;
            transform:translateY(0);
        }
    }

    @media(max-width:768px){
        .card{
            padding:35px;
        }

        .info h1{
            font-size:2.2rem;
        }

        .top{
            justify-content:center;
            text-align:center;
        }
    }
</style>
</head>

<body>

<div class="card">

    <div class="top">
        <div class="avatar">O</div>

        <div class="info">
            <h1>OOO</h1>

            <p>💼 專業領域：資訊科技 / 人工智慧</p>

            <p>
                📧 Email：
                <a href="mailto:aaa@abc.com.tw">
                    aaa@abc.com.tw
                </a>
            </p>

            <p>
                🌐 個人網站：
                <a href="https://C112118202.gowp.space" target="_blank">
                    C112118202.gowp.space
                </a>
            </p>
        </div>
    </div>

    <div class="section">
        <h2>專業技能</h2>

        <div class="skills">
            <div class="skill">人工智慧 AI</div>
            <div class="skill">資訊科技 IT</div>
            <div class="skill">HTML / CSS / JavaScript</div>
            <div class="skill">Python</div>
            <div class="skill">資料分析</div>
            <div class="skill">網頁開發</div>
            <div class="skill">系統管理</div>
            <div class="skill">雲端技術</div>
        </div>
    </div>

    <div class="section">
        <h2>專業證照</h2>

        <div class="cert-list">

            <div class="cert">
                <h3>AI 人工智慧應用認證</h3>
                <p>Artificial Intelligence Certification</p>
            </div>

            <div class="cert">
                <h3>資訊安全基礎認證</h3>
                <p>Cyber Security Fundamentals</p>
            </div>

            <div class="cert">
                <h3>Web 開發技術證照</h3>
                <p>Front-End Development</p>
            </div>

            <div class="cert">
                <h3>雲端服務應用證照</h3>
                <p>Cloud Technology Associate</p>
            </div>

        </div>
    </div>

    <footer>
        © 2026 OOO Personal Digital Card
    </footer>

</div>

<script>
    // 卡片滑鼠微動態效果
    const card = document.querySelector(".card");

    document.addEventListener("mousemove", (e) => {
        const x = (window.innerWidth / 2 - e.pageX) / 40;
        const y = (window.innerHeight / 2 - e.pageY) / 40;

        card.style.transform = `rotateY(${x}deg) rotateX(${-y}deg)`;
    });

    document.addEventListener("mouseleave", () => {
        card.style.transform = "rotateY(0deg) rotateX(0deg)";
    });
</script>

</body>
</html>
