<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minecraft Skins - Sua Coleção de Skins</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #1a1a2e;
            color: #f0f0f0;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, #0f3460 0%, #1a1a2e 100%);
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: bold;
            color: #4ecca3;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            margin-bottom: 10px;
        }
        
        .logo span {
            color: #f0f0f0;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 10px 0;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            color: #f0f0f0;
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            transition: color 0.3s;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: #4ecca3;
            background-color: rgba(78, 204, 163, 0.1);
        }
        
        .hero {
            text-align: center;
            padding: 60px 20px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect fill="%23262645" width="50" height="50"/><rect fill="%23262645" x="50" y="50" width="50" height="50"/><rect fill="%231a1a2e" x="50" y="0" width="50" height="50"/><rect fill="%231a1a2e" x="0" y="50" width="50" height="50"/></svg>') repeat;
        }
        
        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: #4ecca3;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 30px;
            color: #f0f0f0;
        }
        
        .btn {
            display: inline-block;
            background-color: #4ecca3;
            color: #1a1a2e;
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
        
        .btn:hover {
            background-color: #3bb992;
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 40px;
            color: #4ecca3;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: #4ecca3;
            margin: 10px auto;
            border-radius: 2px;
        }
        
        .skin-categories {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .category-btn {
            background-color: #262645;
            color: #f0f0f0;
            border: none;
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 500;
        }
        
        .category-btn:hover, .category-btn.active {
            background-color: #4ecca3;
            color: #1a1a2e;
        }
        
        .skins-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }
        
        .skin-card {
            background-color: #262645;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .skin-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 20px rgba(0, 0, 0, 0.4);
        }
        
        .skin-img {
            width: 100%;
            height: 180px;
            background-color: #1a1a2e;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        
        .skin-img div {
            width: 100px;
            height: 150px;
            background: linear-gradient(45deg, #4ecca3, #2c9c7c);
            border-radius: 5px;
            position: relative;
        }
        
        .skin-info {
            padding: 15px;
        }
        
        .skin-info h3 {
            font-size: 1.2rem;
            margin-bottom: 8px;
            color: #f0f0f0;
        }
        
        .skin-info p {
            color: #a0a0a0;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }
        
        .skin-info a {
            display: inline-block;
            background-color: #4ecca3;
            color: #1a1a2e;
            padding: 8px 15px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 500;
            font-size: 0.9rem;
            transition: background-color 0.3s;
        }
        
        .skin-info a:hover {
            background-color: #3bb992;
        }
        
        .about {
            background-color: #262645;
            padding: 60px 0;
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .about-text h2 {
            font-size: 2.2rem;
            margin-bottom: 20px;
            color: #4ecca3;
        }
        
        .about-text p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .about-image div {
            width: 100%;
            max-width: 400px;
            height: 300px;
            margin: 0 auto;
            background: linear-gradient(45deg, #4ecca3, #2c9c7c);
            border-radius: 10px;
        }
        
        footer {
            background-color: #0f172a;
            padding: 40px 0 20px;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .footer-logo {
            font-size: 2rem;
            font-weight: bold;
            color: #4ecca3;
            margin-bottom: 20px;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .footer-links a {
            color: #f0f0f0;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: #4ecca3;
        }
        
        .copyright {
            color: #a0a0a0;
            font-size: 0.9rem;
            padding-top: 20px;
            border-top: 1px solid #2a2a4a;
            margin-top: 20px;
        }
        
        @media (max-width: 768px) {
            .logo {
                font-size: 2rem;
            }
            
            nav ul {
                flex-wrap: wrap;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .skins-grid {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">Minecraft<span>Skins</span></div>
        <nav>
            <ul>
                <li><a href="#">Início</a></li>
                <li><a href="#">Skins</a></li>
                <li><a href="#">Categorias</a></li>
                <li><a href="#">Upload</a></li>
                <li><a href="#">Sobre</a></li>
            </ul>
        </nav>
    </header>
    
    <section class="hero">
        <h1>Encontre as Melhores Skins para Minecraft</h1>
        <p>Explore nossa coleção de skins incríveis para personalizar seu personagem no Minecraft. De heróis a criaturas fantásticas, temos tudo o que você precisa!</p>
        <a href="#" class="btn">Explorar Skins</a>
    </section>
    
    <section class="container">
        <h2 class="section-title">Skins em Destaque</h2>
        
        <div class="skin-categories">
            <button class="category-btn active">Todas</button>
            <button class="category-btn">Heróis</button>
            <button class="category-btn">Animes</button>
            <button class="category-btn">Criaturas</button>
            <button class="category-btn">Famosos</button>
        </div>
        
        <div class="skins-grid">
            <div class="skin-card">
                <div class="skin-img">
                    <div></div>
                </div>
                <div class="skin-info">
                    <h3>Cyber Samurai</h3>
                    <p>Uma skin futurista com tema de samurai</p>
                    <a href="#">Baixar</a>
                </div>
            </div>
            
            <div class="skin-card">
                <div class="skin-img">
                    <div></div>
                </div>
                <div class="skin-info">
                    <h3>Dragon Warrior</h3>
                    <p>Combine a força de um guerreiro com um dragão</p>
                    <a href="#">Baixar</a>
                </div>
            </div>
            
            <div class="skin-card">
                <div class="skin-img">
                    <div></div>
                </div>
                <div class="skin-info">
                    <h3>Forest Elf</h3>
                    <p>Um élfico místico das florestas antigas</p>
                    <a href="#">Baixar</a>
                </div>
            </div>
            
            <div class="skin-card">
                <div class="skin-img">
                    <div></div>
                </div>
                <div class="skin-info">
                    <h3>Neon Ghost</h3>
                    <p>Uma assustadora fantasma com efeitos neon</p>
                    <a href="#">Baixar</a>
                </div>
            </div>
            
            <div class="skin-card">
                <div class="skin-img">
                    <div></div>
                </div>
                <div class="skin-info">
                    <h3>Steampunk Explorer</h3>
                    <p>Estilo vitoriano com tecnologia steam</p>
                    <a href="#">Baixar</a>
                </div>
            </div>
            
            <div class="skin-card">
                <div class="skin-img">
                    <div></div>
                </div>
                <div class="skin-info">
                    <h3>Ocean Guardian</h3>
                    <p>Protetor das profundezas do oceano</p>
                    <a href="#">Baixar</a>
                </div>
            </div>
        </div>
    </section>
    
    <section class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>Sobre Nossa Coleção</h2>
                    <p>Nosso site é dedicado a fornecer as melhores skins de Minecraft para jogadores de todos os estilos. Trabalhamos com designers talentosos para trazer skins únicas e de alta qualidade.</p>
                    <p>Todas as skins são testadas e otimizadas para garantir a melhor experiência no jogo. Você pode baixar as skins gratuitamente e usar em suas aventuras no Minecraft.</p>
                    <a href="#" class="btn">Saiba Mais</a>
                </div>
                <div class="about-image">
                    <div></div>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="footer-content">
            <div class="footer-logo">MinecraftSkins</div>
            <div class="footer-links">
                <a href="#">Início</a>
                <a href="#">Skins</a>
                <a href="#">Categorias</a>
                <a href="#">Upload</a>
                <a href="#">Sobre</a>
                <a href="#">Contato</a>
                <a href="#">Termos de Uso</a>
                <a href="#">Política de Privacidade</a>
            </div>
            <div class="copyright">
                &copy; 2023 MinecraftSkins. Todos os direitos reservados.
            </div>
        </div>
    </footer>

    <script>
        // Script simples para alternar categorias
        document.addEventListener('DOMContentLoaded', function() {
            const categoryButtons = document.querySelectorAll('.category-btn');
            
            categoryButtons.forEach(button => {
                button.addEventListener('click', function() {
                    // Remove a classe active de todos os botões
                    categoryButtons.forEach(btn => btn.classList.remove('active'));
                    
                    // Adiciona a classe active ao botão clicado
                    this.classList.add('active');
                    
                    // Aqui você normalmente filtraria as skins com base na categoria
                    // Para este exemplo, apenas mudamos a classe active
                });
            });
        });
    </script>
</body>
</html>
