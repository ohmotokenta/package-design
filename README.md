<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>缶ワインパッケージデザイン選定戦略</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Markodwn Parser for AI responses -->
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <style>
        /* Custom Font */
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&display=swap');
        body {
            font-family: 'Noto Sans JP', sans-serif;
            background-color: #F3F4F6;
            color: #2E294E;
        }

        /* Palette Classes */
        .text-primary { color: #D90368; }
        .bg-primary { background-color: #D90368; }
        .border-primary { border-color: #D90368; }
        .hover-bg-primary:hover { background-color: #b00254; }
        
        .text-secondary { color: #2E294E; }
        .bg-secondary { background-color: #2E294E; }
        
        .text-accent { color: #FFD400; }
        .bg-accent { background-color: #FFD400; }
        .hover-bg-accent:hover { background-color: #e6bf00; }

        /* Chart Container Rules - MANDATORY */
        .chart-container {
            position: relative;
            width: 100%;
            margin-left: auto;
            margin-right: auto;
            height: 350px; /* Base height */
            max-height: 400px;
        }

        /* Responsive adjustments for chart containers */
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }

        /* Flowchart Connector Line */
        .flow-line::after {
            content: '';
            position: absolute;
            top: 100%;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 2rem;
            background-color: #cbd5e1;
            z-index: 0;
        }
        .last-step::after {
            display: none;
        }
        
        /* Markdown Styles for AI Output */
        .markdown-body h1, .markdown-body h2, .markdown-body h3 { font-weight: bold; margin-bottom: 0.5em; margin-top: 1em; color: #2E294E; }
        .markdown-body ul { list-style-type: disc; padding-left: 1.5em; margin-bottom: 1em; }
        .markdown-body p { margin-bottom: 0.8em; }
        .markdown-body strong { color: #D90368; }
    </style>
    <!-- 
        NO SVG USED.
        NO MERMAID JS USED.
        Palette: Vibrant Berry & Night (#D90368, #2E294E, #FFD400)
    -->
</head>
<body class="antialiased">

    <!-- Header Section -->
    <header class="bg-secondary text-white py-12 px-4 shadow-lg">
        <div class="max-w-6xl mx-auto text-center">
            <h1 class="text-3xl md:text-5xl font-bold mb-4">缶ワイン パッケージデザイン選定戦略</h1>
            <p class="text-lg md:text-xl opacity-90">
                市場トレンドから最終決定まで：成功するデザイン選定のロードマップ
            </p>
            <div class="mt-6 inline-block bg-primary px-6 py-2 rounded-full font-bold shadow-md">
                PROJECT: CANNED WINE LAUNCH
            </div>
        </div>
    </header>

    <!-- Main Content Grid -->
    <main class="max-w-6xl mx-auto p-6 grid grid-cols-1 md:grid-cols-2 gap-8 -mt-8">

        <!-- SECTION 1: Market Context -->
        <section class="col-span-1 md:col-span-2 bg-white rounded-lg shadow-md p-6 md:p-8">
            <h2 class="text-2xl font-bold text-secondary mb-4 border-l-4 border-primary pl-4">1. 市場背景とデザインの重要性</h2>
            <p class="mb-6 text-gray-600 leading-relaxed">
                選定プロセスに入る前に、なぜパッケージデザインが重要なのかを理解する必要があります。缶ワイン市場は急成長しており、若年層を中心とした新規顧客の獲得競争が激化しています。デザインは「味」以上に最初の購入動機を決定づける要因です。
            </p>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Stat Card -->
                <div class="bg-gray-50 p-6 rounded-lg text-center border-t-4 border-primary">
                    <div class="text-sm text-gray-500 font-bold uppercase tracking-wide">市場成長率 (予測)</div>
                    <div class="text-4xl font-bold text-secondary mt-2">13.2%</div>
                    <div class="text-sm text-gray-400 mt-1">CAGR (年平均成長率)</div>
                </div>
                <!-- Chart Area -->
                <div class="md:col-span-2">
                    <div class="chart-container">
                        <canvas id="marketChart"></canvas>
                    </div>
                    <p class="text-xs text-gray-400 mt-2 text-center">※ データは市場予測に基づくイメージです</p>
                </div>
            </div>
        </section>

        <!-- SECTION 2: Concept & Keywords -->
        <section class="col-span-1 bg-white rounded-lg shadow-md p-6">
            <h2 class="text-2xl font-bold text-secondary mb-4 border-l-4 border-primary pl-4">2. コンセプトキーワード設定</h2>
            <p class="mb-4 text-gray-600 text-sm">
                デザイン選定の「軸」となるキーワードを定義します。ターゲット（ペルソナ）に刺さる感情的価値と言語的価値をレーダーチャートで可視化し、デザインの方向性を定めます。
            </p>
            <div class="bg-blue-50 p-4 rounded mb-4">
                <h3 class="font-bold text-secondary mb-2">主要ペルソナ: 30代 アクティブ・ミレニアル</h3>
                <ul class="text-sm text-gray-700 list-disc list-inside">
                    <li>アウトドアやホームパーティを好む</li>
                    <li>「手軽さ」と「本格感」の両立を求める</li>
                    <li>環境配慮（サステナブル）に関心が高い</li>
                </ul>
            </div>
            <div class="chart-container">
                <canvas id="conceptRadarChart"></canvas>
            </div>
            <p class="text-xs text-gray-400 mt-2">
                <span class="inline-block w-3 h-3 bg-primary rounded-full mr-1"></span>目標イメージ
                <span class="inline-block w-3 h-3 bg-gray-300 rounded-full mr-1 ml-2"></span>競合平均
            </p>
        </section>

        <!-- SECTION 3: Selection Workflow -->
        <section class="col-span-1 bg-white rounded-lg shadow-md p-6">
            <h2 class="text-2xl font-bold text-secondary mb-4 border-l-4 border-primary pl-4">3. 選定フロー (進め方)</h2>
            <p class="mb-6 text-gray-600 text-sm">
                デザイン選定を円滑に進めるための5ステップです。直感に頼らず、ロジックと客観的データに基づいて絞り込みを行います。
            </p>
            
            <div class="flex flex-col space-y-0">
                <!-- Step 1 -->
                <div class="relative pb-8 pl-8 border-l-2 border-gray-200 flow-line">
                    <div class="absolute -left-2.5 top-0 w-5 h-5 rounded-full bg-secondary text-white flex items-center justify-center text-xs font-bold">1</div>
                    <h4 class="font-bold text-lg text-secondary">リサーチ & コンセプト策定</h4>
                    <p class="text-sm text-gray-500">競合調査、ターゲット設定、キーワード定義 (Keyword: Casual, Premium)</p>
                </div>

                <!-- Step 2 -->
                <div class="relative pb-8 pl-8 border-l-2 border-gray-200 flow-line">
                    <div class="absolute -left-2.5 top-0 w-5 h-5 rounded-full bg-secondary text-white flex items-center justify-center text-xs font-bold">2</div>
                    <h4 class="font-bold text-lg text-secondary">ラフデザイン作成 (3-5案)</h4>
                    <p class="text-sm text-gray-500">方向性の異なる案を作成（例：イラスト重視、タイポグラフィ重視、シンプル）</p>
                </div>

                <!-- Step 3 -->
                <div class="relative pb-8 pl-8 border-l-2 border-gray-200 flow-line">
                    <div class="absolute -left-2.5 top-0 w-5 h-5 rounded-full bg-primary text-white flex items-center justify-center text-xs font-bold">3</div>
                    <h4 class="font-bold text-lg text-primary">社内スクリーニング</h4>
                    <p class="text-sm text-gray-500">「ブランド適合性」と「実現可能性」で2案まで絞り込み</p>
                </div>

                <!-- Step 4 -->
                <div class="relative pb-8 pl-8 border-l-2 border-gray-200 flow-line">
                    <div class="absolute -left-2.5 top-0 w-5 h-5 rounded-full bg-secondary text-white flex items-center justify-center text-xs font-bold">4</div>
                    <h4 class="font-bold text-lg text-secondary">消費者調査 (A/Bテスト)</h4>
                    <p class="text-sm text-gray-500">ターゲット層による実査。視認性、購入意向のスコア化</p>
                </div>

                <!-- Step 5 -->
                <div class="relative pl-8 border-l-0 last-step">
                    <div class="absolute -left-2.5 top-0 w-5 h-5 rounded-full bg-accent text-secondary flex items-center justify-center text-xs font-bold">5</div>
                    <h4 class="font-bold text-lg text-secondary">最終決定 & 入稿</h4>
                    <p class="text-sm text-gray-500">法規チェック、色校正を経てフィニッシュ</p>
                </div>
            </div>
        </section>

        <!-- SECTION 4: Evaluation Criteria -->
        <section class="col-span-1 md:col-span-2 bg-white rounded-lg shadow-md p-6 md:p-8">
            <h2 class="text-2xl font-bold text-secondary mb-4 border-l-4 border-primary pl-4">4. 選考基準と重み付け</h2>
            <p class="mb-6 text-gray-600">
                デザインを評価する際は、以下の5つの基準を用います。特に「店頭での視認性（シェルフ・インパクト）」と「ブランドイメージの伝達」は最重要項目です。
            </p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                <div class="chart-container">
                    <canvas id="criteriaChart"></canvas>
                </div>
                <div class="bg-gray-50 p-6 rounded-lg">
                    <h3 class="font-bold text-lg mb-4 text-secondary">チェックポイント解説</h3>
                    <ul class="space-y-4">
                        <li class="flex items-start">
                            <span class="text-2xl mr-2">👀</span>
                            <div>
                                <strong class="block text-sm text-secondary">視認性 (Visibility)</strong>
                                <span class="text-xs text-gray-500">2メートル離れた場所から商品名が読めるか？競合の中で埋もれないか？</span>
                            </div>
                        </li>
                        <li class="flex items-start">
                            <span class="text-2xl mr-2">💡</span>
                            <div>
                                <strong class="block text-sm text-secondary">世界観 (Brand Story)</strong>
                                <span class="text-xs text-gray-500">ターゲットの「飲用シーン」を想起させるか？高級感/カジュアル感のバランス。</span>
                            </div>
                        </li>
                        <li class="flex items-start">
                            <span class="text-2xl mr-2">ℹ️</span>
                            <div>
                                <strong class="block text-sm text-secondary">情報伝達 (Information)</strong>
                                <span class="text-xs text-gray-500">品種（赤・白・泡）、産地、アルコール度数が直感的に分かるか？</span>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- SECTION 5: Research Example -->
        <section class="col-span-1 md:col-span-2 bg-secondary text-white rounded-lg shadow-lg p-6 md:p-8">
            <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-6">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-2 border-l-4 border-accent pl-4">5. 選定メソッド：消費者調査データの活用例</h2>
                    <p class="text-gray-300 text-sm">最終選考に残った「案A（モダン）」と「案B（クラシック）」のA/Bテスト結果イメージ。</p>
                </div>
                <div class="mt-4 md:mt-0 bg-white/10 px-4 py-2 rounded backdrop-blur-sm">
                    <span class="text-accent font-bold">Winner:</span> Design A
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Comparative Chart -->
                <div class="chart-container">
                    <canvas id="abTestChart"></canvas>
                </div>
                
                <!-- Insight Text -->
                <div class="flex flex-col justify-center space-y-6">
                    <div class="bg-white/10 p-4 rounded border-l-4 border-primary">
                        <h4 class="font-bold text-lg mb-1">💡 データからの洞察</h4>
                        <p class="text-sm text-gray-200">
                            「案A」は<strong class="text-accent">20代〜30代の購入意向が圧倒的に高い</strong>結果となりました。
                            「案B」は高級感のスコアが高いものの、「日常的に飲みたいか？」という質問に対しスコアが低迷。
                            ターゲット戦略に基づき、今回は「案A」を採用すべきと判断できます。
                        </p>
                    </div>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <div class="text-center">
                            <div class="text-3xl font-bold text-accent">68%</div>
                            <div class="text-xs text-gray-400">案A 支持率</div>
                        </div>
                        <div class="text-center">
                            <div class="text-3xl font-bold text-gray-400">32%</div>
                            <div class="text-xs text-gray-500">案B 支持率</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SECTION 6: Gemini AI Integration -->
        <section class="col-span-1 md:col-span-2 bg-white rounded-lg shadow-md p-6 md:p-8 border-2 border-accent/20">
            <div class="flex items-center gap-2 mb-4">
                <h2 class="text-2xl font-bold text-secondary border-l-4 border-primary pl-4">6. AI Design Lab (Powered by Gemini)</h2>
                <span class="text-2xl">✨</span>
            </div>
            <p class="mb-6 text-gray-600">
                Gemini APIを活用して、あなたのデザインアイデアを「30代アクティブ・ミレニアル」の視点から評価したり、魅力的なキャッチコピーを生成したりできます。
            </p>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Feature A: Design Critique -->
                <div class="bg-gray-50 p-6 rounded-lg border border-gray-200">
                    <h3 class="font-bold text-lg text-primary mb-3">🎨 デザイン案のAI評価</h3>
                    <p class="text-sm text-gray-500 mb-4">デザインの特徴（色、モチーフ、雰囲気など）を入力すると、ペルソナへの適合度をAIが診断します。</p>
                    
                    <textarea id="designInput" class="w-full p-3 border rounded mb-4 text-sm focus:ring-2 focus:ring-primary outline-none" rows="4" placeholder="例：シルバーの缶にネオンピンクの幾何学模様。ロゴは太字のサンセリフ体で、全体的にサイバーパンクな雰囲気。"></textarea>
                    
                    <button onclick="analyzeDesign()" id="analyzeBtn" class="w-full bg-secondary text-white py-2 rounded font-bold hover:bg-gray-700 transition flex items-center justify-center gap-2">
                        <span>✨ AIで診断する</span>
                    </button>
                    
                    <div id="designResult" class="mt-4 hidden p-4 bg-white rounded border border-gray-200 text-sm markdown-body"></div>
                </div>

                <!-- Feature B: Copywriting -->
                <div class="bg-gray-50 p-6 rounded-lg border border-gray-200">
                    <h3 class="font-bold text-lg text-primary mb-3">✍️ キャッチコピー生成</h3>
                    <p class="text-sm text-gray-500 mb-4">キーワードを入力して、ターゲットに刺さるキャッチコピー案を3つ生成します。</p>
                    
                    <div class="mb-4">
                        <label class="block text-xs text-gray-500 mb-1">キーワード (カンマ区切り)</label>
                        <input type="text" id="keywordInput" class="w-full p-2 border rounded text-sm focus:ring-2 focus:ring-primary outline-none" placeholder="例：週末, アウトドア, 爽快感" value="週末, アウトドア, 爽快感">
                    </div>

                    <button onclick="generateCopy()" id="copyBtn" class="w-full bg-primary text-white py-2 rounded font-bold hover-bg-primary transition flex items-center justify-center gap-2">
                        <span>✨ コピーを生成する</span>
                    </button>
                    
                    <div id="copyResult" class="mt-4 hidden p-4 bg-white rounded border border-gray-200 text-sm markdown-body"></div>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-gray-400 py-8 mt-12 text-center text-sm">
        <p>Generated by Canvas Infographics - Strategic Design Assistant</p>
    </footer>

    <!-- JavaScript for Gemini API -->
    <script>
        const apiKey = ""; // System provides the key

        async function callGemini(prompt, resultElementId, buttonId) {
            const resultDiv = document.getElementById(resultElementId);
            const button = document.getElementById(buttonId);
            const originalBtnText = button.innerHTML;

            // Loading State
            button.disabled = true;
            button.innerHTML = '<span class="animate-spin">↻</span> 生成中...';
            resultDiv.classList.remove('hidden');
            resultDiv.innerHTML = '<p class="text-gray-400 animate-pulse">AIが思考中...</p>';

            try {
                const response = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`, {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify({
                        contents: [{
                            parts: [{ text: prompt }]
                        }]
                    })
                });

                if (!response.ok) {
                    throw new Error(`API Error: ${response.status}`);
                }

                const data = await response.json();
                const aiText = data.candidates[0].content.parts[0].text;
                
                // Parse Markdown and display
                resultDiv.innerHTML = marked.parse(aiText);

            } catch (error) {
                console.error(error);
                resultDiv.innerHTML = `<p class="text-red-500">エラーが発生しました: ${error.message}</p>`;
            } finally {
                button.disabled = false;
                button.innerHTML = originalBtnText;
            }
        }

        function analyzeDesign() {
            const input = document.getElementById('designInput').value;
            if (!input.trim()) {
                alert("デザインの説明を入力してください");
                return;
            }

            const prompt = `
                あなたはプロのパッケージデザイナー兼マーケターです。
                現在、「30代のアクティブなミレニアル世代」をターゲットにした「缶ワイン」のデザインプロジェクトを進めています。
                プロジェクトのキーワードは「カジュアル」「プレミアム感」「アウトドア」「手軽さ」です。
                
                以下のユーザーが考案したデザイン案に対して、ターゲット層に受けるかどうかを評価し、改善アドバイスをしてください。
                出力はMarkdown形式で、以下の構成にしてください：
                1. **総合評価スコア** (10点満点)
                2. **良い点** (箇条書き)
                3. **懸念点・改善アドバイス** (具体的に)

                ユーザーのデザイン案: "${input}"
            `;
            
            callGemini(prompt, 'designResult', 'analyzeBtn');
        }

        function generateCopy() {
            const keywords = document.getElementById('keywordInput').value;
            if (!keywords.trim()) {
                alert("キーワードを入力してください");
                return;
            }

            const prompt = `
                あなたは優秀なコピーライターです。
                「30代のアクティブなミレニアル世代」に向けた、新しい「缶ワイン」の発売キャンペーン用キャッチコピーを3つ考えてください。
                
                入力されたキーワード: "${keywords}"
                
                要件:
                - 短く、リズム感が良いこと
                - 「手軽さ」と「本格的な味」のギャップを感じさせること
                - Markdownのリスト形式で出力すること
                - 各コピーの下に、なぜその言葉を選んだかの短い解説をつけること
            `;

            callGemini(prompt, 'copyResult', 'copyBtn');
        }
    </script>

    <!-- JavaScript for Charts (Existing Logic) -->
    <script>
        // --- Utility Function: Label Splitter (16 char limit) ---
        function splitLabel(label) {
            if (typeof label !== 'string' || label.length <= 16) return label;
            const words = label.split(' ');
            const lines = [];
            let currentLine = words[0];

            for (let i = 1; i < words.length; i++) {
                if ((currentLine + ' ' + words[i]).length <= 16) {
                    currentLine += ' ' + words[i];
                } else {
                    lines.push(currentLine);
                    currentLine = words[i];
                }
            }
            lines.push(currentLine);
            return lines;
        }

        // --- Global Chart Defaults for Tooltips ---
        Chart.defaults.plugins.tooltip.callbacks.title = function(tooltipItems) {
            const item = tooltipItems[0];
            let label = item.chart.data.labels[item.dataIndex];
            if (Array.isArray(label)) {
                return label.join(' ');
            } else {
                return label;
            }
        };
        Chart.defaults.font.family = "'Noto Sans JP', sans-serif";
        Chart.defaults.color = '#4B5563';

        // --- 1. Market Growth Chart (Line) ---
        const ctxMarket = document.getElementById('marketChart').getContext('2d');
        new Chart(ctxMarket, {
            type: 'line',
            data: {
                labels: ['2020', '2021', '2022', '2023', '2024(予)', '2025(予)'],
                datasets: [{
                    label: '缶ワイン市場規模 (億円)',
                    data: [15, 22, 35, 52, 70, 95],
                    borderColor: '#D90368', // Berry Pink
                    backgroundColor: 'rgba(217, 3, 104, 0.1)',
                    borderWidth: 3,
                    pointBackgroundColor: '#FFD400', // Yellow Accent
                    pointRadius: 5,
                    fill: true,
                    tension: 0.4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { display: true, position: 'top' },
                    tooltip: { mode: 'index', intersect: false }
                },
                scales: {
                    y: { beginAtZero: true, grid: { color: '#e5e7eb' } },
                    x: { grid: { display: false } }
                }
            }
        });

        // --- 2. Concept Radar Chart ---
        const ctxRadar = document.getElementById('conceptRadarChart').getContext('2d');
        const radarLabels = ['カジュアル (Casual)', '高級感 (Premium)', '視認性 (Impact)', '環境配慮 (Eco)', 'SNS映え (Photogenic)'];
        
        new Chart(ctxRadar, {
            type: 'radar',
            data: {
                labels: radarLabels.map(l => splitLabel(l)),
                datasets: [{
                    label: '目標コンセプト',
                    data: [90, 60, 95, 80, 85],
                    borderColor: '#D90368',
                    backgroundColor: 'rgba(217, 3, 104, 0.2)',
                    pointBackgroundColor: '#D90368',
                    borderWidth: 2
                }, {
                    label: '市場平均 (競合)',
                    data: [60, 50, 60, 40, 50],
                    borderColor: '#9CA3AF',
                    backgroundColor: 'rgba(156, 163, 175, 0.1)',
                    pointBackgroundColor: '#9CA3AF',
                    borderWidth: 1,
                    borderDash: [5, 5]
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    r: {
                        angleLines: { color: '#e5e7eb' },
                        grid: { color: '#e5e7eb' },
                        pointLabels: {
                            font: { size: 11, weight: 'bold' },
                            color: '#2E294E'
                        },
                        suggestedMin: 0,
                        suggestedMax: 100
                    }
                }
            }
        });

        // --- 3. Criteria Weight Chart (Horizontal Bar) ---
        const ctxCriteria = document.getElementById('criteriaChart').getContext('2d');
        const criteriaLabels = [
            '店頭での視認性 (Shelf Impact)', 
            'ブランド世界観の伝達 (Brand Fit)', 
            '情報の読みやすさ (Legibility)', 
            '印刷コスト効率 (Cost Efficiency)', 
            'シリーズ展開のしやすさ (Scalability)'
        ];

        new Chart(ctxCriteria, {
            type: 'bar',
            data: {
                labels: criteriaLabels.map(l => splitLabel(l)),
                datasets: [{
                    label: '重要度スコア (Weight)',
                    data: [95, 85, 70, 60, 50],
                    backgroundColor: [
                        '#D90368', // Highest priority
                        '#D90368',
                        '#2E294E',
                        '#2E294E',
                        '#9CA3AF'
                    ],
                    borderRadius: 4
                }]
            },
            options: {
                indexAxis: 'y', // Horizontal bar
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { display: false }
                },
                scales: {
                    x: { beginAtZero: true, max: 100 }
                }
            }
        });

        // --- 4. A/B Test Result (Grouped Bar / Stacked) ---
        const ctxAB = document.getElementById('abTestChart').getContext('2d');
        new Chart(ctxAB, {
            type: 'bar',
            data: {
                labels: ['総合評価', '購入意向', '視認性', '高級感'],
                datasets: [
                    {
                        label: '案A (モダン・ポップ)',
                        data: [4.5, 4.8, 4.7, 3.2],
                        backgroundColor: '#FFD400', // Yellow (Accent)
                        borderColor: '#ffffff',
                        borderWidth: 1
                    },
                    {
                        label: '案B (クラシック)',
                        data: [3.2, 2.9, 3.5, 4.6],
                        backgroundColor: 'rgba(255, 255, 255, 0.3)', // Translucent White
                        borderColor: '#ffffff',
                        borderWidth: 1
                    }
                ]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { labels: { color: 'white' } },
                    tooltip: {
                        backgroundColor: '#2E294E',
                        titleColor: '#FFD400'
                    }
                },
                scales: {
                    y: {
                        beginAtZero: true,
                        max: 5,
                        grid: { color: 'rgba(255,255,255,0.1)' },
                        ticks: { color: 'white' }
                    },
                    x: {
                        grid: { display: false },
                        ticks: { color: 'white' }
                    }
                }
            }
        });
    </script>
</body>
</html>
