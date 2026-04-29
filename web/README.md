# Selo H - Website de Certificação de Saúde Mental

Um website premium, otimizado para conversão e SEO, para a certificação Selo H que prova que sua empresa está em conformidade com as melhores diretrizes de saúde mental dos funcionários.

## 🎯 Características

### Design & UX
- ✨ Design premium e minimalista
- 📱 Totalmente responsivo (mobile-first)
- ♿ Acessibilidade WCAG AA
- ⚡ Performance otimizada (LCP < 2.5s)
- 🎨 Design system com tokens CSS

### Copywriting & Marketing
- 💬 Copywriting orientado para conversão
- 📊 Social proof integrado
- 🎁 CTA estratégicos em todo site
- 📋 FAQ com accordion interativo
- 🔍 SEO otimizado desde zero

### Funcionalidades
- 📝 Formulário de captura de leads
- 🔗 Navegação suave com smooth scroll
- 📊 Rastreamento de eventos
- 🎬 Animações sutis e responsivas
- 🔐 Segurança e privacidade

## 📁 Estrutura do Projeto

```
web/
├── index.html                 # Página principal
├── politica-privacidade.html # Política de privacidade
├── termos.html              # Termos de serviço
├── robots.txt               # Robots.txt para SEO
├── sitemap.xml             # Sitemap XML
│
├── css/
│   ├── reset.css           # Reset CSS
│   ├── tokens.css          # Design tokens
│   ├── components.css      # Componentes reutilizáveis
│   └── styles.css          # Estilos principais
│
├── js/
│   └── main.js            # JavaScript interativo
│
└── images/                 # Imagens otimizadas
```

## 🚀 Como Usar

### 1. Instalação Local
```bash
# Clone ou baixe os arquivos
# Abra em um servidor local (não abra direto no navegador)
# Use Live Server do VS Code ou similar
```

### 2. Configuração Necessária

#### Email do Formulário
No arquivo `js/main.js`, atualize a função `simulateFormSubmission()` com sua API de emails:

```javascript
fetch('https://sua-api.com/leads', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(data)
})
```

#### Google Analytics
Adicione no `<head>` do `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR_GA_ID');
</script>
```

#### Meta Tags para Social
Atualize as URLs reais em `index.html`:
- `og:image` - Imagem para preview em redes sociais
- `og:url` - URL do seu domínio
- `twitter:card` - Customização para Twitter

### 3. Hospedagem

**Recomendações:**
- **Vercel** (ideal para static sites)
- **Netlify** (com formulários integrados)
- **AWS S3 + CloudFront** (escalável)
- **Seu próprio servidor** (com HTTPS obrigatório)

**Configuração HTTPS:**
- Obrigatório em produção
- Use Let's Encrypt (grátis)
- Configure certificado SSL

## 🎨 Customização

### Alterar Cores
Edite `css/tokens.css`:

```css
:root {
  --accent-green: #10b981;  /* Cor primária */
  --accent-blue: #0f766e;   /* Cor secundária */
  --gray-900: #0a0e27;      /* Fundo escuro */
}
```

### Alterar Textos
Edite as seções em `index.html`. Principais:
- Hero headline (h1)
- Subtítulo
- Textos de features
- Testimonios
- FAQ

### Adicionar Formulários Reais
No `js/main.js`, implemente integrações com:
- **Zapier** (sem código)
- **Make.com** (automação)
- **EmailJS** (envio direto)
- **sua própria API** (máximo controle)

## ✅ Performance Checklist

- [ ] Google PageSpeed Insights > 90
- [ ] LCP < 2.5s
- [ ] FID < 100ms
- [ ] CLS < 0.1
- [ ] Mobile-friendly test PASS
- [ ] HTTPS ativo
- [ ] Sitemap submetido ao Google Search Console
- [ ] Google Analytics configurado
- [ ] Meta tags sociais validadas

## 🔍 SEO Otimizações

✅ **Implementado:**
- Meta tags essenciais (title, description, keywords)
- Open Graph e Twitter Cards
- Structured Data (Schema.org)
- Sitemap XML
- Robots.txt
- Heading hierarchy semântica
- Alt text em imagens
- Internal linking estratégico
- Mobile-first responsive
- Page speed otimizado

**Para melhorar ainda mais:**
1. Build backlinks de sites relevantes
2. Crie conteúdo complementar (blog)
3. Implemente Rich Snippets adicionais
4. Otimize imagens com WebP/AVIF
5. Implemente breadcrumb schema

## 🛡️ Segurança

- ✅ Validação de formulário client-side
- ✅ HTTPS obrigatório (configure no host)
- ✅ CORS headers configurados
- ✅ Meta tags de segurança
- ⚠️ **TODO:** Implementar rate limiting no servidor
- ⚠️ **TODO:** Implementar CAPTCHA (reCAPTCHA v3)
- ⚠️ **TODO:** Validação server-side de formulário

## 📊 Analytics & Conversão

### Eventos Rastreáveis
- `lead_submission` - Quando um lead envia o formulário
- `cta_click` - Cliques em CTAs
- `faq_expand` - Expansão de FAQ
- `scroll_milestone` - Marcos de scroll

### Otimizações de Conversão
1. **A/B Test Headlines**
   - "Sua Empresa É Incrível com Saúde Mental?"
   - vs. "Sua Empresa Cuida da Saúde Mental?"

2. **A/B Test CTAs**
   - "Solicitar Certificação"
   - vs. "Começar Agora"
   - vs. "Obter Selo H"

3. **A/B Test Form**
   - 5 campos (atual)
   - vs. 3 campos (simplificado)

## 🔧 Manutenção

### Checklist Mensal
- [ ] Verificar erros em Google Search Console
- [ ] Atualizar testimonios/case studies
- [ ] Revisar meta descriptions
- [ ] Checar links quebrados
- [ ] Analisar taxa de bounceate

### Checklist Trimestral
- [ ] Auditoria de SEO
- [ ] Teste de segurança
- [ ] Otimização de imagens
- [ ] Atualização de conteúdo
- [ ] Review de performance

## 📱 Breakpoints Responsivos

- **Desktop:** 1200px+
- **Tablet:** 768px - 1199px
- **Mobile:** 480px - 767px
- **Small Mobile:** < 480px

## ♿ Acessibilidade

Conformidade com **WCAG 2.1 AA**:
- ✅ Contraste de cores 4.5:1
- ✅ Navegação por teclado
- ✅ Sem color-only information
- ✅ Readable text (16px+)
- ✅ Touch targets 44px+
- ✅ Respects prefers-reduced-motion
- ✅ Semantic HTML
- ✅ ARIA labels onde necessário

## 📞 Suporte e Contato

Para questões sobre o website:
- Email: contato@seloh.org.br
- Telefone: (11) 99999-9999
- Website: https://seloh.org

## 📜 Licença

Este website é propriedade da Selo H. Todos os direitos reservados.

---

**Versão:** 1.0  
**Data:** 17 de abril de 2024  
**Status:** Production Ready ✅
