<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>WG 공동체</title>
    <!-- Swiper CSS (슬라이더 라이브러리) -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css"/>
    <style>
        /* 기본 리셋 및 타이포그래피 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Poppins', sans-serif;
            background: #f0f2f5;
            color: #333;
            line-height: 1.6;
        }
        header {
            background: #004080;
            padding: 1rem;
            text-align: center;
            color: #fff;
            position: relative;
        }
        /* 로그인 관련 정보 (오른쪽 상단) */
        .login-info {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 0.9rem;
        }
        .login-info a {
            color: #fff;
            margin-left: 0.8rem;
            text-decoration: none;
            transition: color 0.3s;
        }
        .login-info a:hover {
            color: #ffcc00;
        }

        /* 탭 네비게이션 (상단 표 역할) */
        .tab-nav {
            display: flex;
            justify-content: center;
            background: #0066cc;
            border-bottom: 2px solid #004080;
        }
        .tab-nav button {
            flex: 1;
            padding: 1rem;
            background: transparent;
            border: none;
            color: #fff;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.3s;
        }
        .tab-nav button:hover {
            background: #0059b3;
        }
        .tab-nav button.active {
            background: #004080;
            font-weight: bold;
        }

        /* 콘텐츠 컨테이너 */
        .container {
            max-width: 800px;
            margin: 2rem auto;
            padding: 2rem;
            background: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            margin-bottom: 2rem;
        }
        .container h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #004080;
        }
        .container p {
            font-size: 1rem;
            margin-bottom: 1rem;
        }
        .container strong {
            font-size: 1.2rem;
        }
        .container h3 {
            margin-top: 2rem;
            font-size: 1.5rem;
            color: #0066cc;
            border-bottom: 2px solid #0066cc;
            padding-bottom: 0.5rem;
        }
        dl.faq { margin-top: 1rem; }
        dl.faq dt { font-weight: bold; margin-top: 1rem; }
        dl.faq dd { margin-left: 1rem; margin-top: 0.5rem; color: #555; }
        a { color: #0066cc; text-decoration: none; transition: color 0.3s; }
        a:hover { color: #004080; text-decoration: underline; }

        /* 채용공고 슬라이더 스타일 */
        .jobs-slider {
            margin-top: 2rem;
        }
        .swiper-container {
            width: 100%;
            padding-bottom: 3rem;
        }
        .swiper-slide {
            background: #fff;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            padding: 1rem;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .swiper-slide:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }
        .job-img {
            width: 100px;
            height: 100px;
            object-fit: cover;
            margin: 0 auto 1rem;
            border-radius: 50%;
        }
        .job-title {
            font-size: 1.2rem;
            margin: 0.5rem 0;
            color: #0066cc;
        }
        .job-location {
            font-size: 0.9rem;
            color: #777;
        }
        /* Swiper 네비게이션 & 페이징 */
        .swiper-button-prev,
        .swiper-button-next { color: #004080; }
        .swiper-pagination-bullet { background: #004080; opacity: 0.7; }
        .swiper-pagination-bullet-active { opacity: 1; }

        /* 채용공고 확인하기 버튼 스타일 */
        .check-jobs-btn {
            display: block;
            width: 200px;
            margin: 2rem auto 0;
            padding: 0.8rem 1.5rem;
            background: #1100ff;
            color: #fff;
            text-align: center;
            border-radius: 4px;
            font-weight: bold;
            transition: background 0.3s;
        }
        .check-jobs-btn:hover {
            background: #ffffff;
            color: #1100ff;
            border: 1px solid #1100ff;
        }
    </style>
</head>
<body>
<header>
    <h1>WG 공동체</h1>
    <div class="login-info">
        <a href="login.html">로그인</a>
        <a href="register.html">회원가입</a>
    </div>
</header>

<!-- 탭 네비게이션 (상단 표 역할) -->
<div class="tab-nav">
    <button data-tab="corporation" class="active">WG코퍼레이션</button>
    <button data-tab="foundation">WG재단</button>
    <button data-tab="republic">WG공화국</button>
    <button data-tab="company">WG컴퍼니</button>
    <button data-tab="committee">총위원부</button>
</div>

<!-- WG코퍼레이션 콘텐츠 (예시) -->
<div class="container" id="corporation">
    <h2>WG코퍼레이션</h2>
    <p><strong>주의 ! 공식적인 내용이 아닙니다</strong></p>
    <p><strong>WG코퍼레이션에 오신것을 환영합니다</strong></p>
    <h3>테스트</h3>
    <p>테스트</p>
    <h3>FAQ</h3>
    <dl class="faq">
        <dt>Q. WG코퍼레이션이 무엇인가요?</dt>
        <dd>A. WG공동체의 소통과 운영을 담당하는 곳입니다.</dd>
        <dt>Q. WG코퍼레이션에 가입하려면 어떻게 해야 하나요?</dt>
        <dd>A. WG코퍼레이션 <a href="https://discord.gg/wEdMyuX3" target="_blank"> 디스코드</a>로 가입하면 됩니다.</dd>
        <dt>Q. WG코퍼레이션의 위원이 되려면 어떻게 해야 하나요?</dt>
        <dd>A. 총위원부의 채용 공고를 확인해주세요.</dd>
        <dt>Q. WG</dt>
        <dd>A. 재단</dd>
    </dl>
</div>
<! 뷁>

<div class="container" id="foundation" style="display:none;">
    <h2>WG재단</h2>
    <p><strong>WG재단</strong></p>
    <h3>규칙</h3>
    <p><strong>1. 욕설 사용에 따른 제재 (7일~14일 밴)</strong><br>
        1. 외국어 욕설 사용 금지<br>
        2. 충분히 인식 가능한 욕설 사용 금지<br>
        &nbsp;&nbsp;2-1. 가벼운 단어(예: 바보, 멍청이)는 사용 가능<br>
        &nbsp;&nbsp;2-2. '미친' 등의 단어는 감탄사로만 사용 가능<br>
        3. 갑작스런 욕설은 제재하지 않음 (단, 상황에 따라 다름)
    </p>
    <p><strong>2. 특정 위치에서 3분 이상 존버 금지 (경고 ~ 3일 밴)</strong><br>
        1. 적대진영 대치 시 존버 가능<br>
        2. 카드가 없는 방에 갇힌 경우 존버 가능 (단, 일부러 카드 없이 존버 시 제재)<br>
        3. 같은 구역을 반복 이동하며 존버 제재 회피 시 제재<br>
        4. SCP 914 강화 중인 경우 존버 가능 (아이템 미투입 시 제재)<br>
        5. SCP가 한 개체 남은 경우 SCP는 존버 가능 (단, SCP 049-2는 제외)
    </p>
    <!-- 추가 규칙 시작 -->
    <p><strong>3. 문트롤 금지 (경고 ~ 3일 밴)</strong><br>
        1. 지상을 제외한 모든 구역에서 문트롤 금지<br>
        2. 지상을 제외한 모든 구역에서 아군진영에게 문트롤 금지<br>
        &nbsp;&nbsp;2-1. MTF, 과학자, 카오스, 죄수는 아군으로 규정<br>
        3. 모든 구역에서 SCP에게 쫓기는 상황에서는 문트롤 가능<br>
        &nbsp;&nbsp;3-1. 단, 모든 구역에서 SCP 079만 보고 있는 경우 문트롤 금지<br>
        4. SCP 세력은 모든 구역에서 동일 SCP 진영을 향한 문트롤 금지<br>
        &nbsp;&nbsp;4-1. 고의성이 없으면 제재하지 않음<br>
        &nbsp;&nbsp;4-2. 지속적 실수 시 제재<br>
        5. 중립진영 간 문트롤은 가능 (단, 중립진영은 과학자와 죄수로 규정)<br>
        6. 고위험군 헤비도어에서는 문트롤 적용 안 됨
    </p>
    <p><strong>4. 모든 구역에서 엘베 트롤 금지 (경고 ~ 3일 밴)</strong><br>
        1. SCP에게 쫓기는 경우 제재하지 않음<br>
        &nbsp;&nbsp;1-1. SCP 079만 보고 있는 경우에는 엘베 트롤 금지<br>
        2. MTF/카오스 지원 시, 총 지원 인원 50% 이상이 엘리베이터 이용 시 엘베 트롤 가능<br>
        3. 적대진영 대상은 엘베 트롤 가능 (중립진영 간은 금지)<br>
        4. 고위험군 핵방 엘리베이터에서는 엘베 트롤 적용 안 됨
    </p>
    <p><strong>5. SCP 049-2로 소생 도중 게임 탈주 금지 (5일 밴)</strong><br>
        1. SCP 049-2 소생거부 기능은 사용 가능<br>
        2. 소생 후 30초 이내 잠수는 제재하지 않음<br>
        3. 일부러 게임에 참여하지 않고 탈주 시 제재
    </p>
    <p><strong>7. 정치적, 선정적, 인종차별적 닉네임 및 행위 금지 (영구밴)</strong><br>
        1. 국내외 정치 언급 금지<br>
        &nbsp;&nbsp;1-1. 역사 평가 행위 제재<br>
        &nbsp;&nbsp;1-2. 문제가 될 수 있는 사건 언급 금지<br>
        &nbsp;&nbsp;1-3. 정치적 대화 금지<br>
        2. 성희롱 및 선정적 발언 금지<br>
        &nbsp;&nbsp;2-1. 동성 간도 제재 가능<br>
        &nbsp;&nbsp;2-2. 고의적 선정적 은어 사용 시 제재<br>
        3. 장애인 차별 발언 금지<br>
        4. 타 유저 플레이 비난 금지 (특정 닉네임 언급 시 제재)<br>
        5. 사회적, 세계적 문제 관련 발언 금지 (깊은 토론 및 차별적 표현 사용 시 제재)
    </p>
    <p><strong>8. 핵 혹은 게임에 직접 영향 주는 프로그램 사용 금지 (영구밴)</strong><br>
        1. 게임 플레이에 직접 영향 주는 외부 프로그램 사용 금지<br>
        &nbsp;&nbsp;1-1. 시스템 변경 프로그램은 외부 프로그램으로 간주<br>
        2. 보이스/감마 프로그램 등은 직접 영향 주지 않는 경우 사용 가능<br>
        &nbsp;&nbsp;2-1. 보이스 프로그램은 9번 규칙에 따라 처리<br>
        &nbsp;&nbsp;2-2. 녹화/내장 프로그램 사용 가능<br>
        3. 통화/대화 프로그램을 통한 플레이 시 제재 (친목 목적 시 일부 예외)
    </p>
    <p><strong>9. 상대에게 불쾌한 보이스 사용 금지 (경고 ~ 5일 밴)</strong><br>
        1. 인게임 마이크로 고의적 소음 유발 시 제재<br>
        &nbsp;&nbsp;1-1. 마이크 문제로 인한 경우도 소리가 크면 제재<br>
        2. 관전자 상태에서 노래나 사운드 패드 사용 시 제재<br>
        &nbsp;&nbsp;2-1. 사용 중지 요청 후 계속 사용 시 제재<br>
        3. 정치적·선정적 음악 사용 시 제재 (7번 규칙 연계)
    </p>
    <p><strong>10. 게임 진행에 영향 주는 버그 사용 금지 (경고 ~ 7일 밴)</strong><br>
        1. 버그로 인한 이득 취득 시 제재<br>
        2. 버그로 게임 진행 방해 시 제재<br>
        &nbsp;&nbsp;2-1. 일부러 게임 종료 방해 시 제재<br>
        &nbsp;&nbsp;2-2. 불가피한 경우는 예외<br>
        3. 버그로 타 유저 플레이 방해 시 제재<br>
        4. 버그 사용 시도 자체도 제재
    </p>
    <p><strong>11. 체포된 인원 사살 금지 (30일 밴)</strong><br>
        1. 체포된 유저 사살 금지 (중립진영 포함)<br>
        &nbsp;&nbsp;1-1. 체포된 진영이 적대관계일 경우 체포킬 가능<br>
        2. 체포자가 아닌 인원 사살 금지<br>
        3. 체포 고의 해제 후 사살 시 제재<br>
        4. SCP 진영 여부에 따라 체포킬 가능 여부 결정
    </p>
    <p><strong>12. 적대세력과의 티밍 금지 (경고 ~ 5일 밴)</strong><br>
        1. 고의적 티밍으로 게임 진행 방해 시 제재<br>
        &nbsp;&nbsp;1-1. 티밍으로 체포 또는 끌고 다니는 경우 3분 이상 지속 시 제재<br>
        2. SCP 진영과 티밍 금지 (카오스와 SCP 티밍 모두 포함)<br>
        3. 짧은 접촉(10~30초)은 예외, 아이템 나눔 등은 제재
    </p>
    <p><strong>13. SCP 세력의 고의적 자살 금지 (경고 ~ 3일 밴)</strong><br>
        1. 고의적 자살 시 제재 (단, 30분 이내 자진 신고 시 예외)<br>
        2. 참여하지 않고 탈주 시도 시에도 30분 이내 자진 신고 시 예외
    </p>
    <p><strong>14. 고의적 아군 방해 금지 (5일 밴)</strong><br>
        1. 아군을 고의적으로 죽인 경우 제재<br>
        &nbsp;&nbsp;1-1. 본인이 직접 죽이지 않은 경우는 예외
    </p>
    <h3>플러그인</h3>
</div>

<!-- WG공화국 섹션 (임시 콘텐츠) -->
<div class="container" id="republic" style="display:none;">
    <h2>WG공화국</h2>
    <p>WG공화국에 대한 내용이 여기에 표시됩니다.</p>
    <p>테스트</p>
</div>
<!-- WG컴퍼니 섹션 (임시 콘텐츠) -->
<div class="container" id="company" style="display:none;">
    <h2>WG컴퍼니</h2>
    <p>WG컴퍼니에 대한 내용이 여기에 표시됩니다.</p>
    <h3>링크</h3>

</div>
<!-- 총위원부 섹션: 채용공고 포함 -->
<div class="container" id="committee" style="display:none;">
    <h2>총위원부</h2>
    <p style="text-align: center;">총위원부</p>

    <h3>채용공고</h3>
    <!-- 채용공고 슬라이더 -->
    <div class="jobs-slider">
        <div class="swiper-container">
            <div class="swiper-wrapper">
                <!-- 채용공고 항목 예시 -->
                <div class="swiper-slide">
                    <h3 class="job-title">사무위원</h3>
                    <p class="job-location">총위원부의 사무를 담당합니다</p>
                </div>
                <div class="swiper-slide">
                    <h3 class="job-title">기술위원</h3>
                    <p class="job-location">WG재단의 플러그인과 기술을 담당합니다</p>
                </div>
                <div class="swiper-slide">
                    <h3 class="job-title">운영위원</h3>
                    <p class="job-location">WG재단의 운영을 담당합니다</p>
                </div>
                <div class="swiper-slide">
                    <h3 class="job-title">창작위원</h3>
                    <p class="job-location">WG컴퍼니의 편집, 디자인 등 담당</p>
                </div>
                <div class="swiper-slide">
                    <h3 class="job-title">경영위원</h3>
                    <p class="job-location">WG공동체의 운영을 담당합니다</p>
                </div>
                <div class="swiper-slide">
                    <h3 class="job-title">감찰위원</h3>
                    <p class="job-location">WG공동체 위원들을 감찰합니다</p>
                </div>
                <div class="swiper-slide">
                    <h3 class="job-title">매니저</h3>
                    <p class="job-location">WG공동체 대표 위드고 방송 및 컴퍼니 운영</p>
                </div>
            </div>
            <!-- 페이징 및 네비게이션 -->
            <div class="swiper-pagination"></div>
            <div class="swiper-button-prev"></div>
            <div class="swiper-button-next"></div>
        </div>
    </div>
    <!-- 채용공고 확인하기 버튼 -->
    <a href="https://example.com/jobs" target="_blank" class="check-jobs-btn">채용공고 확인하기</a>
    <h3>문의</h3>
</div>

<!-- Swiper JS -->
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
<script>

    const tabs = document.querySelectorAll('.tab-nav button');
    const sections = document.querySelectorAll('.container');
    tabs.forEach(tab => {
        tab.addEventListener('click', function() {
            tabs.forEach(t => t.classList.remove('active'));
            sections.forEach(sec => sec.style.display = 'none');
            this.classList.add('active');
            const tabId = this.getAttribute('data-tab');
            document.getElementById(tabId).style.display = 'block';
        });
    });

    // Swiper 슬라이더 초기화
    const swiper = new Swiper('.swiper-container', {
        slidesPerView: 3,
        spaceBetween: 20,
        loop: true,
        navigation: {
            nextEl: '.swiper-button-next',
            prevEl: '.swiper-button-prev',
        },
        pagination: {
            el: '.swiper-pagination',
            clickable: true,
        },
        breakpoints: {
            640: { slidesPerView: 1, spaceBetween: 10 },
            768: { slidesPerView: 2, spaceBetween: 15 },
            1024: { slidesPerView: 3, spaceBetween: 20 },
        }
    });
</script>
</body>
</html>

