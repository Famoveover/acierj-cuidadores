# ACIERJ - Guia de Design e Referência da Home

## 📋 Resumo Executivo

A página Home da ACIERJ foi redesenhada com identidade visual inspirada em **movimentos sociais**, transmitindo força, acolhimento e representatividade. O design é moderno, acessível e responsivo.

---

## 🎨 Paleta de Cores

### Primário
- **Vermelho Vibrante** (`#d32f2f`) - Força, mobilização, urgência social
- **Vermelho Escuro** (`#b71c1c`) - Contraste e profundidade

### Secundário (Representatividade)
- **Roxo** (`#7b1fa2`) - Inclusão LGBTQIA+, perspectiva inclusiva
- **Amarelo/Ouro** (`#ffc107`) - Esperança, luz, visibilidade
- **Verde** (`#388e3c`) - Vida, acolhimento, sustentabilidade

### Neutros (Acessibilidade)
- **Preto/Cinza Escuro** (`#1a1a1a`) - Texto principal, navegação
- **Branco** (`#ffffff`) - Fundo padrão, cards
- **Cinza Claro** (`#f0f0f0`) - Seções de fundo alternativo

---

## 📐 Tipografia

### Famílias Tipográficas

| Tipo | Fonte | Uso |
|------|-------|-----|
| **Headlines** | Unna (Serif) | Títulos das seções, Hero, subtítulos |
| **Body** | Montserrat (Sans-serif) | Corpo do texto, descrições, navegação |

### Hierarquia de Tamanhos

```
Hero Title: 3.5rem (responsivo)
Section Title: 2.8rem
H3: 1.5rem
H4: 1.25rem
Base: 1rem
Small: 0.875rem
```

---

## 🏗️ Estrutura das Seções

### 1. **Header (Cabeçalho)**
- Fundo: Gradiente vermelho
- Contém: Logo + Título + Subtítulo
- Sticky (fixo no topo)
- Logo com efeito hover (scale + rotate)

### 2. **Navbar (Navegação)**
- Fundo: Preto sólido
- Links com efeito underline amarelo ao hover
- Botão "Associe-se" destaca em roxo
- Sticky abaixo do header

### 3. **Hero Section**
- Fundo: Gradiente vermelho → roxo
- Elementos decorativos (círculos com opacidade)
- Call-to-action com 2 botões
- Tagline inspirada em movimentos sociais

### 4. **Seção Sobre (About)**
- Grid 2 colunas: Texto + Estatísticas
- 3 cards com gradientes e efeito hover
- Responsivo: colapsa para 1 coluna em mobile

### 5. **Seção Áreas de Atuação**
- Grid 3 colunas (auto-fit)
- 6 cards com ícones emoji
- Borda esquerda vermelha que vira amarela ao hover
- Cards elevam ao hover

### 6. **Seção Movimentos e Bandeiras**
- 5 itens em lista com ícones
- Borda esquerda roxa
- Efeito slide ao hover
- Alinhamento flexível para mobile

### 7. **Seção Projetos**
- Grid 4 colunas adaptável
- Cards com borda superior verde
- Descrição + link "Saiba mais →"
- Hover: borda muda para amarelo e eleva

### 8. **CTA (Chamada para Ação)**
- Fundo: Gradiente vermelho → roxo
- 3 botões centralizados
- Elementos decorativos
- Padding generoso

### 9. **Footer**
- Fundo: Preto escuro
- 4 colunas (grid responsivo)
- Links com efeito cor ao hover
- Seção "bottom" com copyright

---

## ✨ Elementos de Design

### Botões

```
.btn-primary (Amarelo)
- Fundo amarelo, texto escuro
- Hover: amarelo mais escuro + elevação

.btn-secondary (Transparente com borda)
- Borda amarela, texto branco
- Hover: fundo amarelo, texto escuro

.btn-cta-primary (Vermelho)
- Fundo vermelho
- Hover: vermelho escuro + elevação

.btn-cta-secondary (Borda vermelha)
- Borda vermelha, texto vermelho
- Hover: fundo vermelho, texto branco
```

### Efeitos de Interação

- **Hover em botões**: `translateY(-2px)` + elevação de sombra
- **Hover em cards**: `translateY(-8px)` + aumento de sombra
- **Hover em links**: mudança de cor + `translateX(4px)`
- **Hover em movimentos**: `translateX(4px)`
- All transitions: `0.3s ease`

### Sombras

| Tipo | Uso |
|------|-----|
| `--shadow-sm` | Elementos menores |
| `--shadow-md` | Cards padrão |
| `--shadow-lg` | Cards grandes, hover |
| `--shadow-xl` | CTAs, headers |

---

## 📱 Responsividade

### Breakpoints

- **Desktop**: 1200px (max-width)
- **Tablet**: até 768px
- **Mobile**: até 480px

### Transformações por Breakpoint

**Em 768px:**
- Áreas de atuação: 3 colunas → 2 colunas
- About: 2 colunas → 1 coluna
- Stats: coluna → linha (flex-wrap)

**Em 480px:**
- Todos os títulos: responsivos com `clamp()`
- Botões: largura total (exceto em CTAs)
- Navegação: links menores
- Footer: 1 coluna

---

## 🎯 Princípios de Design

### 1. **Força Social**
- Cores vibrantes e contrastantes
- Tipografia serif para headlines (editorial forte)
- Mensagens claras e diretas

### 2. **Acolhimento**
- Espaçamento generoso
- Animações suaves
- Cores quentes e inclusivas

### 3. **Representatividade**
- Paleta inspirada em movimentos sociais (roxo LGBTQIA+, verde, etc.)
- Ícones inclusivos
- Seção específica para "Movimentos e Bandeiras"

### 4. **Mobilização Comunitária**
- CTAs proeminentes
- Múltiplas chamadas para ação
- Seção de projetos e eventos

---

## ♿ Acessibilidade

- **Contraste**: Cores testadas para WCAG AA
- **Tipografia**: `clamp()` para escalabilidade
- **Estrutura Semântica**: HTML com `<section>`, `<article>`, `<nav>`
- **Links**: Descrição clara ("Saiba mais →")
- **Alt Text**: Todas as imagens têm descrição

---

## 🔧 Instruções para Manutenção

### Modificar Cores

Editar as variáveis CSS em `:root {}`:
```css
--color-primary-red: #d32f2f;
--color-accent-purple: #7b1fa2;
--color-accent-yellow: #ffc107;
--color-accent-green: #388e3c;
```

### Modificar Espaçamento

Ajustar variáveis como:
```css
--spacing-lg: 2rem;
--spacing-xl: 3rem;
--spacing-2xl: 4rem;
```

### Modificar Tipografia

```css
--font-serif: "Unna", serif;
--font-sans: "Montserrat", sans-serif;
--font-size-base: 1rem;
```

---

## 📊 Compatibilidade

- **Navegadores**: Chrome, Firefox, Safari, Edge (últimas 2 versões)
- **Mobile**: iOS Safari, Chrome Mobile, Firefox Mobile
- **CSS Features**: Grid, Flexbox, Custom Properties, Gradients
- **Fallbacks**: Não necessários para navegadores modernos (2020+)

---

## 🚀 Próximing Passos (Sugestões)

1. **Adicionar Animações**: AOS (Animate on Scroll) para revelar seções ao scroll
2. **Blog/Notícias**: Sistema dinâmico para "Movimentos e Bandeiras"
3. **Modal de Contato**: Integração de formulário na CTA
4. **Integração com Next.js**: Migrar para App Router se desejado
5. **CSS-in-JS**: Considerar styled-components para modularização
6. **Dark Mode**: Adicionar toggle para modo escuro

---

## 📝 Notas

- A página usa **HTML semântico** para melhor SEO
- CSS é **modular** com seções bem definidas
- **Sem JavaScript** necessário para funcionalidade básica
- Totalmente **responsivo** em todas as resoluções
- Pronto para ser integrado com **Backend/CMS**

