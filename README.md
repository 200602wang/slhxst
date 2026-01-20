# slhxst
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>适老化洗漱池设计 - 带图片放大功能</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background-color: #f5f9ff;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            padding: 30px 20px;
            margin-bottom: 30px;
            background: linear-gradient(to right, #4a6fa5, #2c3e5a);
            color: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(44, 62, 90, 0.2);
        }
        
        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        .header p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 15px;
            opacity: 0.9;
        }
        
        .elderly-badge {
            display: inline-block;
            background-color: #ff9900;
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            font-weight: bold;
            font-size: 1.1rem;
            margin-top: 10px;
            box-shadow: 0 3px 8px rgba(255, 153, 0, 0.3);
        }
        
        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 40px;
        }
        
        @media (max-width: 1100px) {
            .main-content {
                grid-template-columns: 1fr;
            }
        }
        
        .model-section {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .section-title {
            background-color: #4a6fa5;
            color: white;
            padding: 20px;
            font-size: 1.4rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .section-title i {
            font-size: 1.5rem;
        }
        
        .model-container {
            width: 100%;
            height: 550px;
            position: relative;
            background-color: #f0f5ff;
        }
        
        .model-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .model-enlarge-btn {
            position: absolute;
            bottom: 15px;
            right: 15px;
            background: rgba(255, 153, 0, 0.9);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 8px;
            z-index: 10;
        }
        
        .model-enlarge-btn:hover {
            background: rgba(255, 153, 0, 1);
        }
        
        .section-container {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .section-image-container {
            width: 100%;
            height: 550px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: #f8f9fa;
            position: relative;
            cursor: pointer;
            overflow: hidden;
        }
        
        .section-image-container:hover .image-overlay {
            opacity: 1;
        }
        
        .section-image-container img {
            max-width: 100%;
            max-height: 100%;
            object-fit: contain;
            transition: transform 0.3s ease;
        }
        
        .section-image-container:hover img {
            transform: scale(1.02);
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
        
        .image-overlay i {
            font-size: 3rem;
            margin-bottom: 15px;
        }
        
        .image-placeholder {
            text-align: center;
            padding: 30px;
            color: #666;
        }
        
        .image-placeholder i {
            font-size: 4rem;
            color: #ccc;
            margin-bottom: 20px;
        }
        
        .elderly-challenges {
            margin-top: 30px;
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .challenges-title {
            color: #2c3e5a;
            font-size: 1.8rem;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 3px solid #ff9900;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .challenges-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .challenge-item {
            background: #f8fafc;
            padding: 25px;
            border-radius: 12px;
            border-left: 5px solid #4a6fa5;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .challenge-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }
        
        .challenge-item h4 {
            color: #2c3e5a;
            margin-bottom: 15px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .challenge-item h4 i {
            color: #ff9900;
        }
        
        .challenge-item p {
            color: #5a6c7d;
            margin-bottom: 15px;
        }
        
        .solution {
            background-color: #e8f4fc;
            padding: 15px;
            border-radius: 8px;
            margin-top: 15px;
            border-left: 3px solid #27ae60;
        }
        
        .solution strong {
            color: #27ae60;
        }
        
        .info-sections {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        @media (max-width: 768px) {
            .info-sections {
                grid-template-columns: 1fr;
            }
        }
        
        .info-box {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .info-box.construction {
            border-top: 6px solid #e74c3c;
        }
        
        .info-box.materials {
            border-top: 6px solid #27ae60;
        }
        
        .info-box h3 {
            font-size: 1.6rem;
            margin-bottom: 25px;
            color: #2c3e5a;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .note-list {
            list-style-type: none;
        }
        
        .note-list li {
            padding: 15px 0;
            padding-left: 35px;
            border-bottom: 1px solid #f0f0f0;
            position: relative;
        }
        
        .note-list li:last-child {
            border-bottom: none;
        }
        
        .note-list li:before {
            content: "✓";
            color: #4a6fa5;
            font-size: 1.2rem;
            font-weight: bold;
            position: absolute;
            left: 0;
            top: 15px;
        }
        
        .elderly-highlight {
            background-color: #fff8e1;
            padding: 3px 8px;
            border-radius: 4px;
            font-weight: bold;
            color: #d68910;
        }
        
        .materials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 20px;
        }
        
        .material-item {
            background: #f8fafc;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #27ae60;
        }
        
        .material-item h4 {
            color: #2c3e5a;
            margin-bottom: 10px;
            font-size: 1.2rem;
        }
        
        .footer-note {
            background-color: #fff8e1;
            border-left: 5px solid #f39c12;
            padding: 25px;
            border-radius: 12px;
            margin-top: 40px;
            font-size: 1rem;
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
            gap: 20px;
        }
        
        .modal-btn {
            background: rgba(0, 0, 0, 0.7);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            display: flex;
            align-items: center;
            gap: 10px;
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
            padding: 10px 15px;
            border-radius: 5px;
            font-size: 0.9rem;
        }
        
        .zoom-indicator {
            position: absolute;
            top: 20px;
            left: 30px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 10px 15px;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .image-error {
            text-align: center;
            padding: 30px;
            color: #666;
        }
        
        .section-zoom-btn {
            background: rgba(255, 153, 0, 0.9);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: background 0.3s;
        }
        
        .section-zoom-btn:hover {
            background: rgba(255, 153, 0, 1);
        }
    </style>
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-sink"></i> 适老化洗手池设计与无障碍解决方案</h1>
        <p>专为老年人设计的三维模型展示与施工指南 | 解决老年人如厕洗漱不便问题</p>
        <p style="font-size:1rem; margin-top:5px; opacity:0.8;">模型数据：98.7k 三角面 | 49.5k 顶点 | 许可证：CC Attribution</p>
        <div class="elderly-badge">
            <i class="fas fa-wheelchair"></i> 无障碍适老化设计
        </div>
    </div>

    <div class="main-content">
        <div class="model-section">
            <div class="section-title">
                <span><i class="fas fa-cube"></i> 三维模型展示</span>
                <button class="section-zoom-btn" id="enlargeModelBtn">
                    <i class="fas fa-expand"></i> 放大查看
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
            <div style="padding: 15px; color: #666; font-size: 0.9rem; text-align: center;">
                使用鼠标拖拽旋转模型，滚轮缩放。点击右上角按钮可全屏查看。
            </div>
        </div>

        <div class="section-container">
            <div class="section-title">
                <span><i class="fas fa-cut"></i> 适老化剖面结构详图</span>
                <button class="section-zoom-btn" id="enlargeSectionBtn">
                    <i class="fas fa-search-plus"></i> 放大查看
                </button>
            </div>
            <div class="section-image-container" id="sectionImageContainer">
                <img id="sectionImage" 
                     src="https://image2url.com/r2/default/images/1768819927982-247b9674-06f4-422e-8488-77281d523438.png" 
                     alt="适老化洗手池剖面结构详图"
                     onload="handleImageLoad()"
                     onerror="handleImageError()">
                <div class="image-overlay">
                    <i class="fas fa-search-plus"></i>
                    <h3>点击查看大图</h3>
                    <p>点击图片或使用右上角按钮放大查看细节</p>
                </div>
                <div id="loadingMessage" class="image-placeholder" style="display: none; position: absolute;">
                    <i class="fas fa-spinner fa-spin"></i>
                    <h3>正在加载剖面图...</h3>
                </div>
                <div id="errorMessage" class="image-placeholder" style="position: absolute;">
                    <i class="fas fa-exclamation-triangle"></i>
                    <h3>剖面图加载失败</h3>
                    <p>无法从链接加载图片</p>
                    <div style="margin-top: 20px; text-align: left; background: #f0f8ff; padding: 15px; border-radius: 8px;">
                        <p>解决方法：</p>
                        <ol style="margin-left: 20px; margin-top: 10px;">
                            <li>将剖面图保存为 <strong>section_image.png</strong></li>
                            <li>放入与此HTML文件相同的文件夹中</li>
                            <li>刷新页面即可显示</li>
                        </ol>
                    </div>
                </div>
            </div>
            <div style="padding: 15px; color: #666; font-size: 0.9rem; text-align: center;">
                点击图片可放大查看细节。支持鼠标滚轮缩放和拖拽查看。
            </div>
        </div>
    </div>

    <div class="elderly-challenges">
        <h2 class="challenges-title">
            <i class="fas fa-exclamation-triangle"></i> 老年人使用洗手池常见困难与解决方案
        </h2>
        
        <div class="challenges-grid">
            <div class="challenge-item">
                <h4><i class="fas fa-wheelchair"></i> 轮椅使用者接近困难</h4>
                <p>传统洗手池下方空间不足，轮椅无法靠近，导致老年人需要费力前倾，增加摔倒风险。</p>
                <div class="solution">
                    <strong>适老化解决方案：</strong> 悬空式设计，台面下方净空高度≥68cm，深度≥48cm，确保轮椅可轻松进入。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-ruler-vertical"></i> 高度不适导致腰背劳损</h4>
                <p>固定高度的洗手池不适合不同身高的老年人，长期使用导致腰背疼痛和疲劳。</p>
                <div class="solution">
                    <strong>适老化解决方案：</strong> 安装高度75-80cm（含台面），镜面可倾斜或高度可调，适应坐姿和站姿使用。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-hand-paper"></i> 手部力量不足操作困难</h4>
                <p>传统旋转式水龙头对手部关节炎患者操作困难，无法精确控制水温和流量。</p>
                <div class="solution">
                    <strong>适老化解决方案：</strong> 采用单杠杆或感应式龙头，减少操作力度，并安装防烫伤恒温阀。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-balance-scale"></i> 缺乏支撑增加摔倒风险</h4>
                <p>洗手池周边缺乏安全扶手，老年人在洗漱时无处借力，容易失去平衡。</p>
                <div class="solution">
                    <strong>适老化解决方案：</strong> 两侧安装L型安全扶手，承载力≥135kg，表面防滑处理，提供稳定支撑。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-eye"></i> 视力下降导致使用不便</h4>
                <p>老年人视力下降，难以看清传统水龙头位置、皂液器，易造成使用错误。</p>
                <div class="solution">
                    <strong>适老化解决方案：</strong> 高对比度色彩设计，感应式自动出水，语音提示功能，台面下方增加照明。
                </div>
            </div>
            
            <div class="challenge-item">
                <h4><i class="fas fa-first-aid"></i> 紧急情况无法求助</h4>
                <p>老年人在洗手间发生意外时，无法及时呼叫帮助，延误救援时间。</p>
                <div class="solution">
                    <strong>适老化解决方案：</strong> 安装防水紧急呼叫按钮，连接至护理站或家人手机，配备延迟响应防止误触。
                </div>
            </div>
        </div>
    </div>

    <div class="info-sections">
        <div class="info-box construction">
            <h3><i class="fas fa-tools"></i> 适老化施工关键注意事项</h3>
            <ul class="note-list">
                <li><strong>无障碍空间规划</strong>：洗手池前方预留直径≥150cm的轮椅回转空间，侧面接近空间≥80cm。<span class="elderly-highlight">适老化重点</span></li>
                <li><strong>安全扶手安装</strong>：使用膨胀螺栓固定于承重墙，高度75-85cm，距墙间隙3.5-4.5cm。<span class="elderly-highlight">适老化重点</span></li>
                <li><strong>防滑地面处理</strong>：地面使用防滑系数≥0.6的防滑砖，排水坡度1%-2%，确保无积水。</li>
                <li><strong>水温安全控制</strong>：安装防烫伤恒温阀，最高出水温度不超过49℃，避免烫伤风险。</li>
                <li><strong>紧急呼叫系统</strong>：洗手池旁安装防水紧急呼叫按钮，高度距地40-50cm，连接至护理站。</li>
                <li><strong>圆角安全处理</strong>：所有台面边缘做圆角处理（R≥10mm），避免尖角造成伤害。</li>
                <li><strong>辅助照明配置</strong>：台面下方安装感应灯带，避免阴影，提高夜间使用安全性。</li>
            </ul>
        </div>

        <div class="info-box materials">
            <h3><i class="fas fa-clipboard-list"></i> 适老化专用材料说明</h3>
            <div class="materials-grid">
                <div class="material-item">
                    <h4><i class="fas fa-gem"></i> 台面材料</h4>
                    <p><strong>优选材料：</strong>人造石（亚克力）、陶瓷<br>
                    <strong>适老化要求：</strong>浅色系提高对比度，抗菌涂层，边缘圆角处理。</p>
                </div>
                <div class="material-item">
                    <h4><i class="fas fa-box"></i> 柜体材料</h4>
                    <p><strong>优选材料：</strong>防潮实木多层板、不锈钢<br>
                    <strong>适老化要求：</strong>悬空设计，无尖锐门把手，E0级环保标准。</p>
                </div>
                <div class="material-item">
                    <h4><i class="fas fa-faucet"></i> 五金配件</h4>
                    <p><strong>关键部件：</strong>单杠杆龙头、恒温阀、安全扶手<br>
                    <strong>适老化要求：</strong>304不锈钢材质，亚光防滑处理，把手长度≥10cm。</p>
                </div>
                <div class="material-item">
                    <h4><i class="fas fa-paint-roller"></i> 表面处理</h4>
                    <p><strong>柜体涂层：</strong>抗菌烤漆、防指纹涂层<br>
                    <strong>适老化要求：</strong>高对比度色彩，防眩光哑光表面，易清洁。</p>
                </div>
            </div>
        </div>
    </div>

    <div class="footer-note">
        <p><strong><i class="fas fa-exclamation-triangle"></i> 重要提示：</strong> 适老化洗手池的设计和施工需严格遵守《无障碍设计规范》(GB50763-2012)及《老年人照料设施建筑设计标准》(JGJ450-2018)。</p>
        <ol style="margin-top:10px; margin-left:20px;">
            <li>本页面三维模型由 Sketchfab 用户 <strong>风车树下</strong> 创建与分享，遵循 <strong>CC Attribution</strong> 许可协议。</li>
            <li>剖面图需保存为 <strong>section_image.png</strong> 并放置于此HTML文件同一目录下，页面将自动加载显示。</li>
            <li>适老化设计应充分考虑使用者个体差异，建议施工前进行现场适应性测试。</li>
        </ol>
    </div>

    <!-- 剖面图放大模态框 -->
    <div class="modal" id="sectionModal">
        <button class="close-modal" id="closeSectionModal">&times;</button>
        <div class="zoom-indicator" id="zoomIndicator">缩放: 100%</div>
        <div class="modal-content">
            <img id="modalImage" src="" alt="放大后的适老化洗漱池剖面图">
        </div>
        <div class="image-info" id="imageInfo">适老化洗漱池剖面结构详图</div>
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
            <button class="modal-btn" id="rotateBtn">
                <i class="fas fa-redo"></i> 旋转
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
            document.getElementById('errorMessage').style.display = 'none';
            document.getElementById('loadingMessage').style.display = 'none';
            
            // 图片加载成功后，为图片容器添加点击事件
            const imageContainer = document.getElementById('sectionImageContainer');
            const image = document.getElementById('sectionImage');
            
            imageContainer.addEventListener('click', function() {
                openImageModal(image.src);
            });
        }
        
        function handleImageError() {
            document.getElementById('errorMessage').style.display = 'block';
            document.getElementById('loadingMessage').style.display = 'none';
            
            // 尝试加载本地图片
            const img = document.getElementById('sectionImage');
            img.src = 'section_image.png';
        }
        
        // 剖面图模态框控制
        const enlargeSectionBtn = document.getElementById('enlargeSectionBtn');
        const closeSectionModal = document.getElementById('closeSectionModal');
        const sectionModal = document.getElementById('sectionModal');
        const modalImage = document.getElementById('modalImage');
        const zoomInBtn = document.getElementById('zoomInBtn');
        const zoomOutBtn = document.getElementById('zoomOutBtn');
        const resetZoomBtn = document.getElementById('resetZoomBtn');
        const rotateBtn = document.getElementById('rotateBtn');
        const zoomIndicator = document.getElementById('zoomIndicator');
        
        let currentScale = 1;
        let currentRotation = 0;
        
        function openImageModal(imageSrc) {
            modalImage.src = imageSrc;
            sectionModal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
            
            // 重置缩放和旋转
            currentScale = 1;
            currentRotation = 0;
            updateImageTransform();
        }
        
        function updateImageTransform() {
            modalImage.style.transform = `scale(${currentScale}) rotate(${currentRotation}deg)`;
            zoomIndicator.textContent = `缩放: ${Math.round(currentScale * 100)}%`;
            
            // 如果旋转了，显示旋转角度
            if (currentRotation !== 0) {
                zoomIndicator.textContent += ` | 旋转: ${currentRotation}°`;
            }
        }
        
        // 图片缩放功能
        zoomInBtn.addEventListener('click', function(e) {
            e.stopPropagation();
            currentScale = Math.min(currentScale * 1.2, 5); // 最大放大5倍
            updateImageTransform();
        });
        
        zoomOutBtn.addEventListener('click', function(e) {
            e.stopPropagation();
            currentScale = Math.max(currentScale / 1.2, 0.2); // 最小缩小到0.2倍
            updateImageTransform();
        });
        
        resetZoomBtn.addEventListener('click', function(e) {
            e.stopPropagation();
            currentScale = 1;
            currentRotation = 0;
            updateImageTransform();
        });
        
        rotateBtn.addEventListener('click', function(e) {
            e.stopPropagation();
            currentRotation += 90;
            if (currentRotation >= 360) currentRotation = 0;
            updateImageTransform();
        });
        
        // 鼠标滚轮缩放
        sectionModal.addEventListener('wheel', function(e) {
            e.preventDefault();
            if (e.deltaY < 0) {
                // 向上滚动，放大
                currentScale = Math.min(currentScale * 1.1, 5);
            } else {
                // 向下滚动，缩小
                currentScale = Math.max(currentScale / 1.1, 0.2);
            }
            updateImageTransform();
        });
        
        // 图片拖拽功能
        let isDragging = false;
        let startX, startY, translateX = 0, translateY = 0;
        
        modalImage.addEventListener('mousedown', function(e) {
            if (currentScale <= 1) return; // 只有放大后才允许拖拽
            
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
            
            modalImage.style.transform = `scale(${currentScale}) rotate(${currentRotation}deg) translate(${translateX}px, ${translateY}px)`;
        });
        
        document.addEventListener('mouseup', function() {
            isDragging = false;
            modalImage.style.cursor = 'grab';
        });
        
        // 关闭模态框
        closeSectionModal.addEventListener('click', function() {
            sectionModal.style.display = 'none';
            document.body.style.overflow = 'auto';
            
            // 重置拖拽位置
            translateX = 0;
            translateY = 0;
        });
        
        // 点击模态框背景关闭
        sectionModal.addEventListener('click', function(e) {
            if (e.target === sectionModal) {
                sectionModal.style.display = 'none';
                document.body.style.overflow = 'auto';
                
                // 重置拖拽位置
                translateX = 0;
                translateY = 0;
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
            console.log('适老化洗手池页面已加载');
            
            // 为挑战项添加点击效果
            document.querySelectorAll('.challenge-item').forEach(item => {
                item.addEventListener('click', function() {
                    this.style.transform = 'scale(1.02)';
                    setTimeout(() => {
                        this.style.transform = '';
                    }, 200);
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
            
            // 为放大按钮添加点击事件（备用，图片容器已有点击事件）
            document.getElementById('enlargeSectionBtn').addEventListener('click', function() {
                const img = document.getElementById('sectionImage');
                if (img.src && img.naturalHeight > 0) {
                    openImageModal(img.src);
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
                        currentRotation = 0;
                        updateImageTransform();
                    } else if (e.key === 'r' || e.key === 'R') {
                        e.preventDefault();
                        currentRotation += 90;
                        if (currentRotation >= 360) currentRotation = 0;
                        updateImageTransform();
                    }
                }
            });
        });
    </script>
</body>
</html>
