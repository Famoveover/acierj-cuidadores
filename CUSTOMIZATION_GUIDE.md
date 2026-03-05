# ACIERJ - Instruções de Customização e Manutenção

## 📖 Como Usar Esta Página

### Estrutura de Arquivos

```
acierj-cuidadores/
├── index.html              # Página Home (principal)
├── sobre.html              # Página Quem Somos
├── servicos.html           # Página Áreas de Atuação
├── eventos.html            # Página Eventos
├── associe-se.html         # Página Associe-se
├── contato.html            # Página Contato
├── style.css               # Estilos globais (CSS modular)
├── acierj.png              # Logo da associação
├── DESIGN_REFERENCE.md     # (Este arquivo) - Referência completa de design
└── README.md              # Instruções do projeto
```

---

## 🎨 Personalizando a Página

### 1. Alterar Cores

Abra `style.css` e procure pela seção **"1. VARIÁVEIS CSS - PALETA DE CORES"**:

```css
:root {
  /* Cores Primárias (Força Social) */
  --color-primary-red: #d32f2f;        /* Vermelho vibrante */
  --color-primary-dark: #b71c1c;       /* Vermelho escuro */
  
  /* Cores Secundárias (Representatividade) */
  --color-accent-purple: #7b1fa2;      /* Roxo - Inclusão LGBTQIA+ */
  --color-accent-yellow: #ffc107;      /* Amarelo/Ouro - Esperança */
  --color-accent-green: #388e3c;       /* Verde - Vida */
  
  /* Cores de Texto */
  --color-text-dark: #1a1a1a;          /* Preto - Legibilidade */
  --color-text-light: #ffffff;         /* Branco - Contraste */
  --color-text-gray: #4a4a4a;          /* Cinza escuro - Secundário */
}
```

**Exemplo:** Para mudar o vermelho para laranja:
```css
--color-primary-red: #ff6f00;
--color-primary-dark: #e65100;
```

---

### 2. Modificar Tipografia

#### Trocar Fonte do Header/Títulos:

```css
:root {
  --font-serif: "Playfair Display", serif;  /* Nova fonte serif */
}
```

#### Trocar Fonte do Corpo:

```css
:root {
  --font-sans: "Open Sans", sans-serif;  /* Nova fonte sans-serif */
}
```

**Nota:** Adicione a importação no topo do CSS:
```css
@import url("https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Open+Sans:wght@300;400;600;700&display=swap");
```

---

### 3. Ajustar Espaçamento

Todas as distâncias usam variáveis CSS. Para aumentar o espaçamento geral:

```css
:root {
  --spacing-xs: 0.75rem;    /* 0.5rem → 0.75rem */
  --spacing-sm: 1.5rem;     /* 1rem → 1.5rem */
  --spacing-md: 2rem;       /* 1.5rem → 2rem */
  --spacing-lg: 2.5rem;     /* 2rem → 2.5rem */
  --spacing-xl: 4rem;       /* 3rem → 4rem */
}
```

---

### 4. Modificar Gradientes

### Hero Section:
```css
.hero {
  /* Mudou de: vermelho → roxo
     Para: outro gradiente */
  background: linear-gradient(135deg, #ff6f00 0%, #d32f2f 100%);
}
```

### CTA Section:
```css
.cta {
  background: linear-gradient(135deg, #388e3c 0%, #1b5e20 100%);
}
```

---

### 5. Adicionar Nova Seção

#### HTML:
```html
<section class="nova-secao">
  <div class="section-container">
    <h2 class="section-title">Nova Seção</h2>
    <p>Conteúdo aqui...</p>
  </div>
</section>
```

#### CSS:
```css
.nova-secao {
  background: var(--color-bg-gray);
  padding: var(--spacing-3xl) var(--spacing-lg);
  margin-bottom: var(--spacing-3xl);
  border-radius: var(--radius-lg);
}

.nova-secao p {
  color: var(--color-text-gray);
  line-height: var(--line-height-relaxed);
}
```

---

## 🔗 Atualizando Links

Todos os links internos usam caminhos simples:

```html
<a href="sobre.html">Quem Somos</a>
<a href="servicos.html">Áreas de Atuação</a>
<a href="eventos.html">Eventos</a>
<a href="associe-se.html">Associe-se</a>
<a href="contato.html">Contato</a>
```

Se mudar a estrutura de pastas ou nomes de arquivos, atualize:
1. Todos os `href` no `index.html`
2. Links internos em todas as páginas

---

## 📝 Editando Conteúdo

### Hero Section

```html
<section class="hero">
  <div class="hero-content">
    <h2 class="hero-title">Força, Acolhimento e Representatividade</h2>
    <p class="hero-text">
      <!-- Edite aqui -->
    </p>
    <p class="hero-tagline"><!-- Tagline --></p>
    <div class="hero-buttons">
      <a href="..." class="btn btn-primary">Texto do Botão</a>
      <a href="..." class="btn btn-secondary">Outro Botão</a>
    </div>
  </div>
</section>
```

### Seção Áreas de Atuação

```html
<div class="area-card">
  <div class="area-icon">👥</div>  <!-- Mude o emoji -->
  <h3>Nome da Área</h3>
  <p>Descrição da área de atuação...</p>
</div>
```

### Seção Movimentos

```html
<div class="movement-item">
  <span class="movement-icon">🔴</span>  <!-- Emoji -->
  <div>
    <h4>Nome do Movimento</h4>
    <p>Descrição do movimento...</p>
  </div>
</div>
```

### Seção Projetos

```html
<article class="project-card">
  <h3>Nome do Projeto</h3>
  <p>Descrição do projeto...</p>
  <a href="servicos.html" class="card-link">Saiba mais →</a>
</article>
```

---

## 🎨 Usando a Paleta de Cores

### Em Elementos Existentes

```css
/* Para usar a cor vermelha primária */
color: var(--color-primary-red);

/* Para usar o fundo claro */
background: var(--color-bg-light);

/* Para usar a sombra grande */
box-shadow: var(--shadow-lg);

/* Para usar espaçamento */
padding: var(--spacing-lg);
```

### Criando Novos Elementos

```css
.novo-elemento {
  background: var(--color-accent-green);
  color: var(--color-text-light);
  padding: var(--spacing-md) var(--spacing-lg);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-md);
  transition: var(--transition);
}

.novo-elemento:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
}
```

---

## 📱 Testando Responsividade

### No Navegador:
1. Abra `index.html` no navegador
2. Pressione **F12** para abrir DevTools
3. Clique em "Toggle device toolbar" (Ctrl+Shift+M)
4. Teste em diferentes resoluções:
   - Desktop: 1920x1080
   - Tablet: 768x1024
   - Mobile: 375x667

### Breakpoints para Ajustar:

```css
/* Tablet (até 768px) */
@media (max-width: 768px) {
  /* Mudanças para tablet */
}

/* Mobile (até 480px) */
@media (max-width: 480px) {
  /* Mudanças para mobile */
}
```

---

## 🚀 Melhorias Sugeridas

### 1. Adicionar Animações com AOS

```html
<!-- No <head> -->
<link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />

<!-- Nas seções -->
<section class="about" data-aos="fade-up">
  ...
</section>

<!-- Antes de </body> -->
<script src="https://unpkg.com/aos@next/dist/aos.js"></script>
<script>
  AOS.init();
</script>
```

### 2. Integrar Formulário de Contato

```html
<form class="contact-form" action="seu-backend.com/contato" method="POST">
  <input type="email" placeholder="Seu email" required>
  <textarea placeholder="Sua mensagem" required></textarea>
  <button type="submit" class="btn btn-primary">Enviar</button>
</form>
```

### 3. Adicionar Google Analytics

```html
<!-- No <head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXX');
</script>
```

### 4. Meta Tags para SEO

```html
<meta name="description" content="ACIERJ - Associação dos Cuidadores do Estado do Rio de Janeiro...">
<meta name="keywords" content="cuidadores, direitos humanos, saúde mental, inclusão">
<meta property="og:title" content="ACIERJ - Associação dos Cuidadores">
<meta property="og:image" content="acierj.png">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

## 🐛 Troubleshooting

### Página não está carregando CSS
- Verifique se `style.css` está no mesmo diretório que `index.html`
- Limpe o cache do navegador (Ctrl+Shift+Delete)

### Imagens não aparecem
- Verifique se `acierj.png` está no mesmo diretório
- Aumente o tamanho: `width: 150px;` em vez de `100px`

### Cores parecem diferentes
- Pode ser problema de monitor/display
- Teste em navegador diferente
- Considere usar um seletor de cores (hex picker)

### Responsividade não funciona
- Verifique se `meta viewport` está no `<head>`
- Limpe cache (Ctrl+Shift+Delete)
- Teste em abas privadas/incógnito

---

## 📞 Suporte e Recursos

### Google Fonts
Para adicionar novas fontes: https://fonts.google.com/

### Gerador de Gradientes
https://cssgradient.io/

### Verificador de Contraste
https://webaim.org/resources/contrastchecker/

### Ícones Emoji
https://emojipedia.org/

---

## ✅ Checklist de Manutenção

- [ ] Testar em Chrome, Firefox, Safari, Edge
- [ ] Testar responsividade em mobile (375px+)
- [ ] Verificar todos os links funcionam
- [ ] Atualizar copyright no footer com ano atual
- [ ] Validar HTML: https://validator.w3.org/
- [ ] Validar CSS: https://jigsaw.w3.org/css-validator/
- [ ] Testar velocidade: https://pagespeed.web.dev/
- [ ] Verificar acessibilidade: https://www.w3.org/WAI/test-evaluate/

