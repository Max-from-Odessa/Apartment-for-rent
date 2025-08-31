
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Luxury Apartment for Rent in Odessa</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* CSS will be placed here */
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #f59e0b;
            --accent: #10b981;
            --light-bg: #f8fafc;
            --dark-bg: #0f172a;
            --text-dark: #1e293b;
            --text-light: #64748b;
            --white: #ffffff;
            --gray: #e2e8f0;
            --radius: 12px;
            --shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 20px 40px -10px rgba(0, 0, 0, 0.2);
            --transition: all 0.3s ease;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html, body {
            height: 100%;
            background: var(--light-bg);
            color: var(--text-dark);
            font-family: 'Montserrat', 'Roboto', system-ui, sans-serif;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        a {
            color: var(--primary);
            text-decoration: none;
            transition: var(--transition);
        }

        a:hover {
            color: var(--primary-dark);
        }

        img {
            max-width: 100%;
            height: auto;
        }

        .container {
            max-width: 1200px;
            width: 100%;
            margin: 0 auto;
            padding: 0 16px;
        }

        header {
            text-align: center;
            margin: 30px 0;
            padding: 20px;
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            border-radius: var(--radius);
            color: var(--white);
            box-shadow: var(--shadow);
        }

        header h1 {
            font-size: 28px;
            margin: 0;
            font-weight: 700;
        }

        header p {
            margin: 10px 0 0;
            font-size: 18px;
            opacity: 0.9;
        }

        .language-switcher {
            display: flex;
            justify-content: center;
            margin: 20px 0;
            gap: 10px;
        }

        .lang-btn {
            padding: 10px 20px;
            background: var(--gray);
            border: none;
            border-radius: var(--radius);
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .lang-btn.active, .lang-btn:hover {
            background: var(--primary);
            color: var(--white);
        }

        .card {
            background: var(--white);
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            padding: 25px;
            margin: 20px 0;
            transition: var(--transition);
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-lg);
        }

        h2 {
            margin: 0 0 15px;
            color: var(--primary);
            font-size: 24px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        h3 {
            margin: 20px 0 10px;
            color: var(--primary);
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        p {
            margin: 15px 0;
            color: var(--text-dark);
        }

        ul {
            margin: 15px 0;
            padding: 0;
            list-style: none;
        }

        li {
            margin: 10px 0;
            padding-left: 30px;
            position: relative;
        }

        li i {
            position: absolute;
            left: 0;
            top: 2px;
            color: var(--accent);
        }

        .note {
            display: block;
            margin-top: 20px;
            font-weight: 700;
            color: var(--primary-dark);
            padding: 15px;
            border-left: 4px solid var(--primary-dark);
            background: rgba(37, 99, 235, 0.08);
            border-radius: 8px;
        }

        .amenities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .amenity-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px;
            background: var(--light-bg);
            border-radius: var(--radius);
        }

        .amenity-item i {
            color: var(--accent);
            font-size: 20px;
        }

        .gallery-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 40px 0 20px;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .gallery-item {
            position: relative;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            cursor: pointer;
            aspect-ratio: 4/3;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .gallery-item:hover img {
            transform: scale(1.05);
        }

        .gallery-item::after {
            content: '';
            position: absolute;
            inset: 0;
            background: rgba(0, 0, 0, 0.2);
            opacity: 0;
            transition: var(--transition);
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        .lightbox {
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.95);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            z-index: 1000;
            padding: 20px;
        }

        .lightbox.active {
            opacity: 1;
            visibility: visible;
        }

        .lightbox-content {
            position: relative;
            max-width: 90%;
            max-height: 90%;
        }

        .lightbox-content img {
            max-width: 100%;
            max-height: 80vh;
            border-radius: var(--radius);
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6);
        }

        .lightbox-caption {
            position: absolute;
            bottom: -40px;
            left: 0;
            width: 100%;
            text-align: center;
            color: var(--white);
            padding: 10px;
        }

        .lightbox-close {
            position: absolute;
            top: -40px;
            right: 0;
            color: var(--white);
            font-size: 30px;
            background: none;
            border: none;
            cursor: pointer;
            transition: var(--transition);
        }

        .lightbox-close:hover {
            color: var(--secondary);
        }

        .lightbox-control {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            color: var(--white);
            font-size: 40px;
            background: rgba(0, 0, 0, 0.4);
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: none;
            border-radius: 50%;
            cursor: pointer;
            transition: var(--transition);
            z-index: 1001;
        }

        .lightbox-control:hover {
            background: rgba(0, 0, 0, 0.7);
        }

        .lightbox-prev {
            left: 20px;
        }

        .lightbox-next {
            right: 20px;
        }

        .contact-section {
            background: var(--white);
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            padding: 30px;
            margin: 40px 0;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px;
            background: var(--light-bg);
            border-radius: var(--radius);
            transition: var(--transition);
        }

        .contact-item:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow);
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 20px;
        }

        .map-section {
            margin: 40px 0;
        }

        .map-container {
            height: 400px;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .map-placeholder {
            height: 100%;
            background: var(--gray);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-light);
            font-size: 18px;
        }

        footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 40px;
            color: var(--text-light);
            border-top: 1px solid var(--gray);
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 22px;
            }
            
            .gallery {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .lightbox-control {
                width: 40px;
                height: 40px;
                font-size: 24px;
            }
            
            .lightbox-prev {
                left: 10px;
            }
            
            .lightbox-next {
                right: 10px;
            }
            
            .map-container {
                height: 300px;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 10px;
            }
            
            header {
                padding: 15px;
            }
            
            header h1 {
                font-size: 20px;
            }
            
            header p {
                font-size: 16px;
            }
            
            .card {
                padding: 20px;
            }
            
            .gallery {
                grid-template-columns: 1fr 1fr;
            }
            
            .contact-grid {
                grid-template-columns: 1fr;
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animate {
            animation: fadeIn 0.6s ease forwards;
        }

        .delay-1 { animation-delay: 0.1s; }
        .delay-2 { animation-delay: 0.2s; }
        .delay-3 { animation-delay: 0.3s; }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Luxury 1-Bedroom Apartment for Rent in Odessa</h1>
            <p>Середньофонтанська / Среднефонтанская, 30/1 (тихий двір / тихий двор)</p>
        </header>

        <div class="language-switcher">
            <button class="lang-btn active" data-lang="en">English</button>
            <button class="lang-btn" data-lang="ua">Українська</button>
            <button class="lang-btn" data-lang="ru">Русский</button>
        </div>

        <section class="card lang-section" id="en">
            <h2><i class="fas fa-star"></i> Cozy 1-room apartment for rent in Odessa</h2>
            <p>I am renting out my bright and spacious apartment at <strong>30/1 Srednefontanskaya Street</strong>, located inside a quiet and green courtyard. Fresh designer renovation, 8th floor of a 14-story building, total area <strong>44 sq.m</strong>. Layout: open-plan kitchen + living room, hallway, glazed balcony.</p>

            <h3><i class="fas fa-home"></i> Apartment features:</h3>
            <div class="amenities-grid">
                <div class="amenity-item">
                    <i class="fas fa-couch"></i>
                    <span>Modern furniture</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-plug"></i>
                    <span>Household appliances</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-shower"></i>
                    <span>Shower cabin</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-bed"></i>
                    <span>Double bed</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-warehouse"></i>
                    <span>2 large wardrobes</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-fan"></i>
                    <span>Air conditioner</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-tv"></i>
                    <span>TV</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-tshirt"></i>
                    <span>Washing machine</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-wifi"></i>
                    <span>High-speed Wi-Fi</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-parking"></i>
                    <span>Guest parking</span>
                </div>
            </div>

            <p><i class="fas fa-fire"></i> <strong>The house is very warm</strong>, with its own boiler room and a heat meter.</p>

            <p><i class="fas fa-map-marker-alt"></i> <strong>Great location:</strong> excellent transport connections, within walking distance to the Railway Station, Privoz Market, several universities, supermarkets, water station, park, playground, sports ground, kindergarten, and school.</p>

            <span class="note"><i class="fas fa-exclamation-circle"></i> The apartment is rented only to tenants <strong>without pets and children</strong>.</span>
        </section>

        <section class="card lang-section" id="ua" style="display: none;">
            <h2><i class="fas fa-star"></i> Здам 1-кімнатну затишну квартиру в Одесі</h2>
            <p>Пропоную в оренду свою світлу та простору квартиру за адресою <strong>вул. Середньофонтанська, 30/1</strong> — у середині кварталу, в тихому та зеленому подвір'ї. Свіжий дизайнерський ремонт, 8 поверх 14-поверхового будинку, площа <strong>44 м²</strong>. Планування: кухня-студія + кімната, передпокій, засклений балкон.</p>

            <h3><i class="fas fa-home"></i> У квартирі є все необхідне:</h3>
            <div class="amenities-grid">
                <div class="amenity-item">
                    <i class="fas fa-couch"></i>
                    <span>Сучасні меблі</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-plug"></i>
                    <span>Побутова техніка</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-shower"></i>
                    <span>Душова кабіна</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-bed"></i>
                    <span>Двоспальне ліжко</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-warehouse"></i>
                    <span>2 великі шафи</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-fan"></i>
                    <span>Кондиціонер</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-tv"></i>
                    <span>Телевізор</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-tshirt"></i>
                    <span>Пральна машина</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-wifi"></i>
                    <span>Інтернет Wi-Fi</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-parking"></i>
                    <span>Гостьова стоянка</span>
                </div>
            </div>

            <p><i class="fas fa-fire"></i> <strong>Будинок дуже тёплий</strong>, має власну котельню та теплолічильник.</p>

            <p><i class="fas fa-map-marker-alt"></i> <strong>Інфраструктура:</strong> зручна транспортна розв'язка, у пішій доступності Залізничний вокзал, Привоз, університети, супермаркети, бювет, парк, дитячий майданчик, спортмайданчик, дитячий садок і школа.</p>

            <span class="note"><i class="fas fa-exclamation-circle"></i> Квартира здається тільки орендарям <strong>без тварин і дітей</strong>.</span>
        </section>

        <section class="card lang-section" id="ru" style="display: none;">
            <h2><i class="fas fa-star"></i> Сдам 1-комнатную уютную квартиру в Одессе</h2>
            <p>Сдаётся моя светлая и просторная квартира на <strong>ул. Среднефонтанской, 30/1</strong> — внутри квартала, в тихом и зелёном дворе. Свежий дизайнерский ремонт, 8 этаж 14-этажного дома, площадь <strong>44 м²</strong>. Планировка: кухня-студия + комната, прихожая, застеклённый балкон.</p>

            <h3><i class="fas fa-home"></i> В квартире есть всё необходимое:</h3>
            <div class="amenities-grid">
                <div class="amenity-item">
                    <i class="fas fa-couch"></i>
                    <span>Современная мебель</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-plug"></i>
                    <span>Бытовая техника</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-shower"></i>
                    <span>Душевая кабина</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-bed"></i>
                    <span>Двуспальная кровать</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-warehouse"></i>
                    <span>2 больших шкафа</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-fan"></i>
                    <span>Кондиционер</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-tv"></i>
                    <span>Телевизор</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-tshirt"></i>
                    <span>Стиральная машина</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-wifi"></i>
                    <span>Интернет Wi-Fi</span>
                </div>
                <div class="amenity-item">
                    <i class="fas fa-parking"></i>
                    <span>Гостевая парковка</span>
                </div>
            </div>

            <p><i class="fas fa-fire"></i> <strong>Дом очень тёплый</strong>, с собственной котельной и теплосчётчиком.</p>

            <p><i class="fas fa-map-marker-alt"></i> <strong>Инфраструктура:</strong> отличная транспортная развязка, в пешей доступности ЖД вокзал, Привоз, университеты, супермаркеты, бювет, парк, детская площадка, спортплощадка, детсад и школа.</p>

            <span class="note"><i class="fas fa-exclamation-circle"></i> Квартира сдаётся только арендаторам <strong>без животных и детей</strong>.</span>
        </section>

        <div class="gallery-header">
            <h2><i class="fas fa-camera"></i> Photo Gallery</h2>
            <span id="image-counter">1/22</span>
        </div>

        <div class="gallery">
            <div class="gallery-item" data-index="1">
                <img src="https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Living room view" loading="lazy">
            </div>
            <div class="gallery-item" data-index="2">
                <img src="https://images.unsplash.com/photo-1484101403633-562f891dc89a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Kitchen area" loading="lazy">
            </div>
            <div class="gallery-item" data-index="3">
                <img src="https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Bedroom" loading="lazy">
            </div>
            <div class="gallery-item" data-index="4">
                <img src="https://images.unsplash.com/photo-1584622650111-993a426fbf0a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Bathroom" loading="lazy">
            </div>
            <div class="gallery-item" data-index="5">
                <img src="https://images.unsplash.com/photo-1537724326059-2ea202891b59?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Balcony" loading="lazy">
            </div>
            <div class="gallery-item" data-index="6">
                <img src="https://images.unsplash.com/photo-1499793983690-e29da59ef1c2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="View from window" loading="lazy">
            </div>
        </div>

        <div class="lightbox">
            <button class="lightbox-close"><i class="fas fa-times"></i></button>
            <button class="lightbox-control lightbox-prev"><i class="fas fa-chevron-left"></i></button>
            <button class="lightbox-control lightbox-next"><i class="fas fa-chevron-right"></i></button>
            <div class="lightbox-content">
                <img src="" alt="">
                <div class="lightbox-caption"></div>
            </div>
        </div>

        <section class="map-section">
            <h2><i class="fas fa-map-marked-alt"></i> Location</h2>
            <div class="map-container">
                <div class="map-placeholder">
                    <i class="fas fa-map-marker-alt" style="font-size: 40px; margin-right: 15px;"></i>
                    <div>Interactive Map: Среднефонтанская 30/1, Odessa, Ukraine</div>
                </div>
            </div>
        </section>

        <section class="contact-section">
            <h2><i class="fas fa-phone-alt"></i> Contact Information</h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    <div>
                        <h3>Phone</h3>
                        <p>+380 XX XXX XX XX</p>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fab fa-telegram"></i>
                    </div>
                    <div>
                        <h3>Telegram</h3>
                        <p>@username</p>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div>
                        <h3>Email</h3>
                        <p>email@example.com</p>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fab fa-viber"></i>
                    </div>
                    <div>
                        <h3>Viber</h3>
                        <p>+380 XX XXX XX XX</p>
                    </div>
                </div>
            </div>
        </section>

        <footer>
            <p>© 2023 Luxury Apartment Rental • Odessa, Ukraine</p>
        </footer>
    </div>

    <script>
        // JavaScript will be placed here
        document.addEventListener('DOMContentLoaded', function() {
            // Language switching functionality
            const langButtons = document.querySelectorAll('.lang-btn');
            const langSections = document.querySelectorAll('.lang-section');
            
            langButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const targetLang = button.getAttribute('data-lang');
                    
                    // Update active button
                    langButtons.forEach(btn => btn.classList.remove('active'));
                    button.classList.add('active');
                    
                    // Show selected language section, hide others
                    langSections.forEach(section => {
                        if (section.id === targetLang) {
                            section.style.display = 'block';
                            // Add animation class
                            section.classList.add('animate');
                        } else {
                            section.style.display = 'none';
                            section.classList.remove('animate');
                        }
                    });
                });
            });
            
            // Lightbox functionality
            const lightbox = document.querySelector('.lightbox');
            const lightboxImg = lightbox.querySelector('img');
            const lightboxCaption = lightbox.querySelector('.lightbox-caption');
            const lightboxClose = lightbox.querySelector('.lightbox-close');
            const lightboxPrev = lightbox.querySelector('.lightbox-prev');
            const lightboxNext = lightbox.querySelector('.lightbox-next');
            const galleryItems = document.querySelectorAll('.gallery-item');
            const imageCounter = document.getElementById('image-counter');
            
            let currentImageIndex = 1;
            const totalImages = galleryItems.length;
            
            // Open lightbox when clicking on gallery item
            galleryItems.forEach(item => {
                item.addEventListener('click', () => {
                    const imgIndex = item.getAttribute('data-index');
                    currentImageIndex = parseInt(imgIndex);
                    updateLightboxImage();
                    lightbox.classList.add('active');
                    document.body.style.overflow = 'hidden'; // Prevent scrolling when lightbox is open
                });
            });
            
            // Close lightbox
            lightboxClose.addEventListener('click', (e) => {
                e.stopPropagation();
                lightbox.classList.remove('active');
                document.body.style.overflow = ''; // Re-enable scrolling
            });
            
            // Navigate to previous image
            lightboxPrev.addEventListener('click', (e) => {
                e.stopPropagation();
                currentImageIndex = currentImageIndex > 1 ? currentImageIndex - 1 : totalImages;
                updateLightboxImage();
            });
            
            // Navigate to next image
            lightboxNext.addEventListener('click', (e) => {
                e.stopPropagation();
                currentImageIndex = currentImageIndex < totalImages ? currentImageIndex + 1 : 1;
                updateLightboxImage();
            });
            
            // Close lightbox when clicking outside the image
            lightbox.addEventListener('click', (e) => {
                if (e.target === lightbox) {
                    lightbox.classList.remove('active');
                    document.body.style.overflow = '';
                }
            });
            
            // Keyboard navigation
            document.addEventListener('keydown', (e) => {
                if (!lightbox.classList.contains('active')) return;
                
                if (e.key === 'Escape') {
                    lightbox.classList.remove('active');
                    document.body.style.overflow = '';
                } else if (e.key === 'ArrowLeft') {
                    currentImageIndex = currentImageIndex > 1 ? currentImageIndex - 1 : totalImages;
                    updateLightboxImage();
                } else if (e.key === 'ArrowRight') {
                    currentImageIndex = currentImageIndex < totalImages ? currentImageIndex + 1 : 1;
                    updateLightboxImage();
                }
            });
            
            // Update lightbox image and caption
            function updateLightboxImage() {
                const imageSrc = galleryItems[currentImageIndex - 1].querySelector('img').src;
                lightboxImg.src = imageSrc;
                lightboxImg.alt = `Image ${currentImageIndex}`;
                lightboxCaption.textContent = `Image ${currentImageIndex} of ${totalImages}`;
                imageCounter.textContent = `${currentImageIndex}/${totalImages}`;
            }
            
            // Add animation to elements on scroll
            const animateOnScroll = function() {
                const elements = document.querySelectorAll('.card, .gallery-item, .contact-item');
                
                elements.forEach(element => {
                    const elementPosition = element.getBoundingClientRect().top;
                    const screenPosition = window.innerHeight / 1.3;
                    
                    if (elementPosition < screenPosition) {
                        element.classList.add('animate');
                    }
                });
            };
            
            window.addEventListener('scroll', animateOnScroll);
            // Initial call to check elements in view on page load
            animateOnScroll();
            
            // Simulate loading of more images when scrolling to bottom
            window.addEventListener('scroll', function() {
                if ((window.innerHeight + window.scrollY) >= document.body.offsetHeight - 100) {
                    // This would be where you load more images in a real implementation
                    console.log('Load more images...');
                }
            });
        });
    </script>
</body>
</html>
