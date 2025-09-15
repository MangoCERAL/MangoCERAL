<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>崔文红 | AI产品经理</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 24px;
            padding: 40px;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            animation: rotate 20s linear infinite;
        }

        .header-content {
            position: relative;
            z-index: 2;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        h1 {
            font-size: 3.5rem;
            font-weight: 800;
            color: white;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            background: linear-gradient(45deg, #fff, #e0e7ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            font-size: 1.4rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 20px;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            color: white;
            font-size: 1.1rem;
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 25px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }

        .section-title {
            font-size: 2rem;
            font-weight: 700;
            color: #2d3748;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .skill-card {
            background: linear-gradient(135deg, #f7fafc, #edf2f7);
            border-radius: 16px;
            padding: 25px;
            text-align: center;
            border: 2px solid transparent;
            transition: all 0.3s ease;
        }

        .skill-card:hover {
            border-color: #667eea;
            transform: scale(1.05);
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
        }

        .skill-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            display: block;
        }

        .projects-table {
            width: 100%;
            border-collapse: collapse;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .projects-table th {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 20px;
            text-align: left;
            font-weight: 600;
            font-size: 1.1rem;
        }

        .projects-table td {
            padding: 20px;
            border-bottom: 1px solid #e2e8f0;
            vertical-align: top;
        }

        .projects-table tr:hover {
            background: linear-gradient(135deg, #f7fafc, #edf2f7);
        }

        .highlight-text {
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 600;
        }

        .education-item, .award-item {
            background: linear-gradient(135deg, #f0f7ff, #e6f3ff);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 15px;
            border-left: 5px solid #667eea;
        }

        .core-abilities {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .ability-card {
            background: white;
            border-radius: 16px;
            padding: 25px;
            border: 2px solid #e2e8f0;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .ability-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(135deg, #667eea, #764ba2);
        }

        .ability-card:hover {
            border-color: #667eea;
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(102, 126, 234, 0.2);
        }

        .footer {
            text-align: center;
            color: white;
            padding: 30px;
            font-style: italic;
        }

        .tech-badge {
            display: inline-block;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            margin: 3px;
            font-weight: 500;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }
            
            .section {
                padding: 20px;
            }
            
            .projects-table {
                font-size: 0.9rem;
            }
            
            .projects-table th,
            .projects-table td {
                padding: 12px;
            }
        }

        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .floating-circle {
            position: absolute;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            animation: float 6s ease-in-out infinite;
        }

        .floating-circle:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-circle:nth-child(2) {
            width: 120px;
            height: 120px;
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }

        .floating-circle:nth-child(3) {
            width: 60px;
            height: 60px;
            top: 40%;
            left: 80%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-circle"></div>
        <div class="floating-circle"></div>
        <div class="floating-circle"></div>
    </div>

    <div class="container">
        <div class="header">
            <div class="header-content">
                <h1>崔文红</h1>
                <div class="subtitle">AI应用落地 · 跨行业解决方案 · 全栈产品设计</div>
                <div class="contact-info">
                    <div class="contact-item">
                        <span>📧</span>
                        <span>2900780588@qq.com</span>
                    </div>
                    <div class="contact-item">
                        <span>📱</span>
                        <span>15536959658</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">教育背景</h2>
            <div class="education-item">
                <strong>山西财经大学</strong> · 本科 · 全日制
            </div>
            <div class="education-item">
                <strong>上海财经大学</strong> · 硕士 · 在职研究生
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">核心能力</h2>
            <div class="core-abilities">
                <div class="ability-card">
                    <h3 class="highlight-text">产品全周期管理</h3>
                    <p>主导0-1产品搭建，覆盖需求分析、原型设计至上线迭代</p>
                </div>
                <div class="ability-card">
                    <h3 class="highlight-text">技术整合专家</h3>
                    <p>AIGC应用（ChatGPT/Stable Diffusion）及多模态AI（语音克隆/情绪分析）</p>
                    <p>AR/3D交互开发（如裸眼3D H5实现）</p>
                </div>
                <div class="ability-card">
                    <h3 class="highlight-text">数据驱动优化</h3>
                    <p>精通SQL及用户行为分析，通过数据提升产品竞争力</p>
                </div>
                <div class="ability-card">
                    <h3 class="highlight-text">效率突破</h3>
                    <p>自动化流程重构（如减少90%人力操作）</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">重点项目</h2>
            <table class="projects-table">
                <thead>
                    <tr>
                        <th>项目名称</th>
                        <th>关键成果</th>
                        <th>技术亮点</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>雅虎闲置OMS</strong></td>
                        <td>• 自动化下单系统节省90%人力<br>• 3天处理2000+订单</td>
                        <td><span class="tech-badge">接口解析</span><span class="tech-badge">品类重构</span></td>
                    </tr>
                    <tr>
                        <td><strong>全国学生AI心理监测</strong></td>
                        <td>• 集成多模态AI评估系统<br>• 茂名试点→全国推广</td>
                        <td><span class="tech-badge">语音识别</span><span class="tech-badge">BI看板</span></td>
                    </tr>
                    <tr>
                        <td><strong>AR体验HIF机制H5</strong></td>
                        <td>• 开发裸眼3D交互H5，超1000位医生使用</td>
                        <td><span class="tech-badge">AR多模态视频</span></td>
                    </tr>
                    <tr>
                        <td><strong>医象限小程序</strong></td>
                        <td>• 为默沙东提供学术直播平台<br>• 注册用户183+，浏览量4145+</td>
                        <td><span class="tech-badge">直播系统</span><span class="tech-badge">会员体系</span></td>
                    </tr>
                    <tr>
                        <td><strong>健教云小程序</strong></td>
                        <td>• 累计服务20万+用户<br>• 单篇文章阅读量最高13.5万</td>
                        <td><span class="tech-badge">健康宣教系统</span><span class="tech-badge">KOL展示</span></td>
                    </tr>
                </tbody>
            </table>
        </div>

        <div class="section">
            <h2 class="section-title">技能矩阵</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <span class="skill-icon">🗂️</span>
                    <h3>产品工具</h3>
                    <p>Axure | 墨刀 | TAPD/Jira | 飞书协作</p>
                </div>
                <div class="skill-card">
                    <span class="skill-icon">🤖</span>
                    <h3>AI技术栈</h3>
                    <p>ChatGPT | Stable Diffusion | Midjourney | 语音克隆</p>
                </div>
                <div class="skill-card">
                    <span class="skill-icon">📊</span>
                    <h3>数据分析</h3>
                    <p>SQL | BI看板 | 用户行为埋点</p>
                </div>
                <div class="skill-card">
                    <span class="skill-icon">🚀</span>
                    <h3>方法论</h3>
                    <p>PMP认证项目管理 | 敏捷开发 | Kano模型</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">荣誉奖项</h2>
            <div class="award-item">
                <span class="highlight-text">🏆 2025上海AI切磋大会 冠军</span>（AI实战赛道）
            </div>
            <div class="award-item">
                <span class="highlight-text">🏆 2024 AI FOR CODE创意赛 优秀奖</span>（应用赛道）
            </div>
        </div>

        <div class="footer">
            <p><strong>最后更新：2025年9月</strong> · <a href="https://github.com/username" style="color: #e0e7ff;">查看更多案例</a></p>
            <p style="margin-top: 10px; font-size: 0.9rem; opacity: 0.8;">数据来源：个人简历文档，引用请注明出处</p>
        </div>
    </div>
</body>
</html>
