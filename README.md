#洗漱台
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>适老化洗手池施工指南 - 工人专用版</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
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
            background: linear-gradient(to right, #2c5282, #4a6fa5);
            color: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(44, 82, 130, 0.2);
        }
        
        .header h1 {
            font-size: 2.2rem;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        .header-subtitle {
            font-size: 1.1rem;
            max-width: 900px;
            margin: 0 auto 15px;
            opacity: 0.9;
        }
        
        .worker-badge {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background-color: #f39c12;
            color: white;
            padding: 8px 20px;
            border-radius: 25px;
            font-weight: bold;
            font-size: 1rem;
            margin-top: 10px;
            box-shadow: 0 3px 8px rgba(243, 156, 18, 0.3);
        }
        
        /* 主内容区域 - 三维模型和剖面图 */
        .model-section-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
            margin-bottom: 30px;
        }
        
        @media (max-width: 1100px) {
            .model-section-container {
                grid-template-columns: 1fr;
            }
        }
        
        .model-section, .section-container {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            height: 600px;
            display: flex;
            flex-direction: column;
        }
        
        .section-title {
            background-color: #4a6fa5;
            color: white;
            padding: 18px 20px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-shrink: 0;
        }
        
        .section-title i {
            font-size: 1.4rem;
        }
        
        .model-container, .section-image-container {
            width: 100%;
            height: 100%;
            position: relative;
            background-color: #f0f5ff;
            flex-grow: 1;
            overflow: hidden;
        }
        
        .model-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        /* Sketchfab嵌入包装器样式 */
        .sketchfab-embed-wrapper {
            width: 100%;
            height: 100%;
            position: relative;
        }
        
        .sketchfab-embed-wrapper iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .sketchfab-embed-wrapper p {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.9);
            margin: 0;
            padding: 5px;
            font-size: 12px;
            text-align: center;
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
        
        .section-image-container:hover img {
            transform: scale(1.02);
        }
        
        /* 统一的其他区域大小 */
        .uniform-section {
            background: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            height: auto;
            min-height: 500px;
            margin-bottom: 25px;
        }
        
        .section-heading {
            color: #2c3e5a;
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 12px;
            border-bottom: 2px solid #ff9900;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        /* 施工重点区域 */
        .construction-highlights {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .highlight-item {
            background: #f8fafc;
            padding: 20px;
            border-radius: 10px;
            border-left: 5px solid #4a6fa5;
        }
        
        .highlight-item h4 {
            color: #2c3e5a;
            margin-bottom: 12px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .highlight-item p {
            color: #5a6c7d;
            margin-bottom: 10px;
            font-size: 1rem;
        }
        
        .material-tag {
            display: inline-block;
            background-color: #e8f4fc;
            color: #2c5282;
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 0.9rem;
            margin-right: 8px;
            margin-bottom: 8px;
            border: 1px solid #b8d4f0;
        }
        
        /* 材料规格表格 */
        .materials-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        
        .materials-table th {
            background-color: #4a6fa5;
            color: white;
            padding: 15px;
            text-align: left;
            font-weight: 600;
        }
        
        .materials-table td {
            padding: 14px;
            border-bottom: 1px solid #eaeaea;
        }
        
        .materials-table tr:nth-child(even) {
            background-color: #f8fafc;
        }
        
        .materials-table tr:hover {
            background-color: #f0f5ff;
        }
        
        /* 施工步骤 */
        .construction-steps {
            counter-reset: step-counter;
            margin-top: 20px;
        }
        
        .step-item {
            position: relative;
            padding: 20px 0 20px 70px;
            border-bottom: 1px dashed #ddd;
            margin-bottom: 10px;
        }
        
        .step-item:before {
            counter-increment: step-counter;
            content: counter(step-counter);
            position: absolute;
            left: 0;
            top: 15px;
            background-color: #4a6fa5;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        .step-title {
            color: #2c3e5a;
            margin-bottom: 8px;
            font-size: 1.2rem;
        }
        
        .step-tools {
            background-color: #fff8e1;
            padding: 10px;
            border-radius: 6px;
            margin-top: 10px;
            font-size: 0.95rem;
        }
        
        .step-tools i {
            color: #f39c12;
            margin-right: 5px;
        }
        
        /* 安装要点 */
        .installation-points {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .point-item {
            background: #f8fafc;
            padding: 20px;
            border-radius: 10px;
            border-top: 4px solid #27ae60;
        }
        
        .point-item h4 {
            color: #2c3e5a;
            margin-bottom: 12px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .warning {
            background-color: #fff2f2;
            border-left: 4px solid #e74c3c;
            padding: 15px;
            border-radius: 6px;
            margin-top: 20px;
        }
        
        .warning-title {
            color: #e74c3c;
            font-weight: bold;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        /* 工具清单 */
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .tool-item {
            background: #f0f5ff;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            border: 1px solid #d1dceb;
        }
        
        .tool-item i {
            font-size: 2rem;
            color: #4a6fa5;
            margin-bottom: 10px;
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
            transition: all 0.3s;
        }
        
        .section-zoom-btn:hover {
            background: rgba(255, 153, 0, 1);
            transform: scale(1.05);
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
        
        .footer-note {
            background-color: #fff8e1;
            border-left: 5px solid #f39c12;
            padding: 20px;
            border-radius: 10px;
            margin-top: 30px;
            font-size: 0.95rem;
            color: #7d6608;
        }
        
        .footer-note strong {
            color: #d68910;
        }
        
        /* 响应式调整 */
        @media (max-width: 768px) {
            .uniform-section, .model-section, .section-container {
                padding: 15px;
            }
            
            .construction-highlights, .installation-points {
                grid-template-columns: 1fr;
            }
            
            .section-heading {
                font-size: 1.3rem;
            }
        }
        
        /* 图片加载状态样式 */
        .image-loading {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100%;
            color: #4a6fa5;
        }
        
        .image-loading i {
            font-size: 3rem;
            margin-bottom: 15px;
            animation: spin 1.5s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-tools"></i> 适老化洗手池施工指南</h1>
        <p class="header-subtitle">工人专用版 - 三维模型、剖面图与施工要点详解</p>
        <p style="font-size:0.95rem; margin-top:5px; opacity:0.8;">适老化设计 | 无障碍施工 | 材料规格明确 | 施工步骤详细</p>
        <div class="worker-badge">
            <i class="fas fa-hard-hat"></i> 施工人员专用指南
        </div>
    </div>

    <!-- 三维模型和剖面图区域 - 大小相同 -->
    <div class="model-section-container">
        <div class="model-section">
            <div class="section-title">
                <span><i class="fas fa-cube"></i> 三维模型展示</span>
                <button class="section-zoom-btn" id="enlargeModelBtn">
                    <i class="fas fa-expand"></i> 全屏查看
                </button>
            </div>
            <div class="model-container">
                <!-- 更新后的三维模型 -->
                <div class="sketchfab-embed-wrapper"> 
                    <iframe title="浴室洗手池" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/f4c002003a6b45408c7fd5586e435926/embed?autospin=1&preload=1"> 
                    </iframe> 
                    <p style="font-size: 13px; font-weight: normal; margin: 5px; color: #4A4A4A;"> 
                        <a href="https://sketchfab.com/3d-models/f4c002003a6b45408c7fd5586e435926?utm_medium=embed&utm_campaign=share-popup&utm_content=f4c002003a6b45408c7fd5586e435926" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;"> 浴室洗手池 </a> by 
                        <a href="https://sketchfab.com/Feng-Che-Shu?utm_medium=embed&utm_campaign=share-popup&utm_content=f4c002003a6b45408c7fd5586e435926" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;"> 风车树下 </a> on 
                        <a href="https://sketchfab.com?utm_medium=embed&utm_campaign=share-popup&utm_content=f4c002003a6b45408c7fd5586e435926" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;">Sketchfab</a>
                    </p>
                </div>
            </div>
        </div>

        <div class="section-container">
            <div class="section-title">
                <span><i class="fas fa-cut"></i> 洗漱台剖面图</span>
                <button class="section-zoom-btn" id="enlargeSectionBtn">
                    <i class="fas fa-search-plus"></i> 放大查看
                </button>
            </div>
            <div class="section-image-container" id="sectionImageContainer">
                <!-- 图片已更新为您提供的新链接 -->
                <img id="sectionImage" 
                     src="https://files.imagetourl.net/uploads/1769133403711-4dc6afc0-af5e-4b75-848d-c7278f6f4a6a.png" 
                     alt="适老化洗漱台剖面图 - 包含尺寸标注和材料说明"
                     onload="handleImageLoad()"
                     onerror="handleImageError()">
                <div class="image-overlay">
                    <i class="fas fa-search-plus"></i>
                    <h3>点击查看详细剖面图</h3>
                    <p>包含尺寸标注、材料标注和安装要点</p>
                </div>
                <div id="loadingMessage" class="image-loading" style="display: flex; position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: #f0f5ff;">
                    <i class="fas fa-spinner"></i>
                    <h3>正在加载洗漱台剖面图...</h3>
                </div>
                <div id="errorMessage" class="image-placeholder" style="display: none; position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: #f0f5ff;">
                    <i class="fas fa-exclamation-triangle"></i>
                    <h3>洗漱台剖面图加载失败</h3>
                    <p>请按以下步骤操作：</p>
                    <div style="margin-top: 15px; text-align: left; background: #f0f8ff; padding: 15px; border-radius: 8px;">
                        <p><strong>解决方法：</strong></p>
                        <ol style="margin-left: 20px; margin-top: 10px;">
                            <li>将洗漱台剖面图保存为 <strong>section_image.png</strong></li>
                            <li>放入与此HTML文件相同的文件夹中</li>
                            <li>刷新页面即可显示</li>
                        </ol>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 施工重点区域 -->
    <div class="uniform-section">
        <h2 class="section-heading">
            <i class="fas fa-exclamation-circle"></i> 施工重点与材料标注
        </h2>
        
        <div class="construction-highlights">
            <div class="highlight-item">
                <h4><i class="fas fa-ruler-combined"></i> 关键尺寸要求</h4>
                <p><strong>台面高度：</strong>75-80cm（适合坐姿与站姿）</p>
                <p><strong>下方净空：</strong>高≥68cm，深≥48cm（轮椅可进入）</p>
                <p><strong>安全扶手：</strong>距地75-85cm，承载力≥135kg</p>
                <p><strong>前方空间：</strong>直径≥150cm（轮椅回转）</p>
                <div style="margin-top: 10px;">
                    <span class="material-tag">304不锈钢扶手</span>
                    <span class="material-tag">防潮多层板</span>
                    <span class="material-tag">人造石台面</span>
                </div>
            </div>
            
            <div class="highlight-item">
                <h4><i class="fas fa-bolt"></i> 水电安装要点</h4>
                <p><strong>给水管道：</strong>左热右冷，安装防烫伤恒温阀</p>
                <p><strong>排水管道：</strong>防臭存水弯，坡度1%-2%</p>
                <p><strong>电源插座：</strong>防水型，距台面30cm以上</p>
                <p><strong>紧急按钮：</strong>防水型，距地40-50cm</p>
                <div style="margin-top: 10px;">
                    <span class="material-tag">PPR给水管</span>
                    <span class="material-tag">PVC排水管</span>
                    <span class="material-tag">IP66防水插座</span>
                </div>
            </div>
            
            <div class="highlight-item">
                <h4><i class="fas fa-shield-alt"></i> 安全施工要求</h4>
                <p><strong>圆角处理：</strong>所有台面边缘R≥10mm圆角</p>
                <p><strong>防滑地面：</strong>防滑系数≥0.6，无积水</p>
                <p><strong>牢固固定：</strong>柜体与墙体使用膨胀螺栓固定</p>
                <p><strong>无障碍设计：</strong>无门槛，无尖锐凸起</p>
                <div style="margin-top: 10px;">
                    <span class="material-tag">圆角修边条</span>
                    <span class="material-tag">防滑地砖</span>
                    <span class="material-tag">M10膨胀螺栓</span>
                </div>
            </div>
        </div>
        
        <div class="warning">
            <div class="warning-title">
                <i class="fas fa-exclamation-triangle"></i> 重要安全提示
            </div>
            <p>1. 所有安全扶手必须固定于承重墙或实心墙体，严禁固定于轻质隔墙</p>
            <p>2. 恒温阀最高出水温度设定不得超过49℃，防止烫伤</p>
            <p>3. 紧急呼叫按钮必须连接至24小时有人值守的护理站</p>
            <p>4. 所有电气安装必须由持证电工操作，符合安全规范</p>
        </div>
    </div>

    <!-- 材料规格表 -->
    <div class="uniform-section">
        <h2 class="section-heading">
            <i class="fas fa-clipboard-list"></i> 材料清单与规格
        </h2>
        
        <table class="materials-table">
            <thead>
                <tr>
                    <th width="20%">材料名称</th>
                    <th width="25%">规格型号</th>
                    <th width="20%">技术要求</th>
                    <th width="35%">施工注意事项</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>洗手池柜体</strong></td>
                    <td>防潮实木多层板，厚度≥18mm</td>
                    <td>E0级环保标准，防水涂层</td>
                    <td>悬空安装，底部离地≥68cm，使用M8膨胀螺栓固定于墙体</td>
                </tr>
                <tr>
                    <td><strong>人造石台面</strong></td>
                    <td>厚度≥12mm，浅色系</td>
                    <td>抗菌涂层，边缘R10mm圆角</td>
                    <td>与柜体使用专用胶粘接，台面与墙面缝隙≤3mm，用防霉硅胶密封</td>
                </tr>
                <tr>
                    <td><strong>安全扶手</strong></td>
                    <td>304不锈钢，直径35-40mm</td>
                    <td>亚光防滑处理，承载力≥135kg</td>
                    <td>固定于承重墙，距墙间隙3.5-4.5cm，使用M10膨胀螺栓，间距≤40cm</td>
                </tr>
                <tr>
                    <td><strong>单杠杆龙头</strong></td>
                    <td>陶瓷阀芯，低铅铜主体</td>
                    <td>开启角度≤90°，操作力≤5N</td>
                    <td>冷热水管左热右冷，安装防烫伤恒温阀，阀前加装角阀</td>
                </tr>
                <tr>
                    <td><strong>排水组件</strong></td>
                    <td>防臭存水弯，PVC材质</td>
                    <td>水封深度≥50mm，排水管径≥50mm</td>
                    <td>排水坡度1%-2%，存水弯下方留检修口，连接处用专用胶密封</td>
                </tr>
                <tr>
                    <td><strong>辅助照明</strong></td>
                    <td>LED感应灯带，IP65防水</td>
                    <td>色温4000K，照度≥150lx</td>
                    <td>安装于台面下方，离地55-60cm，感应范围1-2m，连接至开关面板</td>
                </tr>
            </tbody>
        </table>
    </div>

    <!-- 施工步骤 -->
    <div class="uniform-section">
        <h2 class="section-heading">
            <i class="fas fa-list-ol"></i> 施工步骤详解
        </h2>
        
        <div class="construction-steps">
            <div class="step-item">
                <div class="step-title">第一步：现场定位与放线</div>
                <p>根据设计图纸在墙面标出洗手池中心线、台面高度线（75-80cm）、安全扶手位置线（75-85cm）和柜体安装线。</p>
                <div class="step-tools">
                    <i class="fas fa-toolbox"></i> <strong>使用工具：</strong>激光水平仪、卷尺、墨斗、记号笔
                </div>
            </div>
            
            <div class="step-item">
                <div class="step-title">第二步：水电管线预埋</div>
                <p>按定位开槽预埋冷热水管（左热右冷）、排水管（φ50mm）、电源线（2.5mm²）和紧急呼叫线。水管试压0.8MPa保持30分钟无渗漏。</p>
                <div class="step-tools">
                    <i class="fas fa-toolbox"></i> <strong>使用工具：</strong>开槽机、PPR热熔器、PVC胶、试压泵
                </div>
            </div>
            
            <div class="step-item">
                <div class="step-title">第三步：墙体加固与柜体安装</div>
                <p>在柜体固定位置安装加固板，使用M8膨胀螺栓将柜体固定于墙体。检查柜体水平度，误差≤2mm。</p>
                <div class="step-tools">
                    <i class="fas fa-toolbox"></i> <strong>使用工具：</strong>冲击钻、水平尺、扳手、螺丝刀
                </div>
            </div>
            
            <div class="step-item">
                <div class="step-title">第四步：台面安装与打磨</div>
                <p>将人造石台面放置于柜体上，调整水平后使用专用胶固定。对台面边缘进行R10mm圆角打磨抛光。</p>
                <div class="step-tools">
                    <i class="fas fa-toolbox"></i> <strong>使用工具：</strong>角磨机、抛光机、结构胶枪、水平尺
                </div>
            </div>
            
            <div class="step-item">
                <div class="step-title">第五步：五金件与安全扶手安装</div>
                <p>安装单杠杆龙头、皂液器，连接冷热水管。安装安全扶手，使用M10膨胀螺栓固定于承重墙，测试承载力。</p>
                <div class="step-tools">
                    <i class="fas fa-toolbox"></i> <strong>使用工具：</strong>扳手、管钳、冲击钻、扭矩扳手
                </div>
            </div>
            
            <div class="step-item">
                <div class="step-title">第六步：电气与辅助设施安装</div>
                <p>安装防水插座、感应灯带和紧急呼叫按钮。连接线路，测试各项功能正常。</p>
                <div class="step-tools">
                    <i class="fas fa-toolbox"></i> <strong>使用工具：</strong>电工钳、螺丝刀、万用表、测电笔
                </div>
            </div>
            
            <div class="step-item">
                <div class="step-title">第七步：收边密封与清洁</div>
                <p>使用防霉硅胶对台面与墙面接缝、柜体与地面接缝进行密封。清洁现场，检查所有功能。</p>
                <div class="step-tools">
                    <i class="fas fa-toolbox"></i> <strong>使用工具：</strong>硅胶枪、刮板、清洁剂、抹布
                </div>
            </div>
        </div>
    </div>

    <!-- 安装要点与工具 -->
    <div class="uniform-section">
        <h2 class="section-heading">
            <i class="fas fa-cogs"></i> 安装要点与工具清单
        </h2>
        
        <div class="installation-points">
            <div class="point-item">
                <h4><i class="fas fa-anchor"></i> 安全扶手安装要点</h4>
                <p>1. 必须固定于实心墙或承重墙，钻孔深度≥70mm</p>
                <p>2. 使用M10膨胀螺栓，每个扶手至少4个固定点</p>
                <p>3. 安装后测试：施加135kg垂直向下力，无松动、变形</p>
                <p>4. 扶手表面为亚光防滑处理，直径35-40mm</p>
            </div>
            
            <div class="point-item">
                <h4><i class="fas fa-tint"></i> 给排水安装要点</h4>
                <p>1. 冷热水管间距150mm，左热右冷</p>
                <p>2. 安装恒温阀，设定最高温度49℃</p>
                <p>3. 排水管坡度1%-2%，存水弯水封≥50mm</p>
                <p>4. 所有接口严密，通水试验无渗漏</p>
            </div>
            
            <div class="point-item">
                <h4><i class="fas fa-lightbulb"></i> 电气安装要点</h4>
                <p>1. 电源插座为IP66防水型，带防溅盒</p>
                <p>2. 紧急呼叫按钮连接至24小时值班室</p>
                <p>3. 感应灯带照度≥150lx，感应距离1-2m</p>
                <p>4. 所有线路穿管保护，接地可靠</p>
            </div>
        </div>
        
        <h3 style="margin-top: 30px; margin-bottom: 15px; color: #2c3e5a;">
            <i class="fas fa-toolbox"></i> 主要施工工具清单
        </h3>
        
        <div class="tools-grid">
            <div class="tool-item">
                <i class="fas fa-ruler"></i>
                <div>激光水平仪</div>
            </div>
            <div class="tool-item">
                <i class="fas fa-hammer"></i>
                <div>冲击钻</div>
            </div>
            <div class="tool-item">
                <i class="fas fa-bolt"></i>
                <div>PPR热熔器</div>
            </div>
            <div class="tool-item">
                <i class="fas fa-screwdriver"></i>
                <div>扭矩扳手</div>
            </div>
            <div class="tool-item">
                <i class="fas fa-tachometer-alt"></i>
                <div>试压泵</div>
            </div>
            <div class="tool-item">
                <i class="fas fa-cut"></i>
                <div>角磨机</div>
            </div>
            <div class="tool-item">
                <i class="fas fa-plug"></i>
                <div>万用表</div>
            </div>
            <div class="tool-item">
                <i class="fas fa-paint-roller"></i>
                <div>硅胶枪</div>
            </div>
        </div>
    </div>

    <div class="footer-note">
        <p><strong><i class="fas fa-clipboard-check"></i> 施工验收标准：</strong></p>
        <ol style="margin-top: 10px; margin-left: 20px;">
            <li>所有尺寸符合设计要求，误差≤3mm</li>
            <li>安全扶手承载力测试≥135kg，无松动</li>
            <li>给水管道试压0.8MPa/30分钟无渗漏</li>
            <li>排水通畅，无积水，存水弯水封正常</li>
            <li>电气设备功能正常，接地可靠</li>
            <li>台面边缘圆角处理，无尖锐棱角</li>
            <li>紧急呼叫按钮响应正常，信号通畅</li>
        </ol>
    </div>

    <!-- 洗漱台剖面图放大模态框 -->
    <div class="modal" id="sectionModal">
        <button class="close-modal" id="closeSectionModal">&times;</button>
        <div class="modal-content">
            <img id="modalImage" src="" alt="洗漱台剖面图 - 放大查看">
        </div>
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
                    src="https://sketchfab.com/models/f4c002003a6b45408c7fd5586e435926/embed?autospin=1&preload=1"
                    style="width:100%; height:100%; border:none;">
            </iframe>
        </div>
    </div>

    <script>
        // 图片加载处理
        function handleImageLoad() {
            console.log('剖面图加载成功');
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
            console.log('剖面图加载失败，尝试加载本地图片');
            const img = document.getElementById('sectionImage');
            const errorDiv = document.getElementById('errorMessage');
            const loadingDiv = document.getElementById('loadingMessage');
            
            // 如果还没有尝试加载本地图片
            if (!img.dataset.triedLocal) {
                img.dataset.triedLocal = true;
                loadingDiv.style.display = 'flex';
                errorDiv.style.display = 'none';
                img.src = 'section_image.png';
            } else {
                // 已经尝试了本地图片，仍然失败
                loadingDiv.style.display = 'none';
                errorDiv.style.display = 'block';
            }
        }
        
        // 洗漱台剖面图模态框控制
        const enlargeSectionBtn = document.getElementById('enlargeSectionBtn');
        const closeSectionModal = document.getElementById('closeSectionModal');
        const sectionModal = document.getElementById('sectionModal');
        const modalImage = document.getElementById('modalImage');
        const zoomInBtn = document.getElementById('zoomInBtn');
        const zoomOutBtn = document.getElementById('zoomOutBtn');
        const resetZoomBtn = document.getElementById('resetZoomBtn');
        
        let currentScale = 1;
        
        function openImageModal(imageSrc) {
            modalImage.src = imageSrc;
            sectionModal.style.display = 'flex';
            document.body.style.overflow = 'hidden';
            
            // 重置缩放
            currentScale = 1;
            updateImageTransform();
        }
        
        function updateImageTransform() {
            modalImage.style.transform = `scale(${currentScale})`;
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
            console.log('适老化洗手池施工指南页面已加载');
            
            // 为材料标签添加点击效果
            document.querySelectorAll('.material-tag').forEach(tag => {
                tag.addEventListener('click', function() {
                    this.style.backgroundColor = '#d1e7ff';
                    setTimeout(() => {
                        this.style.backgroundColor = '#e8f4fc';
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
                document.getElementById('loadingMessage').style.display = 'flex';
            }
            
            // 为放大按钮添加点击事件
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
                
                // 在模态框中，+/- 键控制缩放
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
                        updateImageTransform();
                    }
                }
            });
        });
    </script>
</body>
</html>
