<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Youth Initiatives Support</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #FF6B35;
            --secondary: #004E89;
            --accent: #FFD23F;
            --dark: #1A1423;
            --light: #F8F9FA;
            --gradient: linear-gradient(135deg, #FF6B35 0%, #F7931E 100%);
            --gradient-2: linear-gradient(135deg, #004E89 0%, #1B3A5C 100%);
        }

        body {
            font-family: 'Space Mono', monospace;
            background: var(--light);
            color: var(--dark);
            overflow-x: hidden;
            line-height: 1.6;
        }

        .lang-toggle {
            position: fixed;
            top: 30px;
            right: 30px;
            z-index: 1000;
            display: flex;
            align-items: center;
            gap: 15px;
            background: white;
            padding: 10px 20px;
            border-radius: 50px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            transition: all 0.3s ease;
        }

        .lang-toggle:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
        }

        .lang-label {
            font-size: 14px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--dark);
        }

        .toggle-switch {
            position: relative;
            width: 60px;
            height: 30px;
            background: var(--gradient);
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .toggle-switch::before {
            content: '';
            position: absolute;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: white;
            top: 3px;
            left: 3px;
            transition: all 0.3s ease;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }

        .toggle-switch.active::before {
            left: 33px;
        }

        .hero {
            min-height: 100vh;
            background: var(--gradient);
            position: relative;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 100px 20px 50px;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 800px;
            height: 800px;
            background: radial-gradient(circle, rgba(255, 210, 63, 0.3) 0%, transparent 70%);
            top: -400px;
            right: -400px;
            animation: pulse 8s ease-in-out infinite;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(0, 78, 137, 0.2) 0%, transparent 70%);
            bottom: -300px;
            left: -300px;
            animation: pulse 10s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }

        .hero-content {
            max-width: 1200px;
            text-align: center;
            position: relative;
            z-index: 2;
        }

        .hero-title {
            font-family: 'Syne', sans-serif;
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 800;
            color: white;
            margin-bottom: 30px;
            line-height: 1.1;
            text-transform: uppercase;
            letter-spacing: -2px;
            animation: fadeInUp 1s ease;
        }

        .hero-subtitle {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: rgba(255, 255, 255, 0.95);
            margin-bottom: 50px;
            font-weight: 400;
            animation: fadeInUp 1s ease 0.2s backwards;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .scroll-indicator {
            position: absolute;
            bottom: 50px;
            left: 50%;
            transform: translateX(-50%);
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateX(-50%) translateY(0); }
            50% { transform: translateX(-50%) translateY(10px); }
        }

        .scroll-indicator svg {
            width: 30px;
            height: 30px;
            stroke: white;
            fill: none;
            stroke-width: 2;
        }

        section {
            padding: 100px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-family: 'Syne', sans-serif;
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            margin-bottom: 60px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100px;
            height: 6px;
            background: var(--gradient);
            border-radius: 3px;
        }

        .definition-card {
            background: white;
            padding: 60px;
            border-radius: 30px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
            margin-bottom: 80px;
            position: relative;
            overflow: hidden;
            transition: all 0.4s ease;
        }

        .definition-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 6px;
            height: 100%;
            background: var(--gradient);
        }

        .definition-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.15);
        }

        .definition-text {
            font-size: 1.2rem;
            line-height: 1.8;
            color: #333;
        }

        .includes-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .include-card {
            background: white;
            padding: 40px 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .include-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--gradient);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .include-card:hover::before {
            transform: scaleX(1);
        }

        .include-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.12);
        }

        .include-icon {
            width: 60px;
            height: 60px;
            background: var(--gradient);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            font-size: 28px;
        }

        .include-title {
            font-family: 'Syne', sans-serif;
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--dark);
        }

        .include-desc {
            font-size: 1rem;
            color: #666;
            line-height: 1.6;
        }

        .organizations-section {
            background: var(--gradient-2);
            padding: 100px 20px;
            margin: 100px 0;
            position: relative;
        }

        .organizations-section::before {
            content: '';
            position: absolute;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(255, 210, 63, 0.1) 0%, transparent 70%);
            top: -250px;
            left: 50%;
            transform: translateX(-50%);
        }

        .org-content {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }

        .org-title {
            font-family: 'Syne', sans-serif;
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            color: white;
            margin-bottom: 60px;
        }

        .org-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
        }

        .org-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 50px 40px;
            border-radius: 25px;
            border: 2px solid rgba(255, 255, 255, 0.2);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .org-card::before {
            content: '';
            position: absolute;
            top: -100%;
            left: -100%;
            width: 300%;
            height: 300%;
            background: radial-gradient(circle, rgba(255, 210, 63, 0.15) 0%, transparent 50%);
            transition: all 0.6s ease;
        }

        .org-card:hover::before {
            top: -50%;
            left: -50%;
        }

        .org-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 210, 63, 0.5);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
        }

        .org-card-title {
            font-family: 'Syne', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }

        .org-card-desc {
            color: rgba(255, 255, 255, 0.9);
            line-height: 1.7;
            font-size: 1.05rem;
            position: relative;
            z-index: 2;
        }

        .org-list {
            list-style: none;
            margin-top: 25px;
            position: relative;
            z-index: 2;
        }

        .org-list li {
            color: rgba(255, 255, 255, 0.85);
            padding-left: 30px;
            position: relative;
            margin-bottom: 15px;
            font-size: 1.05rem;
        }

        .org-list li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: 700;
        }

        footer {
            background: var(--dark);
            color: white;
            padding: 60px 20px 30px;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-text {
            font-size: 1rem;
            opacity: 0.7;
            margin-top: 20px;
        }

        @media (max-width: 768px) {
            .hero {
                padding: 80px 20px 40px;
            }

            section {
                padding: 60px 20px;
            }

            .definition-card {
                padding: 40px 30px;
            }

            .includes-grid,
            .org-cards {
                grid-template-columns: 1fr;
            }

            .org-card {
                padding: 40px 30px;
            }

            .lang-toggle {
                top: 20px;
                right: 20px;
                padding: 8px 15px;
            }
        }
    </style>
</head>
<body>
    <div class="lang-toggle">
        <span class="lang-label" id="langLabel">EN</span>
        <div class="toggle-switch" id="toggleSwitch">
        </div>
        <span class="lang-label" id="langLabelRu">RU</span>
    </div>

    <section class="hero">
        <div class="hero-content">
            <h1 class="hero-title" data-en="Youth Initiatives Support" data-ru="Поддержка молодёжных инициатив">Youth Initiatives Support</h1>
            <p class="hero-subtitle" data-en="Empowering the next generation through educational institutions" data-ru="Развитие нового поколения через образовательные учреждения">Empowering the next generation through educational institutions</p>
        </div>
        <div class="scroll-indicator">
            <svg viewBox="0 0 24 24">
                <polyline points="6 9 12 15 18 9"></polyline>
            </svg>
        </div>
    </section>

    <section>
        <h2 class="section-title" data-en="What It Means" data-ru="Что это значит">What It Means</h2>
        <div class="definition-card">
            <p class="definition-text" data-en="Youth initiatives support at the educational institution level refers to comprehensive programs, resources, and organizational frameworks designed to encourage, facilitate, and empower students to develop, propose, and implement their own projects, ideas, and community engagement activities. This approach recognizes young people as active agents of change and provides them with the necessary tools, mentorship, and institutional backing to transform their visions into reality." data-ru="Поддержка молодёжных инициатив на уровне образовательных учреждений означает комплексные программы, ресурсы и организационные структуры, созданные для того, чтобы поощрять, облегчать и расширять возможности студентов разрабатывать, предлагать и реализовывать собственные проекты, идеи и мероприятия для общества. Этот подход признаёт молодых людей активными агентами изменений и предоставляет им необходимые инструменты, наставничество и институциональную поддержку для превращения их идей в реальность.">
                Youth initiatives support at the educational institution level refers to comprehensive programs, resources, and organizational frameworks designed to encourage, facilitate, and empower students to develop, propose, and implement their own projects, ideas, and community engagement activities. This approach recognizes young people as active agents of change and provides them with the necessary tools, mentorship, and institutional backing to transform their visions into reality.
            </p>
        </div>

        <h2 class="section-title" data-en="Key Components" data-ru="Ключевые компоненты">Key Components</h2>
        <div class="includes-grid">
            <div class="include-card">
                <div class="include-icon">💡</div>
                <h3 class="include-title" data-en="Project Funding" data-ru="Финансирование проектов">Project Funding</h3>
                <p class="include-desc" data-en="Financial grants and resources allocated specifically for student-led initiatives, social projects, and innovative ideas" data-ru="Финансовые гранты и ресурсы, выделяемые специально для студенческих инициатив, социальных проектов и инновационных идей">Financial grants and resources allocated specifically for student-led initiatives, social projects, and innovative ideas</p>
            </div>

            <div class="include-card">
                <div class="include-icon">🎯</div>
                <h3 class="include-title" data-en="Mentorship Programs" data-ru="Программы наставничества">Mentorship Programs</h3>
                <p class="include-desc" data-en="Experienced advisors and faculty members who guide students through project development, implementation, and evaluation" data-ru="Опытные консультанты и преподаватели, которые направляют студентов через разработку, реализацию и оценку проектов">Experienced advisors and faculty members who guide students through project development, implementation, and evaluation</p>
            </div>

            <div class="include-card">
                <div class="include-icon">🏛️</div>
                <h3 class="include-title" data-en="Institutional Framework" data-ru="Институциональная структура">Institutional Framework</h3>
                <p class="include-desc" data-en="Official structures, policies, and procedures that legitimize and support youth initiatives within the educational system" data-ru="Официальные структуры, политика и процедуры, которые легитимизируют и поддерживают молодёжные инициативы в образовательной системе">Official structures, policies, and procedures that legitimize and support youth initiatives within the educational system</p>
            </div>

            <div class="include-card">
                <div class="include-icon">🌐</div>
                <h3 class="include-title" data-en="Networking Opportunities" data-ru="Возможности для нетворкинга">Networking Opportunities</h3>
                <p class="include-desc" data-en="Platforms for collaboration, knowledge exchange, and connection with like-minded peers and external partners" data-ru="Платформы для сотрудничества, обмена знаниями и связи с единомышленниками и внешними партнёрами">Platforms for collaboration, knowledge exchange, and connection with like-minded peers and external partners</p>
            </div>

            <div class="include-card">
                <div class="include-icon">📚</div>
                <h3 class="include-title" data-en="Skill Development" data-ru="Развитие навыков">Skill Development</h3>
                <p class="include-desc" data-en="Training in leadership, project management, communication, and other competencies essential for successful initiative implementation" data-ru="Обучение лидерству, управлению проектами, коммуникации и другим компетенциям, необходимым для успешной реализации инициатив">Training in leadership, project management, communication, and other competencies essential for successful initiative implementation</p>
            </div>

            <div class="include-card">
                <div class="include-icon">🏆</div>
                <h3 class="include-title" data-en="Recognition Systems" data-ru="Системы признания">Recognition Systems</h3>
                <p class="include-desc" data-en="Awards, certificates, and public acknowledgment of student achievements to motivate continued engagement and innovation" data-ru="Награды, сертификаты и публичное признание достижений студентов для мотивации дальнейшего участия и инноваций">Awards, certificates, and public acknowledgment of student achievements to motivate continued engagement and innovation</p>
            </div>
        </div>
    </section>

    <div class="organizations-section">
        <div class="org-content">
            <h2 class="org-title" data-en="Youth Organizations at BSPU" data-ru="Молодёжные объединения БГПУ">Youth Organizations at BSPU</h2>
            
            <div class="org-cards">
                <div class="org-card">
                    <h3 class="org-card-title" data-en="Student Council" data-ru="Студенческий совет">Student Council</h3>
                    <p class="org-card-desc" data-en="The primary representative body of students at Belarusian State Pedagogical University, advocating for student interests and coordinating major campus-wide initiatives." data-ru="Основной представительный орган студентов Белорусского государственного педагогического университета, отстаивающий интересы студентов и координирующий крупные общеуниверситетские инициативы.">The primary representative body of students at Belarusian State Pedagogical University, advocating for student interests and coordinating major campus-wide initiatives.</p>
                    <ul class="org-list">
                        <li data-en="Organizes university-wide events and festivals" data-ru="Организует общеуниверситетские мероприятия и фестивали">Organizes university-wide events and festivals</li>
                        <li data-en="Facilitates communication between students and administration" data-ru="Способствует общению между студентами и администрацией">Facilitates communication between students and administration</li>
                        <li data-en="Supports academic and social initiatives" data-ru="Поддерживает академические и социальные инициативы">Supports academic and social initiatives</li>
                    </ul>
                </div>

                <div class="org-card">
                    <h3 class="org-card-title" data-en="Volunteer Center" data-ru="Волонтёрский центр">Volunteer Center</h3>
                    <p class="org-card-desc" data-en="A hub for socially-engaged students who dedicate their time to community service, charitable projects, and helping those in need." data-ru="Центр для социально активных студентов, которые посвящают своё время общественным работам, благотворительным проектам и помощи нуждающимся.">A hub for socially-engaged students who dedicate their time to community service, charitable projects, and helping those in need.</p>
                    <ul class="org-list">
                        <li data-en="Coordinates charity events and fundraisers" data-ru="Координирует благотворительные мероприятия и сбор средств">Coordinates charity events and fundraisers</li>
                        <li data-en="Partners with local NGOs and social organizations" data-ru="Сотрудничает с местными НПО и социальными организациями">Partners with local NGOs and social organizations</li>
                        <li data-en="Promotes civic engagement and social responsibility" data-ru="Продвигает гражданскую активность и социальную ответственность">Promotes civic engagement and social responsibility</li>
                    </ul>
                </div>

                <div class="org-card">
                    <h3 class="org-card-title" data-en="Creative Clubs & Societies" data-ru="Творческие клубы и общества">Creative Clubs & Societies</h3>
                    <p class="org-card-desc" data-en="Diverse student organizations focused on arts, culture, sports, and academic interests, providing platforms for talent development and self-expression." data-ru="Разнообразные студенческие организации, ориентированные на искусство, культуру, спорт и академические интересы, предоставляющие платформы для развития талантов и самовыражения.">Diverse student organizations focused on arts, culture, sports, and academic interests, providing platforms for talent development and self-expression.</p>
                    <ul class="org-list">
                        <li data-en="Dance, theater, and music ensembles" data-ru="Танцевальные, театральные и музыкальные ансамбли">Dance, theater, and music ensembles</li>
                        <li data-en="Debate clubs and intellectual societies" data-ru="Дискуссионные клубы и интеллектуальные общества">Debate clubs and intellectual societies</li>
                        <li data-en="Sports teams and fitness communities" data-ru="Спортивные команды и фитнес-сообщества">Sports teams and fitness communities</li>
                    </ul>
                </div>

                <div class="org-card">
                    <h3 class="org-card-title" data-en="Innovation Lab" data-ru="Лаборатория инноваций">Innovation Lab</h3>
                    <p class="org-card-desc" data-en="A space dedicated to fostering entrepreneurial thinking, technological innovation, and startup development among students interested in creating educational technologies and social ventures." data-ru="Пространство, посвящённое развитию предпринимательского мышления, технологических инноваций и стартапов среди студентов, заинтересованных в создании образовательных технологий и социальных предприятий.">A space dedicated to fostering entrepreneurial thinking, technological innovation, and startup development among students interested in creating educational technologies and social ventures.</p>
                    <ul class="org-list">
                        <li data-en="Provides resources for project prototyping" data-ru="Предоставляет ресурсы для прототипирования проектов">Provides resources for project prototyping</li>
                        <li data-en="Connects students with mentors and investors" data-ru="Связывает студентов с наставниками и инвесторами">Connects students with mentors and investors</li>
                        <li data-en="Hosts hackathons and innovation competitions" data-ru="Проводит хакатоны и конкурсы инноваций">Hosts hackathons and innovation competitions</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <div class="footer-content">
            <h3 class="section-title" style="color: white; margin-bottom: 30px;" data-en="Building Tomorrow's Leaders Today" data-ru="Создаём лидеров завтрашнего дня уже сегодня">Building Tomorrow's Leaders Today</h3>
            <p class="footer-text" data-en="© 2026 Youth Initiatives Support Platform. Empowering students to make a difference." data-ru="© 2026 Платформа поддержки молодёжных инициатив. Даём студентам возможность менять мир.">© 2026 Youth Initiatives Support Platform. Empowering students to make a difference.</p>
        </div>
    </footer>

    <script>
        const toggleSwitch = document.getElementById('toggleSwitch');
        const langLabel = document.getElementById('langLabel');
        const langLabelRu = document.getElementById('langLabelRu');
        let isRussian = false;

        toggleSwitch.addEventListener('click', function() {
            isRussian = !isRussian;
            toggleSwitch.classList.toggle('active');
            
            // Update all elements with data-en and data-ru attributes
            const elements = document.querySelectorAll('[data-en][data-ru]');
            elements.forEach(element => {
                element.textContent = isRussian ? element.getAttribute('data-ru') : element.getAttribute('data-en');
            });
            
            // Update language labels
            if (isRussian) {
                langLabel.style.opacity = '0.5';
                langLabelRu.style.opacity = '1';
            } else {
                langLabel.style.opacity = '1';
                langLabelRu.style.opacity = '0.5';
            }
        });

        // Set initial opacity
        langLabelRu.style.opacity = '0.5';

        // Smooth scroll
        document.querySelector('.scroll-indicator').addEventListener('click', function() {
            window.scrollTo({
                top: window.innerHeight,
                behavior: 'smooth'
            });
        });

        // Parallax effect
        window.addEventListener('scroll', function() {
            const scrolled = window.pageYOffset;
            const hero = document.querySelector('.hero');
            if (hero) {
                hero.style.transform = `translateY(${scrolled * 0.5}px)`;
                hero.style.opacity = 1 - (scrolled / 800);
            }
        });
    </script>
</body>
</html>
