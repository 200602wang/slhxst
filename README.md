<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>适老化洗手池施工指导手册</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&display=swap">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Noto Sans SC', 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f8fafc;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            padding: 25px 20px;
            margin-bottom: 25px;
            background: linear-gradient(to right, #2c3e5a, #4a6fa5);
            color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(44, 62, 90, 0.15);
            position: relative;
            border-left: 6px solid #ff9900;
        }
        
        .header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        .header h1 i {
            color: #ff9900;
        }
        
        .header p {
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto 10px;
            opacity: 0.9;
        }
        
        .elderly-badge {
            display: inline-block;
            background-color: #ff9900;
            color: white;
            padding: 8px 20px;
            border-radius: 30px;
            font-weight: bold;
            font-size: 1rem;
            margin-top: 10px;
            box-shadow: 0 3px 8px rgba(255, 153, 0, 0.3);
        }
        
        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
            margin-bottom: 30px;
        }
        
        @media (max-width: 1100px) {
            .main-content {
                grid-template-columns: 1fr;
            }
        }
        
        .model-section, .section-container {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            height: 580px;
            display: flex;
            flex-direction: column;
        }
        
        .section-title {
            background-color: #3a5a8a;
            color: white;
            padding: 18px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            border-bottom: 2px solid #ff9900;
        }
        
        .section-title i {
            font-size: 1.4rem;
            color: #ff9900;
        }
        
        .model-container, .section-image-container {
            flex: 1;
            width: 100%;
            position: relative;
            background-color: #f0f5ff;
            overflow: hidden;
        }
        
        .model-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .section-image-container {
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }
        
        .section-image-container img {
            max-width: 100%;
            max-height: 100%;
            object-fit: contain;
            transition: transform 0.3s ease;
        }
        
        .section-image-container:hover img {
            transform: scale(1.03);
        }
        
        .image-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
            color: white;
            text-align: center;
            padding: 20px;
        }
        
        .section-image-container:hover .image-overlay {
            opacity: 1;
        }
        
        .section-controls {
            padding: 15px;
            background-color: #f8fafc;
            border-top: 1px solid #eaeaea;
            text-align: center;
            font-size: 0.9rem;
            color: #666;
        }
        
        .section-zoom-btn {
            background: #ff9900;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
        }
        
        .section-zoom-btn:hover {
            background: #e68a00;
        }
        
        .worker-info-sections {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        
        @media (max-width: 768px) {
            .worker-info-sections {
                grid-template-columns: 1fr;
            }
        }
        
        .info-box {
            background: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .info-box h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #2c3e5a;
            display: flex;
            align-items: center;
            gap: 12px;
            padding-bottom: 10px;
            border-bottom: 3px solid #ff9900;
        }
        
        .info-box h3 i {
            color: #ff9900;
        }
        
        .note-list {
            list-style-type: none;
        }
        
        .note-list li {
            padding: 14px 0;
            padding-left: 35px;
            border-bottom: 1px solid #f0f0f0;
            position: relative;
        }
        
        .note-list li:last-child {
            border-bottom: none;
        }
        
        .note-list li:before {
            content: "▶";
            color: #ff9900;
            font-size: 1rem;
            position: absolute;
            left: 0;
            top: 14px;
        }
        
        .material-highlight {
            background-color: #e8f4fc;
            padding: 3px 8px;
            border-radius: 4px;
            font-weight: bold;
            color: #2c3e5a;
            border-left: 3px solid #4a6fa5;
            margin: 0 2px;
        }
        
        .materials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 18px;
        }
        
        .material-item {
            background: #f8fafc;
            padding: 18px;
            border-radius: 10px;
            border-left: 4px solid #4a6fa5;
            transition: transform 0.2s;
        }
        
        .material-item:hover {
            transform: translateY(-3px);
        }
        
        .material-item h4 {
            color: #2c3e5a;
            margin-bottom: 8px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .material-item h4 i {
            color: #ff9900;
        }
        
        .material-item p {
            color: #5a6c7d;
            font-size: 0.95rem;
            line-height: 1.5;
        }
        
        .material-spec {
            margin-top: 10px;
            font-size: 0.85rem;
            color: #666;
            background-color: #f0f8ff;
            padding: 8px;
            border-radius: 5px;
        }
        
        .elderly-challenges {
            margin-top: 30px;
            background: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }
        
        .challenges-title {
            color: #2c3e5a;
            font-size: 1.6rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #ff9900;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .challenges-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
        }
        
        .challenge-item {
            background: #f8fafc;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #4a6fa5;
        }
        
        .challenge-item h4 {
            color: #2c3e5a;
            margin-bottom: 10px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .challenge-item h4 i {
            color: #ff9900;
        }
        
        .solution {
            background-color: #e8f4fc;
            padding: 12px;
            border-radius: 8px;
            margin-top: 12px;
            border-left: 3px solid #27ae60;
        }
        
        .solution strong {
            color: #27ae60;
        }
        
        .construction-steps {
            margin-top: 30px;
        }
        
        .steps-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 15px;
        }
        
        .step-item {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.05);
            border-top: 4px solid #4a6fa5;
            counter-increment: step-counter;
        }
        
        .step-item h4 {
            color: #2c3e5a;
            margin-bottom: 10px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .step-item h4:before {
            content: counter(step-counter);
            background-color: #4a6fa5;
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        .footer-note {
            background-color: #fff8e1;
            border-left: 5px solid #f39c12;
            padding: 20px;
            border-radius: 10px;
            margin-top: 35px;
            font-size: 0.95rem;
            color: #7d6608;
        }
        
        .footer-note strong {
            color: #d68910;
        }
        
        /* 模态框样式 */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            animation: fadeIn 0.3s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .modal-content {
            max-width: 90%;
            max-height: 90%;
            position: relative;
            background: transparent;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content img {
            max-width: 100%;
            max-height: 90vh;
            object-fit: contain;
            border-radius: 5px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }
        
        .close-modal {
            position: absolute;
            top: 20px;
            right: 30px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            border: none;
            font-size: 2.5rem;
            cursor: pointer;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background 0.3s;
            z-index: 2001;
        }
        
        .close-modal:hover {
            background: rgba(0, 0, 0, 0.9);
        }
        
        .modal-controls {
            position: absolute;
            bottom: 30px;
            left: 0;
            width: 100%;
            display: flex;
            justify-content: center;
            gap: 15px;
            z-index: 2001;
        }
        
        .modal-btn {
            background: rgba(0, 0, 0, 0.7);
            color: white;
            border: none;
            padding: 10px 18px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: background 0.3s;
        }
        
        .modal-btn:hover {
            background: rgba(0, 0, 0, 0.9);
        }
        
        .image-info {
            position: absolute;
            bottom: 30px;
            right: 30px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 8px 12px;
            border-radius: 5px;
            font-size: 0.85rem;
        }
        
        .zoom-indicator {
            position: absolute;
            top: 20px;
            left: 30px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 8px 12px;
            border-radius: 5px;
            font-size: 0.9rem;
        }
        
        .sink-info-box {
            padding: 15px;
            background: #f0f8ff;
            border-radius: 8px;
            border-left: 4px solid #4a6fa5;
            margin-top: 15px;
            font-size: 0.9rem;
        }
        
        .sink-info-box h4 {
            color: #2c3e5a;
            margin-bottom: 8px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .sink-info-box ul {
            padding-left: 20px;
            color: #5a6c7d;
        }
        
        .sink-info-box li {
            margin-bottom: 6px;
        }
        
        .worker-tip {
            background-color: #fff8e1;
            border-left: 4px solid #f39c12;
            padding: 12px 15px;
            border-radius: 8px;
            margin: 15px 0;
            font-size: 0.9rem;
            color: #7d6608;
        }
        
        .worker-tip strong {
            color: #d68910;
        }
        
        .dimension-label {
            background-color: #4a6fa5;
            color: white;
            padding: 3px 8px;
            border-radius: 4px;
            font-weight: bold;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-tools"></i> 适老化洗手池施工指导手册</h1>
        <p>专为施工人员设计的适老化洗手池安装指南 | 明确材料规格与施工要点</p>
        <div class="elderly-badge">
            <i class="fas fa-user-friends"></i> 无障碍适老化施工规范
        </div>
    </div>

    <div class="main-content">
        <div class="model-section">
            <div class="section-title">
                <span><i class="fas fa-cube"></i> 三维模型参考</span>
                <button class="section-zoom-btn" id="enlargeModelBtn">
                    <i class="fas fa-expand-alt"></i> 全屏查看
                </button>
            </div>
            <div class="model-container">
                <iframe id="modelIframe" 
                        title="适老化洗手池三维模型"
                        frameborder="0" 
                        allowfullscreen 
                        mozallowfullscreen="true" 
                        webkitallowfullscreen="true" 
                        allow="autoplay; fullscreen; xr-spatial-tracking" 
                        xr-spatial-tracking 
                        execution-while-out-of-viewport 
                        execution-while-not-rendered 
                        web-share 
                        src="https://sketchfab.com/models/dbb26e1513004995ba7d8379e3af0c66/embed?autospin=1&autostart=1&preload=1">
                </iframe>
            </div>
            <div class="section-controls">
                使用鼠标拖拽旋转模型，滚轮缩放。点击右上角按钮可全屏查看。
            </div>
        </div>

        <div class="section-container">
            <div class="section-title">
                <span><i class="fas fa-ruler-combined"></i> 施工剖面图</span>
                <button class="section-zoom-btn" id="enlargeSectionBtn">
                    <i class="fas fa-search-plus"></i> 放大查看
                </button>
            </div>
            <div class="section-image-container" id="sectionImageContainer">
                <!-- 如果图片加载失败，会显示SVG剖面图 -->
                <img id="sectionImage" 
                     src="https://image2url.com/r2/default/images/1768819927982-247b9674-06f4-422e-8488-77281d523438.png" 
                     alt="洗漱台施工剖面图"
                     onload="handleImageLoad()"
                     onerror="handleImageError()">
                <div class="image-overlay">
                    <i class="fas fa-search-plus"></i>
                    <h3>点击查看施工剖面大图</h3>
                    <p>查看材料规格与安装细节</p>
                </div>
                <div id="loadingMessage" class="image-placeholder" style="display: none; position: absolute;">
                    <i class="fas fa-spinner fa-spin"></i>
                    <h3>正在加载剖面图...</h3>
                </div>
            </div>
            <div class="section-controls">
                点击图片可放大查看细节。支持鼠标滚轮缩放和拖拽查看。
            </div>
        </div>
    </div>

    <div class="elderly-challenges">
        <h2 class="challenges-title">
            <i class="fas fa-hard-hat"></i> 施工前须知：老年人使用洗手池常见问题
        </h2>
        
        <div class="challenges-grid">
            <div class="challenge-item">
                <h4><i class="fas fa-wheelchair"></i> 轮椅使用者接近困难</h4>
                <p>传统洗手池下方空间不足，轮椅无法靠近。</p>
                <div class="solution">
                    <strong>施工要点：</strong> 悬空式设计，台面下方净空高度<span class="dimension-label">≥68cm</span>，深度<span class="dimension-label">≥48cm</span>。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-ruler-vertical"></i> 高度不适导致腰背劳损</h4>
                <p>固定高度不适合不同身高的老年人。</p>
                <div class="solution">
                    <strong>施工要点：</strong> 安装高度<span class="dimension-label">75-80cm</span>（含台面），镜面可倾斜或高度可调。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-hand-paper"></i> 手部力量不足操作困难</h4>
                <p>传统旋转式水龙头对关节炎患者操作困难。</p>
                <div class="solution">
                    <strong>施工要点：</strong> 采用单杠杆或感应式龙头，安装防烫伤恒温阀。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-balance-scale"></i> 缺乏支撑增加摔倒风险</h4>
                <p>洗手池周边缺乏安全扶手，老年人无处借力。</p>
                <div class="solution">
                    <strong>施工要点：</strong> 两侧安装L型安全扶手，承载力<span class="dimension-label">≥135kg</span>。
                </div>
            </div>
        </div>
    </div>

    <div class="worker-info-sections">
        <div class="info-box construction">
            <h3><i class="fas fa-hammer"></i> 适老化施工关键步骤</h3>
            <div class="construction-steps">
                <div class="steps-grid">
                    <div class="step-item">
                        <h4>墙面定位与划线</h4>
                        <p>根据设计图纸，确定洗手池中心位置，使用激光水平仪标记高度线（距地面<span class="dimension-label">75-80cm</span>）。</p>
                        <div class="worker-tip">
                            <strong>施工提示：</strong> 确保墙面平整，如不平整需先使用<span class="material-highlight">水泥砂浆</span>找平。
                        </div>
                    </div>
                    
                    <div class="step-item">
                        <h4>安全扶手安装</h4>
                        <p>使用<span class="material-highlight">M10膨胀螺栓</span>固定于承重墙，高度<span class="dimension-label">75-85cm</span>，距墙间隙<span class="dimension-label">3.5-4.5cm</span>。</p>
                        <div class="worker-tip">
                            <strong>施工提示：</strong> 安装后需进行承重测试，确保承载力达到<span class="dimension-label">135kg</span>以上。
                        </div>
                    </div>
                    
                    <div class="step-item">
                        <h4>柜体与台面安装</h4>
                        <p>安装悬空柜体，确保下方净空高度<span class="dimension-label">≥68cm</span>，深度<span class="dimension-label">≥48cm</span>。</p>
                        <div class="worker-tip">
                            <strong>施工提示：</strong> 所有台面边缘需做圆角处理（<span class="dimension-label">R≥10mm</span>），避免尖角。
                        </div>
                    </div>
                    
                    <div class="step-item">
                        <h4>水管与龙头安装</h4>
                        <p>安装防烫伤恒温阀，最高出水温度不超过<span class="dimension-label">49℃</span>。</p>
                        <div class="worker-tip">
                            <strong>施工提示：</strong> 使用<span class="material-highlight">PPR热水管</span>，做好保温处理，防止热量损失。
                        </div>
                    </div>
                    
                    <div class="step-item">
                        <h4>紧急呼叫系统安装</h4>
                        <p>洗手池旁安装防水紧急呼叫按钮，高度距地<span class="dimension-label">40-50cm</span>。</p>
                        <div class="worker-tip">
                            <strong>施工提示：</strong> 按钮需连接至护理站或家人手机，并配有延迟响应防止误触。
                        </div>
                    </div>
                    
                    <div class="step-item">
                        <h4>地面防滑处理</h4>
                        <p>地面使用防滑系数<span class="dimension-label">≥0.6</span>的防滑砖，排水坡度<span class="dimension-label">1%-2%</span>。</p>
                        <div class="worker-tip">
                            <strong>施工提示：</strong> 确保地面无积水，可在淋浴区门口安装防滑地垫。
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="info-box materials">
            <h3><i class="fas fa-clipboard-list"></i> 材料规格与要求</h3>
            <div class="materials-grid">
                <div class="material-item">
                    <h4><i class="fas fa-gem"></i> 台面材料</h4>
                    <p><strong>规格要求：</strong></p>
                    <ul style="padding-left: 20px; margin-top: 8px;">
                        <li>厚度：<span class="dimension-label">≥20mm</span></li>
                        <li>材质：人造石/陶瓷</li>
                        <li>边缘：圆角R≥10mm</li>
                    </ul>
                    <div class="material-spec">
                        推荐：杜邦可丽耐/石英石，浅色系提高对比度
                    </div>
                </div>
                
                <div class="material-item">
                    <h4><i class="fas fa-box"></i> 柜体材料</h4>
                    <p><strong>规格要求：</strong></p>
                    <ul style="padding-left: 20px; margin-top: 8px;">
                        <li>材质：防潮实木多层板</li>
                        <li>环保：E0级标准</li>
                        <li>五金：304不锈钢铰链</li>
                    </ul>
                    <div class="material-spec">
                        推荐：18mm防潮板，无尖锐门把手设计
                    </div>
                </div>
                
                <div class="material-item">
                    <h4><i class="fas fa-faucet"></i> 龙头五金</h4>
                    <p><strong>规格要求：</strong></p>
                    <ul style="padding-left: 20px; margin-top: 8px;">
                        <li>材质：304不锈钢</li>
                        <li>把手长度：≥10cm</li>
                        <li>表面：亚光防滑</li>
                    </ul>
                    <div class="material-spec">
                        推荐：单杠杆龙头，配恒温阀（最高49℃）
                    </div>
                </div>
                
                <div class="material-item">
                    <h4><i class="fas fa-hand-rock"></i> 安全扶手</h4>
                    <p><strong>规格要求：</strong></p>
                    <ul style="padding-left: 20px; margin-top: 8px;">
                        <li>材质：304不锈钢</li>
                        <li>直径：32-38mm</li>
                        <li>承载力：≥135kg</li>
                    </ul>
                    <div class="material-spec">
                        安装：M10膨胀螺栓，距墙3.5-4.5cm
                    </div>
                </div>
                
                <div class="material-item">
                    <h4><i class="fas fa-tint"></i> 水管阀门</h4>
                    <p><strong>规格要求：</strong></p>
                    <ul style="padding-left: 20px; margin-top: 8px;">
                        <li>水管：PPR热水管</li>
                        <li>阀门：防烫伤恒温阀</li>
                        <li>接口：标准4分接口</li>
                    </ul>
                    <div class="material-spec">
                        要求：最高水温≤49℃，带安全锁
                    </div>
                </div>
                
                <div class="material-item">
                    <h4><i class="fas fa-lightbulb"></i> 照明系统</h4>
                    <p><strong>规格要求：</strong></p>
                    <ul style="padding-left: 20px; margin-top: 8px;">
                        <li>类型：LED感应灯</li>
                        <li>色温：4000K自然光</li>
                        <li>防护：IP65防水</li>
                    </ul>
                    <div class="material-spec">
                        安装：台面下方，避免阴影，自动感应
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="footer-note">
        <p><strong><i class="fas fa-exclamation-circle"></i> 施工规范依据：</strong> 本适老化洗手池设计和施工需严格遵守以下国家标准：</p>
        <ol style="margin-top:10px; margin-left:20px;">
            <li><strong>《无障碍设计规范》</strong> (GB50763-2012)</li>
            <li><strong>《老年人照料设施建筑设计标准》</strong> (JGJ450-2018)</li>
            <li><strong>《建筑给水排水设计标准》</strong> (GB50015-2019)</li>
        </ol>
        <div class="worker-tip" style="margin-top:15px;">
            <strong>施工检查要点：</strong> 安装完成后需检查：1) 安全扶手承重测试；2) 恒温阀温度测试；3) 紧急呼叫系统功能测试；4) 地面防滑测试。
        </div>
    </div>

    <!-- 洗漱台剖面图放大模态框 -->
    <div class="modal" id="sectionModal">
        <button class="close-modal" id="closeSectionModal">&times;</button>
        <div class="zoom-indicator" id="zoomIndicator">缩放: 100%</div>
        <div class="modal-content">
            <img id="modalImage" src="" alt="洗漱台施工剖面图 - 放大查看">
        </div>
        <div class="image-info" id="imageInfo">适老化洗手池施工剖面图</div>
        <div class="modal-controls">
            <button class="modal-btn" id="zoomInBtn">
                <i class="fas fa-search-plus"></i> 放大
            </button>
            <button class="modal-btn" id="zoomOutBtn">
                <i class="fas fa-search-minus"></i> 缩小
            </button>
            <button class="modal-btn" id="resetZoomBtn">
                <i class="fas fa-sync-alt"></i> 重置
            </button>
        </div>
    </div>

    <!-- 三维模型放大模态框 -->
    <div class="modal" id="modelModal">
        <div class="modal-content" style="width: 95%; height: 95%;">
            <button class="close-modal" id="closeModelModal">&times;</button>
            <iframe id="modalIframe" 
                    title="适老化洗手池三维模型全屏"
                    frameborder="0" 
                    allowfullscreen 
                    mozallowfullscreen="true" 
                    webkitallowfullscreen="true" 
                    allow="autoplay; fullscreen; xr-spatial-tracking" 
                    xr-spatial-tracking 
                    execution-while-out-of-viewport 
                    execution-while-not-rendered 
                    web-share 
                    src="https://sketchfab.com/models/dbb26e1513004995ba7d8379e3af0c66/embed?autospin=1&autostart=1&preload=1"
                    style="width:100%; height:100%; border:none;">
            </iframe>
        </div>
    </div>

    <script>
        // 图片加载处理
        function handleImageLoad() {
            console.log('剖面图加载成功');
            document.getElementById('loadingMessage').style.display = 'none';
            
            // 图片加载成功后，为图片容器添加点击事件
            const imageContainer = document.getElementById('sectionImageContainer');
            const image = document.getElementById('sectionImage');
            
            imageContainer.addEventListener('click', function() {
                openImageModal(image.src);
            });
        }
        
        function handleImageError() {
            console.log('剖面图加载失败，显示备用SVG');
            document.getElementById('loadingMessage').style.display = 'none';
            
            // 创建SVG剖面图作为备用
            const container = document.getElementById('sectionImageContainer');
            const svgNS = "http://www.w3.org/2000/svg";
            
            // 创建SVG元素
            const svg = document.createElementNS(svgNS, "svg");
            svg.setAttribute("width", "100%");
            svg.setAttribute("height", "100%");
            svg.setAttribute("viewBox", "0 0 800 500");
            
            // 背景
            const bg = document.createElementNS(svgNS, "rect");
            bg.setAttribute("x", "0");
            bg.setAttribute("y", "0");
            bg.setAttribute("width", "800");
            bg.setAttribute("height", "500");
            bg.setAttribute("fill", "#f0f5ff");
            svg.appendChild(bg);
            
            // 标题
            const title = document.createElementNS(svgNS, "text");
            title.setAttribute("x", "400");
            title.setAttribute("y", "40");
            title.setAttribute("text-anchor", "middle");
            title.setAttribute("font-size", "24");
            title.setAttribute("font-weight", "bold");
            title.setAttribute("fill", "#2c3e5a");
            title.textContent = "适老化洗手池施工剖面图";
            svg.appendChild(title);
            
            // 副标题
            const subtitle = document.createElementNS(svgNS, "text");
            subtitle.setAttribute("x", "400");
            subtitle.setAttribute("y", "70");
            subtitle.setAttribute("text-anchor", "middle");
            subtitle.setAttribute("font-size", "16");
            subtitle.setAttribute("fill", "#4a6fa5");
            subtitle.textContent = "(备用示意图，请准备详细施工图纸)";
            svg.appendChild(subtitle);
            
            // 绘制洗手池剖面示意图
            // 墙体
            const wall = document.createElementNS(svgNS, "rect");
            wall.setAttribute("x", "150");
            wall.setAttribute("y", "150");
          wall.setAttribute("width", "500");
            wall.setAttribute("height", "300");
            wall.setAttribute("fill", "#e0e0e0");
            wall.setAttribute("stroke", "#999");
            wall.setAttribute("stroke-width", "2");
            svg.appendChild(wall);
            
            // 台面
            const countertop = document.createElementNS(svgNS, "rect");
            countertop.setAttribute("x", "200");
            countertop.setAttribute("y", "200");
            countertop.setAttribute("width", "400");
            countertop.setAttribute("height", "30");
            countertop.setAttribute("fill", "#a8c6df");
            svg.appendChild(countertop);
            
            // 洗手池
            const sink = document.createElementNS(svgNS, "ellipse");
            sink.setAttribute("cx", "400");
            sink.setAttribute("cy", "260");
            sink.setAttribute("rx", "120");
            sink.setAttribute("ry", "40");
            sink.setAttribute("fill", "#c6e2ff");
            sink.setAttribute("stroke", "#4a6fa5");
            sink.setAttribute("stroke-width", "2");
            svg.appendChild(sink);
            
            // 水管
            const pipe = document.createElementNS(svgNS, "rect");
            pipe.setAttribute("x", "390");
            pipe.setAttribute("y", "300");
            pipe.setAttribute("width", "20");
            pipe.setAttribute("height", "120");
            pipe.setAttribute("fill", "#888");
            svg.appendChild(pipe);
            
            // 安全扶手
            const handrail = document.createElementNS(svgNS, "rect");
            handrail.setAttribute("x", "100");
            handrail.setAttribute("y", "180");
            handrail.setAttribute("width", "30");
            handrail.setAttribute("height", "120");
            handrail.setAttribute("fill", "#4a6fa5");
            svg.appendChild(handrail);
            
            // 标注
            const labels = [
                {x: 100, y: 170, text: "安全扶手", color: "#4a6fa5"},
                {x: 400, y: 240, text: "洗手池", color: "#2c3e5a"},
                {x: 400, y: 190, text: "台面(高度75-80cm)", color: "#2c3e5a"},
                {x: 400, y: 380, text: "给排水管", color: "#2c3e5a"},
                {x: 400, y: 450, text: "轮椅进入空间(高≥68cm)", color: "#ff9900"}
            ];
            
            labels.forEach(label => {
                const text = document.createElementNS(svgNS, "text");
                text.setAttribute("x", label.x);
                text.setAttribute("y", label.y);
                text.setAttribute("text-anchor", "middle");
                text.setAttribute("font-size", "14");
                text.setAttribute("font-weight", "bold");
                text.setAttribute("fill", label.color);
                text.textContent = label.text;
                svg.appendChild(text);
            });
            
            // 轮椅空间标注线
            const wheelchairLine = document.createElementNS(svgNS, "line");
            wheelchairLine.setAttribute("x1", "250");
            wheelchairLine.setAttribute("y1", "430");
            wheelchairLine.setAttribute("x2", "550");
            wheelchairLine.setAttribute("y2", "430");
            wheelchairLine.setAttribute("stroke", "#ff9900");
            wheelchairLine.setAttribute("stroke-width", "2");
            wheelchairLine.setAttribute("stroke-dasharray", "5,5");
            svg.appendChild(wheelchairLine);
            
            const wheelchairLine2 = document.createElementNS(svgNS, "line");
            wheelchairLine2.setAttribute("x1", "250");
            wheelchairLine2.setAttribute("y1", "430");
            wheelchairLine2.setAttribute("x2", "250");
            wheelchairLine2.setAttribute("y2", "350");
            wheelchairLine2.setAttribute("stroke", "#ff9900");
            wheelchairLine2.setAttribute("stroke-width", "2");
            wheelchairLine2.setAttribute("stroke-dasharray", "5,5");
            svg.appendChild(wheelchairLine2);
            
            const wheelchairLine3 = document.createElementNS(svgNS, "line");
            wheelchairLine3.setAttribute("x1", "550");
            wheelchairLine3.setAttribute("y1", "430");
            wheelchairLine3.setAttribute("x2", "550");
            wheelchairLine2.setAttribute("y2", "350");
            wheelchairLine3.setAttribute("stroke", "#ff9900");
            wheelchairLine3.setAttribute("stroke-width", "2");
            wheelchairLine3.setAttribute("stroke-dasharray", "5,5");
            svg.appendChild(wheelchairLine3);
            
            // 高度标注
            const heightLine = document.createElementNS(svgNS, "line");
            heightLine.setAttribute("x1", "650");
            heightLine.setAttribute("y1", "200");
            heightLine.setAttribute("x2", "650");
            heightLine.setAttribute("y2", "268");
            heightLine.setAttribute("stroke", "#2c3e5a");
            heightLine.setAttribute("stroke-width", "2");
            svg.appendChild(heightLine);
            
            const heightArrow1 = document.createElementNS(svgNS, "polygon");
            heightArrow1.setAttribute("points", "645,200 655,200 650,195");
            heightArrow1.setAttribute("fill", "#2c3e5a");
            svg.appendChild(heightArrow1);
            
            const heightArrow2 = document.createElementNS(svgNS, "polygon");
            heightArrow2.setAttribute("points", "645,268 655,268 650,273");
            heightArrow2.setAttribute("fill", "#2c3e5a");
            svg.appendChild(heightArrow2);
            
            const heightText = document.createElementNS(svgNS, "text");
            heightText.setAttribute("x", "670");
            heightText.setAttribute("y", "234");
            heightText.setAttribute("text-anchor", "start");
            heightText.setAttribute("font-size", "14");
            heightText.setAttribute("font-weight", "bold");
            heightText.setAttribute("fill", "#2c3e5a");
            heightText.textContent = "68cm";
            svg.appendChild(heightText);
            
            // 将SVG添加到容器
            container.innerHTML = '';
            container.appendChild(svg);
            
            // 为SVG添加点击事件
            container.addEventListener('click', function() {
                // 将SVG转换为数据URL
                const svgString = new XMLSerializer().serializeToString(svg);
                const svgBlob = new Blob([svgString], {type: 'image/svg+xml;charset=utf-8'});
                const svgUrl = URL.createObjectURL(svgBlob);
                openImageModal(svgUrl);
            });
        }
        
        // 洗漱台剖面图模态框控制
        const enlargeSectionBtn = document.getElementById('enlargeSectionBtn');
        const closeSectionModal = document.getElementById('closeSectionModal');
        const sectionModal = document.getElementById('sectionModal');
        const modalImage = document.getElementById('modalImage');
        const zoomInBtn = document.getElementById('zoomInBtn');
        const zoomOutBtn = document.getElementById('zoomOutBtn');
        const resetZoomBtn = document.getElementById('resetZoomBtn');
        const zoomIndicator = document.getElementById('zoomIndicator');
        
        let currentScale = 1;
        let isDragging = false;
        let startX, startY, translateX = 0, translateY = 0;
        
        function openImageModal(imageSrc) {
            modalImage.src = imageSrc;
            sectionModal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
            
            // 重置缩放和位置
            currentScale = 1;
            translateX = 0;
            translateY = 0;
            updateImageTransform();
        }
        
        function updateImageTransform() {
            modalImage.style.transform = `scale(${currentScale}) translate(${translateX}px, ${translateY}px)`;
            zoomIndicator.textContent = `缩放: ${Math.round(currentScale * 100)}%`;
        }
        
        // 图片缩放功能
        zoomInBtn.addEventListener('click', function(e) {
            e.stopPropagation();
            currentScale = Math.min(currentScale * 1.2, 5);
            updateImageTransform();
        });
        
        zoomOutBtn.addEventListener('click', function(e) {
            e.stopPropagation();
            currentScale = Math.max(currentScale / 1.2, 0.2);
            updateImageTransform();
        });
        
        resetZoomBtn.addEventListener('click', function(e) {
            e.stopPropagation();
            currentScale = 1;
            translateX = 0;
            translateY = 0;
            updateImageTransform();
        });
        
        // 鼠标滚轮缩放
        sectionModal.addEventListener('wheel', function(e) {
            e.preventDefault();
            if (e.deltaY < 0) {
                currentScale = Math.min(currentScale * 1.1, 5);
            } else {
                currentScale = Math.max(currentScale / 1.1, 0.2);
            }
            updateImageTransform();
        });
        
        // 图片拖拽功能
        modalImage.addEventListener('mousedown', function(e) {
            if (currentScale <= 1) return;
            
            isDragging = true;
            startX = e.clientX - translateX;
            startY = e.clientY - translateY;
            modalImage.style.cursor = 'grabbing';
        });
        
        document.addEventListener('mousemove', function(e) {
            if (!isDragging) return;
            
            e.preventDefault();
            translateX = e.clientX - startX;
            translateY = e.clientY - startY;
            
            updateImageTransform();
        });
        
        document.addEventListener('mouseup', function() {
            isDragging = false;
            modalImage.style.cursor = 'grab';
        });
        
        // 关闭模态框
        closeSectionModal.addEventListener('click', function() {
            sectionModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        // 点击模态框背景关闭
        sectionModal.addEventListener('click', function(e) {
            if (e.target === sectionModal) {
                sectionModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });
        
        // 三维模型模态框控制
        const enlargeModelBtn = document.getElementById('enlargeModelBtn');
        const closeModelModal = document.getElementById('closeModelModal');
        const modelModal = document.getElementById('modelModal');
        
        enlargeModelBtn.addEventListener('click', function() {
            modelModal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
        });
        
        closeModelModal.addEventListener('click', function() {
            modelModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        modelModal.addEventListener('click', function(e) {
            if (e.target === modelModal) {
                modelModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });
        
        // 页面加载后初始化
        document.addEventListener('DOMContentLoaded', function() {
            console.log('适老化洗手池施工指导页面已加载');
            
            // 为挑战项添加点击效果
            document.querySelectorAll('.challenge-item').forEach(item => {
                item.addEventListener('click', function() {
                    this.style.transform = 'scale(1.02)';
                    setTimeout(() => {
                        this.style.transform = '';
                    }, 200);
                });
            });
            
            // 为材料项添加点击效果
            document.querySelectorAll('.material-item').forEach(item => {
                item.addEventListener('click', function() {
                    this.style.boxShadow = '0 6px 15px rgba(0, 0, 0, 0.1)';
                    setTimeout(() => {
                        this.style.boxShadow = '';
                    }, 300);
                });
            });
            
            // 初始化图片状态
            const img = document.getElementById('sectionImage');
            if (img.complete) {
                if (img.naturalHeight === 0) {
                    handleImageError();
                } else {
                    handleImageLoad();
                }
            } else {
                document.getElementById('loadingMessage').style.display = 'block';
            }
            
            // 为放大按钮添加点击事件
            document.getElementById('enlargeSectionBtn').addEventListener('click', function() {
                const img = document.getElementById('sectionImage');
                if (img.src && img.naturalHeight > 0) {
                    openImageModal(img.src);
                } else {
                    // 如果图片加载失败，尝试使用SVG
                    const container = document.getElementById('sectionImageContainer');
                    const svg = container.querySelector('svg');
                    if (svg) {
                        const svgString = new XMLSerializer().serializeToString(svg);
                        const svgBlob = new Blob([svgString], {type: 'image/svg+xml;charset=utf-8'});
                        const svgUrl = URL.createObjectURL(svgBlob);
                        openImageModal(svgUrl);
                    }
                }
            });
            
            // 键盘快捷键支持
            document.addEventListener('keydown', function(e) {
                // ESC键关闭模态框
                if (e.key === 'Escape') {
                    if (sectionModal.style.display === 'flex') {
                        sectionModal.style.display = 'none';
                        document.body.style.overflow = 'auto';
                    }
                    if (modelModal.style.display === 'flex') {
                        modelModal.style.display = 'none';
                        document.body.style.overflow = 'auto';
                    }
                }
                
                // +/- 键缩放图片
                if (sectionModal.style.display === 'flex') {
                    if (e.key === '+' || e.key === '=') {
                        e.preventDefault();
                        currentScale = Math.min(currentScale * 1.2, 5);
                        updateImageTransform();
                    } else if (e.key === '-' || e.key === '_') {
                        e.preventDefault();
                        currentScale = Math.max(currentScale / 1.2, 0.2);
                        updateImageTransform();
                    } else if (e.key === '0') {
                        e.preventDefault();
                        currentScale = 1;
                        translateX = 0;
                        translateY = 0;
                        updateImageTransform();
                    }
                }
            });
        });
    </script>
</body>
</html>
