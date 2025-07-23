<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>昭和の歴史クイズ</title>
    <style>
        body {
            font-family: 'Hiragino Kaku Gothic Pro', 'ヒラギノ角ゴ Pro W3', Meiryo, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }
        .container {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
        h1 {
            text-align: center;
            color: #2c3e50;
            margin-bottom: 30px;
            font-size: 2.2em;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        .question {
            margin-bottom: 25px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 10px;
            border-left: 5px solid #3498db;
        }
        .question h3 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.1em;
        }
        .options {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        .option {
            display: flex;
            align-items: center;
            padding: 10px;
            background: white;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        .option:hover {
            background: #e3f2fd;
            transform: translateX(5px);
        }
        .option input[type="radio"] {
            margin-right: 10px;
            transform: scale(1.2);
        }
        .option.selected {
            background: #e3f2fd;
            border-color: #2196f3;
        }
        .submit-btn {
            display: block;
            width: 200px;
            margin: 30px auto;
            padding: 15px;
            background: linear-gradient(45deg, #4CAF50, #45a049);
            color: white;
            border: none;
            border-radius: 25px;
            font-size: 1.1em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.3);
        }
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(76, 175, 80, 0.4);
        }
        .result {
            margin-top: 30px;
            padding: 25px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        .score {
            font-size: 2.5em;
            font-weight: bold;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        .message {
            font-size: 1.2em;
            margin-bottom: 15px;
        }
        .correct-answers {
            background: rgba(255,255,255,0.1);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            text-align: left;
        }
        .correct-answers h4 {
            color: #fff;
            margin-bottom: 15px;
            text-align: center;
        }
        .answer-item {
            margin: 8px 0;
            padding: 5px 0;
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }
        .question-number {
            background: #3498db;
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-weight: bold;
            margin-right: 10px;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>📚 昭和の歴史クイズ</h1>
        
        <form id="quizForm">
            <!-- 問題1 -->
            <div class="question">
                <h3><span class="question-number">1</span>昭和天皇が即位したのは何年？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q1" value="a">1924年</label>
                    <label class="option"><input type="radio" name="q1" value="b">1926年</label>
                    <label class="option"><input type="radio" name="q1" value="c">1928年</label>
                </div>
            </div>

            <!-- 問題2 -->
            <div class="question">
                <h3><span class="question-number">2</span>1929年に起こった世界恐慌の影響で、日本で起こった経済危機は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q2" value="a">昭和恐慌</label>
                    <label class="option"><input type="radio" name="q2" value="b">大正恐慌</label>
                    <label class="option"><input type="radio" name="q2" value="c">平成恐慌</label>
                </div>
            </div>

            <!-- 問題3 -->
            <div class="question">
                <h3><span class="question-number">3</span>1931年に起こった満州事変のきっかけとなった事件は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q3" value="a">盧溝橋事件</label>
                    <label class="option"><input type="radio" name="q3" value="b">柳条湖事件</label>
                    <label class="option"><input type="radio" name="q3" value="c">張作霖爆殺事件</label>
                </div>
            </div>

            <!-- 問題4 -->
            <div class="question">
                <h3><span class="question-number">4</span>1932年に起こった5・15事件で暗殺された総理大臣は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q4" value="a">犬養毅</label>
                    <label class="option"><input type="radio" name="q4" value="b">浜口雄幸</label>
                    <label class="option"><input type="radio" name="q4" value="c">原敬</label>
                </div>
            </div>

            <!-- 問題5 -->
            <div class="question">
                <h3><span class="question-number">5</span>1936年に起こった2・26事件の中心となった軍人グループは？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q5" value="a">統制派</label>
                    <label class="option"><input type="radio" name="q5" value="b">皇道派</label>
                    <label class="option"><input type="radio" name="q5" value="c">国粋派</label>
                </div>
            </div>

            <!-- 問題6 -->
            <div class="question">
                <h3><span class="question-number">6</span>1937年に日中戦争が本格化するきっかけとなった事件は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q6" value="a">盧溝橋事件</label>
                    <label class="option"><input type="radio" name="q6" value="b">上海事変</label>
                    <label class="option"><input type="radio" name="q6" value="c">満州事変</label>
                </div>
            </div>

            <!-- 問題7 -->
            <div class="question">
                <h3><span class="question-number">7</span>1940年に日本が締結した軍事同盟は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q7" value="a">日独伊三国同盟</label>
                    <label class="option"><input type="radio" name="q7" value="b">日独同盟</label>
                    <label class="option"><input type="radio" name="q7" value="c">日独伊西四国同盟</label>
                </div>
            </div>

            <!-- 問題8 -->
            <div class="question">
                <h3><span class="question-number">8</span>太平洋戦争開戦時の総理大臣は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q8" value="a">近衛文麿</label>
                    <label class="option"><input type="radio" name="q8" value="b">東條英機</label>
                    <label class="option"><input type="radio" name="q8" value="c">広田弘毅</label>
                </div>
            </div>

            <!-- 問題9 -->
            <div class="question">
                <h3><span class="question-number">9</span>真珠湾攻撃が行われたのは何年？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q9" value="a">1940年</label>
                    <label class="option"><input type="radio" name="q9" value="b">1941年</label>
                    <label class="option"><input type="radio" name="q9" value="c">1942年</label>
                </div>
            </div>

            <!-- 問題10 -->
            <div class="question">
                <h3><span class="question-number">10</span>1942年に行われたミッドウェー海戦の結果は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q10" value="a">日本の大勝利</label>
                    <label class="option"><input type="radio" name="q10" value="b">引き分け</label>
                    <label class="option"><input type="radio" name="q10" value="c">日本の大敗北</label>
                </div>
            </div>

            <!-- 問題11 -->
            <div class="question">
                <h3><span class="question-number">11</span>1945年8月6日に原爆が投下された都市は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q11" value="a">広島</label>
                    <label class="option"><input type="radio" name="q11" value="b">長崎</label>
                    <label class="option"><input type="radio" name="q11" value="c">東京</label>
                </div>
            </div>

            <!-- 問題12 -->
            <div class="question">
                <h3><span class="question-number">12</span>1945年8月15日の天皇の終戦の詔書は何と呼ばれた？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q12" value="a">玉音放送</label>
                    <label class="option"><input type="radio" name="q12" value="b">終戦放送</label>
                    <label class="option"><input type="radio" name="q12" value="c">降伏放送</label>
                </div>
            </div>

            <!-- 問題13 -->
            <div class="question">
                <h3><span class="question-number">13</span>戦後の占領政策を統括した連合国軍最高司令官は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q13" value="a">アイゼンハワー</label>
                    <label class="option"><input type="radio" name="q13" value="b">マッカーサー</label>
                    <label class="option"><input type="radio" name="q13" value="c">ニミッツ</label>
                </div>
            </div>

            <!-- 問題14 -->
            <div class="question">
                <h3><span class="question-number">14</span>1947年に施行された日本国憲法の三大原理は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q14" value="a">国民主権・基本的人権の尊重・平和主義</label>
                    <label class="option"><input type="radio" name="q14" value="b">民主主義・自由主義・平等主義</label>
                    <label class="option"><input type="radio" name="q14" value="c">立憲主義・法治主義・民主主義</label>
                </div>
            </div>

            <!-- 問題15 -->
            <div class="question">
                <h3><span class="question-number">15</span>1950年に勃発した戦争により日本経済が好転したのは？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q15" value="a">ベトナム戦争</label>
                    <label class="option"><input type="radio" name="q15" value="b">朝鮮戦争</label>
                    <label class="option"><input type="radio" name="q15" value="c">中東戦争</label>
                </div>
            </div>

            <!-- 問題16 -->
            <div class="question">
                <h3><span class="question-number">16</span>1951年に調印されたサンフランシスコ講和条約の首席全権は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q16" value="a">吉田茂</label>
                    <label class="option"><input type="radio" name="q16" value="b">岸信介</label>
                    <label class="option"><input type="radio" name="q16" value="c">鳩山一郎</label>
                </div>
            </div>

            <!-- 問題17 -->
            <div class="question">
                <h3><span class="question-number">17</span>1955年に保守合同により結成された政党は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q17" value="a">自由党</label>
                    <label class="option"><input type="radio" name="q17" value="b">民主党</label>
                    <label class="option"><input type="radio" name="q17" value="c">自由民主党</label>
                </div>
            </div>

            <!-- 問題18 -->
            <div class="question">
                <h3><span class="question-number">18</span>1960年に起こった安保闘争の対象となった条約は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q18" value="a">日米安全保障条約</label>
                    <label class="option"><input type="radio" name="q18" value="b">日米友好条約</label>
                    <label class="option"><input type="radio" name="q18" value="c">日米通商条約</label>
                </div>
            </div>

            <!-- 問題19 -->
            <div class="question">
                <h3><span class="question-number">19</span>1964年に開催された東京オリンピックの開会式はいつ？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q19" value="a">10月10日</label>
                    <label class="option"><input type="radio" name="q19" value="b">10月12日</label>
                    <label class="option"><input type="radio" name="q19" value="c">10月15日</label>
                </div>
            </div>

            <!-- 問題20 -->
            <div class="question">
                <h3><span class="question-number">20</span>1968年に起こった大学紛争で特に有名になった大学は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q20" value="a">早稲田大学</label>
                    <label class="option"><input type="radio" name="q20" value="b">東京大学</label>
                    <label class="option"><input type="radio" name="q20" value="c">慶應義塾大学</label>
                </div>
            </div>

            <!-- 問題21 -->
            <div class="question">
                <h3><span class="question-number">21</span>1970年に開催された万国博覧会の会場は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q21" value="a">東京</label>
                    <label class="option"><input type="radio" name="q21" value="b">大阪</label>
                    <label class="option"><input type="radio" name="q21" value="c">名古屋</label>
                </div>
            </div>

            <!-- 問題22 -->
            <div class="question">
                <h3><span class="question-number">22</span>1972年に日中国交正常化を実現した総理大臣は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q22" value="a">田中角栄</label>
                    <label class="option"><input type="radio" name="q22" value="b">佐藤栄作</label>
                    <label class="option"><input type="radio" name="q22" value="c">三木武夫</label>
                </div>
            </div>

            <!-- 問題23 -->
            <div class="question">
                <h3><span class="question-number">23</span>1973年に起こった石油危機（オイルショック）の原因は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q23" value="a">第四次中東戦争</label>
                    <label class="option"><input type="radio" name="q23" value="b">イラン革命</label>
                    <label class="option"><input type="radio" name="q23" value="c">湾岸戦争</label>
                </div>
            </div>

            <!-- 問題24 -->
            <div class="question">
                <h3><span class="question-number">24</span>1976年に起こったロッキード事件で逮捕された元総理大臣は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q24" value="a">田中角栄</label>
                    <label class="option"><input type="radio" name="q24" value="b">三木武夫</label>
                    <label class="option"><input type="radio" name="q24" value="c">福田赳夫</label>
                </div>
            </div>

            <!-- 問題25 -->
            <div class="question">
                <h3><span class="question-number">25</span>1980年代前半の「不沈艦」発言で知られる総理大臣は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q25" value="a">鈴木善幸</label>
                    <label class="option"><input type="radio" name="q25" value="b">中曽根康弘</label>
                    <label class="option"><input type="radio" name="q25" value="c">竹下登</label>
                </div>
            </div>

            <!-- 問題26 -->
            <div class="question">
                <h3><span class="question-number">26</span>1985年に調印されたプラザ合意の結果、円はどうなった？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q26" value="a">円安</label>
                    <label class="option"><input type="radio" name="q26" value="b">円高</label>
                    <label class="option"><input type="radio" name="q26" value="c">変化なし</label>
                </div>
            </div>

            <!-- 問題27 -->
            <div class="question">
                <h3><span class="question-number">27</span>1986年に起こったチェルノブイリ原発事故の影響を日本で最も受けた産業は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q27" value="a">農業</label>
                    <label class="option"><input type="radio" name="q27" value="b">漁業</label>
                    <label class="option"><input type="radio" name="q27" value="c">工業</label>
                </div>
            </div>

            <!-- 問題28 -->
            <div class="question">
                <h3><span class="question-number">28</span>1987年に利上げを開始し、バブル経済の抑制を図った日銀総裁は？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q28" value="a">三重野康</label>
                    <label class="option"><input type="radio" name="q28" value="b">澄田智</label>
                    <label class="option"><input type="radio" name="q28" value="c">前川春雄</label>
                </div>
            </div>

            <!-- 問題29 -->
            <div class="question">
                <h3><span class="question-number">29</span>昭和64年は何日間続いた？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q29" value="a">6日間</label>
                    <label class="option"><input type="radio" name="q29" value="b">7日間</label>
                    <label class="option"><input type="radio" name="q29" value="c">8日間</label>
                </div>
            </div>

            <!-- 問題30 -->
            <div class="question">
                <h3><span class="question-number">30</span>昭和天皇が崩御され、平成に改元されたのは？</h3>
                <div class="options">
                    <label class="option"><input type="radio" name="q30" value="a">1989年1月7日</label>
                    <label class="option"><input type="radio" name="q30" value="b">1989年1月8日</label>
                    <label class="option"><input type="radio" name="q30" value="c">1989年1月9日</label>
                </div>
            </div>

            <button type="button" class="submit-btn" onclick="calculateScore()">結果を見る</button>
        </form>

        <div id="result" class="result" style="display: none;">
            <div class="score" id="scoreDisplay"></div>
            <div class="message" id="message"></div>
            <div class="correct-answers">
                <h4>🔍 正解一覧</h4>
                <div id="answers"></div>
            </div>
        </div>
    </div>

    <script>
        // 正解データ
        const correctAnswers = {
            q1: 'b', q2: 'a', q3: 'b', q4: 'a', q5: 'b',
            q6: 'a', q7: 'a', q8: 'b', q9: 'b', q10: 'c',
            q11: 'a', q12: 'a', q13: 'b', q14: 'a', q15: 'b',
            q16: 'a', q17: 'c', q18: 'a', q19: 'a', q20: 'b',
            q21: 'b', q22: 'a', q23: 'a', q24: 'a', q25: 'b',
            q26: 'b', q27: 'a', q28: 'a', q29: 'b', q30: 'b'
        };

        const answerTexts = {
            q1: '1926年（大正15年12月25日に即位）',
            q2: '昭和恐慌',
            q3: '柳条湖事件',
            q4: '犬養毅',
            q5: '皇道派',
            q6: '盧溝橋事件',
            q7: '日独伊三国同盟',
            q8: '東條英機',
            q9: '1941年',
            q10: '日本の大敗北',
            q11: '広島',
            q12: '玉音放送',
            q13: 'マッカーサー',
            q14: '国民主権・基本的人権の尊重・平和主義',
            q15: '朝鮮戦争',
            q16: '吉田茂',
            q17: '自由民主党',
            q18: '日米安全保障条約',
            q19: '10月10日',
            q20: '東京大学',
            q21: '大阪',
            q22: '田中角栄',
            q23: '第四次中東戦争',
            q24: '田中角栄',
            q25: '中曽根康弘',
            q26: '円高',
            q27: '農業',
            q28: '三重野康',
            q29: '7日間',
            q30: '1989年1月8日'
        };

        // ラジオボタン選択時のスタイル変更
        document.addEventListener('change', function(e) {
            if (e.target.type === 'radio') {
                const questionDiv = e.target.closest('.question');
                const options = questionDiv.querySelectorAll('.option');
                options.forEach(option => option.classList.remove('selected'));
                e.target.closest('.option').classList.add('selected');
            }
        });

        function calculateScore() {
            const form = document.getElementById('quizForm');
            const formData = new FormData(form);
            let score = 0;
            let totalQuestions = 30;

            for (let i = 1; i <= totalQuestions; i++) {
                const answer = formData.get(`q${i}`);
                if (answer === correctAnswers[`q${i}`]) {
                    score++;
                }
            }

            displayResult(score, totalQuestions);
        }

        function displayResult(score, total) {
            const percentage = Math.round((score / total) * 100);
            const scoreDisplay = document.getElementById('scoreDisplay');
            const message = document.getElementById('message');
            const answersDiv = document.getElementById('answers');
            
            scoreDisplay.textContent = `${score} / ${total}点`;
            
            let messageText = '';
            if (percentage >= 90) {
                messageText = '🎉 素晴らしい！昭和史の専門家レベルです！';
            } else if (percentage >= 80) {
                messageText = '👏 とても良くできました！昭和史に詳しいですね！';
            } else if (percentage >= 70) {
                messageText = '😊 なかなか良い成績です！';
            } else if (percentage >= 60) {
                messageText = '📚 もう少し勉強すれば更に良くなりそうです';
            } else {
                messageText = '💪 昭和史の復習をしてみましょう！';
            }
            
            message.textContent = `${messageText} (正答率: ${percentage}%)`;
            
            // 正解一覧を表示
            let answersHTML = '';
            for (let i = 1; i <= total; i++) {
                answersHTML += `<div class="answer-item">問${i}: ${answerTexts[`q${i}`]}</div>`;
            }
            answersDiv.innerHTML = answersHTML;
            
            document.getElementById('result').style.display = 'block';
            document.getElementById('result').scrollIntoView({ behavior: 'smooth' });
        }
    </script>
</body>
</html>
