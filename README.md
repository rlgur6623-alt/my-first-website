[index.html.html](https://github.com/user-attachments/files/28419893/index.html.html)
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>부와지성 | 가치투자와 초사고의 완성</title>
    <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard/dist/web/static/pretendard.css" />
    <style>
        /* [디자인 시스템 가이드 적용] */
        :root {
            --bg-dark: #1A1A2E; /* 딥 네이비 */
            --point-orange: #FF6B35; /* CTA 오렌지 */
            --point-gold: #FFD700; /* 골드 */
            --bg-cream: #F9F7F4; /* 크림 */
            --text-main: #222222;
        }

        /* 기본 리셋 및 폰트 설정 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Pretendard', sans-serif; color: var(--text-main); line-height: 1.6; background-color: #fff; }
        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }
        
        .container { max-width: 1000px; margin: 0 auto; padding: 80px 20px; }
        .text-center { text-align: center; }
        .highlight { color: var(--point-orange); font-weight: 800; }
        
        /* CTA 버튼 스타일 */
        .btn-cta {
            display: inline-block;
            background-color: var(--point-orange);
            color: white;
            font-size: 22px;
            font-weight: 900;
            padding: 20px 40px;
            border-radius: 10px;
            box-shadow: 0 10px 20px rgba(255, 107, 53, 0.3);
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
            width: 100%;
            max-width: 400px;
            text-align: center;
        }
        .btn-cta:hover { transform: translateY(-3px); box-shadow: 0 15px 25px rgba(255, 107, 53, 0.5); }

        /* [HEADER] 고정 네비게이션 */
        header { position: fixed; top: 0; width: 100%; background: rgba(255,255,255,0.95); box-shadow: 0 2px 10px rgba(0,0,0,0.05); z-index: 100; padding: 15px 20px; text-align: center; }
        header .header-title { font-weight: 800; font-size: 20px; color: var(--bg-dark); }

        /* [SECTION 1] 히어로 (다크 배경) */
        .hero { background-color: var(--bg-dark); color: white; text-align: center; padding: 150px 20px 100px; }
        .hero h1 { font-size: 42px; font-weight: 900; line-height: 1.3; margin-bottom: 20px; word-break: keep-all; }
        .hero p { font-size: 20px; color: #ccc; margin-bottom: 40px; }
        .hero .social-proof-badge { display: block; margin-top: 15px; color: var(--point-gold); font-weight: bold; }

        /* [SECTION 2] 고통 공감 (크림 배경) */
        .pain { background-color: var(--bg-cream); }
        .pain h2 { font-size: 32px; font-weight: 800; margin-bottom: 40px; }
        .checklist { max-width: 600px; margin: 0 auto; text-align: left; background: white; padding: 30px; border-radius: 15px; box-shadow: 0 5px 15px rgba(0,0,0,0.05); }
        .checklist li { font-size: 18px; margin-bottom: 15px; padding-left: 30px; position: relative; }
        .checklist li::before { content: '✓'; position: absolute; left: 0; color: #dc3545; font-weight: bold; }
        .pain-footer { margin-top: 30px; font-size: 22px; font-weight: bold; color: var(--bg-dark); }

        /* [SECTION 3] 권위 입증 */
        .authority h2 { font-size: 32px; font-weight: 800; margin-bottom: 30px; }
        .profile-box { background: #f8f9fa; padding: 40px; border-radius: 15px; border: 1px solid #eee; }
        .profile-box p { font-size: 18px; margin-bottom: 10px; }

        /* [SECTION 4] 사회적 증명 (숫자) */
        .numbers { background-color: var(--bg-dark); color: white; padding: 60px 20px; }
        .number-grid { display: flex; justify-content: space-around; flex-wrap: wrap; max-width: 800px; margin: 0 auto; gap: 20px; }
        .num-item h3 { font-size: 48px; color: var(--point-gold); margin-bottom: 10px; }
        .num-item p { font-size: 18px; color: #ddd; }

        /* [SECTION 5] 해결책 & 목차 */
        .solution h2 { font-size: 32px; font-weight: 800; margin-bottom: 40px; }
        .toc-box { border: 1px solid #ddd; border-radius: 10px; padding: 20px; margin-bottom: 10px; background: #fff; text-align: left; }
        .toc-box h4 { font-size: 20px; margin-bottom: 10px; color: var(--bg-dark); }

        /* [SECTION 6] 후기 */
        .reviews { background-color: var(--bg-cream); }
        .review-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .review-card { background: white; padding: 25px; border-radius: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); text-align: left; }
        .stars { color: var(--point-gold); font-size: 20px; margin-bottom: 10px; }
        .review-card .date { font-size: 13px; color: #888; display: block; margin-bottom: 10px; }

        /* [SECTION 7] 가격 및 혜택 */
        .price-section { border: 4px solid var(--bg-dark); border-radius: 20px; padding: 50px 20px; margin: 40px auto; max-width: 700px; background: white; }
        .timer-box { background: #ffebee; color: #c62828; padding: 10px; border-radius: 5px; font-weight: bold; margin-bottom: 30px; display: inline-block; }
        .price-original { text-decoration: line-through; color: #999; font-size: 24px; }
        .price-discount { font-size: 52px; font-weight: 900; color: #dc3545; margin: 10px 0; }
        .value-stack { text-align: left; margin: 30px auto; max-width: 400px; background: #f8f9fa; padding: 20px; border-radius: 10px; }
        .value-stack li { margin-bottom: 10px; border-bottom: 1px dashed #ccc; padding-bottom: 10px; }
        .guarantee { margin-top: 20px; font-weight: bold; color: #28a745; }

        /* [SECTION 8] FAQ */
        .faq { background: var(--bg-cream); }
        details { background: white; margin-bottom: 15px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.05); text-align: left; }
        summary { padding: 20px; font-size: 18px; font-weight: bold; cursor: pointer; list-style: none; }
        summary::-webkit-details-marker { display: none; }
        details p { padding: 0 20px 20px; color: #555; }

        /* [우하단 플로팅 팝업] */
        .floating-popup {
            position: fixed; bottom: 20px; right: 20px; background: white; padding: 15px 20px;
            border-radius: 10px; box-shadow: 0 5px 20px rgba(0,0,0,0.15); border-left: 4px solid var(--point-orange);
            z-index: 1000; font-size: 14px; font-weight: bold;
            opacity: 0; transform: translateY(20px); transition: all 0.5s ease;
        }
        .floating-popup.show { opacity: 1; transform: translateY(0); }
        
        /* 모바일 대응 */
        @media (max-width: 768px) {
            .hero h1 { font-size: 32px; }
            .price-discount { font-size: 40px; }
            .num-item h3 { font-size: 36px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-title">부와지성 (Wealth & Intellect)</div>
    </header>

    <section class="hero">
        <div class="container">
            <h1 style="color:white;">시장 트렌드에 흔들리지 않는<br><span style="color:var(--point-orange);">행동경제학과 가치투자의 비밀</span></h1>
            <p>월급 외 수익을 만드는 가장 본질적이고 압도적인 투자 철학을 공개합니다.</p>
            <button class="btn-cta">지금 바로 노하우 확인하기 →</button>
            <span class="social-proof-badge">★★★★★ 누적 열람 12,847명 돌파</span>
        </div>
    </section>

    <section class="pain">
        <div class="container text-center">
            <h2>혹시 지금 이런 상황 아닌가요?</h2>
            <ul class="checklist">
                <li>좋은 기업인 건 아는데, 도대체 <strong>언제 사야 할지</strong> 모르겠다.</li>
                <li>남들이 돈 벌었다는 소식에 휩쓸려 <strong>뇌동매매</strong>를 반복한다.</li>
                <li>재무제표를 보긴 하지만, <strong>실제 투자 전략</strong>으로 연결하지 못한다.</li>
                <li>시장 하락장이 오면 <strong>불안감에 잠을 이루지 못한다</strong>.</li>
            </ul>
            <p class="pain-footer">당신의 잘못이 아닙니다. 단지 <span class="highlight">인간의 심리적 편향</span>을 통제하는 방법을 몰랐을 뿐입니다.</p>
        </div>
    </section>

    <section class="authority container text-center">
        <h2>왜 '부와지성'을 믿어야 할까요?</h2>
        <div class="profile-box">
            <h3 style="margin-bottom: 20px; color: var(--bg-dark);">저자 소개</h3>
            <p>✓ 심도 있는 가치투자 전문 블로그 운영 및 기업 분석</p>
            <p>✓ 행동경제학과 심리학을 결합한 독보적 투자 인사이트 도출</p>
            <p>✓ BYD, 알파벳 등 글로벌 핵심 기업 정밀 분석 리포트 발행</p>
            <p style="margin-top:20px; color:#666;">"투자는 결국 기업의 본질과 인간의 심리를 꿰뚫어 보는 작업입니다."</p>
        </div>
    </section>

    <section class="numbers">
        <div class="container text-center">
            <div class="number-grid">
                <div class="num-item">
                    <h3 class="counter" data-target="98">0</h3>
                    <p>수익 실현 평균 만족도 (%)</p>
                </div>
                <div class="num-item">
                    <h3 class="counter" data-target="4.9">0</h3>
                    <p>평균 별점 (5.0 만점)</p>
                </div>
                <div class="num-item">
                    <h3 class="counter" data-target="67">0</h3>
                    <p>심화 자료 재구매율 (%)</p>
                </div>
            </div>
        </div>
    </section>

    <section class="solution container text-center">
        <h2>이 전자책 하나면 흔들림이 사라집니다</h2>
        <p style="margin-bottom: 30px;">당신의 투자 기준을 명확하게 세워줄 핵심 목차</p>
        
        <div class="toc-box">
            <h4>Chapter 1. 투자의 심리학 (왜 우리는 실수하는가)</h4>
            <p>행동경제학으로 분석하는 투자 실패의 근본적 원인과 회피 본능 극복하기</p>
        </div>
        <div class="toc-box">
            <h4>Chapter 2. 진정한 내재가치 평가법</h4>
            <p>시장의 노이즈를 걸러내고 저평가된 흑진주를 발굴하는 3단계 분석 프레임워크</p>
        </div>
        <div class="toc-box">
            <h4>Chapter 3. 마인드셋과 실전 적용</h4>
            <p>명상과 통제력을 통한 평상심 유지, 그리고 실전 포트폴리오 구축 전략</p>
        </div>
        
        <br>
        <button class="btn-cta" style="font-size: 18px; padding: 15px 30px;">목차만 봐도 사고 싶다면? 지금 결제하기</button>
    </section>

    <section class="reviews">
        <div class="container text-center">
            <h2>이미 검증된 압도적 후기들</h2>
            <div class="review-grid">
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="date">2026. 05. 28 | 김** 님</span>
                    <p>"가치투자의 기본기부터 멘탈 관리까지 이 가격에 풀려도 되나 싶을 정도입니다. 뇌동매매를 완벽히 고쳤어요!"</p>
                </div>
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="date">2026. 05. 25 | 이** 님</span>
                    <p>"투자 서적 수십 권을 읽었지만 이렇게 본질을 날카롭게 찌르는 글은 처음입니다. 블로그 글도 다 정주행했습니다."</p>
                </div>
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="date">2026. 05. 21 | 박** 님</span>
                    <p>"단순한 주식 책이 아닙니다. 세상을 보는 지혜와 통찰을 얻어갑니다. 실전 적용 템플릿이 정말 유용해요."</p>
                </div>
            </div>
        </div>
    </section>

    <section class="container text-center">
        <div class="price-section">
            <div class="timer-box" id="countdown">🔥 특가 마감까지 23:59:59 남음</div>
            <h2>출시 기념 한정 특가</h2>
            <div class="price-original">정가 97,000원</div>
            <div class="price-discount">29,000원</div>
            
            <ul class="value-stack">
                <li>📚 본권: 부와지성 전자책 (29,000원 상당)</li>
                <li>🎁 보너스 1: 기업 분석 체크리스트 (9,900원 상당)</li>
                <li>🎁 보너스 2: 멘탈 관리 명상 가이드 (14,900원 상당)</li>
                <li style="border:none; font-weight:bold; color:var(--point-orange);">총 53,800원의 가치 ➔ 오늘만 29,000원</li>
            </ul>

            <div class="guarantee">🛡️ 불만족 시 7일 이내 100% 전액 환불 보장</div>
            <br>
            <button class="btn-cta">지금 바로 혜택가에 구매하기 →</button>
            <p style="margin-top:15px; font-size:14px; color:#888;">토스페이, 카카오페이, 신용카드 결제 가능</p>
        </div>
    </section>

    <section class="faq">
        <div class="container text-center">
            <h2>자주 묻는 질문 (FAQ)</h2>
            <div style="max-width: 800px; margin: 0 auto;">
                <details>
                    <summary>Q. 초보자도 바로 이해하고 실천할 수 있나요?</summary>
                    <p>A. 네, 어려운 재무 용어를 최소화하고 행동경제학적 관점에서 쉽게 풀어내어 주식 투자를 처음 시작하시는 분들도 즉각적으로 적용할 수 있습니다.</p>
                </details>
                <details>
                    <summary>Q. 구매하면 어떻게 받아볼 수 있나요?</summary>
                    <p>A. 결제 즉시 입력하신 이메일로 PDF 파일과 부록 자료 다운로드 링크가 자동 발송됩니다.</p>
                </details>
                <details>
                    <summary>Q. 정말 100% 환불이 되나요?</summary>
                    <p>A. 네, 내용에 만족하지 못하셨다면 구매 후 7일 이내에 고객센터 이메일로 연락주시면 묻지도 따지지도 않고 전액 환불해 드립니다.</p>
                </details>
            </div>
        </div>
    </section>

    <section class="hero" style="padding-top: 100px;">
        <div class="container">
            <h2 style="font-size: 32px; margin-bottom: 20px;">지금 이 페이지를 닫으면, <br>6개월 뒤에도 똑같은 자리에 있을 겁니다.</h2>
            <p>망설임은 기회를 놓치는 가장 확실한 방법입니다.</p>
            <button class="btn-cta" style="background-color: white; color: var(--bg-dark);">지금 당장 변화 시작하기</button>
        </div>
    </section>

    <div class="floating-popup" id="buyPopup">
        💰 서울에 사는 이**님이 방금 구매하셨습니다!
    </div>

    <script>
        // 1. 카운트다운 타이머 (24시간 기준)
        let time = 24 * 60 * 60; // 24시간
        const timerEl = document.getElementById('countdown');
        setInterval(() => {
            let h = Math.floor(time / 3600);
            let m = Math.floor((time % 3600) / 60);
            let s = time % 60;
            timerEl.innerHTML = `🔥 특가 마감까지 ${h.toString().padStart(2,'0')}:${m.toString().padStart(2,'0')}:${s.toString().padStart(2,'0')} 남음`;
            time > 0 ? time-- : time = 0;
        }, 1000);

        // 2. 우하단 실시간 구매 팝업 (FOMO 유발)
        const popup = document.getElementById('buyPopup');
        const names = ['김**', '이**', '박**', '최**', '정**'];
        const regions = ['서울', '부산', '경기', '인천', '대구'];
        setInterval(() => {
            const randomName = names[Math.floor(Math.random() * names.length)];
            const randomRegion = regions[Math.floor(Math.random() * regions.length)];
            popup.innerHTML = `💰 ${randomRegion}에 사는 ${randomName}님이 방금 구매하셨습니다!`;
            
            popup.classList.add('show');
            setTimeout(() => { popup.classList.remove('show'); }, 4000);
        }, 12000); // 12초마다 반복

        // 3. 숫자 카운트업 애니메이션 (Intersection Observer 활용)
        const counters = document.querySelectorAll('.counter');
        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    const target = entry.target;
                    const finalValue = parseFloat(target.getAttribute('data-target'));
                    const duration = 2000; // 2초
                    const stepTime = 20; // 0.02초마다 업데이트
                    const steps = duration / stepTime;
                    const increment = finalValue / steps;
                    let current = 0;
                    
                    const timer = setInterval(() => {
                        current += increment;
                        if(current >= finalValue) {
                            target.innerText = finalValue % 1 !== 0 ? finalValue.toFixed(1) : finalValue;
                            clearInterval(timer);
                        } else {
                            target.innerText = finalValue % 1 !== 0 ? current.toFixed(1) : Math.floor(current);
                        }
                    }, stepTime);
                    observer.unobserve(target); // 한 번만 실행
                }
            });
        }, { threshold: 0.5 });

        counters.forEach(counter => observer.observe(counter));
    </script>
</body>
</html>
