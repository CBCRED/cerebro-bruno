# 🤖 CBCRED — WhatsApp Bot API Oficial
**Data:** 17/04/2026  
**Status:** ✅ Bot funcionando

---

## 🎯 O que foi construído

Bot de atendimento automático no WhatsApp usando a **API oficial da Meta (Cloud API)**, rodando em Node.js com funil de vendas para consignado e FGTS.

---

## 🔑 Credenciais

| Item | Valor |
|------|-------|
| **App ID** | `808044922371515` |
| **App Name** | CBCRED Atendimento Bot |
| **Phone Number ID** | `1112071925318511` |
| **Número de teste** | `+1 555 189 1477` |
| **WABA ID** | `17552955552544708` |
| **Verify Token** | `cbcred_webhook_2024` |
| **Email Meta** | emprestimocbcred@gmail.com |
| **Portfólio Meta** | Cb cred tere |

> ⚠️ O WHATSAPP_TOKEN expira em 24h — gerar novo em:
> https://developers.facebook.com/apps/808044922371515/use_cases/customize/wa-dev-console/

---

## 📁 Projeto no Computador

**Pasta:** `C:\cbcred-bot`

```
C:\cbcred-bot\
├── index.js       ← Servidor + webhook + bot
├── package.json   ← Dependências Node.js
└── .env           ← Variáveis de ambiente (token, etc)
```

### Arquivo .env
```
WHATSAPP_TOKEN=EAALe6ZA6PfbsBRCtcwCO8INOZA9ZCY9AVeHrzGICE2EfynsbYpfaeZAPhBO90aycaumUvz7pNJoO1msNd
PHONE_NUMBER_ID=1112071925318511
VERIFY_TOKEN=cbcred_webhook_2024
PORT=3000
```

---

## 🚀 Como Iniciar o Bot Todo Dia

### Passo 1 — Abrir PowerShell e rodar o bot
```powershell
cd C:\cbcred-bot
node index.js
```
✅ Deve aparecer: **"Bot rodando na porta 3000"**

### Passo 2 — Abrir OUTRA janela do PowerShell e rodar o ngrok
```powershell
ngrok http 3000
```
✅ Vai aparecer uma URL tipo: `https://xxxxx.ngrok-free.app`

### Passo 3 — Se a URL do ngrok mudar
Atualizar o webhook na Meta:
1. Acessar: https://developers.facebook.com/apps/808044922371515
2. Ir em: Casos de uso → Configuração → Configuração
3. Atualizar a **URL de callback** com a nova URL + `/webhook`
4. Redigitar o token: `cbcred_webhook_2024`
5. Clicar em **"Verificar e salvar"**

### Passo 4 — Renovar o Token (a cada 24h)
1. Acessar: https://developers.facebook.com/apps/808044922371515
2. Ir em: Casos de uso → Configuração da API
3. Clicar em **"Gerar token de acesso"**
4. Copiar o novo token
5. Abrir `C:\cbcred-bot\.env` e substituir o `WHATSAPP_TOKEN`
6. Reiniciar o bot: `Ctrl+C` e `node index.js` novamente

---

## 🌐 Contas Criadas Hoje

| Serviço | Email | Observação |
|---------|-------|------------|
| Meta for Developers | emprestimocbcred@gmail.com | App ID: 808044922371515 |
| ngrok | brunoflpster@gmail.com | Token salvo no PC |

---

## 💬 Funil de Respostas do Bot

| Palavra-chave | Resposta |
|---------------|----------|
| `fgts` / `aniversario` | Explica Saque-Aniversário e pede CPF |
| `consignado` / `emprestimo` | Pergunta se é servidor, aposentado ou CLT |
| `taxa` / `juros` | Informa taxas a partir de 1,29% ao mês |
| `1` / `sim` / `quero` | Pede dados para proposta |
| Qualquer outra | Menu com 3 opções |

---

## 🔜 Próximos Passos

- [ ] **VPS** — Hospedar o bot 24h (Railway, Render ou Hostinger ~R$20/mês)
- [ ] **Token permanente** — Gerar token que não expira via System User
- [ ] **IA** — Conectar Claude ou GPT para respostas inteligentes
- [ ] **Número real** — Vincular número da CBCRED (requer desinstalar WhatsApp do chip)
- [ ] **Templates** — Criar e aprovar templates para disparos em massa
- [ ] **Verificar empresa** — Verificar CB CRED no Meta Business para aumentar limites

---

## 📚 Links Úteis

| Link | Para quê |
|------|----------|
| https://developers.facebook.com/apps/808044922371515 | Painel do App |
| https://dashboard.ngrok.com | Painel do ngrok |
| https://business.facebook.com | Meta Business Manager |

---

## 🏗️ Arquitetura do Sistema

```
Cliente (WhatsApp)
        ↓ mensagem
Meta Cloud API
        ↓ POST /webhook
ngrok (túnel público)
        ↓
Bot Node.js (porta 3000)
        ↓ lógica do funil
Meta Cloud API
        ↓ resposta
Cliente (WhatsApp)
```

---

*Criado em 17/04/2026 — Sessão de 4 horas do zero ao bot funcionando* 🚀
