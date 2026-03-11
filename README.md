<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>STEM Careers Survey - Research Presentation</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #1a1a2e;
            color: #eee;
            overflow: hidden;
        }
        
        .slide {
            display: none;
            width: 100vw;
            height: 100vh;
            padding: 50px 80px;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            position: relative;
        }
        
        .slide.active {
            display: flex;
            flex-direction: column;
            animation: fadeIn 0.5s;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .slide-number {
            position: absolute;
            top: 30px;
            right: 50px;
            color: #e94560;
            font-weight: bold;
            font-size: 18px;
        }
        
        h1 {
            font-size: 52px;
            color: #e94560;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
        h2 {
            font-size: 38px;
            color: #0f3460;
            background: #e94560;
            padding: 15px 30px;
            display: inline-block;
            margin-bottom: 30px;
            border-radius: 8px;
        }
        
        h3 {
            font-size: 28px;
            color: #e94560;
            margin-bottom: 20px;
            border-bottom: 3px solid #e94560;
            padding-bottom: 10px;
        }
        
        p, li {
            font-size: 22px;
            line-height: 1.6;
            margin-bottom: 15px;
            color: #ddd;
        }
        
        .subtitle {
            font-size: 26px;
            color: #aaa;
            margin-bottom: 40px;
        }
        
        .meta-box {
            background: #0f3460;
            padding: 20px 30px;
            border-radius: 10px;
            margin-top: auto;
            display: flex;
            gap: 50px;
        }
        
        .meta-item strong {
            color: #e94560;
            display: block;
            font-size: 14px;
            text-transform: uppercase;
        }
        
        .content-split {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            flex: 1;
        }
        
        .chart-box {
            background: #0f3460;
            padding: 40px;
            border-radius: 15px;
            text-align: center;
        }
        
        .big-number {
            font-size: 80px;
            font-weight: bold;
            color: #e94560;
            display: block;
        }
        
        .stat-label {
            font-size: 20px;
            color: #aaa;
        }
        
        ul {
            list-style: none;
            padding-left: 0;
        }
        
        ul li::before {
            content: "▸ ";
            color: #e94560;
            font-weight: bold;
            margin-right: 10px;
        }
        
        .highlight {
            background: #e94560;
            color: white;
            padding: 5px 15px;
            border-radius: 5px;
            font-weight: bold;
        }
        
        .two-col {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin-top: 30px;
        }
        
        .info-card {
            background: #0f3460;
            padding: 25px;
            border-radius: 10px;
            border-left: 5px solid #e94560;
        }
        
        .info-card h4 {
            color: #e94560;
            font-size: 20px;
            margin-bottom: 10px;
        }
        
        .info-card p {
            font-size: 18px;
            margin: 0;
        }
        
        .findings-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            margin-top: 30px;
        }
        
        .finding {
            background: #0f3460;
            padding: 30px;
            border-radius: 12px;
            position: relative;
        }
        
        .finding-num {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 48px;
            color: #e94560;
            opacity: 0.3;
            font-weight: bold;
        }
        
        .finding h4 {
            color: #e94560;
            font-size: 22px;
            margin-bottom: 10px;
        }
        
        .finding p {
            font-size: 16px;
            color: #bbb;
            margin: 0;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            font-size: 18px;
        }
        
        th {
            background: #e94560;
            color: white;
            padding: 15px;
            text-align: left;
        }
        
        td {
            padding: 15px;
            border-bottom: 1px solid #333;
        }
        
        tr:hover {
            background: #0f3460;
        }
        
        .conclusion-box {
            background: #0f3460;
            border: 3px solid #e94560;
            border-radius: 15px;
            padding: 40px;
            margin-top: 30px;
        }
        
        .conclusion-box h3 {
            border: none;
            margin-top: 0;
        }
        
        .nav-hint {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0,0,0,0.7);
            padding: 10px 30px;
            border-radius: 20px;
            font-size: 14px;
            color: #aaa;
            z-index: 1000;
        }
        
        .thank-you {
            text-align: center;
            justify-content: center;
            align-items: center;
        }
        
        .thank-you h1 {
            font-size: 80px;
            margin-bottom: 30px;
        }
        
        .thank-you p {
            font-size: 28px;
            color: #aaa;
        }
    </style>
</head>
<body>

    <!-- Slide 1: Title -->
    <div class="slide active">
        <div class="slide-number">1/10</div>
        <h1>STEM Careers</h1>
        <p class="subtitle">Research Findings: Student Career Interests in Kazakhstan</p>
        <div style="margin-top: 50px;">
            <p style="font-size: 24px; font-style: italic; color: #aaa;">
                "What STEM careers are today's high school students in Kazakhstan interested in, 
                and what factors influence their choices?"
            </p>
        </div>
        <div class="meta-box">
            <div class="meta-item">
                <strong>Class</strong>
                11E, NSPM School
            </div>
            <div class="meta-item">
                <strong>Location</strong>
                Almaty, Kazakhstan
            </div>
            <div class="meta-item">
                <strong>Participants</strong>
                13 Students
            </div>
            <div class="meta-item">
                <strong>Date</strong>
                March 2025
            </div>
        </div>
    </div>

    <!-- Slide 2: Research Overview -->
    <div class="slide">
        <div class="slide-number">2/10</div>
        <h2>Research Overview</h2>
        <div class="content-split">
            <div>
                <h3>Demographics</h3>
                <ul>
                    <li><span class="highlight">13 students</span> from Class 11E</li>
                    <li>Age range: <strong>16-18 years old</strong></li>
                    <li>Gender: 9 male (69%), 3 female (23%), 1 other (8%)</li>
                    <li>School: NSPM, Bukhar-Zhirau 36, Almaty</li>
                </ul>
                
                <h3 style="margin-top: 30px;">Methodology</h3>
                <ul>
                    <li>Survey method: <strong>9 questions</strong></li>
                    <li>Data collection: In-class questionnaire</li>
                    <li>Analysis: Quantitative data visualization</li>
                </ul>
            </div>
            <div class="chart-box">
                <span class="big-number">13</span>
                <p class="stat-label">Total Respondents</p>
                <div style="margin-top: 30px; text-align: left;">
                    <p style="font-size: 16px; color: #888; margin-bottom: 10px;">Gender Distribution</p>
                    <div style="background: #333; height: 30px; border-radius: 15px; overflow: hidden; display: flex;">
                        <div style="width: 69%; background: #3498db; display: flex; align-items: center; justify-content: center; font-size: 12px;">69% Male</div>
                        <div style="width: 23%; background: #e94560; display: flex; align-items: center; justify-content: center; font-size: 12px;">23% Female</div>
                        <div style="width: 8%; background: #f39c12; display: flex; align-items: center; justify-content: center; font-size: 12px;">8%</div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Slide 3: Survey Questions -->
    <div class="slide">
        <div class="slide-number">3/10</div>
        <h2>Survey Questions</h2>
        <div class="content-full">
            <p style="margin-bottom: 30px; color: #aaa;">Nine comprehensive questions covering demographics, interests, influences, and perceptions:</p>
            
            <div class="two-col">
                <div class="info-card">
                    <h4>Q1-Q3: Background & Interests</h4>
                    <p>Gender, preferred STEM field, and career intention</p>
                </div>
                <div class="info-card">
                    <h4>Q4-Q6: Influences & Confidence</h4>
                    <p>Sources of influence, self-confidence, and gender equality perceptions</p>
                </div>
                <div class="info-card">
                    <h4>Q7-Q8: Motivation & Participation</h4>
                    <p>Reasons for STEM choice and extracurricular involvement</p>
                </div>
                <div class="info-card">
                    <h4>Q9: Success Factors</h4>
                    <p>Key factors believed necessary for STEM success</p>
                </div>
            </div>
            
            <div class="highlight" style="margin-top: 40px; text-align: center; padding: 20px;">
                All questions designed to answer our main research question about interests and influencing factors
            </div>
        </div>
    </div>

    <!-- Slide 4: Key Finding 1 - IT Dominates -->
    <div class="slide">
        <div class="slide-number">4/10</div>
        <h2>Key Finding 1: IT Dominates Interest</h2>
        <div class="content-split">
            <div>
                <div class="chart-box" style="margin-bottom: 30px;">
                    <span class="big-number">76.9%</span>
                    <p class="stat-label">chose IT/Software Development</p>
                    <p style="margin-top: 15px; font-size: 16px; color: #888;">10 out of 13 students</p>
                </div>
                
                <div style="background: #0f3460; padding: 20px; border-radius: 10px;">
                    <p style="margin: 0; font-size: 18px;"><strong>Other fields:</strong></p>
                    <p style="margin: 5px 0; font-size: 16px;">• Engineering: 2 students (15.4%)</p>
                    <p style="margin: 5px 0; font-size: 16px;">• Mathematics: 1 student (7.7%)</p>
                    <p style="margin: 5px 0; font-size: 16px;">• No interest in pure Science</p>
                </div>
            </div>
            <div>
                <h3>Why IT is #1</h3>
                <ul>
                    <li>Global tech industry growth</li>
                    <li>High salary prospects</li>
                    <li>Remote work opportunities</li>
                    <li>Startup culture influence</li>
                    <li>Visible success stories (Google, Apple, etc.)</li>
                </ul>
                <div class="highlight" style="margin-top: 30px;">
                    IT outperforms all other STEM fields combined by 5:1 ratio
                </div>
            </div>
        </div>
    </div>

    <!-- Slide 5: Key Finding 2 - Career Intent -->
    <div class="slide">
        <div class="slide-number">5/10</div>
        <h2>Key Finding 2: Strong Career Intent</h2>
        <div class="content-split">
            <div>
                <div class="chart-box">
                    <span class="big-number">84.7%</span>
                    <p class="stat-label">plan to pursue STEM careers</p>
                    <p style="margin-top: 20px; font-size: 18px;">
                        <span style="color: #2ecc71;">● 46%</span> Yes, definitely<br>
                        <span style="color: #3498db;">● 38%</span> Probably yes<br>
                        <span style="color: #f39c12;">● 8%</span> Not sure yet<br>
                        <span style="color: #e94560;">● 8%</span> Probably not
                    </p>
                </div>
                <p style="margin-top: 20px; text-align: center; font-size: 18px; color: #2ecc71;">
                    ✓ Not a single student said "No, definitely not"
                </p>
            </div>
            <div>
                <h3>What This Means</h3>
                <ul>
                    <li>Class 11E is <strong>ambitious and future-focused</strong></li>
                    <li>STEM education is effectively motivating students</li>
                    <li>Students see viable career paths in STEM</li>
                    <li>Only small uncertainty (16%) about career choice</li>
                </ul>
                <div class="info-card" style="margin-top: 30px;">
                    <h4>Implication</h4>
                    <p>This high intent suggests strong engagement with STEM subjects and positive perception of STEM job market in Kazakhstan.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Slide 6: Key Finding 3 - Social Influence -->
    <div class="slide">
        <div class="slide-number">6/10</div>
        <h2>Key Finding 3: Friends are #1 Influence</h2>
        <div class="content-full">
            <p style="margin-bottom: 30px;">Multiple answers allowed — students could select all applicable sources of influence:</p>
            
            <table>
                <tr>
                    <th>Influence Source</th>
                    <th>Mentions</th>
                    <th>Percentage</th>
                    <th>Rank</th>
                </tr>
                <tr style="background: rgba(233, 69, 96, 0.2);">
                    <td><strong>Friends</strong></td>
                    <td>8</td>
                    <td>61.5%</td>
                    <td>🥇 1st</td>
                </tr>
                <tr>
                    <td>Parents / Family</td>
                    <td>6</td>
                    <td>46.2%</td>
                    <td>🥈 2nd (tied)</td>
                </tr>
                <tr>
                    <td>Teacher at school</td>
                    <td>6</td>
                    <td>46.2%</td>
                    <td>🥈 2nd (tied)</td>
                </tr>
                <tr>
                    <td>Books or magazines</td>
                    <td>6</td>
                    <td>46.2%</td>
                    <td>🥈 2nd (tied)</td>
                </tr>
                <tr>
                    <td>Internet / YouTube</td>
                    <td>4</td>
                    <td>30.8%</td>
                    <td>5th</td>
                </tr>
                <tr>
                    <td>TV shows or movies</td>
                    <td>4</td>
                    <td>30.8%</td>
                    <td>5th</td>
                </tr>
            </table>
            
            <div class="highlight" style="margin-top: 30px; text-align: center;">
                Peer culture plays a crucial role in career decisions — friends outrank family and teachers
            </div>
        </div>
    </div>

    <!-- Slide 7: Key Finding 4 - Confidence & Participation -->
    <div class="slide">
        <div class="slide-number">7/10</div>
        <h2>Key Finding 4: Confidence & Participation</h2>
        <div class="two-col" style="margin-top: 50px;">
            <div class="chart-box">
                <span class="big-number">77%</span>
                <p class="stat-label">attended STEM activities</p>
                <div style="margin-top: 20px; text-align: left; font-size: 16px;">
                    <p>• 46% — Yes, regularly</p>
                    <p>• 31% — Yes, a few times</p>
                    <p>• 23% — No, but would like to</p>
                </div>
                <p style="margin-top: 15px; color: #2ecc71; font-size: 16px;">
                    High engagement with extracurricular STEM
                </p>
            </div>
            <div class="chart-box">
                <span class="big-number">46.2%</span>
                <p class="stat-label">feel VERY confident in STEM</p>
                <div style="margin-top: 20px; text-align: left; font-size: 16px;">
                    <p>• 46% — Very confident</p>
                    <p>• 8% — Somewhat confident</p>
                    <p>• 23% — Not very confident</p>
                    <p>• 15% — Not confident at all</p>
                    <p>• 8% — Neutral</p>
                </div>
                <p style="margin-top: 15px; color: #f39c12; font-size: 16px;">
                    Room for confidence-building remains
                </p>
            </div>
        </div>
    </div>

    <!-- Slide 8: Additional Insights -->
    <div class="slide">
        <div class="slide-number">8/10</div>
        <h2>Additional Insights</h2>
        <div class="content-split">
            <div>
                <h3>Gender Equality Perception</h3>
                <div class="chart-box" style="margin-bottom: 20px;">
                    <span class="big-number">53.8%</span>
                    <p class="stat-label">believe STEM is equally accessible</p>
                </div>
                <ul style="font-size: 18px;">
                    <li>54% — Yes, completely equal</li>
                    <li>23% — No, boys have more opportunities</li>
                    <li>15% — Mostly equal, some exceptions</li>
                    <li>8% — Never thought about this</li>
                </ul>
            </div>
            <div>
                <h3>Motivation & Success Factors</h3>
                <div class="info-card" style="margin-bottom: 20px;">
                    <h4>Main Reason for STEM Choice</h4>
                    <p><span class="highlight">58%</span> enjoy problem-solving & logical thinking<br>
                    <span style="color: #aaa;">25% — Parents/teachers recommendation<br>
                    17% — Good salary and job opportunities</span></p>
                </div>
                <div class="info-card">
                    <h4>Key to Success in STEM</h4>
                    <p><span class="highlight">53.8%</span> Natural talent/intelligence<br>
                    <span style="color: #aaa;">30.8% — Hard work and dedication<br>
                    7.7% — Good teachers and mentors<br>
                    7.7% — Passion and interest</span></p>
                </div>
            </div>
        </div>
    </div>

    <!-- Slide 9: Conclusions -->
    <div class="slide">
        <div class="slide-number">9/10</div>
        <h2>Conclusions</h2>
        <div class="findings-grid">
            <div class="finding">
                <div class="finding-num">1</div>
                <h4>IT/Software Dominates</h4>
                <p>76.9% preference reflects global tech trends among youth. Traditional science fields lack interest.</p>
            </div>
            <div class="finding">
                <div class="finding-num">2</div>
                <h4>Strong STEM Intent</h4>
                <p>84.7% plan STEM careers. Class 11E is ambitious, future-focused, and sees opportunities.</p>
            </div>
            <div class="finding">
                <div class="finding-num">3</div>
                <h4>Peer Influence is Critical</h4>
                <p>Friends rank #1 influence (61.5%), surpassing family and teachers. Peer culture shapes choices.</p>
            </div>
            <div class="finding">
                <div class="finding-num">4</div>
                <h4>High Engagement</h4>
                <p>77% participate in STEM activities. However, only 46% feel very confident — confidence gap exists.</p>
            </div>
        </div>
        
        <div class="conclusion-box" style="margin-top: 40px;">
            <h3>Final Takeaway</h3>
            <p>Kazakhstan's high school students are <strong>tech-oriented, socially-influenced, and STEM-committed</strong>, 
            but need support in building confidence and exploring diverse STEM fields beyond IT.</p>
        </div>
    </div>

    <!-- Slide 10: Thank You -->
    <div class="slide thank-you">
        <div class="slide-number">10/10</div>
        <h1>Thank You</h1>
        <p>Questions & Discussion</p>
        <div style="margin-top: 50px; color: #666; font-size: 18px;">
            <p>Research conducted by Class 11E, NSPM School</p>
            <p>Almaty, Kazakhstan | March 2025</p>
        </div>
    </div>

    <div class="nav-hint">
        Use ← → arrow keys or click to navigate | ESC to exit fullscreen
    </div>

    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide');
        const totalSlides = slides.length;

        function showSlide(n) {
            slides.forEach(slide => slide.classList.remove('active'));
            currentSlide = (n + totalSlides) % totalSlides;
            slides[currentSlide].classList.add('active');
        }

        document.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowRight' || e.key === ' ') {
                showSlide(currentSlide + 1);
            } else if (e.key === 'ArrowLeft') {
                showSlide(currentSlide - 1);
            } else if (e.key === 'Escape') {
                if (document.fullscreenElement) {
                    document.exitFullscreen();
                }
            } else if (e.key === 'f' || e.key === 'F') {
                document.documentElement.requestFullscreen();
            }
        });

        document.addEventListener('click', (e) => {
            const x = e.clientX / window.innerWidth;
            if (x > 0.7) {
                showSlide(currentSlide + 1);
            } else if (x < 0.3) {
                showSlide(currentSlide - 1);
            }
        });

        // Auto-hide nav hint after 5 seconds
        setTimeout(() => {
            document.querySelector('.nav-hint').style.opacity = '0';
        }, 5000);
    </script>
</body>
</html>
