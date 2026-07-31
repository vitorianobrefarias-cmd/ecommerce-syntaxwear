# SyntaxWear - Tênis e Sneakers Online 👟

> "Transforme qualquer passo em presença."

🔗 **Acesse o site online:** [https://vitorianobrefarias-cmd.github.io/ecommerce-syntaxwear/](https://vitorianobrefarias-cmd.github.io/ecommerce-syntaxwear/)

O **SyntaxWear** é uma interface moderna e responsiva de e-commerce focada na venda de tênis e sneakers exclusivos. O projeto foi desenvolvido com foco em alta performance, fidelidade visual e estruturação limpa de código, servindo como uma vitrine virtual para calçados casuais, modernos, esportivos e futuristas.

---

## 🚀 Demonstração Visual & Design

O design do site possui uma pegada urbana e sofisticada, utilizando tons neutros combinados com detalhes vibrantes em roxo (`#6329A2` / `#7c3aed`). 

### Seções Principais do Site
1. **Header Fixo Responsivo:** Com acesso rápido às categorias principais (Masculino, Feminino, Outlet), localização de lojas físicas, seção "Sobre", área do usuário, suporte e carrinho.
2. **Hero Section (Destaque):** Apresenta o modelo premium **Krypton One**, com chamadas diretas para ação ("Ver Modelos" e "Comprar").
3. **Categorias Principais:** Cards visuais refinados com efeito de overlay no hover para os estilos: **Casual**, **Moderno**, **Esporte** e **Futurista**.
4. **Vitrine em CSS Grid:** Um grid assimétrico marcante que exibe produtos em alta definição de forma diagramada, adaptando-se dinamicamente conforme a tela do dispositivo.
5. **Rodapé Completo:** Integrado com formulário de inscrição em newsletter, redes sociais estruturadas em SVG (Instagram, WhatsApp, TikTok, Facebook) e mapa de links rápidos.

---

## 🛠️ Tecnologias Utilizadas

A stack foi mantida enxuta e extremamente performática, priorizando o uso nativo dos recursos dos navegadores:

*   **HTML5 Semântico:** Uso correto de tags como `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` para melhor acessibilidade e SEO.
*   **CSS3 Avançado:**
    *   **Custom Properties (Variáveis CSS):** Para gestão eficiente de fontes e tokens.
    *   **Flexbox & CSS Grid:** Layouts flexíveis e o grid assimétrico complexo.
    *   **Media Queries:** Responsividade completa para Desktop, Tablet e Mobile.
*   **Google Fonts:** Integração das fontes de alta qualidade:
    *   *Ubuntu* (principal)
    *   *Inter*
    *   *Edu AU VIC WA NT Guides*

---

## 📐 Estrutura de Pastas e Arquivos

A arquitetura do projeto é modular, facilitando a escalabilidade de estilos através da separação por componentes:

```text
C:\Users\Vitoria Nobre\ecommerce-syntaxwear\
├── index.html                  # Página principal (Landing Page do e-commerce)
├── README.md                   # Documentação completa do projeto
├── css/                        # Diretório de folhas de estilo
│   ├── reset.css               # Reset de estilos cross-browser
│   ├── variables.css           # Variáveis globais e tokens (fontes, cores)
│   ├── bases.css               # Estilos globais do body, container 'main' e botões (.btn)
│   └── componentes/            # Estilos isolados por componentes da interface
│       ├── header.css          # Cabeçalho de navegação e menu mobile
│       ├── hero.css            # Banner principal e CTA (Call to Action)
│       ├── product-category.css # Cards de categorias com efeitos de overlay
│       ├── product-grid.css    # Vitrine em Grid Assimétrico responsivo
│       └── footer.css          # Layout do rodapé, redes sociais e newsletter
└── images/                     # Diretório de recursos visuais
    ├── banners/                # Banners para o Hero (Desktop e Mobile)
    ├── favicons/               # Ícones de navegador
    ├── logo/                   # Identidade visual da marca (SyntaxWear em SVG)
    ├── icons/                  # Ícones utilitários em formato vetorial SVG
    └── products/               # Fotografias de tênis em alta definição
```

---

## 💡 Destaques de Engenharia & CSS

### 1. Menu Responsivo Mobile (Sem JavaScript)
O cabeçalho utiliza a técnica inteligente do **Checkbox Hack** no CSS para controlar a abertura do menu hambúrguer em telas menores.
*   Um `input[type="checkbox"]` invisível é vinculado à label `.menu-icon`.
*   Ao clicar na label, o estado do checkbox muda, ativando a regra CSS:
    ```css
    .menu-toggle:checked ~ .nav-container {
        right: 0; /* Traz o menu mobile lateral para a tela */
    }
    ```
Isso garante uma navegação mobile fluida, leve e com **zero linhas de JavaScript**.

### 2. Grid de Produtos Assimétrico
A vitrine de produtos utiliza `grid-template-areas` para obter uma disposição única, saindo do tradicional formato em blocos idênticos:
```css
.grid-section {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(3, 300px);
    grid-template-areas:
        "top1 top1 top2 top2"
        "top1 top1 midL midR"
        "bottomL bottomL midL bottomR";
    gap: 30px;
}
```
Em telas menores (`max-width: 768px`), o grid se reorganiza automaticamente em duas colunas com alturas adaptadas, priorizando a usabilidade no celular.

---

## 💻 Como Rodar o Projeto Localmente

Por se tratar de um site estático (Frontend Vanilla), não é necessário instalar dependências pesadas para rodá-lo:

1.  **Clonar ou baixar** este repositório em sua máquina local.
2.  Abrir o arquivo `index.html` diretamente em seu navegador web (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari, etc.).
3.  *(Recomendado)* Para uma experiência de desenvolvimento em tempo real, utilize a extensão **Live Server** no VS Code ou qualquer servidor HTTP estático simples.

---

## 🔒 Licença e Direitos

Copyright © 2026 **SyntaxWear**. Todos os direitos reservados.
Projetado e desenvolvido como uma demonstração de excelência em design e desenvolvimento web moderno.
