# ACIERJ - CSS Snippets Prontos para Copiar/Colar

Aqui você encontra trechos de código prontos para copiar e usar nas customizações mais comuns.

---

## 🎨 Snippets CSS

### 1. Adicionar um Botão Novo

```css
.btn-custom {
  background-color: var(--color-accent-green);
  color: var(--color-text-light);
  padding: var(--spacing-md) var(--spacing-lg);
  border-radius: var(--radius-lg);
  font-weight: 700;
  text-decoration: none;
  display: inline-block;
  transition: var(--transition);
}

.btn-custom:hover {
  background-color: #2e7d32;
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}
```

---

### 2. Destacar uma Seção com Borda Lateral

```css
.highlight-section {
  border-left: 6px solid var(--color-primary-red);
  padding: var(--spacing-lg);
  background: var(--color-bg-gray);
  border-radius: var(--radius-lg);
  transition: var(--transition);
}

.highlight-section:hover {
  border-left-color: var(--color-accent-yellow);
  box-shadow: var(--shadow-md);
}
```

---

### 3. Card com Ícone Personalizado

```css
.card-with-icon {
  text-align: center;
  padding: var(--spacing-lg);
  background: var(--color-text-light);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-sm);
  transition: var(--transition);
}

.card-with-icon:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-lg);
}

.card-icon {
  font-size: 2.5rem;
  margin-bottom: var(--spacing-md);
}

.card-with-icon h3 {
  color: var(--color-primary-red);
  margin-bottom: var(--spacing-sm);
  font-family: var(--font-serif);
}

.card-with-icon p {
  color: var(--color-text-gray);
  line-height: var(--line-height-relaxed);
}
```

---

### 4. Badge/Etiqueta Colorida

```css
.badge {
  display: inline-block;
  padding: 0.4rem 0.8rem;
  border-radius: var(--radius-sm);
  font-size: var(--font-size-xs);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.badge-red {
  background-color: var(--color-primary-red);
  color: var(--color-text-light);
}

.badge-purple {
  background-color: var(--color-accent-purple);
  color: var(--color-text-light);
}

.badge-green {
  background-color: var(--color-accent-green);
  color: var(--color-text-light);
}

.badge-yellow {
  background-color: var(--color-accent-yellow);
  color: var(--color-text-dark);
}
```

**HTML:**
```html
<span class="badge badge-red">Urgente</span>
<span class="badge badge-purple">Inclusão</span>
<span class="badge badge-green">Vida</span>
```

---

### 5. Grid de Imagens/Galeria

```css
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--spacing-lg);
  margin: var(--spacing-lg) 0;
}

.gallery-item {
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-md);
  transition: var(--transition);
}

.gallery-item:hover {
  transform: scale(1.05);
  box-shadow: var(--shadow-lg);
}

.gallery-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
}
```

---

### 6. Linhas Decorativas

```css
.divider-line {
  height: 4px;
  background: linear-gradient(90deg, 
    var(--color-primary-red) 0%, 
    var(--color-accent-yellow) 50%, 
    var(--color-accent-purple) 100%);
  margin: var(--spacing-xl) 0;
  border-radius: 2px;
}

.divider-dots {
  text-align: center;
  font-size: 1.5rem;
  color: var(--color-primary-red);
  margin: var(--spacing-xl) 0;
  letter-spacing: 8px;
}
```

**HTML:**
```html
<div class="divider-line"></div>
<div class="divider-dots">• • •</div>
```

---

### 7. Caixa de Destaque/Alert

```css
.alert-box {
  padding: var(--spacing-lg);
  border-radius: var(--radius-lg);
  border-left: 5px solid;
  margin: var(--spacing-lg) 0;
}

.alert-info {
  background-color: #e3f2fd;
  border-left-color: #2196f3;
  color: #1565c0;
}

.alert-success {
  background-color: #e8f5e9;
  border-left-color: var(--color-accent-green);
  color: #2e7d32;
}

.alert-warning {
  background-color: #fff3e0;
  border-left-color: #ff9800;
  color: #e65100;
}

.alert-danger {
  background-color: #ffebee;
  border-left-color: var(--color-primary-red);
  color: #c62828;
}

.alert-box strong {
  display: block;
  margin-bottom: var(--spacing-xs);
  font-weight: 700;
}
```

**HTML:**
```html
<div class="alert-box alert-info">
  <strong>Informação:</strong> Novo evento agendado para próxima semana.
</div>
```

---

### 8. Timeline/Cronograma

```css
.timeline {
  position: relative;
  padding: var(--spacing-xl) 0;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 4px;
  height: 100%;
  background: var(--color-primary-red);
}

.timeline-item {
  margin-bottom: var(--spacing-xl);
  width: 48%;
}

.timeline-item:nth-child(odd) {
  margin-left: 0;
  text-align: right;
  padding-right: var(--spacing-lg);
}

.timeline-item:nth-child(even) {
  margin-left: 52%;
  padding-left: var(--spacing-lg);
}

.timeline-content {
  background: var(--color-text-light);
  padding: var(--spacing-lg);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-md);
}

.timeline-date {
  font-weight: 700;
  color: var(--color-primary-red);
  font-family: var(--font-serif);
}

@media (max-width: 768px) {
  .timeline::before {
    left: 20px;
  }
  
  .timeline-item,
  .timeline-item:nth-child(odd),
  .timeline-item:nth-child(even) {
    width: 100%;
    margin: 0;
    padding-left: 60px;
    text-align: left;
  }
}
```

---

### 9. Acordeão (Accordion)

```css
.accordion {
  border-radius: var(--radius-lg);
  overflow: hidden;
}

.accordion-item {
  border-bottom: 1px solid var(--color-bg-gray);
}

.accordion-item:last-child {
  border-bottom: none;
}

.accordion-header {
  background: var(--color-text-light);
  padding: var(--spacing-lg);
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: var(--transition);
  border-left: 4px solid var(--color-primary-red);
}

.accordion-header:hover {
  background: var(--color-bg-gray);
}

.accordion-header h4 {
  margin: 0;
  color: var(--color-primary-red);
  font-family: var(--font-serif);
}

.accordion-icon {
  font-size: 1.5rem;
  transition: var(--transition);
}

.accordion-item.active .accordion-icon {
  transform: rotate(180deg);
}

.accordion-content {
  padding: 0 var(--spacing-lg);
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease;
}

.accordion-item.active .accordion-content {
  padding: var(--spacing-lg);
  max-height: 500px;
}

.accordion-content p {
  color: var(--color-text-gray);
  line-height: var(--line-height-relaxed);
}
```

**JavaScript necessário:**
```javascript
document.querySelectorAll('.accordion-header').forEach(header => {
  header.addEventListener('click', () => {
    const item = header.parentElement;
    item.classList.toggle('active');
  });
});
```

---

### 10. Breadcrumb (Navegação)

```css
.breadcrumb {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
  padding: var(--spacing-md) 0;
  font-size: var(--font-size-sm);
}

.breadcrumb a {
  color: var(--color-primary-red);
  text-decoration: none;
  transition: var(--transition);
}

.breadcrumb a:hover {
  color: var(--color-accent-purple);
  text-decoration: underline;
}

.breadcrumb span {
  color: var(--color-text-gray);
}

.breadcrumb-separator {
  color: var(--color-text-gray);
  margin: 0 var(--spacing-xs);
}

.breadcrumb-current {
  color: var(--color-text-dark);
  font-weight: 600;
}
```

**HTML:**
```html
<nav class="breadcrumb">
  <a href="index.html">Início</a>
  <span class="breadcrumb-separator">/</span>
  <a href="servicos.html">Serviços</a>
  <span class="breadcrumb-separator">/</span>
  <span class="breadcrumb-current">Cuidadores</span>
</nav>
```

---

## 📋 Snippets HTML

### 1. Seção com Título Destacado

```html
<section class="custom-section">
  <div class="section-container">
    <h2 class="section-title">Título da Seção</h2>
    <p class="section-intro">Introdução ou descrição breve...</p>
    
    <!-- Conteúdo aqui -->
  </div>
</section>
```

---

### 2. Card Simples

```html
<div class="custom-card">
  <div class="card-icon">📌</div>
  <h3>Título do Card</h3>
  <p>Descrição breve do conteúdo do card.</p>
  <a href="#" class="card-link">Saiba mais →</a>
</div>
```

---

### 3. Lista com Ícones

```html
<ul class="icon-list">
  <li><span class="icon">✓</span> <strong>Item Um:</strong> Descrição aqui</li>
  <li><span class="icon">✓</span> <strong>Item Dois:</strong> Descrição aqui</li>
  <li><span class="icon">✓</span> <strong>Item Três:</strong> Descrição aqui</li>
</ul>
```

**CSS:**
```css
.icon-list {
  list-style: none;
  padding: 0;
}

.icon-list li {
  display: flex;
  gap: var(--spacing-md);
  margin-bottom: var(--spacing-md);
  color: var(--color-text-gray);
}

.icon-list .icon {
  color: var(--color-primary-red);
  font-weight: 700;
  min-width: 20px;
}
```

---

### 4. Citação/Quote

```html
<blockquote class="quote">
  <p>"A força dos cuidadores é a força de uma sociedade que escolhe se importar com todos."</p>
  <footer>— ACIERJ</footer>
</blockquote>
```

**CSS:**
```css
.quote {
  border-left: 5px solid var(--color-primary-red);
  padding: var(--spacing-lg);
  padding-left: var(--spacing-xl);
  background: var(--color-bg-gray);
  border-radius: var(--radius-lg);
  margin: var(--spacing-xl) 0;
  font-style: italic;
}

.quote p {
  margin: 0 0 var(--spacing-md) 0;
  color: var(--color-text-dark);
  font-size: var(--font-size-lg);
}

.quote footer {
  color: var(--color-text-gray);
  font-style: normal;
  font-weight: 600;
}
```

---

## 🎯 Dicas de Customização

### Quando Copiar/Colar

1. ✅ Você quer adicionar um novo componente
2. ✅ Você quer estender funcionalidade
3. ✅ Você quer criar variações de estilos
4. ✅ Você quer experimentar sem quebrar o CSS principal

### O Que Nunca Fazer

1. ❌ Modificar as variáveis CSS `:root` sem testes
2. ❌ Duplicar código ao invés de estender
3. ❌ Usar cores hardcoded ao invés das variáveis
4. ❌ Ignorar responsividade em mobile

### Boas Práticas

```css
/* ✅ BOM - Usa variáveis */
.novo-elemento {
  color: var(--color-text-dark);
  padding: var(--spacing-md);
}

/* ❌ RUIM - Hardcoded */
.novo-elemento {
  color: #1a1a1a;
  padding: 16px;
}
```

---

## 📝 Template Pronto para Nova Seção

```html
<section class="nova-secao">
  <div class="section-container">
    <h2 class="section-title">Nova Seção</h2>
    <p class="section-intro">Introdução opcional...</p>
    
    <div class="nova-secao-content">
      <!-- Seu conteúdo aqui -->
    </div>
  </div>
</section>
```

```css
.nova-secao {
  background-color: var(--color-bg-light);
  padding: var(--spacing-3xl) var(--spacing-lg);
  margin-bottom: var(--spacing-3xl);
  border-radius: var(--radius-lg);
}

.nova-secao-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: var(--spacing-lg);
}

@media (max-width: 768px) {
  .nova-secao {
    padding: var(--spacing-fl) var(--spacing-md);
  }
}
```

---

**💡 Dica:** Sempre teste em mobile depois de adicionar novos snippets!

