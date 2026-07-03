# 📦 Componentes CSS - E-Shoes

Biblioteca de componentes CSS reutilizáveis e responsivos para o projeto E-Shoes.

## 📁 Estrutura

```
css/components/
├── header.css          # Cabeçalho e navegação
├── hero.css            # Seção hero/banner principal
├── product-card.css    # Card individual de produto
├── product-grid.css    # Grid de produtos
├── newsletter.css      # Seção de newsletter
├── panel.css           # Painéis genéricos
├── footer.css          # Rodapé
├── index.css           # Arquivo principal (importa todos)
└── README.md           # Este arquivo
```

## 🚀 Como Usar

### Importar todos os componentes

**No seu arquivo CSS principal:**
```css
@import url('./components/index.css');
```

**Ou no HTML `<head>`:**
```html
<link rel="stylesheet" href="css/components/index.css">
```

### Importar componentes específicos

```css
@import url('./components/header.css');
@import url('./components/hero.css');
@import url('./components/product-grid.css');
```

---

## 📋 Componentes Disponíveis

### 1. **Header** (`header.css`)

Cabeçalho sticky com navegação principal e menu do usuário.

**Classes principais:**
- `.site-header` - Container principal
- `.site-nav` - Navegação principal
- `.user-nav` - Navegação do usuário

**Exemplo:**
```html
<header class="site-header">
  <h1>
    <a href="/">
      <img src="logo.png" alt="E-Shoes">
    </a>
  </h1>
  <nav class="site-nav">
    <ul>
      <li><a href="#">Masculino</a></li>
      <li><a href="#">Feminino</a></li>
    </ul>
  </nav>
  <nav class="user-nav">
    <ul>
      <li><a href="#">Carrinho</a></li>
      <li><a href="#">Conta</a></li>
    </ul>
  </nav>
</header>
```

---

### 2. **Hero** (`hero.css`)

Seção hero com CTA buttons e animações.

**Classes principais:**
- `.hero` - Container principal
- `.hero__title` - Título
- `.hero__subtitle` - Subtítulo
- `.hero__cta` - Container de botões
- `.hero__button` - Botão
- `.hero__button--solid` - Botão sólido

**Exemplo:**
```html
<section class="hero">
  <div class="hero__content">
    <h1 class="hero__title">Bem-vindo à E-Shoes</h1>
    <p class="hero__subtitle">Encontre os melhores tênis</p>
    <div class="hero__cta">
      <button class="hero__button hero__button--solid">Explorar</button>
      <button class="hero__button">Saiba Mais</button>
    </div>
  </div>
</section>
```

---

### 3. **Product Card** (`product-card.css`)

Card individual de um produto.

**Classes principais:**
- `.product-card` - Container
- `.product-card__image` - Imagem
- `.product-card__title` - Título
- `.product-card__price-current` - Preço atual
- `.product-card__price-original` - Preço original
- `.product-card__badge` - Badge de desconto
- `.product-card__btn` - Botão
- `.product-card__btn--primary` - Botão primário

**Exemplo:**
```html
<div class="product-card">
  <img src="product.jpg" class="product-card__image" alt="Produto">
  <span class="product-card__badge">-30%</span>
  
  <div class="product-card__content">
    <span class="product-card__category">Tênis</span>
    <h3 class="product-card__title">Nike Air Max</h3>
    
    <div class="product-card__rating">
      <span class="product-card__stars">★★★★☆</span>
      <span class="product-card__reviews">(125 avaliações)</span>
    </div>
    
    <div class="product-card__price">
      <span class="product-card__price-original">R$ 199,90</span>
      <span class="product-card__price-current">R$ 139,90</span>
      <span class="product-card__discount">-30%</span>
    </div>
    
    <div class="product-card__actions">
      <button class="product-card__btn product-card__btn--primary">
        Comprar
      </button>
      <button class="product-card__icon-btn">❤</button>
    </div>
  </div>
</div>
```

---

### 4. **Product Grid** (`product-grid.css`)

Grid responsivo para exibir múltiplos produtos.

**Classes principais:**
- `.grid-produtos` - Grid principal
- `.grid-produtos--dense` - Versão compacta
- `.grid-produtos--spacious` - Versão espaçosa
- `.produtos-wrapper` - Wrapper com sidebar
- `.produtos-sidebar` - Filtros
- `.produtos-main` - Área principal

**Responsividade:**
- Desktop grande: 4 colunas (1400px+)
- Desktop: 3 colunas (1024px+)
- Tablet: 2 colunas (768px+)
- Mobile: 1 coluna (<768px)

**Exemplo:**
```html
<div class="grid-produtos">
  <div class="product-card"><!-- ... --></div>
  <div class="product-card"><!-- ... --></div>
  <div class="product-card"><!-- ... --></div>
</div>
```

---

### 5. **Newsletter** (`newsletter.css`)

Seção de inscrição em newsletter com gradiente.

**Classes principais:**
- `.newsletter` - Container
- `.newsletter__title` - Título
- `.newsletter__form` - Formulário
- `.newsletter__input` - Input de email
- `.newsletter__button` - Botão de envio

**Exemplo:**
```html
<section class="newsletter">
  <h2 class="newsletter__title">Receba Nossas Novidades</h2>
  <p class="newsletter__description">Fique atualizado com as últimas coleções</p>
  
  <form class="newsletter__form">
    <input 
      type="email" 
      class="newsletter__input" 
      placeholder="seu@email.com"
    >
    <button class="newsletter__button">Inscrever</button>
  </form>
  
  <label class="newsletter__check">
    <input type="checkbox">
    Concordo com os termos
  </label>
</section>
```

---

### 6. **Panel** (`panel.css`)

Painel genérico para organizar conteúdo.

**Classes principais:**
- `.panel` - Container base
- `.panel__header` - Cabeçalho
- `.panel__title` - Título
- `.panel__body` - Corpo
- `.panel__footer` - Rodapé
- `.panel--featured` - Painel em destaque
- `.panel--hover` - Com efeito hover

**Exemplo:**
```html
<div class="panel panel--hover">
  <div class="panel__header">
    <h3 class="panel__title">Informações do Pedido</h3>
  </div>
  
  <div class="panel__body">
    <div class="panel__content-item">
      <span class="panel__content-label">Pedido:</span>
      <span class="panel__content-value">#12345</span>
    </div>
    <div class="panel__content-item">
      <span class="panel__content-label">Status:</span>
      <span class="panel__content-value">Enviado</span>
    </div>
  </div>
  
  <div class="panel__footer">
    <button class="btn btn-primary">Ver Detalhes</button>
  </div>
</div>
```

---

### 7. **Footer** (`footer.css`)

Rodapé completo com links, redes sociais e informações.

**Classes principais:**
- `.site-footer` - Container principal
- `.footer-inner` - Conteúdo interno
- `.footer-section` - Seção de links
- `.footer-contato` - Informações de contato
- `.footer-social` - Redes sociais
- `.footer-bottom` - Rodapé com créditos

**Exemplo:**
```html
<footer class="site-footer">
  <div class="container footer-inner">
    <section class="footer-section">
      <h3 class="footer-section__title">Sobre</h3>
      <ul class="footer-section__list">
        <li><a href="#" class="footer-section__link">Quem Somos</a></li>
        <li><a href="#" class="footer-section__link">Carreiras</a></li>
      </ul>
    </section>
    
    <section class="footer-contato">
      <div class="footer-contato__item">
        <span class="footer-contato__icon">📞</span>
        <div class="footer-contato__content">
          <div class="footer-contato__label">Telefone</div>
          <a href="tel:+5511999999999" class="footer-contato__value">
            +55 11 9999-9999
          </a>
        </div>
      </div>
    </section>
    
    <section class="footer-social">
      <div class="footer-social__title">Redes Sociais</div>
      <a href="#" class="footer-social__link">f</a>
      <a href="#" class="footer-social__link">📷</a>
      <a href="#" class="footer-social__link">𝕏</a>
    </section>
  </div>
  
  <div class="footer-bottom">
    <div class="footer-bottom__credit">
      &copy; 2024 E-Shoes. Todos os direitos reservados.
    </div>
    <div class="footer-bottom__legal">
      <a href="#" class="footer-bottom__legal-link">Privacidade</a>
      <a href="#" class="footer-bottom__legal-link">Termos</a>
    </div>
  </div>
</footer>
```

---

## 🎨 Variáveis CSS Utilizadas

Os componentes usam as seguintes variáveis CSS (definidas em `variable.css`):

```css
--color-primary        /* Azul principal */
--color-primary-dark   /* Azul escuro */
--color-dark           /* Cor escura */
--color-light          /* Branco */
--color-light-gray     /* Cinza claro */
--color-border         /* Cor de borda */
--color-text-secondary /* Texto secundário */
```

---

## 📱 Responsividade

Todos os componentes são totalmente responsivos:

| Breakpoint | Tipo | Colunas (Grid) |
|---|---|---|
| `≥ 1400px` | Desktop Grande | 4 |
| `1024px - 1399px` | Desktop | 3 |
| `768px - 1023px` | Tablet | 2 |
| `< 768px` | Mobile | 1 |

---

## ⚡ Performance

- ✅ Sem dependências externas
- ✅ CSS puro e otimizado
- ✅ Carregamento modular
- ✅ Animações suaves com GPU
- ✅ Compatível com navegadores modernos

---

## ♿ Acessibilidade

- ✅ Semântica HTML apropriada
- ✅ Atributos ARIA quando necessário
- ✅ Contraste de cores adequado
- ✅ Navegação por teclado
- ✅ Suporte a leitores de tela

---

## 🔧 Customização

Para customizar um componente:

1. **Via variáveis CSS:**
```css
:root {
  --color-primary: #sua-cor;
}
```

2. **Sobrescrevendo classes:**
```css
.hero__title {
  font-size: 4rem; /* Sobrescreve o original */
}
```

3. **Editando os arquivos** (se necessário)

---

## 📝 Convenção de Nomenclatura

Utilizamos a metodologia **BEM (Block Element Modifier)**:

```
.component              /* Bloco */
.component__element     /* Elemento */
.component--modifier    /* Modificador */
```

**Exemplo:**
```
.product-card           /* Bloco */
.product-card__image    /* Elemento */
.product-card--featured /* Modificador */
```

---

## 🚀 Dicas de Uso

### 1. Importação Eficiente
```css
/* ❌ Evitar múltiplas importações */
@import url('./header.css');
@import url('./hero.css');

/* ✅ Preferir usar index.css */
@import url('./index.css');
```

### 2. Combinando Componentes
```html
<!-- Usar panel dentro de hero -->
<section class="hero">
  <div class="panel">
    <div class="panel__body">
      <!-- conteúdo -->
    </div>
  </div>
</section>
```

### 3. Estados Customizados
```html
<!-- Adicionar classes para estados -->
<div class="product-card is-loading">
<div class="product-card is-disabled">
<div class="product-card is-selected">
```

---

## 📧 Documentação

Para exemplos completos e mais informações, consulte cada arquivo `.css` individual.

---

**Última atualização:** 2024
**Versão:** 1.0
