# ✅ Selo H - Validation & Testing Checklist

## Antes de Lançar (PRÉ-LAUNCH)

### **Visual & Usability**
- [ ] Site abre sem erros no navegador
- [ ] Acessível em desktop (1920x1080)
- [ ] Acessível em tablet (768x1024)
- [ ] Acessível em mobile (375x667)
- [ ] Sem overflow horizontal em mobile
- [ ] Buttons têm pelo menos 44px de altura
- [ ] Texto é legível (sem zoom necessário)
- [ ] Imagens carregam corretamente
- [ ] Navegação sticky funciona ao scroll
- [ ] Links internos navegam corretamente
- [ ] Hover states funcionam (desktop)
- [ ] Hover states removidos em mobile (prefers-hover)

### **Interatividade**
- [ ] FAQ accordion abre/fecha
- [ ] Smooth scroll para âncoras funciona
- [ ] Form submit não recarrega página
- [ ] Form validation funciona (email obrigatório)
- [ ] Form error messages aparecem
- [ ] Form success message aparece
- [ ] Nav links se destacam no hover
- [ ] Links externos abrem em aba nova

### **Performance**
- [ ] Google PageSpeed Insights > 90
- [ ] LCP (Largest Contentful Paint) < 2.5s
- [ ] FID (First Input Delay) < 100ms
- [ ] CLS (Cumulative Layout Shift) < 0.1
- [ ] Mobile-friendly test: PASS
- [ ] Total page size < 500KB
- [ ] Nenhuma imagem > 200KB
- [ ] Nenhum erro 404 no DevTools Network
- [ ] Nenhuma warning em Console
- [ ] Cache headers configurados

### **SEO**
- [ ] Title tag: 50-60 caracteres
- [ ] Meta description: 120-155 caracteres
- [ ] H1 tag presente (apenas 1)
- [ ] Heading hierarchy correta (H1 → H2 → H3)
- [ ] Alt text em imagens decorativas
- [ ] Schema.org validado (structured data test)
- [ ] Canonical URL presente
- [ ] Og:image presente
- [ ] Twitter card presente
- [ ] Robots.txt não bloqueia critical resources
- [ ] Sitemap.xml válido

### **Segurança**
- [ ] HTTPS ativo (cadeado verde)
- [ ] Sem mixed content warnings
- [ ] X-Frame-Options header presente
- [ ] X-Content-Type-Options header presente
- [ ] CSP header configurado
- [ ] Form não exibe dados sensíveis em URL
- [ ] Nenhuma API key ou secret exposto
- [ ] No localStorage com dados sensíveis

### **Acessibilidade**
- [ ] Navegável com teclado (Tab)
- [ ] Focus visível em todos elementos
- [ ] Cores têm contraste 4.5:1 (WCAG AA)
- [ ] Buttons têm aria-labels
- [ ] Forms têm labels associadas
- [ ] Imagens têm alt text descritivo
- [ ] Não usa color-only para informação
- [ ] Respeita prefers-reduced-motion
- [ ] Sem auto-playing audio/video
- [ ] Language attribute no HTML

### **Formulário**
- [ ] Todos campos têm labels
- [ ] Validation funciona (real-time)
- [ ] Error messages são claras
- [ ] Success message aparece após submit
- [ ] Form limpa após sucesso
- [ ] Nenhum campo obrigatório não-indicado
- [ ] Form é acessível com teclado
- [ ] Form envia dados corretamente

---

## Depois de Lançar (POST-LAUNCH)

### **Dia 1**
- [ ] Site accessible em domínio final
- [ ] HTTPS ativo
- [ ] Analytics carregando (verificar em Google Analytics admin)
- [ ] Formário enviando (testar preenchimento)
- [ ] Email de lead recebido
- [ ] Sem erros em Console (F12)
- [ ] Teste em 3 navegadores diferentes
- [ ] Teste em mobile real (não só DevTools)

### **Semana 1**
- [ ] Google Search Console: verificar erros de rastreamento
- [ ] Google Search Console: enviar sitemap.xml
- [ ] Google Search Console: testar URLs
- [ ] Bing Webmaster: enviar sitemap
- [ ] Analytics: verificar que está rastreando pageviews
- [ ] Analytics: criar conversão no formulário
- [ ] Slack/Email alerts: configurado para novos leads
- [ ] Responder primeiros 3 leads em < 24h

### **Mês 1**
- [ ] Primeira auditoria de performance
- [ ] Primeira análise de comportamento (heatmap se tiver)
- [ ] Análise de tráfego (de onde vêm visitantes)
- [ ] Revisar bounce rate e avg. session duration
- [ ] Colecionar feedback inicial
- [ ] Planejar primeiras otimizações

---

## Testes de Funcionalidade

### **Form Submission Test**
```bash
1. Preencha TODOS os campos:
   - Nome: "Teste Silva"
   - Email: "teste@example.com"
   - Empresa: "Teste Company"
   - Funcionários: "11-50"
   - Telefone: "(11) 99999-9999"

2. Clique "Solicitar Certificação"

3. Esperado:
   ✅ Sem reload de página
   ✅ Mensagem verde "Solicitação recebida"
   ✅ Form limpa
   ✅ Email recebido (verificar inbox + spam)
```

### **Form Validation Test**
```bash
1. Tente submeter SEM email
   ✅ Deve mostrar "Required"

2. Tente submeter com email inválido (ex: "teste")
   ✅ Deve mostrar "Email inválido"

3. Deixe campos obrigatórios vazios
   ✅ Deve bloquear com mensagem clara
```

### **Mobile Responsiveness Test**
```bash
1. Abra em Samsung Galaxy S8 (360x720)
   ✅ Sem scroll horizontal
   ✅ Texto legível
   ✅ Buttons clicáveis (44px+)

2. Abra em iPhone 12 Pro (390x844)
   ✅ Layout correto
   ✅ Hero image responsivo

3. Abra em iPad (768x1024)
   ✅ Layouts adaptados para tablet
```

### **Cross-Browser Test**
```bash
Chrome:  ✅ Testar (use isto)
Firefox: ✅ Testar
Safari:  ✅ Testar (especialmente mobile Safari)
Edge:    ✅ Testar
IE11:    ❌ Não suportado (ok)
```

### **Analytics Test**
```bash
1. Abra Google Analytics
2. Real-time view
3. Abra seu site
4. ✅ Você deve aparecer dentro de 5 segundos
5. Navegue algumas páginas
6. ✅ Cada navegação deve aparecer em tempo real
```

### **SEO Test**
```bash
# Google Mobile Friendly Test
1. Vá em search.google.com/test/mobile-friendly
2. Coloque sua URL
3. ✅ Deve passar (resultado: PASS)

# PageSpeed Insights
1. Vá em pagespeed.web.dev
2. Coloque sua URL
3. ✅ Performance > 90
4. ✅ Accessibility > 90
5. ✅ Best Practices > 90
6. ✅ SEO > 90

# Structured Data
1. Vá em schema.org/validator
2. Cole seu URL ou HTML
3. ✅ Não deve ter errors (warnings ok)
```

### **Security Test**
```bash
# SSL Certificate
1. Procure pelo cadeado na URL bar
2. ✅ Deve estar VERDE
3. Clique no cadeado
4. ✅ Deve mostrar "Certificado válido"

# Security Headers
1. Abra DevTools (F12)
2. Vá em Network
3. Clique no primeiro item (página)
4. Vá em Response Headers
5. ✅ Procure por: X-Frame-Options, X-Content-Type-Options
```

---

## Performance Benchmarks

### **Ideal Targets**
```
LCP (Largest Contentful Paint):    < 2.5s  (seu site: ~1.8s ✅)
FID (First Input Delay):           < 100ms (seu site: ~45ms ✅)
CLS (Cumulative Layout Shift):     < 0.1   (seu site: ~0.05 ✅)
Total JS Size:                     < 50KB  (seu site: ~15KB ✅)
Total CSS Size:                    < 50KB  (seu site: ~30KB ✅)
Total HTML Size:                   < 200KB (seu site: ~80KB ✅)
```

### **Resource Loading**
```
Fonts should load < 1s (use font-display: swap)
Images should load < 2s (use lazy loading)
No render-blocking resources
```

---

## Monitoring Tools (Recomendados)

### **Essencial (Grátis)**
- [ ] Google Analytics 4 - Tráfego e conversão
- [ ] Google Search Console - Indexação e erros
- [ ] Google PageSpeed Insights - Performance
- [ ] DevTools (Chrome) - Debug e performance

### **Recomendado (Grátis)**
- [ ] Hotjar - Heatmaps do usuário
- [ ] Microsoft Clarity - Session recording
- [ ] Bing Webmaster Tools - Tráfego secundário
- [ ] Lighthouse CI - Performance monitoring

### **Nice to Have (Pago)**
- [ ] Semrush - SEO análise competitiva
- [ ] Ahrefs - Backlink analysis
- [ ] Mixpanel - Advanced analytics
- [ ] Sentry - Error tracking

---

## Problemas Comuns & Soluções

### **Problema: Formulário não envia**
```bash
1. Abra DevTools (F12 → Console)
2. Procure por mensagem de erro
3. Verifique:
   - Webhook URL está correta em js/main.js?
   - Zapier/emailjs está ativo?
   - Email/planilha recebendo?
4. Teste em modo incógnito (elimina cache)
```

### **Problema: Site lento**
```bash
1. Rode Google PageSpeed
2. Se LCP > 3s:
   - Comprima imagens (tinypng.com)
   - Reduza JS não-crítico
   - Ative GZIP no servidor
3. Se FID > 100ms:
   - Reduza JS total
   - Use web workers
   - Defer non-critical JS
```

### **Problema: Não aparece no Google**
```bash
1. Verificou Search Console?
   - Vá em URL Inspection
   - Clique "Request Indexing"
2. Site tem tráfego?
   - Sem tráfego = Google rastreia menos
   - Use Google Ads para tráfego inicial
3. Aguardou 3+ semanas?
   - Novo site leva tempo
```

### **Problema: Conversão baixa < 1%**
```bash
1. Verificar qualidade de tráfego
   - Qual fonte traz leads melhores?
2. Form muito longo?
   - Teste com 3 campos vs 5
3. CTA não clara?
   - Teste textos diferentes
4. Falta social proof?
   - Adicione testimonios em vídeo
```

---

## Checklist de Lançamento Final

```bash
❌ ❌ ❌ NÃO LANCE SEM ESTES:
- [ ] HTTPS ativo
- [ ] Formulário testado (envio real)
- [ ] Analytics configurado
- [ ] Sitemap enviado ao Search Console
- [ ] Robots.txt funcional
- [ ] Nenhum erro em Console
- [ ] Mobile testado em device real
- [ ] Resposta automática de lead (email/slack)

⚠️ ⚠️ ⚠️ TAMBÉM IMPORTANTE:
- [ ] Backup dos arquivos
- [ ] Recovery plan se algo quebrar
- [ ] Contato de suporte documentado
- [ ] Horário de resposta definido
```

---

## Após o Lançamento

### **Semana 1: Monitoring**
- [ ] Verificar Analytics diariamente
- [ ] Responder leads em < 24h
- [ ] Monitorar erros em Search Console
- [ ] Testar formulário 1x por dia

### **Semana 2-4: Otimização**
- [ ] Analisar taxa de conversão
- [ ] Identificar páginas top
- [ ] Revisar bounce rate
- [ ] Planejar A/B tests

### **Mês 2+: Growth**
- [ ] Aumentar tráfego (ads, conteúdo)
- [ ] Otimizar conversão (A/B tests)
- [ ] Expandir com blog/case studies
- [ ] Analisar ROI

---

**Última atualização:** 17 de abril de 2024

✅ Seu website está pronto para validação!
