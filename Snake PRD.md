貪食蛇遊戲增強版 PRD
一、專案概述
專案名稱：貪食蛇遊戲增強版

一句話描述：一個具有多種遊戲模式、自訂外觀和增強功能的現代化貪食蛇遊戲

版本：2.0.0

二、問題與目標
問題陳述
現有的貪食蛇遊戲功能較為基礎，僅提供經典玩法，缺乏多樣性與創新元素，難以維持玩家的長期興趣。遊戲介面也較為簡樸，缺少視覺吸引力與自訂選項。

目標
在現有代碼基礎上，增加新的遊戲模式與功能，提升遊戲可玩性

改善使用者介面，提供更豐富的視覺回饋與自訂選項

優化遊戲體驗，增加成就系統與社交分享功能

確保遊戲在不同裝置上都有良好的表現

三、目標用戶
用戶特徵
年齡：8-35歲

類型：休閒遊戲玩家、懷舊遊戲愛好者、尋找打發時間應用程式的用戶

使用場景：通勤時、休息時間、短暫等待期間

用戶需求
希望有更多遊戲變化，避免單調重複

想要挑戰不同難度與模式

期望遊戲有視覺吸引力與個人化選項

需要簡單直觀的控制方式

想要追蹤遊戲進度與成就

四、用戶故事
用戶故事1：作為休閒玩家，我想要嘗試不同的遊戲模式，以便獲得新鮮的遊戲體驗

用戶故事2：作為競爭型玩家，我想要挑戰更高的分數與成就，以便與朋友分享比較

用戶故事3：作為視覺導向用戶，我想要自訂遊戲外觀，以便創造個性化的遊戲體驗

五、功能需求與驗收標準
功能1：新增遊戲模式
描述：在現有經典模式基礎上，新增兩種遊戲模式

時間挑戰模式：在限定時間內獲取最高分數

生存模式：隨時間增加障礙物，考驗生存能力

驗收標準（Given/When/Then）：

Given 用戶進入遊戲主選單

When 用戶點擊"模式選擇"按鈕

Then 系統顯示經典模式、時間挑戰模式、生存模式三個選項

When 用戶選擇時間挑戰模式

Then 遊戲開始時顯示倒數計時器，時間結束時遊戲結束

When 用戶選擇生存模式

Then 遊戲每30秒隨機生成一個障礙物，障礙物會阻擋蛇的移動路徑

功能2：成就系統
描述：新增成就系統，記錄玩家的遊戲里程碑

收集成就：吃過所有種類的水果

分數成就：達到特定分數門檻

生存成就：在生存模式下存活特定時間

連擊成就：連續吃到多個水果而不間斷

驗收標準（Given/When/Then）：

Given 玩家達成一項成就條件

When 遊戲進行中

Then 畫面顯示成就解鎖通知，包含成就名稱與圖示

Given 玩家查看成就頁面

When 玩家點擊"成就"按鈕

Then 系統顯示所有成就列表，包括已解鎖與未解鎖成就

功能3：視覺效果增強
描述：增強遊戲視覺效果，增加動畫與粒子效果

水果收集特效：吃到水果時出現粒子爆炸效果

蛇身特效：根據移動速度顯示拖尾效果

炸彈警示效果：炸彈即將消失前閃爍警示

遊戲開始/結束過場動畫

驗收標準（Given/When/Then）：

Given 玩家吃到一個水果

When 蛇頭接觸水果時

Then 水果位置出現粒子爆炸效果，粒子朝不同方向散開

Given 炸彈將在3秒內消失

When 遊戲進行中

Then 炸彈開始閃爍紅色警示效果

Given 遊戲結束

When 蛇碰撞到邊界或自身

Then 蛇身出現破碎粒子效果，畫面淡出轉為遊戲結束畫面

功能4：社交分享功能
描述：新增分數分享功能，允許玩家分享成績到社交平台

分數截圖：生成包含分數、難度和時間的遊戲結果圖片

社交分享：一鍵分享到Twitter、Facebook等平台

分享文字模板：提供多種有趣的分享文案模板

驗收標準（Given/When/Then）：

Given 遊戲結束畫面顯示

When 玩家點擊"分享成績"按鈕

Then 系統生成包含遊戲結果的圖片預覽

When 玩家選擇分享平台

Then 系統開啟對應分享介面，包含預設分享文字與圖片

功能5：音效系統
描述：為遊戲添加音效與背景音樂

背景音樂：可選擇的多種遊戲背景音樂

音效：移動音效、吃水果音效、炸彈音效、遊戲結束音效

音量控制：獨立控制音樂與音效音量

驗收標準（Given/When/Then）：

Given 遊戲進行中

When 玩家移動蛇

Then 播放輕微的移動音效

Given 玩家吃到水果

When 蛇頭接觸水果時

Then 播放對應水果的收集音效

Given 玩家進入設定頁面

When 玩家調整音量滑桿

Then 對應的音量即時改變，並可聽到預覽音效

六、技術約束
必須遵守
基於現有HTML5 Canvas實作，保持純前端解決方案

維持對現代瀏覽器的兼容性（Chrome、Firefox、Safari、Edge最新版本）

保持遊戲檔案輕量，載入時間不超過3秒

確保遊戲在行動裝置與桌機上都能順暢執行

兼容性要求
支援鍵盤控制（WASD/方向鍵）

響應式設計，支援最小320px寬度的行動裝置

離線可用，所有資源本地載入

支援觸控操作（未來擴展）

不要做
不引入大型遊戲引擎或框架

不實作需要伺服器端的多人遊戲功能（本版本）

不實作需要付費的解鎖內容

不實作過於複雜的控制方案（保持簡單直觀）

七、現有代碼分析與擴展點
現有代碼提供了一個功能完整的貪食蛇遊戲基礎，包含：

基本遊戲循環與繪製系統

多種水果與炸彈機制

難度選擇系統

簡單的皮膚自訂功能

本地分數儲存

擴展點：

遊戲模式切換：在init()函數中增加模式參數

成就系統：新增achievements物件，與localStorage整合

視覺特效：在drawGame()函數中增加特效繪製層

音效系統：新增Audio物件管理與控制

社交分享：使用Canvas.toDataURL()生成分享圖片

技術架構建議：

將遊戲邏輯與繪製邏輯進一步分離

建立統一的遊戲狀態管理物件

實作事件驅動系統處理遊戲事件（吃水果、觸發炸彈等）

建立配置檔案管理遊戲參數

現有代碼

<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>貪食蛇增強版 - 多模式挑戰</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            user-select: none;
            -webkit-user-select: none;
        }
        
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: #fff;
            padding: 10px;
            overflow: hidden;
        }
        
        .header {
            text-align: center;
            margin-bottom: 15px;
        }
        
        h1 {
            font-size: 2rem;
            margin-bottom: 5px;
            color: #4dff91;
            text-shadow: 0 0 10px rgba(77, 255, 145, 0.5);
        }
        
        .subtitle {
            font-size: 1rem;
            color: #a0a0c0;
        }
        
        .game-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            width: 100%;
            max-width: 600px;
        }
        
        .game-info {
            display: flex;
            justify-content: space-between;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.3);
            padding: 10px 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .info-box {
            text-align: center;
            min-width: 80px;
        }
        
        .score-label { font-size: 0.9rem; color: #a0a0c0; }
        .score { font-size: 1.8rem; font-weight: bold; color: #4dff91; }
        .time-label { font-size: 0.9rem; color: #a0a0c0; }
        .time { font-size: 1.5rem; font-weight: bold; color: #4d9fff; }
        
        .game-board-container {
            position: relative;
            width: 100%;
            background-color: transparent; 
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        #gameCanvas {
            border-radius: 10px;
            background-color: #0f3460;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            display: block;
            border: 4px solid rgba(255, 77, 77, 0.3);
        }

        .shake {
            border: 4px solid red !important;
            animation: shake 0.5s;
        }

        @keyframes shake {
            0% { transform: translate(1px, 1px) rotate(0deg); }
            10% { transform: translate(-1px, -2px) rotate(-1deg); }
            20% { transform: translate(-3px, 0px) rotate(1deg); }
            30% { transform: translate(3px, 2px) rotate(0deg); }
            40% { transform: translate(1px, -1px) rotate(1deg); }
            50% { transform: translate(-1px, 2px) rotate(-1deg); }
            60% { transform: translate(-3px, 1px) rotate(0deg); }
            70% { transform: translate(3px, 1px) rotate(-1deg); }
            80% { transform: translate(-1px, -1px) rotate(1deg); }
            90% { transform: translate(1px, 2px) rotate(0deg); }
            100% { transform: translate(1px, -2px) rotate(-1deg); }
        }
        
        /* 模式選擇器 */
        .mode-selector {
            display: flex;
            justify-content: center;
            gap: 5px;
            width: 100%;
            margin-bottom: 5px;
            flex-wrap: wrap;
        }
        
        .mode-btn {
            flex: 1;
            padding: 8px 5px;
            font-size: 0.85rem;
            background-color: #6c63ff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            min-width: 70px;
        }
        
        .mode-btn.active { background-color: #ff9a4d; }

        .difficulty-selector {
            display: flex;
            justify-content: center;
            gap: 5px;
            width: 100%;
            margin-bottom: 5px;
            flex-wrap: wrap;
        }
        
        .difficulty-btn {
            flex: 1;
            padding: 8px 5px;
            font-size: 0.85rem;
            background-color: #4d9fff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            min-width: 60px;
        }
        
        .difficulty-btn.active { background-color: #ff9a4d; }

        .skin-selector {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 5px;
            width: 100%;
        }

        .skin-option {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid transparent;
        }

        .skin-option.selected {
            border-color: white;
            transform: scale(1.1);
            box-shadow: 0 0 10px rgba(255,255,255,0.5);
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            width: 100%;
            margin-top: 10px;
        }
        
        button.action-btn {
            padding: 10px 25px;
            font-size: 1rem;
            background-color: #4dff91;
            color: #16213e;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            transition: transform 0.1s;
        }

        button.action-btn:active { transform: scale(0.95); }

        #restartBtn { background-color: #ff9a4d; }
        #pauseBtn { background-color: #4d9fff; }
        
        /* 遊戲結束畫面 */
        .game-over {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(0, 0, 0, 0.95);
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            z-index: 20;
            width: 80%;
            max-width: 350px;
            display: none;
            box-shadow: 0 0 20px rgba(0,0,0,0.8);
            border: 2px solid #ff4d4d;
        }
        
        .game-over h2 { color: #ff4d4d; margin-bottom: 10px; font-size: 2rem; }
        .game-over p { margin-bottom: 5px; font-size: 1rem; }
        
        /* 成就彈窗 */
        .achievement-popup {
            position: absolute;
            top: 20%;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(0, 0, 0, 0.9);
            padding: 15px 20px;
            border-radius: 10px;
            text-align: center;
            z-index: 30;
            display: none;
            border: 2px solid #ffd700;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
        }
        
        .achievement-popup h3 { color: #ffd700; margin-bottom: 5px; }
        
        /* 成就按鈕 */
        .achievements-btn {
            position: fixed;
            top: 10px;
            right: 10px;
            width: 40px;
            height: 40px;
            background-color: #9b59b6;
            color: white;
            border: none;
            border-radius: 50%;
            font-size: 1.2rem;
            cursor: pointer;
            z-index: 10;
        }
        
        /* 成就頁面 */
        .achievements-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.95);
            z-index: 100;
            display: none;
            justify-content: center;
            align-items: center;
        }
        
        .achievements-content {
            background-color: #1a1a2e;
            padding: 20px;
            border-radius: 10px;
            width: 90%;
            max-width: 500px;
            max-height: 80%;
            overflow-y: auto;
        }
        
        .achievements-content h2 { 
            color: #ffd700; 
            text-align: center; 
            margin-bottom: 20px;
            border-bottom: 2px solid #ffd700;
            padding-bottom: 10px;
        }
        
        .achievement-item {
            display: flex;
            align-items: center;
            background-color: rgba(255, 255, 255, 0.1);
            padding: 10px;
            border-radius: 8px;
            margin-bottom: 10px;
        }
        
        .achievement-icon {
            font-size: 2rem;
            margin-right: 15px;
            min-width: 50px;
            text-align: center;
        }
        
        .achievement-info h4 { color: #fff; margin-bottom: 5px; }
        .achievement-info p { color: #a0a0c0; font-size: 0.9rem; }
        
        .achievement-locked { opacity: 0.5; }
        
        .close-modal {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            color: white;
            font-size: 2rem;
            cursor: pointer;
        }
        
        /* 分享按鈕 */
        .share-btn {
            position: fixed;
            top: 60px;
            right: 10px;
            width: 40px;
            height: 40px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 50%;
            font-size: 1.2rem;
            cursor: pointer;
            z-index: 10;
        }
        
        /* 設定按鈕 */
        .settings-btn {
            position: fixed;
            top: 110px;
            right: 10px;
            width: 40px;
            height: 40px;
            background-color: #2ecc71;
            color: white;
            border: none;
            border-radius: 50%;
            font-size: 1.2rem;
            cursor: pointer;
            z-index: 10;
        }
        
        /* 設定面板 */
        .settings-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.95);
            z-index: 100;
            display: none;
            justify-content: center;
            align-items: center;
        }
        
        .settings-content {
            background-color: #1a1a2e;
            padding: 20px;
            border-radius: 10px;
            width: 90%;
            max-width: 400px;
        }
        
        .setting-item {
            margin-bottom: 15px;
        }
        
        .setting-item label {
            display: block;
            margin-bottom: 5px;
            color: #fff;
        }
        
        .setting-item input[type="range"] {
            width: 100%;
        }
        
        .instructions {
            font-size: 0.9rem;
            color: #c0c0e0;
            text-align: center;
            background: rgba(0,0,0,0.3);
            padding: 10px;
            border-radius: 8px;
            margin-top: 10px;
            width: 100%;
            max-width: 600px;
        }

        .item-legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 5px;
            font-size: 1.2rem;
        }
        
        /* 障礙物樣式 */
        .obstacle-preview {
            background-color: #7f8c8d;
            border-radius: 3px;
        }
        
        /* 組合連擊顯示 */
        .combo-display {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 2.5rem;
            font-weight: bold;
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.8);
            z-index: 5;
            display: none;
        }

        /* PC 端樣式優化 */
        @media (min-width: 601px) {
            #gameCanvas { width: 400px; height: 400px; }
        }
        
        /* 遊戲模式標籤 */
        .mode-indicator {
            position: absolute;
            top: 10px;
            left: 10px;
            background-color: rgba(0,0,0,0.7);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            z-index: 5;
        }
        
        .time-mode { color: #4d9fff; border: 1px solid #4d9fff; }
        .survival-mode { color: #e74c3c; border: 1px solid #e74c3c; }
        .classic-mode { color: #2ecc71; border: 1px solid #2ecc71; }
    </style>
</head>
<body>
    <!-- 成就按鈕 -->
    <button class="achievements-btn" id="achievementsBtn">🏆</button>
    
    <!-- 分享按鈕 -->
    <button class="share-btn" id="shareBtn">📤</button>
    
    <!-- 設定按鈕 -->
    <button class="settings-btn" id="settingsBtn">⚙️</button>
    
    <div class="header">
        <h1>貪食蛇增強版</h1>
        <p class="subtitle">多模式挑戰 • 成就系統 • 視覺特效</p>
    </div>
    
    <div class="game-container">
        <!-- 計分板 -->
        <div class="game-info">
            <div class="info-box">
                <div class="score-label">分數</div>
                <div class="score" id="score">0</div>
            </div>
            <div class="info-box">
                <div class="score-label">最高分</div>
                <div class="score" id="highScore">0</div>
            </div>
            <div class="info-box">
                <div class="time-label">時間</div>
                <div class="time" id="timeDisplay">00:00</div>
            </div>
            <div class="info-box">
                <div class="score-label">連擊</div>
                <div class="score" id="comboCount">0</div>
            </div>
        </div>

        <!-- 遊戲模式選擇 -->
        <div class="mode-selector">
            <button class="mode-btn active" data-mode="classic">經典模式</button>
            <button class="mode-btn" data-mode="time">時間挑戰</button>
            <button class="mode-btn" data-mode="survival">生存模式</button>
        </div>
        
        <!-- 皮膚選擇 -->
        <div class="skin-selector">
            <div class="skin-option selected" style="background-color: #4dff91;" onclick="setSkin('#4dff91', this)"></div>
            <div class="skin-option" style="background-color: #ff4d4d;" onclick="setSkin('#ff4d4d', this)"></div>
            <div class="skin-option" style="background-color: #4d9fff;" onclick="setSkin('#4d9fff', this)"></div>
            <div class="skin-option" style="background-color: #ffd700;" onclick="setSkin('#ffd700', this)"></div>
            <div class="skin-option" style="background-color: #9b59b6;" onclick="setSkin('#9b59b6', this)"></div>
        </div>
        
        <!-- 困難度選擇 -->
        <div class="difficulty-selector">
            <button class="difficulty-btn active" data-diff="easy">簡單</button>
            <button class="difficulty-btn" data-diff="normal">普通</button>
            <button class="difficulty-btn" data-diff="hard">困難</button>
            <button class="difficulty-btn" data-diff="expert">專家</button>
            <button class="difficulty-btn" data-diff="insane">瘋狂</button>
        </div>
        
        <!-- 遊戲主容器 -->
        <div class="game-board-container">
            <!-- 模式標示 -->
            <div class="mode-indicator classic-mode" id="modeIndicator">經典模式</div>
            
            <!-- 連擊顯示 -->
            <div class="combo-display" id="comboDisplay"></div>
            
            <canvas id="gameCanvas" width="400" height="400"></canvas>
            
            <!-- 成就彈窗 -->
            <div class="achievement-popup" id="achievementPopup">
                <h3>成就解鎖！</h3>
                <p id="achievementName"></p>
                <p id="achievementDesc"></p>
            </div>
            
            <!-- 遊戲結束畫面 -->
            <div class="game-over" id="gameOverScreen">
                <h2>遊戲結束</h2>
                <p>分數: <span id="finalScore">0</span></p>
                <p>模式: <span id="finalMode">經典模式</span></p>
                <p>困難度: <span id="finalDiff">簡單</span></p>
                <p>遊戲時間: <span id="finalTime">00:00</span></p>
                <p id="newRecordMsg" style="display:none; color:#4dff91; font-weight:bold;">🎉 新紀錄！ 🎉</p>
                <div id="achievementsEarned" style="margin-top:10px;"></div>
                <button class="action-btn" id="playAgainBtn" style="margin-top:10px; width:100%;">再玩一次</button>
            </div>
        </div>
        
        <!-- 控制按鈕 -->
        <div class="controls">
            <button id="startBtn" class="action-btn">開始</button>
            <button id="pauseBtn" class="action-btn">暫停</button>
            <button id="restartBtn" class="action-btn">重置</button>
        </div>
        
        <!-- 遊戲說明 -->
        <div class="instructions">
            <p>使用 <strong>WASD</strong> 或 <strong>↑↓←→</strong> 控制移動</p>
            <div class="item-legend">
                <span title="蘋果 +10分">🍎</span>
                <span title="葡萄 +50分">🍇</span>
                <span title="炸彈 -50分">💣</span>
                <span title="障礙物 (生存模式)">⬛</span>
            </div>
        </div>
    </div>
    
    <!-- 成就模態框 -->
    <div class="achievements-modal" id="achievementsModal">
        <div class="achievements-content">
            <h2>🏆 成就系統</h2>
            <button class="close-modal" id="closeAchievements">&times;</button>
            <div id="achievementsList">
                <!-- 成就將動態生成 -->
            </div>
        </div>
    </div>
    
    <!-- 設定模態框 -->
    <div class="settings-modal" id="settingsModal">
        <div class="settings-content">
            <h2>⚙️ 遊戲設定</h2>
            <button class="close-modal" id="closeSettings">&times;</button>
            
            <div class="setting-item">
                <label for="musicVolume">背景音樂音量</label>
                <input type="range" id="musicVolume" min="0" max="100" value="50">
            </div>
            
            <div class="setting-item">
                <label for="soundVolume">音效音量</label>
                <input type="range" id="soundVolume" min="0" max="100" value="70">
            </div>
            
            <div class="setting-item">
                <label for="showEffects">顯示視覺特效</label>
                <input type="checkbox" id="showEffects" checked>
            </div>
            
            <button class="action-btn" id="saveSettings" style="width:100%; margin-top:20px;">儲存設定</button>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        
        // DOM 元素
        const scoreEl = document.getElementById('score');
        const highScoreEl = document.getElementById('highScore');
        const timeDisplay = document.getElementById('timeDisplay');
        const comboCount = document.getElementById('comboCount');
        const comboDisplay = document.getElementById('comboDisplay');
        const gameOverScreen = document.getElementById('gameOverScreen');
        const finalScoreEl = document.getElementById('finalScore');
        const finalModeEl = document.getElementById('finalMode');
        const finalDiffEl = document.getElementById('finalDiff');
        const finalTimeEl = document.getElementById('finalTime');
        const newRecordMsg = document.getElementById('newRecordMsg');
        const achievementsEarned = document.getElementById('achievementsEarned');
        const achievementPopup = document.getElementById('achievementPopup');
        const achievementName = document.getElementById('achievementName');
        const achievementDesc = document.getElementById('achievementDesc');
        const modeIndicator = document.getElementById('modeIndicator');
        
        // 遊戲狀態
        let snake = [];
        let items = []; // 水果陣列
        let obstacles = []; // 障礙物 (生存模式)
        let bomb = null; // 炸彈
        let direction = 'right';
        let nextDirection = 'right';
        let score = 0;
        let combo = 0;
        let comboTimeout = null;
        let gameRunning = false;
        let gamePaused = false;
        let gameLoop;
        let gameSpeed = 150;
        let currentMode = 'classic'; // classic, time, survival
        let currentDifficulty = 'easy';
        let skinColor = '#4dff91';
        let gameTime = 0; // 遊戲時間 (秒)
        let timeLimit = 180; // 時間挑戰模式時間限制 (秒)
        let gameTimer;
        
        // 粒子效果陣列
        let particles = [];
        
        // 成就系統
        let achievements = JSON.parse(localStorage.getItem('snakeAchievements')) || {};
        let unlockedAchievements = new Set(); // 本次遊戲解鎖的成就
        
        // 遊戲設定
        let settings = JSON.parse(localStorage.getItem('snakeSettings')) || {
            musicVolume: 50,
            soundVolume: 70,
            showEffects: true
        };
        
        // 高分記錄
        let highScores = JSON.parse(localStorage.getItem('snakeHighScores')) || {};
        
        // 遊戲模式設定
        const gameModes = {
            classic: { name: "經典模式", timeLimit: null },
            time: { name: "時間挑戰", timeLimit: 180 }, // 3分鐘
            survival: { name: "生存模式", timeLimit: null }
        };
        
        // 困難度設定
        const difficultySettings = {
            easy: { name: "簡單", speed: 150, minSpeed: 80, obstacleSpawnTime: 60 },
            normal: { name: "普通", speed: 120, minSpeed: 60, obstacleSpawnTime: 45 },
            hard: { name: "困難", speed: 90, minSpeed: 40, obstacleSpawnTime: 30 },
            expert: { name: "專家", speed: 70, minSpeed: 25, obstacleSpawnTime: 20 },
            insane: { name: "瘋狂", speed: 50, minSpeed: 10, obstacleSpawnTime: 15 }
        };
        
        // 成就定義
        const achievementDefinitions = [
            { id: 'first_game', name: '初出茅廬', description: '完成第一場遊戲', icon: '🎮', condition: (stats) => stats.gamesPlayed >= 1 },
            { id: 'score_100', name: '百分達人', description: '單場遊戲達到100分', icon: '💯', condition: (stats) => stats.highScore >= 100 },
            { id: 'score_500', name: '五百大師', description: '單場遊戲達到500分', icon: '🏆', condition: (stats) => stats.highScore >= 500 },
            { id: 'fruit_collector', name: '水果收藏家', description: '收集所有種類的水果', icon: '🍎', condition: (stats) => stats.fruitsCollected.apple > 0 && stats.fruitsCollected.grape > 0 },
            { id: 'bomb_survivor', name: '炸彈生存者', description: '一場遊戲中躲避5個炸彈', icon: '💣', condition: (stats) => stats.bombsAvoided >= 5 },
            { id: 'combo_master', name: '連擊大師', description: '達成10連擊', icon: '⚡', condition: (stats) => stats.maxCombo >= 10 },
            { id: 'time_challenge', name: '時間戰士', description: '在時間挑戰模式獲得200分', icon: '⏱️', condition: (stats) => stats.timeModeScore >= 200 },
            { id: 'survival_expert', name: '生存專家', description: '在生存模式存活5分鐘', icon: '🛡️', condition: (stats) => stats.survivalTime >= 300 },
            { id: 'all_difficulties', name: '全能挑戰者', description: '在所有困難度下游玩過', icon: '🌟', condition: (stats) => stats.difficultiesPlayed.length >= 5 },
            { id: 'speed_demon', name: '速度惡魔', description: '在瘋狂難度下游玩', icon: '🌀', condition: (stats) => stats.difficultiesPlayed.includes('insane') }
        ];
        
        // 遊戲統計
        let gameStats = JSON.parse(localStorage.getItem('snakeGameStats')) || {
            gamesPlayed: 0,
            highScore: 0,
            fruitsCollected: { apple: 0, grape: 0 },
            bombsAvoided: 0,
            maxCombo: 0,
            timeModeScore: 0,
            survivalTime: 0,
            difficultiesPlayed: []
        };
        
        // 網格設定
        const gridSize = 20;
        const gridWidth = canvas.width / gridSize;
        const gridHeight = canvas.height / gridSize;
        
        // 物品類型
        const itemTypes = [
            { type: 'apple', emoji: '🍎', score: 10, chance: 0.6 },
            { type: 'grape', emoji: '🍇', score: 50, chance: 0.4 }
        ];
        
        // 初始化遊戲
        function init() {
            // 更新最高分顯示
            const scoreKey = `${currentMode}_${currentDifficulty}`;
            highScores[scoreKey] = highScores[scoreKey] || 0;
            highScoreEl.innerText = highScores[scoreKey];
            
            // 重置遊戲狀態
            snake = [
                {x: 5, y: 10}, 
                {x: 4, y: 10}, 
                {x: 3, y: 10}, 
                {x: 2, y: 10}
            ];
            score = 0;
            combo = 0;
            scoreEl.innerText = score;
            comboCount.innerText = combo;
            direction = 'right';
            nextDirection = 'right';
            gameTime = 0;
            timeDisplay.innerText = '00:00';
            
            // 根據模式設定遊戲速度
            gameSpeed = difficultySettings[currentDifficulty].speed;
            
            // 清空物品和障礙物
            items = [];
            obstacles = [];
            bomb = null;
            particles = [];
            
            // 生成初始水果
            generateFruits(2 + Math.floor(Math.random() * 2));
            
            // 生成炸彈
            generateBomb();
            
            // 更新模式指示器
            updateModeIndicator();
            
            // 重置本次遊戲解鎖的成就
            unlockedAchievements.clear();
            
            // 繪製初始畫面
            drawGame();
            
            // 更新統計中的難度記錄
            if (!gameStats.difficultiesPlayed.includes(currentDifficulty)) {
                gameStats.difficultiesPlayed.push(currentDifficulty);
                saveGameStats();
            }
        }
        
        // 更新模式指示器
        function updateModeIndicator() {
            modeIndicator.textContent = gameModes[currentMode].name;
            modeIndicator.className = 'mode-indicator';
            
            if (currentMode === 'time') {
                modeIndicator.classList.add('time-mode');
            } else if (currentMode === 'survival') {
                modeIndicator.classList.add('survival-mode');
            } else {
                modeIndicator.classList.add('classic-mode');
            }
        }
        
        // 生成水果
        function generateFruits(count) {
            for(let i = 0; i < count; i++) {
                spawnOneItem();
            }
        }
        
        function spawnOneItem() {
            let valid = false;
            let newItem = {};
            
            while(!valid) {
                newItem = {
                    x: Math.floor(Math.random() * gridWidth),
                    y: Math.floor(Math.random() * gridHeight)
                };
                
                valid = isPositionValid(newItem.x, newItem.y);
            }
            
            const rand = Math.random();
            const type = rand < 0.6 ? itemTypes[0] : itemTypes[1];
            
            newItem.type = type.type;
            newItem.emoji = type.emoji;
            newItem.scoreVal = type.score;
            
            items.push(newItem);
        }
        
        // 生成炸彈
        function generateBomb() {
            let valid = false;
            let newBomb = {};
            
            while(!valid) {
                newBomb = {
                    x: Math.floor(Math.random() * gridWidth),
                    y: Math.floor(Math.random() * gridHeight)
                };
                
                valid = isPositionValid(newBomb.x, newBomb.y);
            }
            
            newBomb.type = 'bomb';
            newBomb.emoji = '💣';
            newBomb.scoreVal = -50;
            newBomb.spawnTime = Date.now();
            newBomb.duration = 3000 + Math.random() * 4000;
            newBomb.warning = false; // 是否正在警告
            
            bomb = newBomb;
        }
        
        // 生成障礙物 (生存模式)
        function generateObstacle() {
            let valid = false;
            let newObstacle = {};
            
            // 嘗試最多50次找到有效位置
            let attempts = 0;
            while(!valid && attempts < 50) {
                newObstacle = {
                    x: Math.floor(Math.random() * gridWidth),
                    y: Math.floor(Math.random() * gridHeight)
                };
                
                valid = isPositionValid(newObstacle.x, newObstacle.y);
                attempts++;
            }
            
            if (valid) {
                obstacles.push(newObstacle);
                createParticles(newObstacle.x * gridSize + gridSize/2, newObstacle.y * gridSize + gridSize/2, '#7f8c8d', 5);
            }
        }
        
        // 檢查位置是否有效
        function isPositionValid(x, y) {
            // 檢查是否與蛇身重疊
            for(let part of snake) {
                if(part.x === x && part.y === y) return false;
            }
            
            // 檢查是否與水果重疊
            for(let item of items) {
                if(item.x === x && item.y === y) return false;
            }
            
            // 檢查是否與炸彈重疊
            if(bomb && bomb.x === x && bomb.y === y) return false;
            
            // 檢查是否與障礙物重疊
            for(let obstacle of obstacles) {
                if(obstacle.x === x && obstacle.y === y) return false;
            }
            
            return true;
        }
        
        // 繪製遊戲
        function drawGame() {
            // 清除畫布
            ctx.fillStyle = '#0f3460';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 繪製網格
            drawGrid();
            
            // 繪製障礙物 (生存模式)
            drawObstacles();
            
            // 繪製水果
            drawItems();
            
            // 繪製炸彈
            drawBomb();
            
            // 繪製粒子效果
            drawParticles();
            
            // 繪製蛇
            drawSnake();
        }
        
        // 繪製網格
        function drawGrid() {
            ctx.strokeStyle = '#1a508b';
            ctx.lineWidth = 0.5;
            
            // 垂直線
            for(let i = 0; i <= canvas.width; i += gridSize) {
                ctx.beginPath();
                ctx.moveTo(i, 0);
                ctx.lineTo(i, canvas.height);
                ctx.stroke();
            }
            
            // 水平線
            for(let i = 0; i <= canvas.height; i += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, i);
                ctx.lineTo(canvas.width, i);
                ctx.stroke();
            }
        }
        
        // 繪製障礙物
        function drawObstacles() {
            if (currentMode !== 'survival') return;
            
            ctx.fillStyle = '#7f8c8d';
            for(let obstacle of obstacles) {
                ctx.fillRect(
                    obstacle.x * gridSize + 1, 
                    obstacle.y * gridSize + 1, 
                    gridSize - 2, 
                    gridSize - 2
                );
                
                // 添加內部陰影效果
                ctx.fillStyle = 'rgba(0,0,0,0.3)';
                ctx.fillRect(
                    obstacle.x * gridSize + 4, 
                    obstacle.y * gridSize + 4, 
                    gridSize - 8, 
                    gridSize - 8
                );
                ctx.fillStyle = '#7f8c8d';
            }
        }
        
        // 繪製水果
        function drawItems() {
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            
            for(let item of items) {
                ctx.fillText(
                    item.emoji, 
                    item.x * gridSize + gridSize/2, 
                    item.y * gridSize + gridSize/2 + 2
                );
            }
        }
        
        // 繪製炸彈
        function drawBomb() {
            if(!bomb) return;
            
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            
            // 如果炸彈即將消失，添加閃爍效果
            const timeLeft = bomb.duration - (Date.now() - bomb.spawnTime);
            if (timeLeft < 2000) {
                // 閃爍效果：每250ms切換一次
                const shouldShow = Math.floor(Date.now() / 250) % 2 === 0;
                if (shouldShow) {
                    ctx.fillText(
                        bomb.emoji, 
                        bomb.x * gridSize + gridSize/2, 
                        bomb.y * gridSize + gridSize/2 + 2
                    );
                }
                
                // 添加紅色警示圈
                if (settings.showEffects) {
                    ctx.strokeStyle = 'rgba(255, 0, 0, 0.5)';
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.arc(
                        bomb.x * gridSize + gridSize/2,
                        bomb.y * gridSize + gridSize/2,
                        gridSize/2 + 2,
                        0,
                        Math.PI * 2
                    );
                    ctx.stroke();
                }
            } else {
                ctx.fillText(
                    bomb.emoji, 
                    bomb.x * gridSize + gridSize/2, 
                    bomb.y * gridSize + gridSize/2 + 2
                );
            }
        }
        
        // 繪製粒子效果
        function drawParticles() {
            if (!settings.showEffects) return;
            
            for(let i = particles.length - 1; i >= 0; i--) {
                const p = particles[i];
                
                ctx.fillStyle = p.color;
                ctx.globalAlpha = p.alpha;
                
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.globalAlpha = 1.0;
                
                // 更新粒子
                p.x += p.vx;
                p.y += p.vy;
                p.alpha -= 0.02;
                p.size *= 0.95;
                
                // 移除消失的粒子
                if (p.alpha <= 0 || p.size <= 0.5) {
                    particles.splice(i, 1);
                }
            }
        }
        
        // 繪製蛇
        function drawSnake() {
            snake.forEach((part, index) => {
                // 蛇頭使用較亮顏色
                if(index === 0) {
                    ctx.fillStyle = lightenColor(skinColor, 30);
                    
                    // 繪製眼睛
                    ctx.fillStyle = '#fff';
                    let eyeX1 = part.x * gridSize + 4;
                    let eyeX2 = part.x * gridSize + 12;
                    let eyeY = part.y * gridSize + 4;
                    
                    // 根據方向調整眼睛位置
                    if (direction === 'right') {
                        eyeX1 = part.x * gridSize + 12;
                        eyeX2 = part.x * gridSize + 12;
                        eyeY = part.y * gridSize + 6;
                    } else if (direction === 'left') {
                        eyeX1 = part.x * gridSize + 4;
                        eyeX2 = part.x * gridSize + 4;
                        eyeY = part.y * gridSize + 6;
                    } else if (direction === 'up') {
                        eyeX1 = part.x * gridSize + 6;
                        eyeX2 = part.x * gridSize + 12;
                        eyeY = part.y * gridSize + 4;
                    } else if (direction === 'down') {
                        eyeX1 = part.x * gridSize + 6;
                        eyeX2 = part.x * gridSize + 12;
                        eyeY = part.y * gridSize + 12;
                    }
                    
                    ctx.fillRect(eyeX1, eyeY, 4, 4);
                    ctx.fillRect(eyeX2, eyeY, 4, 4);
                    ctx.fillStyle = lightenColor(skinColor, 30);
                } else {
                    // 蛇身使用漸變透明度
                    const alpha = 1 - (index / snake.length) * 0.6;
                    ctx.globalAlpha = alpha;
                    ctx.fillStyle = skinColor;
                }
                
                // 繪製蛇身
                ctx.fillRect(part.x * gridSize + 1, part.y * gridSize + 1, gridSize - 2, gridSize - 2);
                
                // 重置透明度
                ctx.globalAlpha = 1.0;
                
                // 添加蛇身內部效果
                if(index > 0) {
                    ctx.fillStyle = 'rgba(255,255,255,0.1)';
                    ctx.fillRect(part.x * gridSize + 4, part.y * gridSize + 4, gridSize - 8, gridSize - 8);
                }
            });
            
            // 添加蛇尾拖尾效果
            if (settings.showEffects && snake.length > 5) {
                const tail = snake[snake.length - 1];
                createParticles(
                    tail.x * gridSize + gridSize/2,
                    tail.y * gridSize + gridSize/2,
                    skinColor,
                    1
                );
            }
        }
        
        // 顏色亮化函數
        function lightenColor(color, percent) {
            const num = parseInt(color.slice(1), 16);
            const amt = Math.round(2.55 * percent);
            const R = (num >> 16) + amt;
            const G = (num >> 8 & 0x00FF) + amt;
            const B = (num & 0x0000FF) + amt;
            
            return `#${(
                0x1000000 + 
                (R < 255 ? R < 1 ? 0 : R : 255) * 0x10000 + 
                (G < 255 ? G < 1 ? 0 : G : 255) * 0x100 + 
                (B < 255 ? B < 1 ? 0 : B : 255)
            ).toString(16).slice(1)}`;
        }
        
        // 創建粒子效果
        function createParticles(x, y, color, count) {
            if (!settings.showEffects) return;
            
            for(let i = 0; i < count; i++) {
                particles.push({
                    x: x,
                    y: y,
                    size: Math.random() * 5 + 2,
                    color: color,
                    vx: (Math.random() - 0.5) * 4,
                    vy: (Math.random() - 0.5) * 4,
                    alpha: 1.0
                });
            }
        }
        
        // 顯示連擊效果
        function showComboEffect(count) {
            if (count < 3) return;
            
            comboDisplay.textContent = `${count} 連擊!`;
            comboDisplay.style.display = 'block';
            comboDisplay.style.opacity = 1;
            
            // 根據連擊數調整字體大小和顏色
            let fontSize = 2.0;
            let color = '#ffd700';
            
            if (count >= 10) {
                fontSize = 3.0;
                color = '#ff0000';
            } else if (count >= 7) {
                fontSize = 2.8;
                color = '#ff6b6b';
            } else if (count >= 5) {
                fontSize = 2.5;
                color = '#4dff91';
            }
            
            comboDisplay.style.fontSize = `${fontSize}rem`;
            comboDisplay.style.color = color;
            comboDisplay.style.textShadow = `0 0 10px ${color}`;
            
            // 淡出效果
            setTimeout(() => {
                comboDisplay.style.opacity = 0;
                setTimeout(() => {
                    comboDisplay.style.display = 'none';
                }, 500);
            }, 1000);
        }
        
        // 遊戲邏輯更新
        function update() {
            // 檢查炸彈時間
            if(bomb) {
                if(Date.now() - bomb.spawnTime > bomb.duration) {
                    // 炸彈消失，增加炸彈躲避統計
                    gameStats.bombsAvoided++;
                    saveGameStats();
                    
                    bomb = null;
                    setTimeout(generateBomb, 1000);
                }
            }
            
            // 更新方向
            direction = nextDirection;
            let head = {x: snake[0].x, y: snake[0].y};
            
            // 根據方向移動頭部
            if(direction === 'up') head.y--;
            if(direction === 'down') head.y++;
            if(direction === 'left') head.x--;
            if(direction === 'right') head.x++;
            
            // 碰撞檢測
            if(head.x < 0 || head.x >= gridWidth || head.y < 0 || head.y >= gridHeight || checkCollision(head)) {
                gameOver();
                return;
            }
            
            // 新增：生存模式障礙物碰撞檢測
            if (currentMode === 'survival') {
                for(let obstacle of obstacles) {
                    if(head.x === obstacle.x && head.y === obstacle.y) {
                        gameOver();
                        return;
                    }
                }
            }
            
            // 移動蛇
            snake.unshift(head);
            
            // 檢查是否吃到水果
            let ate = false;
            for(let i = 0; i < items.length; i++) {
                if(head.x === items[i].x && head.y === items[i].y) {
                    // 增加分數
                    score += items[i].scoreVal;
                    scoreEl.innerText = score;
                    
                    // 更新水果收集統計
                    if (items[i].type === 'apple') {
                        gameStats.fruitsCollected.apple++;
                    } else if (items[i].type === 'grape') {
                        gameStats.fruitsCollected.grape++;
                    }
                    
                    // 創建粒子效果
                    createParticles(
                        head.x * gridSize + gridSize/2,
                        head.y * gridSize + gridSize/2,
                        items[i].type === 'apple' ? '#ff4d4d' : '#9b59b6',
                        10
                    );
                    
                    // 移除被吃掉的水果並生成新的
                    items.splice(i, 1);
                    spawnOneItem();
                    
                    // 增加連擊
                    combo++;
                    comboCount.innerText = combo;
                    
                    // 顯示連擊效果
                    if (combo >= 3) {
                        showComboEffect(combo);
                    }
                    
                    // 重置連擊計時器
                    if (comboTimeout) clearTimeout(comboTimeout);
                    comboTimeout = setTimeout(() => {
                        if (combo > gameStats.maxCombo) {
                            gameStats.maxCombo = combo;
                            saveGameStats();
                        }
                        combo = 0;
                        comboCount.innerText = 0;
                    }, 2000);
                    
                    ate = true;
                    break;
                }
            }
            
            // 檢查是否吃到炸彈
            if(bomb && head.x === bomb.x && head.y === bomb.y) {
                score += bomb.scoreVal;
                scoreEl.innerText = score;
                snake.pop(); // 吃到炸彈減少長度
                
                // 創建爆炸效果
                createParticles(
                    head.x * gridSize + gridSize/2,
                    head.y * gridSize + gridSize/2,
                    '#ff4d4d',
                    15
                );
                
                bomb = null;
                triggerShake();
                setTimeout(generateBomb, 1000);
                
                // 重置連擊
                if (combo > gameStats.maxCombo) {
                    gameStats.maxCombo = combo;
                    saveGameStats();
                }
                combo = 0;
                comboCount.innerText = 0;
                if (comboTimeout) clearTimeout(comboTimeout);
                
                ate = true;
            }
            
            // 如果沒有吃到東西，移除尾部
            if(!ate) {
                snake.pop();
            }
            
            // 隨遊戲進行增加速度
            if(score > 0 && score % 50 === 0) {
                const setting = difficultySettings[currentDifficulty];
                if(gameSpeed > setting.minSpeed) {
                    gameSpeed -= 5;
                }
            }
            
            // 生存模式：定期生成障礙物
            if (currentMode === 'survival' && gameTime > 0 && gameTime % difficultySettings[currentDifficulty].obstacleSpawnTime === 0) {
                generateObstacle();
            }
        }
        
        // 碰撞檢測
        function checkCollision(head) {
            for(let part of snake) {
                if(part.x === head.x && part.y === head.y) return true;
            }
            return false;
        }
        
        // 震動效果
        function triggerShake() {
            canvas.classList.add('shake');
            setTimeout(() => canvas.classList.remove('shake'), 500);
        }
        
        // 遊戲主循環
        function gameStep() {
            if(!gameRunning || gamePaused) return;
            update();
            drawGame();
            gameLoop = setTimeout(gameStep, gameSpeed);
        }
        
        // 遊戲結束
        function gameOver() {
            gameRunning = false;
            gamePaused = false;
            clearTimeout(gameLoop);
            clearInterval(gameTimer);
            
            // 更新遊戲統計
            gameStats.gamesPlayed++;
            if (score > gameStats.highScore) {
                gameStats.highScore = score;
            }
            
            // 模式特定統計
            if (currentMode === 'time') {
                if (score > gameStats.timeModeScore) {
                    gameStats.timeModeScore = score;
                }
            } else if (currentMode === 'survival') {
                if (gameTime > gameStats.survivalTime) {
                    gameStats.survivalTime = gameTime;
                }
            }
            
            saveGameStats();
            
            // 檢查並解鎖成就
            checkAchievements();
            
            // 更新遊戲結束畫面
            finalScoreEl.innerText = score;
            finalModeEl.innerText = gameModes[currentMode].name;
            finalDiffEl.innerText = difficultySettings[currentDifficulty].name;
            finalTimeEl.innerText = formatTime(gameTime);
            
            // 檢查是否打破紀錄
            const scoreKey = `${currentMode}_${currentDifficulty}`;
            if(score > highScores[scoreKey]) {
                highScores[scoreKey] = score;
                localStorage.setItem('snakeHighScores', JSON.stringify(highScores));
                highScoreEl.innerText = score;
                newRecordMsg.style.display = 'block';
            } else {
                newRecordMsg.style.display = 'none';
            }
            
            // 顯示本次遊戲解鎖的成就
            displayUnlockedAchievements();
            
            // 顯示遊戲結束畫面
            gameOverScreen.style.display = 'block';
        }
        
        // 檢查成就
        function checkAchievements() {
            achievementDefinitions.forEach(achievement => {
                // 如果成就已經解鎖，跳過
                if (achievements[achievement.id]) return;
                
                // 檢查成就條件
                if (achievement.condition(gameStats)) {
                    // 解鎖成就
                    achievements[achievement.id] = true;
                    unlockedAchievements.add(achievement);
                    
                    // 顯示成就彈窗
                    showAchievementPopup(achievement);
                }
            });
            
            // 儲存成就狀態
            localStorage.setItem('snakeAchievements', JSON.stringify(achievements));
        }
        
        // 顯示成就彈窗
        function showAchievementPopup(achievement) {
            achievementName.textContent = achievement.name;
            achievementDesc.textContent = achievement.description;
            
            achievementPopup.style.display = 'block';
            achievementPopup.style.top = '20%';
            
            // 3秒後自動隱藏
            setTimeout(() => {
                achievementPopup.style.display = 'none';
            }, 3000);
        }
        
        // 顯示本次遊戲解鎖的成就
        function displayUnlockedAchievements() {
            if (unlockedAchievements.size === 0) {
                achievementsEarned.innerHTML = '';
                return;
            }
            
            let html = '<p>🎉 本次解鎖成就:</p>';
            unlockedAchievements.forEach(achievement => {
                html += `<p>${achievement.icon} ${achievement.name}</p>`;
            });
            
            achievementsEarned.innerHTML = html;
        }
        
        // 儲存遊戲統計
        function saveGameStats() {
            localStorage.setItem('snakeGameStats', JSON.stringify(gameStats));
        }
        
        // 儲存遊戲設定
        function saveSettings() {
            localStorage.setItem('snakeSettings', JSON.stringify(settings));
        }
        
        // 載入遊戲設定
        function loadSettings() {
            document.getElementById('musicVolume').value = settings.musicVolume;
            document.getElementById('soundVolume').value = settings.soundVolume;
            document.getElementById('showEffects').checked = settings.showEffects;
        }
        
        // 格式化時間 (秒轉為 MM:SS)
        function formatTime(seconds) {
            const mins = Math.floor(seconds / 60);
            const secs = seconds % 60;
            return `${mins.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`;
        }
        
        // 更新遊戲時間顯示
        function updateGameTime() {
            if (!gameRunning || gamePaused) return;
            
            gameTime++;
            timeDisplay.textContent = formatTime(gameTime);
            
            // 時間挑戰模式檢查時間限制
            if (currentMode === 'time' && gameTime >= timeLimit) {
                gameOver();
            }
        }
        
        // 載入成就列表
        function loadAchievements() {
            const container = document.getElementById('achievementsList');
            container.innerHTML = '';
            
            achievementDefinitions.forEach(achievement => {
                const isUnlocked = achievements[achievement.id] || false;
                
                const achievementEl = document.createElement('div');
                achievementEl.className = `achievement-item ${isUnlocked ? '' : 'achievement-locked'}`;
                
                achievementEl.innerHTML = `
                    <div class="achievement-icon">${achievement.icon}</div>
                    <div class="achievement-info">
                        <h4>${achievement.name}</h4>
                        <p>${achievement.description}</p>
                        <p><small>${isUnlocked ? '✅ 已解鎖' : '🔒 未解鎖'}</small></p>
                    </div>
                `;
                
                container.appendChild(achievementEl);
            });
        }
        
        // 分享遊戲成績
        function shareScore() {
            // 創建分享文字
            const shareText = `我在貪食蛇增強版獲得了 ${score} 分！\n` +
                            `模式: ${gameModes[currentMode].name}\n` +
                            `困難度: ${difficultySettings[currentDifficulty].name}\n` +
                            `#貪食蛇 #遊戲`;
            
            // 嘗試使用 Web Share API
            if (navigator.share) {
                navigator.share({
                    title: '貪食蛇增強版成績',
                    text: shareText,
                    url: window.location.href
                }).catch(console.error);
            } else {
                // 降級方案：複製到剪貼簿
                navigator.clipboard.writeText(shareText).then(() => {
                    alert('成績已複製到剪貼簿！\n\n' + shareText);
                }).catch(() => {
                    // 如果 clipboard API 不可用，顯示分享文字
                    prompt('請複製以下文字分享您的成績:', shareText);
                });
            }
        }
        
        // 初始化事件監聽器
        function initEventListeners() {
            // 開始按鈕
            document.getElementById('startBtn').onclick = () => {
                if(!gameRunning) {
                    if(gamePaused) {
                        gamePaused = false;
                    } else {
                        init();
                    }
                    gameRunning = true;
                    gameStep();
                    
                    // 開始計時器
                    gameTimer = setInterval(updateGameTime, 1000);
                }
            };
            
            // 暫停按鈕
            document.getElementById('pauseBtn').onclick = () => {
                if(gameRunning) {
                    gamePaused = !gamePaused;
                    if(!gamePaused) {
                        gameStep();
                    }
                }
            };
            
            // 重置按鈕
            document.getElementById('restartBtn').onclick = () => {
                gameRunning = false;
                gamePaused = false;
                clearTimeout(gameLoop);
                clearInterval(gameTimer);
                init();
            };
            
            // 再玩一次按鈕
            document.getElementById('playAgainBtn').onclick = () => {
                gameOverScreen.style.display = 'none';
                init();
                gameRunning = true;
                gameStep();
                gameTimer = setInterval(updateGameTime, 1000);
            };
            
            // 模式選擇
            document.querySelectorAll('.mode-btn').forEach(btn => {
                btn.onclick = () => {
                    document.querySelectorAll('.mode-btn').forEach(b => b.classList.remove('active'));
                    btn.classList.add('active');
                    currentMode = btn.dataset.mode;
                    
                    // 更新時間限制顯示
                    if (currentMode === 'time') {
                        timeLimit = gameModes[currentMode].timeLimit;
                    }
                    
                    // 重置遊戲
                    if(gameRunning) {
                        gameRunning = false;
                        clearTimeout(gameLoop);
                        clearInterval(gameTimer);
                        gamePaused = false;
                        init();
                    } else {
                        init();
                    }
                };
            });
            
            // 困難度選擇
            document.querySelectorAll('.difficulty-btn').forEach(btn => {
                btn.onclick = () => {
                    document.querySelectorAll('.difficulty-btn').forEach(b => b.classList.remove('active'));
                    btn.classList.add('active');
                    currentDifficulty = btn.dataset.diff;
                    gameSpeed = difficultySettings[currentDifficulty].speed;
                    
                    // 更新最高分顯示
                    const scoreKey = `${currentMode}_${currentDifficulty}`;
                    highScoreEl.innerText = highScores[scoreKey] || 0;
                    
                    if(gameRunning) {
                        gameRunning = false;
                        clearTimeout(gameLoop);
                        clearInterval(gameTimer);
                        gamePaused = false;
                        init();
                    } else {
                        init();
                    }
                };
            });
            
            // 成就按鈕
            document.getElementById('achievementsBtn').onclick = () => {
                loadAchievements();
                document.getElementById('achievementsModal').style.display = 'flex';
            };
            
            // 分享按鈕
            document.getElementById('shareBtn').onclick = shareScore;
            
            // 設定按鈕
            document.getElementById('settingsBtn').onclick = () => {
                loadSettings();
                document.getElementById('settingsModal').style.display = 'flex';
            };
            
            // 關閉成就模態框
            document.getElementById('closeAchievements').onclick = () => {
                document.getElementById('achievementsModal').style.display = 'none';
            };
            
            // 關閉設定模態框
            document.getElementById('closeSettings').onclick = () => {
                document.getElementById('settingsModal').style.display = 'none';
            };
            
            // 儲存設定
            document.getElementById('saveSettings').onclick = () => {
                settings.musicVolume = parseInt(document.getElementById('musicVolume').value);
                settings.soundVolume = parseInt(document.getElementById('soundVolume').value);
                settings.showEffects = document.getElementById('showEffects').checked;
                
                saveSettings();
                document.getElementById('settingsModal').style.display = 'none';
            };
            
            // 按鍵監聽 (WASD + 方向鍵)
            document.addEventListener('keydown', (e) => {
                const k = e.key;
                const c = e.code;
                
                // 防止滾動
                if (["ArrowUp", "ArrowDown", "ArrowLeft", "ArrowRight", " ", "Spacebar"].includes(k) || 
                    c.startsWith("Key")) {
                    e.preventDefault();
                }
                
                // 方向判斷
                if ((k === 'ArrowUp' || k === 'w' || k === 'W' || c === 'KeyW') && direction !== 'down') {
                    nextDirection = 'up';
                } else if ((k === 'ArrowDown' || k === 's' || k === 'S' || c === 'KeyS') && direction !== 'up') {
                    nextDirection = 'down';
                } else if ((k === 'ArrowLeft' || k === 'a' || k === 'A' || c === 'KeyA') && direction !== 'right') {
                    nextDirection = 'left';
                } else if ((k === 'ArrowRight' || k === 'd' || k === 'D' || c === 'KeyD') && direction !== 'left') {
                    nextDirection = 'right';
                }
                
                // 空格鍵暫停/繼續
                if (k === ' ' || k === 'Spacebar') {
                    if (gameRunning) {
                        gamePaused = !gamePaused;
                        if (!gamePaused) {
                            gameStep();
                        }
                    }
                }
                
                // Enter鍵開始遊戲
                if (k === 'Enter' && !gameRunning) {
                    document.getElementById('startBtn').click();
                }
            });
        }
        
        // 皮膚選擇函數
        window.setSkin = function(color, el) {
            skinColor = color;
            document.querySelectorAll('.skin-option').forEach(e => e.classList.remove('selected'));
            el.classList.add('selected');
            if(!gameRunning) drawGame();
        };
        
        // 頁面載入完成後初始化
        window.onload = function() {
            init();
            initEventListeners();
            loadSettings();
        };
    </script>
</body>
</html>