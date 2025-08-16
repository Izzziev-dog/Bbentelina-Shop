# Bentelina-Shop
<!DOCTYPE html>  
<html lang="ru">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Bentelina - элитная парфюмерия со всего мира</title>  
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">  
    <style>  
        /* Основные стили */  
        * {  
            margin: 0;  
            padding: 0;  
            box-sizing: border-box;  
            font-family: 'Montserrat', 'Arial', sans-serif;  
        }  
          
        body {  
            background-color: #f9f3f0;  
            color: #333;  
            line-height: 1.6;  
        }  
          
        .container {  
            max-width: 1200px;  
            margin: 0 auto;  
            padding: 0 20px;  
        }  
          
        /* Шапка сайта */  
        header {  
            background-color: rgba(255, 255, 255, 0.95);  
            padding: 15px 0;  
            position: fixed;  
            width: 100%;  
            z-index: 100;  
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);  
            transition: all 0.3s ease;  
        }  
          
        .header-content {  
            display: flex;  
            justify-content: space-between;  
            align-items: center;  
        }  
          
        .logo {  
            font-size: 28px;  
            font-weight: 700;  
            color: #b08e77;  
            letter-spacing: 1px;  
        }  
          
        nav ul {  
            display: flex;  
            list-style: none;  
        }  
          
        nav ul li {  
            margin-left: 30px;  
            position: relative;  
        }  
          
        nav ul li a {  
            color: #333;  
            text-decoration: none;  
            font-weight: 500;  
            transition: color 0.3s;  
            font-size: 16px;  
        }  
          
        nav ul li a:hover {  
            color: #b08e77;  
        }  
          
        nav ul li a::after {  
            content: '';  
            position: absolute;  
            width: 0;  
            height: 2px;  
            background: #b08e77;  
            bottom: -5px;  
            left: 0;  
            transition: width 0.3s;  
        }  
          
        nav ul li a:hover::after {  
            width: 100%;  
        }  
          
        /* Герой-секция */  
        .hero {  
            height: 100vh;  
            background: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),   
                        url('https://images.unsplash.com/photo-1592945403244-b3fbafd7f539?ixlib=rb-1.2.1&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;  
            display: flex;  
            align-items: center;  
            text-align: center;  
            color: #fff;  
        }  
          
        .hero-content h1 {  
            font-size: 52px;  
            margin-bottom: 20px;  
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);  
        }  
          
        .hero-content p {  
            font-size: 22px;  
            margin-bottom: 30px;  
            max-width: 800px;  
            margin-left: auto;  
            margin-right: auto;  
            text-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);  
        }  
          
        .btn {  
            display: inline-block;  
            background-color: #b08e77;  
            color: #fff;  
            padding: 14px 35px;  
            border-radius: 30px;  
            text-decoration: none;  
            font-weight: 600;  
            transition: all 0.3s;  
            border: 2px solid #b08e77;  
            text-transform: uppercase;  
            letter-spacing: 1px;  
            font-size: 14px;  
        }  
          
        .btn:hover {  
            background-color: transparent;  
            color: #fff;  
            transform: translateY(-3px);  
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);  
        }  
          
        /* Секция о магазине */  
        .about {  
            padding: 120px 0;  
            background-color: #fff;  
        }  
          
        .section-title {  
            text-align: center;  
            margin-bottom: 60px;  
            font-size: 36px;  
            color: #b08e77;  
            position: relative;  
        }  
          
        .section-title::after {  
            content: '';  
            display: block;  
            width: 80px;  
            height: 3px;  
            background: #b08e77;  
            margin: 15px auto 0;  
        }  
          
        .about-content {  
            display: flex;  
            align-items: center;  
            gap: 50px;  
        }  
          
        .about-text {  
            flex: 1;  
        }  
          
        .about-text h3 {  
            font-size: 28px;  
            margin-bottom: 20px;  
            color: #555;  
        }  
          
        .about-text p {  
            margin-bottom: 15px;  
            font-size: 16px;  
            color: #666;  
        }  
          
        .about-image {  
            flex: 1;  
            border-radius: 10px;  
            overflow: hidden;  
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);  
        }  
          
        .about-image img {  
            width: 100%;  
            height: auto;  
            display: block;  
            transition: transform 0.5s;  
        }  
          
        .about-image:hover img {  
            transform: scale(1.05);  
        }  
          
        /* Особенности */  
        .features {  
            padding: 100px 0;  
            background-color: #f9f3f0;  
        }  
          
        .features-grid {  
            display: grid;  
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));  
            gap: 30px;  
        }  
          
        .feature {  
            background-color: #fff;  
            padding: 40px 30px;  
            border-radius: 10px;  
            text-align: center;  
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);  
            transition: all 0.3s;  
        }  
          
        .feature:hover {  
            transform: translateY(-10px);  
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);  
        }  
          
        .feature-icon {  
            font-size: 50px;  
            color: #b08e77;  
            margin-bottom: 20px;  
        }  
          
        .feature h3 {  
            margin-bottom: 15px;  
            font-size: 22px;  
            color: #555;  
        }  
          
        .feature p {  
            color: #777;  
            font-size: 15px;  
        }  
          
        /* Галерея парфюмов */  
        .perfume-gallery {  
            padding: 100px 0;  
            background-color: #fff;  
        }  
          
        .gallery-grid {  
            display: grid;  
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));  
            gap: 25px;  
            margin-top: 50px;  
        }  
          
        .perfume-item {  
            position: relative;  
            border-radius: 10px;  
            overflow: hidden;  
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);  
            transition: all 0.3s;  
        }  
          
        .perfume-item:hover {  
            transform: translateY(-10px);  
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);  
        }  
          
        .perfume-item img {  
            width: 100%;  
            height: 300px;  
            object-fit: cover;  
            display: block;  
            transition: transform 0.5s;  
        }  
          
        .perfume-item:hover img {  
            transform: scale(1.1);  
        }  
          
        .perfume-info {  
            position: absolute;  
            bottom: 0;  
            left: 0;  
            right: 0;  
            background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);  
            padding: 20px;  
            color: #fff;  
        }  
          
        .perfume-info h3 {  
            font-size: 18px;  
            margin-bottom: 5px;  
        }  
          
        .perfume-info .price {  
            font-weight: 700;  
            font-size: 20px;  
            color: #b08e77;  
        }  
          
        /* Подвал */  
        footer {  
            background-color: #333;  
            padding: 70px 0 30px;  
            color: #fff;  
        }  
          
        .footer-content {  
            display: grid;  
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));  
            gap: 40px;  
            margin-bottom: 50px;  
        }  
          
        .footer-column h3 {  
            font-size: 20px;  
            margin-bottom: 25px;  
            color: #b08e77;  
            position: relative;  
            padding-bottom: 10px;  
        }  
          
        .footer-column h3::after {  
            content: '';  
            position: absolute;  
            left: 0;  
            bottom: 0;  
            width: 40px;  
            height: 2px;  
            background: #b08e77;  
        }  
          
        .footer-column ul {  
            list-style: none;  
        }  
          
        .footer-column ul li {  
            margin-bottom: 12px;  
        }  
          
        .footer-column ul li a {  
            color: #ccc;  
            text-decoration: none;  
            transition: color 0.3s;  
        }  
          
        .footer-column ul li a:hover {  
            color: #b08e77;  
            padding-left: 5px;  
        }  
          
        .footer-bottom {  
            text-align: center;  
            padding-top: 30px;  
            border-top: 1px solid #444;  
            color: #999;  
            font-size: 14px;  
        }  
          
        /* Анимации */  
        .animate-on-scroll {  
            opacity: 0;  
            transform: translateY(30px);  
            transition: opacity 0.6s, transform 0.6s;  
        }  
          
        .animate-on-scroll.visible {  
            opacity: 1;  
            transform: translateY(0);  
        }  
          
        .delay-1 {  
            transition-delay: 0.2s;  
        }  
          
        .delay-2 {  
            transition-delay: 0.4s;  
        }  
          
        .delay-3 {  
            transition-delay: 0.6s;  
        }  
    </style>  
</head>  
<body>  
    <!-- Шапка сайта -->  
    <header>  
        <div class="container">  
            <div class="header-content">  
                <div class="logo">BENTELINA</div>  
  <header>  
    <div class="container">  
        <div class="header-content">  
            <div class="logo">BENTELINA</div>  
            <div class="header-actions">  
                <a href="#search" class="search-btn"><i class="fas fa-search"></i></a>  
                <a href="#profile" class="profile-btn"><i class="far fa-user"></i></a>  
            </div>  
        </div>  
    </div>  
</header>  
  
<style>  
    /* Обновлённые стили шапки */  
    header {  
        background-color: rgba(255, 255, 255, 0.98);  
        padding: 15px 0;  
        position: fixed;  
        width: 100%;  
        z-index: 100;  
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);  
    }  
      
    .header-content {  
        display: flex;  
        justify-content: space-between;  
        align-items: center;  
    }  
      
    .header-actions a {  
        color: #333;  
        font-size: 18px;  
        margin-left: 20px;  
        transition: color 0.3s;  
    }  
      
    .header-actions a:hover {  
        color: #b08e77;  
    }  
</style>  
  
    </header>  
  
    <!-- Герой-секция -->  
    <section class="hero">  
        <div class="container">  
            <div class="hero-content animate__animated animate__fadeIn">  
                <h1>Элитная парфюмерия со всего мира</h1>  
                <p>Bentelina - это уникальная коллекция изысканных ароматов от ведущих мировых домов моды и нишевых парфюмеров</p>  
                <a href="#gallery" class="btn animate__animated animate__pulse animate__infinite animate__slower">Открыть каталог</a>  
            </div>  
        </div>  
    </section>  
  
    <!-- Секция о магазине -->  
    <section id="about" class="about">  
        <div class="container">  
            <h2 class="section-title animate-on-scroll">О НАШЕМ МАГАЗИНЕ</h2>  
            <div class="about-content">  
                <div class="about-text animate-on-scroll delay-1">  
                    <h3>Bentelina - мир изысканных ароматов</h3>  
                    <p>Мы - премиальный бутик парфюмерии, предлагающий эксклюзивные ароматы со всего мира. Наша коллекция включает в себя как культовые ароматы от ведущих модных домов, так и редкие нишевые композиции от независимых парфюмеров.</p>  
                    <p>Основанный в 2010 году, наш магазин быстро завоевал репутацию среди ценителей прекрасного благодаря индивидуальному подходу к каждому клиенту и тщательно подобранному ассортименту.</p>  
                    <p>Мы сотрудничаем напрямую с производителями, что гарантирует подлинность каждого флакона и лучшие цены для наших клиентов.</p>  
                </div>  
                <div class="about-image animate-on-scroll delay-2">  
                    <img src="https://images.unsplash.com/photo-1594035910387-fea47794261f?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Магазин Bentelina">  
                </div>  
            </div>  
        </div>  
    </section>  
  
    <!-- Преимущества -->  
    <section id="features" class="features">  
        <div class="container">  
            <h2 class="section-title animate-on-scroll">НАШИ ПРЕИМУЩЕСТВА</h2>  
            <div class="features-grid">  
                <div class="feature animate-on-scroll delay-1">  
                    <div class="feature-icon">🌎</div>  
                    <h3>Ароматы со всего мира</h3>  
                    <p>Мы собрали для вас лучшие парфюмерные композиции из Франции, Италии, Великобритании, США и других стран.</p>  
                </div>  
                  
                <div class="feature animate-on-scroll delay-2">  
                    <div class="feature-icon">✔️</div>  
                    <h3>Гарантия подлинности</h3>  
                    <p>Все ароматы поставляются напрямую от производителей или официальных дистрибьюторов с полным комплектом документов.</p>  
                </div>  
                  
                <div class="feature animate-on-scroll delay-3">  
                    <div class="feature-icon">💎</div>  
                    <h3>Эксклюзивные предложения</h3>  
                    <p>У нас вы найдете редкие и ограниченные серии, которые не представлены в обычных парфюмерных сетях.</p>  
                </div>  
            </div>  
        </div>  
    </section>  
  
    <!-- Галерея парфюмов -->  
    <section id="gallery" class="perfume-gallery">  
        <div class="container">  
            <h2 class="section-title animate-on-scroll">ПОПУЛЯРНЫЕ АРОМАТЫ</h2>  
            <div class="gallery-grid">  
                <div class="perfume-item animate-on-scroll delay-1">  
                    <img src="https://images.unsplash.com/photo-1594035910387-fea47794261f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Chanel №5">  
                    <div class="perfume-info">  
                        <h3>Chanel №5</h3>  
                        <div class="price">12 490 ₽</div>  
                    </div>  
                </div>  
                  
                <div class="perfume-item animate-on-scroll delay-2">  
                    <img src="https://images.unsplash.com/photo-1594035910387-fea47794261f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Dior Sauvage">  
                    <div class="perfume-info">  
                        <h3>Dior Sauvage</h3>  
                        <div class="price">9 990 ₽</div>  
                    </div>  
                </div>  
                  
                <div class="perfume-item animate-on-scroll delay-1">  
                    <img src="https://images.unsplash.com/photo-1594035910387-fea47794261f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Tom Ford Black Orchid">  
                    <div class="perfume-info">  
                        <h3>Tom Ford Black Orchid</h3>  
                        <div class="price">15 790 ₽</div>  
                    </div>  
                </div>  
                  
                <div class="perfume-item animate-on-scroll delay-2">  
                    <img src="https://images.unsplash.com/photo-1594035910387-fea47794261f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Creed Aventus">  
                    <div class="perfume-info">  
                        <h3>Creed Aventus</h3>  
                        <div class="price">22 500 ₽</div>  
                    </div>  
                </div>  
            </div>  
        </div>  
    </section>  
  
    <!-- Подвал -->  
    <footer id="contacts">  
        <div class="container">  
            <div class="footer-content">  
                <div class="footer-column">  
                    <h3>О Bentelina</h3>  
                    <p>Элитный бутик парфюмерии с 2010 года. Мы предлагаем только лучшие ароматы от мировых брендов.</p>  
                </div>  
                  
                <div class="footer-column">  
                    <h3>Контакты</h3>  
                    <ul>  
                        <li>Москва, ул. Тверская, 18</li>  
                        <li>+7 (495) 123-45-67</li>  
                        <li>info@bentelina.ru</li>  
                    </ul>  
                </div>  
                  
                <div class="footer-column">  
                    <h3>Часы работы</h3>  
                    <ul>  
                        <li>Пн-Пт: 10:00 - 21:00</li>  
                        <li>Сб-Вс: 11:00 - 20:00</li>  
                    </ul>  
                </div>  
                  
                <div class="footer-column">  
                    <h3>Полезные ссылки</h3>  
                    <ul>  
                        <li><a href="#">Доставка и оплата</a></li>  
                        <li><a href="#">Возврат и обмен</a></li>  
                        <li><a href="#">Политика конфиденциальности</a></li>  
                    </ul>  
                </div>  
            </div>  
              
            <div class="footer-bottom">  
                <p>© 2023 Bentelina. Все права защищены.</p>  
            </div>  
        </div>  
    </footer>  
  
    <script>  
        // Плавная прокрутка для якорных ссылок  
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {  
            anchor.addEventListener('click', function (e) {  
                e.preventDefault();  
                  
                document.querySelector(this.getAttribute('href')).scrollIntoView({  
                    behavior: 'smooth'  
                });  
            });  
        });  
          
        // Изменение шапки при прокрутке  
        window.addEventListener('scroll', function() {  
            const header = document.querySelector('header');  
            if (window.scrollY > 50) {  
                header.style.background = 'rgba(255, 255, 255, 0.98)';  
                header.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.1)';  
            } else {  
                header.style.background = 'rgba(255, 255, 255, 0.95)';  
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';  
            }  
        });  
          
        // Анимация при скролле  
        const animateElements = document.querySelectorAll('.animate-on-scroll');  
          
        const observer = new IntersectionObserver((entries) => {  
            entries.forEach(entry => {  
                if (entry.isIntersecting) {  
                    entry.target.classList.add('visible');  
                    observer.unobserve(entry.target);  
                }  
            });  
        }, {  
            threshold: 0.1  
        });  
          
        animateElements.forEach(element => {  
            observer.observe(element);  
        });  
    </script>  
</body>  
</html>  
  
<!DOCTYPE html>  
<html lang="ru">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Bentelina - элитная парфюмерия со всего мира</title>  
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">  
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">  
    <style>  
        /* (Предыдущие стили остаются без изменений) */  
  
        /* Стили для плавающих кнопок */  
        .fab-container {  
            position: fixed;  
            bottom: 30px;  
            right: 30px;  
            z-index: 999;  
            display: flex;  
            flex-direction: column;  
            align-items: flex-end;  
        }  
          
        .fab-main {  
            width: 60px;  
            height: 60px;  
            border-radius: 50%;  
            background: linear-gradient(135deg, #b08e77, #d4a992);  
            color: white;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            font-size: 24px;  
            box-shadow: 0 4px 20px rgba(176, 142, 119, 0.3);  
            cursor: pointer;  
            transition: all 0.3s;  
            position: relative;  
            z-index: 2;  
        }  
          
        .fab-main:hover {  
            transform: scale(1.1);  
            box-shadow: 0 6px 25px rgba(176, 142, 119, 0.4);  
        }  
          
        .fab-buttons {  
            display: flex;  
            flex-direction: column;  
            align-items: flex-end;  
            margin-bottom: 15px;  
            opacity: 0;  
            visibility: hidden;  
            transform: translateY(20px);  
            transition: all 0.3s;  
            position: absolute;  
            bottom: 70px;  
            right: 0;  
        }  
          
        .fab-buttons.show {  
            opacity: 1;  
            visibility: visible;  
            transform: translateY(0);  
        }  
          
        .fab-button {  
            width: 50px;  
            height: 50px;  
            border-radius: 50%;  
            background-color: white;  
            color: #b08e77;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            margin-top: 10px;  
            box-shadow: 0 3px 15px rgba(0, 0, 0, 0.1);  
            cursor: pointer;  
            transition: all 0.3s;  
            position: relative;  
        }  
          
        .fab-button:hover {  
            transform: scale(1.1);  
            background-color: #f5f5f5;  
        }  
          
        .fab-button .tooltip {  
            position: absolute;  
            right: 70px;  
            background-color: #333;  
            color: white;  
            padding: 5px 10px;  
            border-radius: 5px;  
            font-size: 12px;  
            white-space: nowrap;  
            opacity: 0;  
            visibility: hidden;  
            transition: all 0.3s;  
        }  
          
        .fab-button:hover .tooltip {  
            opacity: 1;  
            visibility: visible;  
            right: 60px;  
        }  
          
        .fab-button .badge {  
            position: absolute;  
            top: -5px;  
            right: -5px;  
            background-color: #e74c3c;  
            color: white;  
            border-radius: 50%;  
            width: 20px;  
            height: 20px;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            font-size: 10px;  
            font-weight: bold;  
        }  
    </style>  
</head>  
<body>  
    <!-- (Предыдущий HTML-код остается без изменений) -->  
  
    <!-- Плавающие кнопки -->  
    <div class="fab-container">  
        <div class="fab-buttons">  
            <div class="fab-button">  
                <i class="fas fa-shopping-cart"></i>  
                <span class="tooltip">Корзина (3)</span>  
                <span class="badge">3</span>  
            </div>  
            <div class="fab-button">  
                <i class="fas fa-heart"></i>  
                <span class="tooltip">Избранное</span>  
            </div>  
            <div class="fab-button">  
                <i class="fas fa-search"></i>  
                <span class="tooltip">Поиск</span>  
            </div>  
            <div class="fab-button">  
                <i class="fas fa-headset"></i>  
                <span class="tooltip">Поддержка</span>  
            </div>  
        </div>  
        <div class="fab-main" id="fabMain">  
            <i class="fas fa-plus"></i>  
        </div>  
    </div>  
  
    <script>  
        // (Предыдущий JavaScript код остается без изменений)  
  
        // Управление плавающими кнопками  
        const fabMain = document.getElementById('fabMain');  
        const fabButtons = document.querySelector('.fab-buttons');  
          
        fabMain.addEventListener('click', function() {  
            fabButtons.classList.toggle('show');  
            this.querySelector('i').classList.toggle('fa-plus');  
            this.querySelector('i').classList.toggle('fa-times');  
        });  
          
        // Закрывать кнопки при клике вне области  
        document.addEventListener('click', function(e) {  
            if (!e.target.closest('.fab-container')) {  
                fabButtons.classList.remove('show');  
                fabMain.querySelector('i').classList.remove('fa-times');  
                fabMain.querySelector('i').classList.add('fa-plus');  
            }  
        });  
    </script>  
</body>  
</html>  
  
<!-- ======= Секция "Категории парфюмерии" ======= -->  
<section id="categories" class="categories-section" style="padding: 80px 0; background-color: #fff;">  
  <div class="container">  
    <h2 class="section-title animate-on-scroll">Наши коллекции</h2>  
      
    <!-- Категория 1: Женские ароматы -->  
    <div class="category animate-on-scroll delay-1">  
      <h3 class="category-title">  
        <i class="fas fa-venus" style="color: #e83e8c; margin-right: 10px;"></i>  
        Женские ароматы  
        <a href="#women" class="view-all">Смотреть все →</a>  
      </h3>  
        
      <div class="products-grid">  
        <!-- Товар 1 -->  
        <div class="product-card">  
          <div class="product-badge">Хит</div>  
          <img src="https://via.placeholder.com/300x300?text=Chanel+No5" alt="Chanel №5">  
          <div class="product-info">  
            <h4>Chanel №5</h4>  
            <p class="brand">Chanel</p>  
            <div class="price">12 490 ₽ <span class="old-price">14 990 ₽</span></div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
          
        <!-- Товар 2 -->  
        <div class="product-card">  
          <img src="https://via.placeholder.com/300x300?text=Miss+Dior" alt="Miss Dior">  
          <div class="product-info">  
            <h4>Miss Dior</h4>  
            <p class="brand">Dior</p>  
            <div class="price">10 990 ₽</div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
          
        <!-- Товар 3 -->  
        <div class="product-card">  
          <div class="product-badge">New</div>  
          <img src="https://via.placeholder.com/300x300?text=Libre" alt="Libre">  
          <div class="product-info">  
            <h4>Libre</h4>  
            <p class="brand">Yves Saint Laurent</p>  
            <div class="price">11 790 ₽</div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
      </div>  
    </div>  
      
    <!-- Категория 2: Мужские ароматы -->  
    <div class="category animate-on-scroll delay-2">  
      <h3 class="category-title">  
        <i class="fas fa-mars" style="color: #3498db; margin-right: 10px;"></i>  
        Мужские ароматы  
        <a href="#men" class="view-all">Смотреть все →</a>  
      </h3>  
        
      <div class="products-grid">  
        <!-- Товар 1 -->  
        <div class="product-card">  
          <img src="https://via.placeholder.com/300x300?text=Sauvage" alt="Sauvage">  
          <div class="product-info">  
            <h4>Sauvage</h4>  
            <p class="brand">Dior</p>  
            <div class="price">9 990 ₽</div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
          
        <!-- Товар 2 -->  
        <div class="product-card">  
          <div class="product-badge">-20%</div>  
          <img src="https://via.placeholder.com/300x300?text=Bleu+de+Chanel" alt="Bleu de Chanel">  
          <div class="product-info">  
            <h4>Bleu de Chanel</h4>  
            <p class="brand">Chanel</p>  
            <div class="price">10 392 ₽ <span class="old-price">12 990 ₽</span></div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
          
        <!-- Товар 3 -->  
        <div class="product-card">  
          <img src="https://via.placeholder.com/300x300?text=Acqua+di+Gio" alt="Acqua di Gio">  
          <div class="product-info">  
            <h4>Acqua di Gio</h4>  
            <p class="brand">Giorgio Armani</p>  
            <div class="price">8 990 ₽</div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
      </div>  
    </div>  
      
    <!-- Категория 3: Нишевая парфюмерия -->  
    <div class="category animate-on-scroll delay-3">  
      <h3 class="category-title">  
        <i class="fas fa-star" style="color: #f1c40f; margin-right: 10px;"></i>  
        Нишевая коллекция  
        <a href="#niche" class="view-all">Смотреть все →</a>  
      </h3>  
        
      <div class="products-grid">  
        <!-- Товар 1 -->  
        <div class="product-card">  
          <div class="product-badge">Эксклюзив</div>  
          <img src="https://via.placeholder.com/300x300?text=Aventus" alt="Aventus">  
          <div class="product-info">  
            <h4>Aventus</h4>  
            <p class="brand">Creed</p>  
            <div class="price">22 500 ₽</div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
          
        <!-- Товар 2 -->  
        <div class="product-card">  
          <img src="https://via.placeholder.com/300x300?text=Black+Afgano" alt="Black Afgano">  
          <div class="product-info">  
            <h4>Black Afgano</h4>  
            <p class="brand">Nasomatto</p>  
            <div class="price">18 990 ₽</div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
          
        <!-- Товар 3 -->  
        <div class="product-card">  
          <img src="https://via.placeholder.com/300x300?text=Oud+Wood" alt="Oud Wood">  
          <div class="product-info">  
            <h4>Oud Wood</h4>  
            <p class="brand">Tom Ford</p>  
            <div class="price">24 990 ₽</div>  
            <button class="add-to-cart">В корзину</button>  
          </div>  
        </div>  
      </div>  
    </div>  
  </div>  
</section>  
  
<style>  
  /* Стили для секции категорий */  
  .categories-section {  
    padding: 80px 0;  
  }  
    
  .category {  
    margin-bottom: 60px;  
  }  
    
  .category-title {  
    display: flex;  
    align-items: center;  
    font-size: 24px;  
    margin-bottom: 25px;  
    padding-bottom: 10px;  
    border-bottom: 1px solid #eee;  
    color: #555;  
  }  
    
  .view-all {  
    margin-left: auto;  
    font-size: 14px;  
    color: #b08e77;  
    text-decoration: none;  
    transition: all 0.3s;  
  }  
    
  .view-all:hover {  
    color: #8a6d5b;  
    text-decoration: underline;  
  }  
    
  .products-grid {  
    display: grid;  
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));  
    gap: 25px;  
  }  
    
  .product-card {  
    background: #fff;  
    border-radius: 10px;  
    overflow: hidden;  
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);  
    transition: all 0.3s;  
    position: relative;  
  }  
    
  .product-card:hover {  
    transform: translateY(-5px);  
    box-shadow: 0 10px 25px rgba(0,0,0,0.1);  
  }  
    
  .product-badge {  
    position: absolute;  
    top: 10px;  
    right: 10px;  
    background: #b08e77;  
    color: white;  
    padding: 3px 10px;  
    border-radius: 20px;  
    font-size: 12px;  
    font-weight: bold;  
    z-index: 2;  
  }  
    
  .product-card img {  
    width: 100%;  
    height: 280px;  
    object-fit: cover;  
    border-bottom: 1px solid #f0f0f0;  
  }  
    
  .product-info {  
    padding: 20px;  
  }  
    
  .product-info h4 {  
    font-size: 18px;  
    margin-bottom: 5px;  
    color: #333;  
  }  
    
  .brand {  
    color: #777;  
    font-size: 14px;  
    margin-bottom: 10px;  
  }  
    
  .price {  
    font-weight: bold;  
    font-size: 18px;  
    color: #b08e77;  
    margin-bottom: 15px;  
  }  
    
  .old-price {  
    text-decoration: line-through;  
    color: #999;  
    font-size: 14px;  
    font-weight: normal;  
    margin-left: 8px;  
  }  
    
  .add-to-cart {  
    width: 100%;  
    padding: 10px;  
    background: #f5f5f5;  
    border: none;  
    border-radius: 5px;  
    color: #b08e77;  
    font-weight: 600;  
    cursor: pointer;  
    transition: all 0.3s;  
  }  
    
  .add-to-cart:hover {  
    background: #b08e77;  
    color: white;  
  }  
</style>  
  
<script>  
  // Обработчик для кнопок "В корзину"  
  document.querySelectorAll('.add-to-cart').forEach(button => {  
    button.addEventListener('click', function() {  
      const productCard = this.closest('.product-card');  
      const productName = productCard.querySelector('h4').textContent;  
        
      // Анимация добавления  
      this.textContent = '✓ Добавлено';  
      this.style.background = '#4CAF50';  
      this.style.color = 'white';  
        
      // Восстановление кнопки через 2 секунды  
      setTimeout(() => {  
        this.textContent = 'В корзину';  
        this.style.background = '#f5f5f5';  
        this.style.color = '#b08e77';  
      }, 2000);  
        
      // Здесь можно добавить логику добавления в корзину  
      console.log(`Товар "${productName}" добавлен в корзину`);  
        
      // Обновление счетчика в FAB-кнопке  
      const cartBadge = document.querySelector('.fab-button .badge');  
      cartBadge.textContent = parseInt(cartBadge.textContent) + 1;  
    });  
  });  
</script>  
  
<!-- Нижнее меню -->  
<nav class="bottom-nav">  
    <a href="#home" class="nav-item active">  
        <i class="fas fa-home"></i>  
        <span>Главная</span>  
    </a>  
    <a href="#catalog" class="nav-item">  
        <i class="fas fa-list"></i>  
        <span>Каталог</span>  
    </a>  
    <a href="#cart" class="nav-item cart-btn">  
        <i class="fas fa-shopping-cart"></i>  
        <span>Корзина</span>  
        <span class="cart-count">3</span>  
    </a>  
    <a href="#favorites" class="nav-item">  
        <i class="fas fa-heart"></i>  
        <span>Избранное</span>  
    </a>  
    <a href="#profile" class="nav-item">  
        <i class="far fa-user"></i>  
        <span>Профиль</span>  
    </a>  
</nav>  
  
<style>  
    /* Стили нижнего меню */  
    .bottom-nav {  
        position: fixed;  
        bottom: 0;  
        left: 0;  
        right: 0;  
        background: white;  
        display: flex;  
        justify-content: space-around;  
        padding: 10px 0;  
        box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);  
        z-index: 999;  
    }  
      
    .nav-item {  
        display: flex;  
        flex-direction: column;  
        align-items: center;  
        text-decoration: none;  
        color: #777;  
        font-size: 12px;  
        transition: all 0.3s;  
        position: relative;  
        padding: 5px 10px;  
    }  
      
    .nav-item i {  
        font-size: 20px;  
        margin-bottom: 3px;  
    }  
      
    .nav-item.active {  
        color: #b08e77;  
    }  
      
    .nav-item:hover {  
        color: #b08e77;  
    }  
      
    .cart-count {  
        position: absolute;  
        top: -5px;  
        right: 0;  
        background: #e74c3c;  
        color: white;  
        border-radius: 50%;  
        width: 18px;  
        height: 18px;  
        display: flex;  
        align-items: center;  
        justify-content: center;  
        font-size: 10px;  
        font-weight: bold;  
    }  
      
    @media (min-width: 768px) {  
        .bottom-nav {  
            display: none; /* Скрываем на десктопах */  
        }  
    }  
</style>  
  
<script>  
    // Подсветка активного пункта меню  
    document.querySelectorAll('.nav-item').forEach(item => {  
        item.addEventListener('click', function() {  
            document.querySelectorAll('.nav-item').forEach(i => i.classList.remove('active'));  
            this.classList.add('active');  
        });  
    });  
</script>  
  
// Показываем FAB-кнопки только на десктопах  
function updateFabVisibility() {  
    const fabContainer = document.querySelector('.fab-container');  
    if (window.innerWidth >= 768) {  
        fabContainer.style.display = 'block';  
    } else {  
        fabContainer.style.display = 'none';  
    }  
}  
  
window.addEventListener('resize', updateFabVisibility);  
updateFabVisibility();  
