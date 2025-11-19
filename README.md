<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>现代简洁宣传网页</title>
    <style>
        /* 基础样式重置 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Helvetica Neue', Arial, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
        /* 容器样式 */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 导航栏样式 */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: #2c3e50;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: #555;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: #3498db;
        }
        
        /* Banner样式 */
        .banner {
            background: linear-gradient(135deg, #3498db, #2c3e50);
            color: white;
            padding: 100px 0;
            text-align: center;
            margin-bottom: 60px;
        }
        
        .banner-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .banner h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            font-weight: 700;
        }
        
        .banner p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .cta-button {
            display: inline-block;
            background-color: white;
            color: #3498db;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        }
        
        /* 活动亮点/产品优势模块 */
        .features {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: #2c3e50;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: #7f8c8d;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            width: 60px;
            height: 60px;
            background-color: #e8f4fc;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            color: #3498db;
            font-size: 24px;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #2c3e50;
        }
        
        .feature-card p {
            color: #7f8c8d;
        }
        
        /* 图片展示区 */
        .gallery {
            padding: 80px 0;
            background-color: white;
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
        }
        
        .gallery-item {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
            height: 250px;
        }
        
        .gallery-item:hover {
            transform: scale(1.03);
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        /* 行动召唤区 */
        .action-section {
            padding: 80px 0;
            text-align: center;
            background-color: #f8f9fa;
        }
        
        .action-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        .action-button {
            display: inline-flex;
            align-items: center;
            background-color: white;
            color: #3498db;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
        }
        
        .action-button:hover {
            background-color: #3498db;
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(52, 152, 219, 0.3);
        }
        
        .action-button i {
            margin-right: 8px;
        }
        
        /* 页脚样式 */
        footer {
            background-color: #2c3e50;
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: #ecf0f1;
        }
        
        .footer-column p, .footer-column a {
            color: #bdc3c7;
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column a:hover {
            color: #3498db;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #34495e;
            color: #95a5a6;
            font-size: 0.9rem;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
                padding: 15px 0;
            }
            
            .nav-links {
                margin-top: 15px;
            }
            
            .nav-links li {
                margin-left: 15px;
                margin-right: 15px;
            }
            
            .banner h1 {
                font-size: 2.2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .action-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .action-button {
                width: 80%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <!-- 顶部导航 -->
    <header>
        <div class="container nav-container">
            <div class="logo">品牌名称</div>
            <ul class="nav-links">
                <li><a href="#">首页</a></li>
                <li><a href="#">关于我们</a></li>
                <li><a href="#">产品服务</a></li>
                <li><a href="#">活动资讯</a></li>
                <li><a href="#">联系我们</a></li>
            </ul>
        </div>
    </header>

    <!-- 首页大Banner -->
    <section class="banner">
        <div class="container banner-content">
            <h1>创意改变生活</h1>
            <p>我们致力于提供最优质的产品与服务，让每一个创意都能成为现实</p>
            <a href="#" class="cta-button">了解更多</a>
        </div>
    </section>

    <!-- 活动亮点/产品优势 -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>我们的优势</h2>
                <p>我们专注于提供高品质的产品与服务，满足您的各种需求</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">✓</div>
                    <h3>专业品质</h3>
                    <p>我们拥有专业团队，确保每一个项目都能达到最高标准，满足客户的期望。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⏱</div>
                    <h3>高效服务</h3>
                    <p>我们注重效率，承诺在最短时间内完成项目交付，节省您宝贵的时间。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">❤</div>
                    <h3>客户至上</h3>
                    <p>我们始终将客户需求放在首位，提供个性化解决方案和优质的售后服务。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 图片展示区 -->
    <section class="gallery">
        <div class="container">
            <div class="section-title">
                <h2>作品展示</h2>
                <p>欣赏我们过往的精彩项目与成果</p>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1558655146-9f40138edfeb?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="项目展示1">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1559028012-481c04fa702d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="项目展示2">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1559028012-481c04fa702d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="项目展示3">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1558655146-9f40138edfeb?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="项目展示4">
                </div>
            </div>
        </div>
    </section>

    <!-- 行动召唤区 -->
    <section class="action-section">
        <div class="container">
            <div class="section-title">
                <h2>立即联系我们</h2>
                <p>如果您对我们的产品或服务感兴趣，请通过以下方式与我们取得联系</p>
            </div>
            <div class="action-buttons">
                <a href="weixin://" class="action-button">
                    <i>💬</i> 微信联系
                </a>
                <a href="tel:13800138000" class="action-button">
                    <i>📞</i> 电话咨询
                </a>
                <a href="https://example.com" class="action-button" target="_blank">
                    <i>🌐</i> 访问官网
                </a>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>关于我们</h3>
                    <p>我们是一家专注于创意设计与产品开发的公司，致力于为客户提供最优质的解决方案。</p>
                </div>
                <div class="footer-column">
                    <h3>联系方式</h3>
                    <p>电话: 138-0013-8000</p>
                    <p>邮箱: contact@example.com</p>
                    <p>地址: 北京市朝阳区某某街道123号</p>
                </div>
                <div class="footer-column">
                    <h3>快速链接</h3>
                    <a href="#">首页</a>
                    <a href="#">关于我们</a>
                    <a href="#">产品服务</a>
                    <a href="#">活动资讯</a>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 品牌名称. 保留所有权利.</p>
            </div>
        </div>
    </footer>
</body>
</html>
