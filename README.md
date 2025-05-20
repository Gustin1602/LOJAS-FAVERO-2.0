
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lojas Fávero</title>
    <style>
        /* Estilos Globais */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 15px 0;
            text-align: center;
        }

        nav ul {
            list-style-type: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
        }

        h1 {
            margin: 0;
        }

        /* Estilo do conteúdo principal */
        main {
            padding: 20px;
        }

        h2 {
            text-align: center;
            margin-bottom: 30px;
        }

        /* Ofertas do Dia */
        .ofertas {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
        }

        .oferta {
            background-color: #ffeb3b;
            color: #333;
            padding: 20px;
            width: 23%;
            text-align: center;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .oferta:hover {
            transform: scale(1.05);
        }

        /* Estilo dos produtos */
        section {
            display: inline-block;
            width: 30%;
            margin: 10px 1%;
            padding: 15px;
            background-color: white;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        section:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
        }

        section img {
            width: 100%;
            height: auto;
        }

        section h3 {
            color: #333;
            margin: 10px 0;
        }

        section p {
            color: #666;
            margin: 5px 0;
        }

        section .preco-antigo {
            text-decoration: line-through;
            color: #999;
            font-size: 14px;
        }

        section .preco-atual {
            color: #e53935;
            font-size: 18px;
            font-weight: bold;
        }

        section button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s ease;
        }

        section button:hover {
            background-color: #218838;
        }

        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 5px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
            font-size: 12px;
        }

        /* Responsividade */
        @media (max-width: 768px) {
            section {
                width: 45%;
            }

            .oferta {
                width: 45%;
            }
        }

        @media (max-width: 480px) {
            section {
                width: 90%;
            }

            .oferta {
                width: 90%;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Lojas Fávero</h1>
        <nav>
            <ul>
                 <li><a href="LOGIN.html">Login/Cadastro</a></li>
                <li><a href="TELA DE INICIO.html">Ofertas do Dia</a></li>
                <li><a href="OUTROS PRODUTOS.html">Outros Produtos</a></li>
                <li><a href="CONTATO.html">Contato</a></li>
               

                <li><a href="#" onclick="mostrarCarrinho()">Carrinho (<span id="carrinho-count">0</span>)</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- Ofertas do Dia -->
        <h2>Ofertas do Dia</h2>
        <section class="ofertas">
            <div class="oferta">
                <h3>Frete Grátis!</h3>
                <p>Em compras acima de R$ 100,00.</p>
            </div>
            <div class="oferta">
                <h3>Desconto de 10%</h3>
                <p>Em produtos selecionados.</p>
            </div>
            <div class="oferta">
                <h3>Compre 2, leve 3!</h3>
                <p>Em produtos da categoria X.</p>
            </div>
            <div class="oferta">
                <h3>Parcelamento em até 12x</h3>
                <p>Sem juros nas compras acima de R$ 200,00.</p>
            </div>
        </section>

        <!-- Produtos em Promoção -->
        <h2>Produtos em Promoção</h2>

        <section id="produto-1">
            <h3>Smartphone Iphone 15</h3>
            <p><strong>Marca: Iphone</strong></p>
            <img src="file:///C:/Users/Microlins/OneDrive/Imagens/preto--1--ka9jox3f2g.webp" alt="Smartphone Iphone 15">
            <p>Smartphone com 128GB de memória, câmera de 48MP, e bateria de 5000mAh.</p>
            <p class="preco-antigo">R$ 999,90</p>
            <p class="preco-atual">R$ 799,90</p>
            <button onclick="adicionarAoCarrinho('Smartphone Iphone 15', 799.90)">Adicionar ao Carrinho</button>
        </section>

        <section id="produto-2">
            <h3>Notebook Gamer Acer Nitro V</h3>
            <p><strong>Marca: Acer</strong></p>
            <img src="file:///C:/Users/Microlins/OneDrive/Imagens/164166-800-auto.webp" alt="Notebook Gamer Acer Nitro V">
            <p>Notebook com processador Intel i7, 16GB de RAM e SSD de 512GB.</p>
            <p class="preco-antigo">R$ 2.499,90</p>
            <p class="preco-atual">R$ 1.999,90</p>
            <button onclick="adicionarAoCarrinho('Notebook Gamer Acer Nitro V', 1999.90)">Adicionar ao Carrinho</button>
        </section>

        <section id="produto-3">
            <h3>Fone de Ouvido JBL</h3>
            <p><strong>Marca: JBL</strong></p>
            <img src="file:///C:/Users/Microlins/OneDrive/Imagens/0-JBLLIVE770PTO-PRD-1500-1.webp" alt="Fone de Ouvido JBL">
            <p>Fone de ouvido sem fio, com som de alta qualidade e cancelamento de ruído.</p>
            <p class="preco-antigo">R$ 399,90</p>
            <p class="preco-atual">R$ 299,90</p>
            <button onclick="adicionarAoCarrinho('Fone de Ouvido JBL', 299.90)">Adicionar ao Carrinho</button>
        </section>

       <section id="produto-4">
    <h3>TV 50" Samsung</h3>
    <p><strong>Marca: Samsung</strong></p>
    <img src="file:///C:/Users/Microlins/OneDrive/Imagens/3069506190_2GG.webp" alt="TV 50 Samsung">
    <p>TV 4K Ultra HD com tecnologia QLED e Smart TV integrada.</p>
    <p class="preco-antigo">R$ 3.499,90</p>
    <p class="preco-atual">R$ 2.899,90</p>
    <button onclick='adicionarAoCarrinho("TV 50\" Samsung", 2899.90)'>Adicionar ao Carrinho</button>
</section>


        <section id="produto-5">
            <h3>Tablet Samsung Galaxy Tab S9 Ultra</h3>
            <p><strong>Marca: Samsung</strong></p>
            <img src="file:///C:/Users/Microlins/OneDrive/Imagens/br-galaxy-tab-s9-ultra-wifi-x910-sm-x910nzahzto-538051636.webp" alt="Tablet Samsung Galaxy Tab S9 Ultra">
            <p>Tablet com 64GB de memória, tela de 10.4", e bateria de 7040mAh.</p>
            <p class="preco-antigo">R$ 1.499,90</p>
            <p class="preco-atual">R$ 1.299,90</p>
            <button onclick="adicionarAoCarrinho('Tablet Samsung Galaxy Tab S9 Ultra', 1299.90)">Adicionar ao Carrinho</button>
        </section>

        <section id="produto-6">
            <h3>Câmera Nikon D7200</h3>
            <p><strong>Marca:</strong> Nikon</p>
            <img src="file:///C:/Users/Microlins/OneDrive/Imagens/1.webp" alt="Câmera Nikon D7200">
            <p>Câmera DSLR D7200 com lente 18-55mm e 24.2 MP.</p>
            <p class="preco-antigo">R$ 2.699,90</p>
            <p class="preco-atual">R$ 2.199,90</p>
            <button onclick="adicionarAoCarrinho('Câmera Nikon D7200', 2199.90)">Adicionar ao Carrinho</button>
        </section>

        <!-- Novos Produtos Adicionados -->
        <section id="produto-7">
            <h3>Smartwatch Positivo</h3>
            <p><strong>Marca Positivo: TechWear</strong></p>
            <img src="file:///C:/Users/Microlins/OneDrive/Imagens/01_SMARTWATCH_POSITIVO_WATCH_ESSENTIAL_2024_PRETO_1000X1000.webp" alt="Smartwatch Positivo">
            <p>Smartwatch com monitoramento de saúde, GPS e tela de 1.8".</p>
            <p class="preco-antigo">R$ 599,90</p>
            <p class="preco-atual">R$ 499,90</p>
            <button onclick="adicionarAoCarrinho('Smartwatch Positivo', 499.90)">Adicionar ao Carrinho</button>
        </section>

        <section id="produto-8">
            <h3>Câmera de Segurança SafeHome</h3>
            <p><strong>Marca: SafeHome</strong></p>
            <img src="file:///C:/Users/Microlins/OneDrive/Imagens/51oDoNsN1ZL._AC_UF894,1000_QL80_.jpg" alt="Câmera de Segurança SafeHome">
            <p>Câmera de segurança com visão noturna e áudio bidirecional.</p>
            <p class="preco-antigo">R$ 399,90</p>
            <p class="preco-atual">R$ 299,90</p>
            <button onclick="adicionarAoCarrinho('Câmera de Segurança SafeHome', 299.90)">Adicionar ao Carrinho</button>
        </section>

<section id="produto-9">
    <h3>Caixa de Som Bluetooth</h3>
    <p><strong>Marca: SoundMax</strong></p>
    <img src="file:///C:/Users/Microlins/OneDrive/Imagens/caixa-torre-bluetooth-xt1200t-tws-polyvox.jpg" alt="Caixa de Som Bluetooth">
    <p>Caixa de som portátil com som de alta qualidade e 12 horas de autonomia.</p>
    <p class="preco-antigo">R$ 299,90</p>
    <p class="preco-atual">R$ 249,90</p>
    <button onclick="adicionarAoCarrinho('Caixa de Som Bluetooth', 249.90)">Adicionar ao Carrinho</button>


</section>

<script>
    let carrinho = JSON.parse(localStorage.getItem('carrinho')) || [];

    function adicionarAoCarrinho(produto, preco) {
        carrinho.push({ produto, preco });
        localStorage.setItem('carrinho', JSON.stringify(carrinho));
        atualizarContador();
        alert(`${produto} foi adicionado ao carrinho.`);
    }

    function atualizarContador() {
        document.getElementById('carrinho-count').textContent = carrinho.length;
    }

    function mostrarCarrinho() {
        window.location.href = 'carrinho.html';
    }

    atualizarContador(); // Atualiza o contador ao carregar a página
</script>


