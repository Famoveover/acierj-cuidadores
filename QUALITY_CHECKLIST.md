# ACIERJ - Checklist de Qualidade e Validação

Este documento serve como guia para validar e garantir a qualidade da página antes de publicar.

---

## ✅ Checklist de Qualidade

### 🎨 Design & Visual

- [ ] Elementos visuais carregam corretamente
- [ ] Logo aparece sem distorção
- [ ] Cores correspondem à paleta definida
- [ ] Tipografia está legível em todos os tamanhos
- [ ] Espaçamento está consistente
- [ ] Nenhum elemento sobrepõe outro
- [ ] Gradientes renderizam corretamente
- [ ] Sombras estão sutis e profissionais
- [ ] Bordas estão com raio consistente

### 📱 Responsividade

- [ ] Desktop (1920x1080): Layout perfeito
- [ ] Tablet (768x1024): Sem deformações
- [ ] Mobile (375x667): Completamente usável
- [ ] Scroll horizontal: Não existe
- [ ] Imagens: Escaladas proporcionalmente
- [ ] Texto: Legível em todos os tamanhos
- [ ] Botões: Clicáveis em mobile (mín. 44px)
- [ ] Navbar: Funciona em mobile
- [ ] Navigation: Acessível sem scroll excessivo

### 🔗 Navegação & Links

- [ ] Todos os links de navegação funcionam
- [ ] Links internos estão corretos
- [ ] Não há links quebrados
- [ ] Menu horizontal em desktop
- [ ] Links têm estado hover visível
- [ ] Links visitados têm cor diferente (opcional)
- [ ] Breadcrumb funciona (se implementado)
- [ ] Botões CTA levam aos destinos corretos

### ♿ Acessibilidade (WCAG 2.1)

**Contraste (AA mínimo)**
- [ ] Texto escuro sobre fundo claro (4.5:1)
- [ ] Texto claro sobre fundo escuro (4.5:1)
- [ ] Botões têm contraste suficiente
- [ ] Nenhum texto em cores de baixo contraste

**Estrutura & Semântica**
- [ ] Hierarquia de headings correta (h1 → h2 → h3)
- [ ] Apenas 1 `<h1>` por página (opcional em SPAs)
- [ ] `<header>`, `<nav>`, `<main>`, `<footer>` semânticos
- [ ] `<section>` e `<article>` usados corretamente
- [ ] Listas (`<ul>`, `<ol>`) estruturadas
- [ ] Links descritivos (não "clique aqui")

**Interatividade**
- [ ] Todos os botões funcionam com Tab
- [ ] Ordem de tab lógica
- [ ] Elementos focados têm indicador visuais
- [ ] Sem armadilhas de teclado
- [ ] Modais fecham com ESC

**Alternativos**
- [ ] Todas as imagens têm `alt` descriptivo
- [ ] Ícones emoji: `alt` ou `role="img"`
- [ ] Vídeos têm legendas (se houver)
- [ ] Áudio tem transcrição (se houver)

**Linguagem**
- [ ] `lang="pt-BR"` no `<html>`
- [ ] Mudanças de idioma marcadas com `lang`
- [ ] Abreviações explicadas na primeira menção
- [ ] Jargão técnico definido

### 🔍 SEO (Search Engine Optimization)

- [ ] Meta description presente e relevante
- [ ] Títulos da página únicos e descritivos
- [ ] Heading 1 presente e único
- [ ] Estrutura de headings correta
- [ ] URLs amigáveis (sem caracteres especiais)
- [ ] Imagens com alt text descritivo
- [ ] Meta keywords (opcional moderna)
- [ ] Open Graph tags (og:title, og:description, og:image)
- [ ] Schema.org markup (se aplicável)
- [ ] Sitemap.xml (para múltiplas páginas)
- [ ] robots.txt configurado

### ⚡ Performance

**Carregamento**
- [ ] Página carrega em < 3 segundos
- [ ] Imagens otimizadas (< 100KB cada)
- [ ] CSS minificado (ou pequeno)
- [ ] Sem JavaScript desnecessário
- [ ] Nenhum arquivo grande bloqueando render

**Recursos**
- [ ] Google Fonts carregam corretamente
- [ ] Fontes têm fallback declarado
- [ ] Não há requests 404
- [ ] Recursos externos carregam via HTTPS

**Mobile**
- [ ] LCP (Largest Contentful Paint) < 2.5s
- [ ] FID (First Input Delay) < 100ms
- [ ] CLS (Cumulative Layout Shift) < 0.1
- [ ] Speed Score > 80 (Google PageSpeed)

### 🔒 Segurança

- [ ] Link HTTPS funciona
- [ ] Certificate válido
- [ ] Sem erros de segurança no console
- [ ] Nenhum conteúdo inseguro (mixed content)
- [ ] Headers de segurança configurados
- [ ] Sem vulnerabilidades XSS
- [ ] Formulários validam entrada (se houver)

### 🐛 Bugs & Erros

- [ ] Console do navegador (F12): Sem erros
- [ ] Console do navegador: Sem warnings
- [ ] Nenhum elemento com `display: none` não proposital
- [ ] Nenhuma tag HTML incompleta
- [ ] Arquivo CSS válido
- [ ] Nenhuma classe CSS não usada
- [ ] Variáveis CSS todas usadas

### 📝 Conteúdo

- [ ] Sem erros de digitação
- [ ] Sem erros gramaticais
- [ ] Coerência terminológica
- [ ] Nenhum placeholder de "Lorem ipsum"
- [ ] Datas atualizadas
- [ ] Copyright com ano correto
- [ ] Citações/fontes creditadas
- [ ] Links patrocinados marcados

### 🌐 Navegadores

**Chromium-based** (Chrome, Edge, Brave)
- [ ] Chrome (últimas 2 versões)
- [ ] Edge (últimas 2 versões)
- [ ] Chrome Mobile

**Firefox**
- [ ] Firefox Desktop (últimas 2 versões)
- [ ] Firefox Mobile

**Safari**
- [ ] Safari Desktop (últimas 2 versões)
- [ ] Safari iOS

**Testes Específicos**
- [ ] Layout correto em 1920x1080
- [ ] Layout correto em 1024x768
- [ ] Layout correto em 768x1024
- [ ] Layout correto em 375x667
- [ ] Sem zoom distorcendo layout
- [ ] Sem scrollbar horizontal

---

## 🛠️ Ferramentas de Validação

### Online (Recomendado)

| Ferramenta | URL | Propósito |
|-----------|-----|----------|
| **Google PageSpeed** | https://pagespeed.web.dev/ | Performance, SEO, UX |
| **W3C HTML Validator** | https://validator.w3.org/ | Validação HTML |
| **W3C CSS Validator** | https://jigsaw.w3.org/css-validator/ | Validação CSS |
| **WebAIM Contrast** | https://webaim.org/resources/contrastchecker/ | Contraste de cores |
| **WAVE** | https://wave.webaim.org/ | Acessibilidade |
| **Lighthouse** | Built-in Chrome DevTools | Tudo junto |
| **Mobile-Friendly** | https://search.google.com/test/mobile-friendly | Mobile |

### No Navegador (F12 DevTools)

```javascript
// No Console, rode estes comandos:

// 1. Verificar todos os links internos
console.log(document.querySelectorAll('a[href]'));

// 2. Verificar imagens sem alt
console.log(document.querySelectorAll('img:not([alt])'));

// 3. Contar headings
console.log('H1:', document.querySelectorAll('h1').length);
console.log('H2:', document.querySelectorAll('h2').length);
console.log('H3:', document.querySelectorAll('h3').length);

// 4. Verificar contraste (instale extensão aXe ou WAVE)
// Abra WAVE e veja erros de acessibilidade
```

---

## 📊 Pontuações Alvo

### Google Lighthouse (Chrome DevTools)

| Métrica | Target | Status |
|---------|--------|--------|
| Performance | ≥ 80 | ⬚ |
| Accessibility | ≥ 90 | ⬚ |
| Best Practices | ≥ 85 | ⬚ |
| SEO | ≥ 90 | ⬚ |

### Web Vitals

| Métrica | Target | Status |
|---------|--------|--------|
| LCP | < 2.5s | ⬚ |
| FID | < 100ms | ⬚ |
| CLS | < 0.1 | ⬚ |

---

## 🔄 Processo de Validação Pré-Deploy

### Fase 1: Desenvolvimento Local

```bash
# 1. Inicie servidor local
python -m http.server 8000

# 2. Teste em http://localhost:8000
# 3. Abra Chrome DevTools (F12)
# 4. Verifique console (Ctrl+Shift+J)
```

**Checklist:**
- [ ] Sem erros no console
- [ ] Responsividade OK em mobile
- [ ] Todos os links funcionam
- [ ] Imagens carregam

### Fase 2: Validação Técnica

```bash
# 1. Valide HTML
# Abra: https://validator.w3.org/
# Upload: index.html
# Resultado: 0 erros

# 2. Valide CSS
# Abra: https://jigsaw.w3.org/css-validator/
# Upload: style.css
# Resultado: 0 erros
```

**Checklist:**
- [ ] HTML válido
- [ ] CSS válido
- [ ] Nenhum aviso crítico

### Fase 3: Performance

```bash
# 1. Google PageSpeed
# Abra: https://pagespeed.web.dev/
# Digite: seu-dominio.com
# Alvo: Score > 80
```

**Checklist:**
- [ ] Performance ≥ 80
- [ ] Accessibility ≥ 90
- [ ] SEO ≥ 90

### Fase 4: Acessibilidade

```bash
# 1. WAVE Browser Extension
# Install: https://wave.webaim.org/extension/
# Resultado: 0 erros, 0 alertas críticos

# 2. Manual Checklist
# [] Tabbing order é lógico
# [] Botões têm labels
# [] Imagens têm alt
# [] Cores têm contraste
```

**Checklist:**
- [ ] WAVE: 0 erros
- [ ] Contraste OK
- [ ] Teclado funciona

### Fase 5: Cross-Browser

```
Testar em:
[ ] Chrome (Desktop)
[ ] Firefox (Desktop)
[ ] Safari (Desktop, iOS)
[ ] Edge
[ ] Chrome Mobile
```

**Checklist:**
- [ ] Layout igual em todos browsers
- [ ] Sem visual glitches
- [ ] Performance similar

### Fase 6: Conteúdo Final

- [ ] Sem typos
- [ ] Informações corretas
- [ ] Links atualizados
- [ ] Redes sociais linkadas
- [ ] Contato correto

---

## 🚀 Deploy Checklist

Antes de publicar em produção:

- [ ] Backup dos arquivos antigos
- [ ] Todos os checklists acima completados
- [ ] Cache do navegador limpo
- [ ] Testes finais em produção
- [ ] Monitoramento ativado
- [ ] Equipe notificada
- [ ] Documentação atualizada

---

## 📈 Monitoramento Pós-Deploy

Acompanhe estas métricas regularmente:

- **Google Analytics**: Tráfego, bounce rate
- **Search Console**: Indexação, erros
- **Lighthouse**: Performance trends
- **Uptime Monitor**: Disponibilidade 24/7
- **Error Tracking**: Erros em produção

---

## 🔧 Correção de Problemas Comuns

### Problema: Página lenta em mobile
**Solução:**
1. Comprima imagens (ImageOptim, TinyPNG)
2. Minifique CSS
3. Remova fontes não usadas
4. Lazy-load imagens

### Problema: Layout quebrado em mobile
**Solução:**
1. Verifique `meta viewport`
2. Use `clamp()` para tamanhos responsivos
3. Teste em DevTools mobile
4. Use `max-width` em containers

### Problema: Fontes não carregam
**Solução:**
1. Verifique URL do Google Fonts
2. Declare fallback fonts
3. Use `font-display: swap`
4. Teste em modo offline

### Problema: Links quebrados
**Solução:**
1. Use ferramentas como Broken Link Checker
2. Valide todas as URLs
3. Teste clicks em DevTools
4. Implemente Custom 404

---

## 📞 Suporte

Se encontrar problemas:

1. Verifique este checklist
2. Procure em [DESIGN_REFERENCE.md](DESIGN_REFERENCE.md)
3. Veja [CUSTOMIZATION_GUIDE.md](CUSTOMIZATION_GUIDE.md)
4. Consulte [CSS_SNIPPETS.md](CSS_SNIPPETS.md)
5. Entre em contato: contato@acierj.org.br

---

**Última Atualização:** 2025
**Versão:** 1.0.0
**Status:** ✅ Pronto para Uso

