<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FitZone Pro</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #111;
      color: #fff;
    }

    header {
      background: #000;
      padding: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 28px;
      font-weight: bold;
      color: #f00;
    }

    .nav-links {
      display: flex;
      gap: 20px;
    }

    .nav-links a {
      color: #fff;
      text-decoration: none;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: #f00;
    }

    .lang-switcher {
      margin-left: 20px;
    }

    .hero {
      text-align: center;
      padding: 100px 20px;
      background: url('https://images.unsplash.com/photo-1599058917212-d750089bc1df?fit=crop&w=1200&q=80') no-repeat center center/cover;
    }

    .overlay {
      background: rgba(0, 0, 0, 0.7);
      padding: 60px 20px;
    }

    .hero h1 {
      font-size: 48px;
      color: #fff;
      margin-bottom: 20px;
    }

    .hero p {
      font-size: 20px;
      color: #ddd;
    }

    section {
      padding: 60px 20px;
      text-align: center;
    }

    section h2 {
      color: #f00;
      margin-bottom: 20px;
    }

    section p {
      max-width: 700px;
      margin: 0 auto;
      line-height: 1.6;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">FitZone Pro</div>
    <div class="nav-links">
      <!-- روابط التنقل مع ترجمات -->
      <a href="#home" data-en="Home" data-fr="Accueil" data-ar="الرئيسية">Home</a>
      <a href="#about" data-en="About" data-fr="À propos" data-ar="من نحن">About</a>
      <a href="#services" data-en="Services" data-fr="Services" data-ar="الخدمات">Services</a>
      <a href="#plans" data-en="Plans" data-fr="Plans" data-ar="الخطط">Plans</a>
      <a href="#contact" data-en="Contact" data-fr="Contact" data-ar="اتصل بنا">Contact</a>
      <!-- اختيار اللغة -->
      <select class="lang-switcher">
        <option value="en">English</option>
        <option value="fr">Français</option>
        <option value="ar">العربية</option>
      </select>
    </div>
  </header>

  <section class="hero">
    <div class="overlay">
      <h1 id="hero-title">Welcome to FitZone Pro</h1>
      <p id="hero-subtitle">Your ultimate destination for fitness and bodybuilding coaching</p>
    </div>
  </section>

  <!-- قسم من نحن -->
  <section id="about">
    <h2 data-en="About Us" data-fr="À propos de nous" data-ar="من نحن">About Us</h2>
    <p id="about-text">We are a team of certified fitness and nutrition experts dedicated to transforming lives with custom workout plans and nutritional guidance.</p>
  </section>

  <!-- قسم الخدمات -->
  <section id="services">
    <h2 data-en="Our Services" data-fr="Nos services" data-ar="خدماتنا">Our Services</h2>
    <p id="services-text">Personal coaching, bodybuilding programs, meal planning, weight loss strategies, online classes and more.</p>
  </section>

  <!-- قسم الخطط -->
  <section id="plans">
    <h2 data-en="Our Plans" data-fr="Nos plans" data-ar="خططنا">Our Plans</h2>
    <p id="plans-text">Choose from basic to elite coaching plans. Whether you’re a beginner or a pro, we have the right plan for you.</p>
  </section>

  <!-- قسم التواصل -->
  <section id="contact">
    <h2 data-en="Contact Us" data-fr="Contactez-nous" data-ar="اتصل بنا">Contact Us</h2>
    <p id="contact-text">Reach us at contact@fitzonepro.com or follow us on Instagram and TikTok @fitzonepro</p>
  </section>

  <script>
    // مراجع لعناصر الصفحة للتغيير حسب اللغة
    const langSwitcher = document.querySelector('.lang-switcher');
    const navLinks = document.querySelectorAll('.nav-links a');
    const heroTitle = document.getElementById('hero-title');
    const heroSubtitle = document.getElementById('hero-subtitle');
    const aboutText = document.getElementById('about-text');
    const servicesText = document.getElementById('services-text');
    const plansText = document.getElementById('plans-text');
    const contactText = document.getElementById('contact-text');

    // النصوص المترجمة لكل لغة
    const translations = {
      en: {
        heroTitle: 'Welcome to FitZone Pro',
        heroSubtitle: 'Your ultimate destination for fitness and bodybuilding coaching',
        about: 'We are a team of certified fitness and nutrition experts dedicated to transforming lives with custom workout plans and nutritional guidance.',
        services: 'Personal coaching, bodybuilding programs, meal planning, weight loss strategies, online classes and more.',
        plans: 'Choose from basic to elite coaching plans. Whether you’re a beginner or a pro, we have the right plan for you.',
        contact: 'Reach us at contact@fitzonepro.com or follow us on Instagram and TikTok @fitzonepro'
      },
      fr: {
        heroTitle: 'Bienvenue chez FitZone Pro',
        heroSubtitle: 'Votre destination ultime pour le fitness et le coaching de musculation',
        about: 'Nous sommes une équipe d’experts certifiés en fitness et en nutrition dédiée à transformer des vies grâce à des programmes personnalisés.',
        services: 'Coaching personnel, programmes de musculation, plans alimentaires, stratégies de perte de poids, cours en ligne et plus.',
        plans: 'Choisissez parmi nos forfaits de coaching, du niveau de base au niveau élite. Que vous soyez débutant ou pro, nous avons un plan pour vous.',
        contact: 'Contactez-nous à contact@fitzonepro.com ou suivez-nous sur Instagram et TikTok @fitzonepro'
      },
      ar: {
        heroTitle: 'مرحبًا بك في FitZone Pro',
        heroSubtitle: 'وجهتك المثالية للتدريب على اللياقة وبناء الأجسام',
        about: 'نحن فريق من خبراء اللياقة والتغذية المعتمدين نسعى لتغيير حياة الناس من خلال برامج تدريب وتغذية مخصصة.',
        services: 'تدريب شخصي، برامج كمال أجسام، تخطيط وجبات، استراتيجيات فقدان الوزن، دروس عبر الإنترنت والمزيد.',
        plans: 'اختر من بين خطط التدريب الأساسية وحتى النخبة. سواء كنت مبتدئًا أو محترفًا، لدينا الخطة المناسبة لك.',
        contact: 'راسلنا على contact@fitzonepro.com أو تابعنا على Instagram و TikTok @fitzonepro'
      }
    };

    // حدث تغيير اللغة
    langSwitcher.addEventListener('change', (e) => {
      const lang = e.target.value;

      // تحديث روابط التنقل
      navLinks.forEach(link => {
        link.textContent = link.getAttribute(`data-${lang}`);
      });

      // تحديث عناوين الأقسام
      document.querySelector('#about h2').textContent = document.querySelector('#about h2').getAttribute(`data-${lang}`);
      document.querySelector('#services h2').textContent = document.querySelector('#services h2').getAttribute(`data-${lang}`);
      document.querySelector('#plans h2').textContent = document.querySelector('#plans h2').getAttribute(`data-${lang}`);
      document.querySelector('#contact h2').textContent = document.querySelector('#contact h2').getAttribute(`data-${lang}`);

      // تحديث النصوص الداخلية
      heroTitle.textContent = translations[lang].heroTitle;
      heroSubtitle.textContent = translations[lang].heroSubtitle;
      aboutText.textContent = translations[lang].about;
      servicesText.textContent = translations[lang].services;
      plansText.textContent = translations[lang].plans;
      contactText.textContent = translations[lang].contact;

      // تغيير اتجاه النص إذا كانت اللغة عربية
      document.documentElement.lang = lang;
      document.body.dir = (lang === 'ar') ? 'rtl' : 'ltr';
    });
  </script>
</body>
</html>
