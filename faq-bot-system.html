<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>カスタマイズ可能なFAQボット</title>
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .container {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .faq-bot {
            flex: 1;
            min-width: 300px;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 20px;
            background-color: #f9f9f9;
            margin-bottom: 20px;
        }

        .admin-panel {
            flex: 1;
            min-width: 300px;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 20px;
            background-color: #f5f5f5;
        }

        h1, h2 {
            color: #2c3e50;
        }

        .chat-container {
            height: 400px;
            overflow-y: auto;
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 10px;
            margin-bottom: 15px;
            background-color: white;
        }

        .message {
            margin-bottom: 10px;
            padding: 8px 12px;
            border-radius: 18px;
            max-width: 80%;
            word-wrap: break-word;
        }

        .user-message {
            background-color: #e1f5fe;
            margin-left: auto;
            border-bottom-right-radius: 5px;
        }

        .bot-message {
            background-color: #f1f1f1;
            margin-right: auto;
            border-bottom-left-radius: 5px;
        }

        .input-container {
            display: flex;
        }

        input[type="text"] {
            flex: 1;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }

        button {
            padding: 10px 15px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-left: 10px;
            font-size: 16px;
        }

        button:hover {
            background-color: #45a049;
        }

        .faq-item {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 10px;
            margin-bottom: 10px;
        }

        .faq-item input {
            width: 100%;
            margin-bottom: 5px;
        }

        .action-buttons {
            display: flex;
            justify-content: flex-end;
            gap: 10px;
        }

        .delete-btn {
            background-color: #f44336;
        }

        .delete-btn:hover {
            background-color: #d32f2f;
        }

        textarea {
            width: 100%;
            height: 80px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
            margin-bottom: 10px;
            resize: vertical;
        }

        .tabs {
            display: flex;
            margin-bottom: 20px;
        }

        .tab {
            padding: 10px 20px;
            background-color: #ddd;
            cursor: pointer;
            border-radius: 5px 5px 0 0;
            margin-right: 5px;
        }

        .tab.active {
            background-color: #4CAF50;
            color: white;
        }

        .panel {
            display: none;
        }

        .panel.active {
            display: block;
        }

        .save-load-container {
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid #ddd;
        }

        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .faq-bot, .admin-panel {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <h1>カスタマイズ可能なFAQボット</h1>
    
    <div class="container">
        <!-- FAQボット部分 -->
        <div class="faq-bot">
            <h2>FAQ ボット</h2>
            <div class="chat-container" id="chatContainer">
                <div class="message bot-message">こんにちは！質問があればお気軽にどうぞ。</div>
            </div>
            <div class="input-container">
                <input type="text" id="userInput" placeholder="質問を入力してください...">
                <button onclick="sendMessage()">送信</button>
            </div>
        </div>
        
        <!-- 管理パネル部分 -->
        <div class="admin-panel">
            <h2>管理パネル</h2>
            
            <div class="tabs">
                <div class="tab active" onclick="switchTab(this, 'editFaq')">FAQ編集</div>
                <div class="tab" onclick="switchTab(this, 'importExport')">インポート/エクスポート</div>
            </div>
            
            <div class="panel active" id="editFaq">
                <div id="faqList">
                    <!-- FAQリストがここに生成されます -->
                </div>
                <button onclick="addNewFaq()">新規FAQ追加</button>
            </div>
            
            <div class="panel" id="importExport">
                <div class="save-load-container">
                    <h3>FAQデータの保存・読み込み</h3>
                    <button onclick="exportFAQs()">FAQをエクスポート</button>
                    <p>または FAQデータをインポート:</p>
                    <textarea id="importData" placeholder="JSONデータをここに貼り付けてください..."></textarea>
                    <button onclick="importFAQs()">インポート</button>
                </div>
            </div>
        </div>
    </div>

    <script>
        // FAQデータの初期セット
        let faqData = [
            {
                question: "このサービスについて教えてください",
                answer: "これはカスタマイズ可能なFAQボットです。お客様からのよくある質問に自動で回答します。"
            },
            {
                question: "営業時間はいつですか",
                answer: "平日の9時から17時まで営業しています。土日祝日はお休みです。"
            },
            {
                question: "返品ポリシーを知りたいです",
                answer: "商品到着後7日以内であれば、未使用品に限り返品可能です。カスタマーサービスまでご連絡ください。"
            }
        ];

        // ページ読み込み時にローカルストレージからFAQデータを読み込む
        document.addEventListener('DOMContentLoaded', function() {
            const storedData = localStorage.getItem('faqBotData');
            if (storedData) {
                try {
                    faqData = JSON.parse(storedData);
                } catch (e) {
                    console.error('保存されたデータの解析エラー:', e);
                }
            }
            renderFaqList();
        });

        // FAQリストのレンダリング
        function renderFaqList() {
            const faqList = document.getElementById('faqList');
            faqList.innerHTML = '';
            
            faqData.forEach((faq, index) => {
                const faqItem = document.createElement('div');
                faqItem.className = 'faq-item';
                faqItem.innerHTML = `
                    <input type="text" placeholder="質問" value="${faq.question}" onchange="updateFaq(${index}, 'question', this.value)">
                    <textarea placeholder="回答" onchange="updateFaq(${index}, 'answer', this.value)">${faq.answer}</textarea>
                    <div class="action-buttons">
                        <button class="delete-btn" onclick="deleteFaq(${index})">削除</button>
                    </div>
                `;
                faqList.appendChild(faqItem);
            });
            
            // FAQデータをローカルストレージに保存
            saveFaqs();
        }

        // 新規FAQの追加
        function addNewFaq() {
            faqData.push({
                question: "",
                answer: ""
            });
            renderFaqList();
        }

        // FAQの更新
        function updateFaq(index, field, value) {
            faqData[index][field] = value;
            saveFaqs();
        }

        // FAQの削除
        function deleteFaq(index) {
            if (confirm('このFAQを削除してもよろしいですか？')) {
                faqData.splice(index, 1);
                renderFaqList();
            }
        }

        // メッセージ送信処理
        function sendMessage() {
            const userInput = document.getElementById('userInput');
            const chatContainer = document.getElementById('chatContainer');
            const userQuery = userInput.value.trim();
            
            if (userQuery === '') return;
            
            // ユーザーのメッセージを表示
            const userMessageDiv = document.createElement('div');
            userMessageDiv.className = 'message user-message';
            userMessageDiv.textContent = userQuery;
            chatContainer.appendChild(userMessageDiv);
            
            // 回答を検索
            setTimeout(() => {
                const botMessageDiv = document.createElement('div');
                botMessageDiv.className = 'message bot-message';
                
                // FAQ内で質問を検索
                const matchedFaq = findMatchingFaq(userQuery);
                
                if (matchedFaq) {
                    botMessageDiv.textContent = matchedFaq.answer;
                } else {
                    botMessageDiv.textContent = "申し訳ありませんが、その質問についての情報はありません。別の質問をお試しください。";
                }
                
                chatContainer.appendChild(botMessageDiv);
                chatContainer.scrollTop = chatContainer.scrollHeight;
            }, 500);
            
            // 入力フィールドをクリア
            userInput.value = '';
        }

        // FAQで一致するものを検索
        function findMatchingFaq(query) {
            query = query.toLowerCase();
            
            // 完全一致または部分一致を探す
            for (const faq of faqData) {
                if (faq.question.toLowerCase() === query) {
                    return faq; // 完全一致
                }
            }
            
            // キーワードマッチング（より高度な検索が必要な場合はここを拡張）
            for (const faq of faqData) {
                if (faq.question.toLowerCase().includes(query) || 
                    query.includes(faq.question.toLowerCase())) {
                    return faq;
                }
            }
            
            return null; // 一致するものがない
        }

        // タブの切り替え
        function switchTab(clickedTab, tabId) {
            // すべてのタブとパネルから active クラスを削除
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
            });
            document.querySelectorAll('.panel').forEach(panel => {
                panel.classList.remove('active');
            });
            
            // クリックされたタブとそれに対応するパネルに active クラスを追加
            clickedTab.classList.add('active');
            document.getElementById(tabId).classList.add('active');
        }

        // FAQデータのエクスポート
        function exportFAQs() {
            const jsonData = JSON.stringify(faqData, null, 2);
            const blob = new Blob([jsonData], { type: 'application/json' });
            const url = URL.createObjectURL(blob);
            
            const a = document.createElement('a');
            a.href = url;
            a.download = 'faq_data.json';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
        }

        // FAQデータのインポート
        function importFAQs() {
            const importData = document.getElementById('importData').value;
            
            try {
                const newFaqData = JSON.parse(importData);
                if (Array.isArray(newFaqData)) {
                    faqData = newFaqData;
                    renderFaqList();
                    alert('FAQデータを正常にインポートしました！');
                    document.getElementById('importData').value = '';
                } else {
                    alert('無効なデータ形式です。JSONの配列が必要です。');
                }
            } catch (e) {
                alert('JSONデータの解析に失敗しました: ' + e.message);
            }
        }

        // FAQデータの保存
        function saveFaqs() {
            localStorage.setItem('faqBotData', JSON.stringify(faqData));
        }

        // Enterキーで送信
        document.getElementById('userInput').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });
    </script>
</body>
</html>
