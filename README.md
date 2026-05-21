<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Shree Sonal Auto - Used Two Wheelers, Mandvi</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;900&family=Open+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    :root {
      --black: #0a0a0a;
      --dark: #141414;
      --card: #1e1e1e;
      --gold: #f5c518;
      --gold-dark: #c9a014;
      --white: #ffffff;
      --gray: #9ca3af;
      --light-gray: #f3f4f6;
      --blue: #1a3a6e;
    }
    html { scroll-behavior: smooth; }
    body { font-family: 'Open Sans', sans-serif; background: var(--black); color: var(--white); overflow-x: hidden; }

    /* NAV */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      background: rgba(10,10,10,0.95); backdrop-filter: blur(12px);
      padding: 14px 40px; display: flex; align-items: center; justify-content: space-between;
      border-bottom: 1px solid rgba(245,197,24,0.2);
    }
    .nav-logo { display: flex; align-items: center; gap: 12px; }
    .nav-logo img { width: 48px; height: 48px; border-radius: 50%; object-fit: cover; border: 2px solid var(--gold); }
    .nav-logo-text { font-family: 'Montserrat', sans-serif; font-size: 1.1rem; font-weight: 800; color: var(--white); line-height: 1.2; }
    .nav-logo-text span { color: var(--gold); }
    .nav-links { display: flex; gap: 28px; list-style: none; }
    .nav-links a { text-decoration: none; font-size: 0.85rem; font-weight: 600; color: rgba(255,255,255,0.75); letter-spacing: 0.5px; transition: color 0.2s; text-transform: uppercase; }
    .nav-links a:hover { color: var(--gold); }
    .nav-cta { background: var(--gold); color: var(--black); padding: 10px 22px; border-radius: 6px; font-size: 0.85rem; font-weight: 700; text-decoration: none; transition: all 0.2s; text-transform: uppercase; letter-spacing: 0.5px; }
    .nav-cta:hover { background: var(--gold-dark); transform: translateY(-1px); }

    /* HERO */
    .hero {
      min-height: 100vh;
      background: linear-gradient(135deg, #0a0a0a 0%, #141414 50%, #0d1f3c 100%);
      display: flex; align-items: center; justify-content: center;
      text-align: center; padding: 120px 24px 80px; position: relative; overflow: hidden;
    }
    .hero-bg-text {
      position: absolute; font-family: 'Montserrat', sans-serif; font-size: 20vw;
      font-weight: 900; color: rgba(245,197,24,0.04); letter-spacing: -5px;
      top: 50%; left: 50%; transform: translate(-50%, -50%); white-space: nowrap; user-select: none;
    }
    .hero-badge {
      display: inline-block; background: rgba(245,197,24,0.1); border: 1px solid rgba(245,197,24,0.3);
      color: var(--gold); font-size: 0.75rem; font-weight: 700; letter-spacing: 3px;
      text-transform: uppercase; padding: 7px 20px; border-radius: 4px; margin-bottom: 24px;
      animation: fadeUp 0.8s ease both;
    }
    .hero-logo { width: 120px; height: 120px; border-radius: 50%; object-fit: cover; border: 3px solid var(--gold); margin-bottom: 24px; box-shadow: 0 0 40px rgba(245,197,24,0.3); animation: fadeUp 0.8s 0.1s ease both; }
    .hero h1 { font-family: 'Montserrat', sans-serif; font-size: clamp(2.5rem, 6vw, 5rem); font-weight: 900; color: white; line-height: 1.05; letter-spacing: -1px; animation: fadeUp 0.8s 0.2s ease both; }
    .hero h1 span { color: var(--gold); }
    .hero-sub { font-size: 1.05rem; color: rgba(255,255,255,0.6); margin-top: 16px; font-weight: 300; letter-spacing: 0.5px; animation: fadeUp 0.8s 0.35s ease both; }
    .hero-since { display: inline-block; margin-top: 12px; background: var(--gold); color: var(--black); font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 0.8rem; padding: 5px 16px; border-radius: 4px; letter-spacing: 2px; animation: fadeUp 0.8s 0.4s ease both; }
    .hero-btns { margin-top: 40px; display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; animation: fadeUp 0.8s 0.5s ease both; }
    .btn-gold { background: var(--gold); color: var(--black); padding: 14px 32px; border-radius: 6px; font-weight: 700; font-size: 0.95rem; text-decoration: none; transition: all 0.2s; display: inline-block; font-family: 'Montserrat', sans-serif; letter-spacing: 0.5px; }
    .btn-gold:hover { background: var(--gold-dark); transform: translateY(-2px); box-shadow: 0 8px 24px rgba(245,197,24,0.3); }
    .btn-outline-gold { background: transparent; color: var(--gold); padding: 14px 32px; border-radius: 6px; font-weight: 700; font-size: 0.95rem; text-decoration: none; border: 2px solid var(--gold); transition: all 0.2s; display: inline-block; font-family: 'Montserrat', sans-serif; letter-spacing: 0.5px; }
    .btn-outline-gold:hover { background: rgba(245,197,24,0.1); transform: translateY(-2px); }
    .hero-stats { display: flex; gap: 48px; justify-content: center; flex-wrap: wrap; margin-top: 56px; animation: fadeUp 0.8s 0.6s ease both; }
    .stat { text-align: center; }
    .stat-num { font-family: 'Montserrat', sans-serif; font-size: 2.2rem; font-weight: 900; color: var(--gold); line-height: 1; }
    .stat-label { font-size: 0.78rem; color: rgba(255,255,255,0.5); margin-top: 4px; text-transform: uppercase; letter-spacing: 1px; }

    /* SECTION BASE */
    .section-dark { background: var(--dark); padding: 90px 24px; }
    .section-black { background: var(--black); padding: 90px 24px; }
    .section-inner { max-width: 1100px; margin: 0 auto; }
    .section-label { font-size: 0.72rem; font-weight: 700; letter-spacing: 3px; text-transform: uppercase; color: var(--gold); margin-bottom: 12px; }
    .section-title { font-family: 'Montserrat', sans-serif; font-size: clamp(1.8rem, 4vw, 2.6rem); font-weight: 800; color: var(--white); line-height: 1.2; }
    .section-title span { color: var(--gold); }
    .divider { width: 48px; height: 3px; background: var(--gold); margin-top: 16px; border-radius: 2px; }

    /* WHY US */
    .why-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; margin-top: 48px; }
    .why-card { background: var(--card); border: 1px solid rgba(245,197,24,0.1); border-radius: 12px; padding: 28px 24px; transition: transform 0.25s, border-color 0.25s; }
    .why-card:hover { transform: translateY(-5px); border-color: rgba(245,197,24,0.4); }
    .why-icon { font-size: 2rem; margin-bottom: 14px; }
    .why-card h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 1rem; color: var(--white); }
    .why-card p { color: var(--gray); font-size: 0.875rem; margin-top: 8px; line-height: 1.6; }

    /* VEHICLES */
    .vehicles-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; margin-top: 48px; }
    .vehicle-card { background: var(--card); border: 1px solid rgba(255,255,255,0.06); border-radius: 12px; padding: 24px; text-align: center; transition: all 0.25s; }
    .vehicle-card:hover { border-color: var(--gold); transform: translateY(-4px); }
    .vehicle-icon { font-size: 2.5rem; margin-bottom: 12px; }
    .vehicle-card h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 0.95rem; color: var(--white); }
    .vehicle-card p { color: var(--gray); font-size: 0.82rem; margin-top: 6px; }

    /* HAPPY CUSTOMERS */
    .customers-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 24px; margin-top: 48px; }
    .customer-card { border-radius: 16px; overflow: hidden; position: relative; }
    .customer-card img { width: 100%; height: 380px; object-fit: cover; object-position: top; display: block; transition: transform 0.4s; }
    .customer-card:hover img { transform: scale(1.04); }
    .customer-overlay { position: absolute; bottom: 0; left: 0; right: 0; background: linear-gradient(transparent, rgba(0,0,0,0.85)); padding: 24px 20px 20px; }
    .congrats-badge { display: inline-block; background: var(--gold); color: var(--black); font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 0.72rem; padding: 4px 12px; border-radius: 4px; letter-spacing: 1px; margin-bottom: 6px; }
    .customer-overlay p { color: rgba(255,255,255,0.85); font-size: 0.85rem; }

    /* INSTAGRAM */
    .insta-section { background: linear-gradient(135deg, #833ab4, #fd1d1d, #f77737); padding: 80px 24px; text-align: center; }
    .insta-inner { max-width: 700px; margin: 0 auto; }
    .insta-logo { width: 90px; height: 90px; border-radius: 20px; object-fit: cover; margin: 0 auto 20px; display: block; border: 3px solid white; box-shadow: 0 8px 30px rgba(0,0,0,0.3); }
    .insta-section h2 { font-family: 'Montserrat', sans-serif; font-size: clamp(1.8rem, 4vw, 2.4rem); font-weight: 800; color: white; }
    .insta-handle { font-size: 1.2rem; color: rgba(255,255,255,0.9); margin-top: 8px; font-weight: 600; letter-spacing: 1px; }
    .insta-section p { color: rgba(255,255,255,0.8); margin-top: 10px; font-size: 0.95rem; }
    .btn-white { display: inline-block; margin-top: 28px; background: white; color: #833ab4; padding: 14px 36px; border-radius: 6px; font-weight: 700; font-size: 0.95rem; text-decoration: none; transition: all 0.2s; font-family: 'Montserrat', sans-serif; }
    .btn-white:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,0,0,0.2); }

    /* CONTACT */
    .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; margin-top: 48px; }
    .contact-card { background: var(--card); border: 1px solid rgba(245,197,24,0.15); border-radius: 12px; padding: 28px 24px; display: flex; align-items: flex-start; gap: 16px; transition: border-color 0.2s; }
    .contact-card:hover { border-color: rgba(245,197,24,0.4); }
    .contact-icon { font-size: 1.6rem; margin-top: 2px; }
    .contact-card h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 0.85rem; color: var(--gold); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 6px; }
    .contact-card p { color: var(--gray); font-size: 0.9rem; line-height: 1.6; }
    .contact-card a { color: var(--white); text-decoration: none; font-weight: 600; font-size: 1rem; }
    .contact-card a:hover { color: var(--gold); }
    .map-btn { display: inline-block; margin-top: 32px; }

    /* FOOTER */
    footer { background: #050505; border-top: 1px solid rgba(245,197,24,0.15); text-align: center; padding: 30px 24px; }
    footer p { color: rgba(255,255,255,0.4); font-size: 0.82rem; }
    footer span { color: var(--gold); }


    /* VEHICLE SHOWCASE */
    .vgrid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 24px; margin-top: 48px; }
    .vcard { background: var(--card); border: 1px solid rgba(255,255,255,0.06); border-radius: 14px; overflow: hidden; transition: all 0.3s; }
    .vcard:hover { transform: translateY(-6px); border-color: var(--gold); box-shadow: 0 12px 40px rgba(245,197,24,0.15); }
    .vcard-img-wrap { position: relative; background: #111; }
    .vcard-img-wrap img { width: 100%; height: 220px; object-fit: contain; padding: 16px; display: block; transition: transform 0.4s; }
    .vcard:hover .vcard-img-wrap img { transform: scale(1.05); }
    .vcard-badge { position: absolute; top: 12px; left: 12px; background: rgba(245,197,24,0.15); border: 1px solid rgba(245,197,24,0.4); color: var(--gold); font-size: 0.7rem; font-weight: 700; letter-spacing: 1px; padding: 4px 10px; border-radius: 4px; text-transform: uppercase; }
    .vcard-info { padding: 20px; border-top: 1px solid rgba(255,255,255,0.06); }
    .vcard-info h3 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 1rem; color: var(--white); margin-bottom: 4px; }
    .vcard-info p { color: var(--gray); font-size: 0.82rem; margin-bottom: 14px; }
    .vcard-btn { display: inline-block; background: var(--gold); color: var(--black); font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 0.8rem; padding: 8px 18px; border-radius: 5px; text-decoration: none; transition: all 0.2s; letter-spacing: 0.5px; }
    .vcard-btn:hover { background: var(--gold-dark); transform: translateY(-1px); }


    /* HAPPY CUSTOMERS */
    .cust-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 20px; margin-top: 48px; }
    .cust-card { border-radius: 14px; overflow: hidden; position: relative; border: 1px solid rgba(245,197,24,0.1); transition: all 0.3s; }
    .cust-card:hover { border-color: var(--gold); transform: translateY(-5px); box-shadow: 0 12px 40px rgba(245,197,24,0.15); }
    .cust-img-wrap { position: relative; overflow: hidden; }
    .cust-img-wrap img { width: 100%; height: 380px; object-fit: cover; object-position: top; display: block; transition: transform 0.4s; }
    .cust-card:hover .cust-img-wrap img { transform: scale(1.04); }
    .cust-overlay { position: absolute; bottom: 0; left: 0; right: 0; background: linear-gradient(transparent, rgba(0,0,0,0.88)); padding: 28px 18px 18px; }
    .cust-badge { display: inline-block; background: var(--gold); color: var(--black); font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 0.72rem; padding: 4px 12px; border-radius: 4px; letter-spacing: 1px; margin-bottom: 6px; }
    .cust-handle { color: rgba(255,255,255,0.85); font-size: 0.85rem; margin-top: 4px; }

    @keyframes fadeUp { from { opacity: 0; transform: translateY(28px); } to { opacity: 1; transform: translateY(0); } }
    @media (max-width: 640px) { nav { padding: 12px 16px; } .nav-links { display: none; } .hero-stats { gap: 28px; } }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">
    <img src="data:image/jpeg;base64,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
