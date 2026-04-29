# ⚡ Selo H - Quick Start (5 Minutos)

## O que você tem
✅ Website pronto (production-ready)
✅ Copywriting orientado para conversão
✅ SEO otimizado
✅ Mobile-first design
✅ Formulário de captura de leads

## Próximos 3 passos

### **1️⃣ HOSPEDAGEM (5 min)**

**Escolha uma:**

#### A. Vercel (Recomendado - Super fácil)
```bash
1. Vá em vercel.com → Sign up
2. Clique "New Project"
3. Conecte seu GitHub ou selecione "Import Project"
4. Aponte pasta /web
5. Clique Deploy
6. Pronto! Seu site está live em vercel-app-name.vercel.app
```

#### B. Netlify (Alternativa fácil)
```bash
1. Vá em netlify.com → Sign up
2. Clique "Add new site"
3. Arraste pasta /web na área de drag-drop
4. Pronto! Seu site está live
```

#### C. Seu próprio servidor
```bash
1. Upload pasta /web via FTP para /public_html/
2. Configure HTTPS no painel de controle
3. Aponte domínio para o servidor
4. Pronto!
```

---

### **2️⃣ DOMÍNIO (5 min)**

```bash
# Se não tiver domínio:
1. Vá em registro.br (Brasil) ou godaddy.com
2. Busque: seloh.org (ou seu nome)
3. Compre o domínio
4. Aguarde confirmação

# Apontar domínio para hospedagem:
1. Vá em seu registrador (onde comprou o domínio)
2. Procure por "DNS" ou "Apontar domínio"
3. Use os nameservers do seu hosting:
   - Vercel: Siga instruções na dashboard
   - Netlify: Siga instruções na dashboard
   - Seu server: Use IP do servidor
4. Aguarde propagação (5-48h)
```

---

### **3️⃣ FORMULÁRIO (10 min)**

O formulário não envia nada. Você precisa conectar a uma API.

**Escolha uma (mais fácil para hardest):**

#### ✨ Opção 1: Zapier (MAIS FÁCIL)
```bash
1. Vá em zapier.com → Sign up grátis
2. Clique "Create Zap"
3. Trigger: "Webhooks by Zapier" → "Catch Raw Hook"
4. Copy a URL gerada (webhook_url)
5. Action: "Google Sheets" → "Create Spreadsheet Row"
6. Conecte sua conta Google
7. Selecione/crie planilha

8. Agora edite js/main.js:
   - Procure: "simulateFormSubmission"
   - Substitua fetch URL pela webhook_url do Zapier
   
9. Teste: Preencha formulário → deve aparecer no Sheets

PRONTO! Cada lead entra automaticamente numa planilha.
```

#### ⚡ Opção 2: Seu próprio email (MAIS CONTROLE)
```bash
1. Vá em emailjs.com → Sign up grátis
2. Conecte sua conta Gmail/Outlook
3. Copie Service ID, Template ID, Public Key

4. No index.html, adicione antes de </body>:
   <script type="text/javascript"
     src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/index.min.js"></script>

5. No js/main.js, edite simulateFormSubmission():
   emailjs.init("SUA_PUBLIC_KEY");
   const result = await emailjs.send(
     "SUA_SERVICE_ID",
     "SUA_TEMPLATE_ID",
     data
   );

6. Teste: Preencha formulário → deve receber email

PRONTO! Cada lead vai direto pro seu email.
```

#### 🔗 Opção 3: Seu CRM (SE TEM CONTA)
```bash
Ferramentas que podem integrar:
- HubSpot (grátis)
- Pipedrive
- Salesforce
- Monday.com
- Cualquier API REST

Edit js/main.js → fetch sua API endpoint
```

---

## ✅ Checklist Mínimo (HOJE)

- [ ] Hospedagem ativa
- [ ] Domínio apontando
- [ ] Formulário enviando leads
- [ ] Testar em mobile (abrir em iPhone/Android)
- [ ] Testar em desktop (Chrome, Firefox, Safari)

---

## 📊 Verificar se está tudo certo

```bash
# 1. Abra seu site no navegador
https://seulodminio.com.br

# 2. Deveria ver:
  ✅ Logo "Selo H"
  ✅ Navbar com links
  ✅ Hero section com "Sua Empresa É Incrível?"
  ✅ Scroll vê features, FAQ, form
  ✅ Form funciona (não dá erro)

# 3. Testes técnicos:
  Abra DevTools (F12)
  Console tab → não deve ter erros vermelhos
  Se tiver erro → mande screenshot
```

---

## 🚀 Próximo: Gerar Tráfego

Depois que site estiver funcional:

### **Semana 1: Tráfego Orgânico (Grátis)**
- Compartilhe no LinkedIn (seu perfil pessoal)
- Envie para 50-100 contatos diretos
- Poste no WhatsApp/Telegram

### **Semana 2: Google Ads (Pago)**
- Vá em google.com/ads
- Crie conta
- Budget inicial: R$ 50-100/dia
- Campaign type: "Leads"

### **Semana 3: Analytics (Monitoramento)**
- Vá em analytics.google.com
- Clique em "Começar"
- Pegue código do Analytics
- Cole no `<head>` do index.html (logo após <title>)
- Agora você vê: visitantes, taxa de conversão, tudo

---

## 📞 Dúvidas Comuns

**P: Quanto custa hospedagem?**
R: Vercel e Netlify = Grátis até 100k requests/mês

**P: E se o formulário não funcionar?**
R: Abra DevTools (F12 → Console). Se tiver erro, mande screenshot.

**P: Posso mudar as cores?**
R: Sim! Edit `css/tokens.css`. Mude `--accent-green` e `--accent-blue`.

**P: Quanto tempo leva aparecer no Google?**
R: 3-4 semanas até indexar. 2-3 meses para ranquear bem.

**P: Qual deve ser minha taxa de conversão?**
R: 2-3% é baseline. Com otimização: 5-7%.

---

## 📍 Arquivos Importantes

```
web/
├── index.html          ← Página principal (edite textos aqui)
├── js/main.js         ← JavaScript (edit webhook URL aqui)
├── css/styles.css     ← Estilos (edit cores aqui)
├── DELIVERY.md        ← Documentação completa
├── STRATEGY.md        ← Como converter
└── ROADMAP.md         ← Próximos meses
```

---

## 💡 Última Dica

**Seu website está 95% pronto. Os 5% que faltam é você dirigindo tráfego.**

Tráfego + Website conversão-ready = Leads consistentes.

Sem tráfego = Ninguém vê.

**Portanto: Comece a dirigir tráfego HOJE.**

---

**Tempo total setup:** 30 minutos  
**Tempo até primeira conversão:** 2-7 dias  
**Tempo até otimização real:** 30 dias

🎉 Boa sorte!

P.S.: Qualquer dúvida, veja os documentos:
- `DELIVERY.md` - Setup detalhado
- `STRATEGY.md` - Como funciona conversão
- `README.md` - Tudo técnico
