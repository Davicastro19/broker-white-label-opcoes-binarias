# broker-white-label-opcoes-binarias

Plataforma white-label de opções binárias (BO): Next.js + FastAPI, autenticação Supabase. Conta DEMO/REAL, KYC com upload, preços em tempo real, abertura/fechamento de posições, **sistema de afiliados**, e painel admin. Pagamentos via XGate (depósito PIX e saques PIX/crypto) com webhooks. Pronta para deploy.

Plataforma BO white-label pronta para venda. CORE sólido: captura de candles em tempo real, motor de compra/venda, **gestão de afiliados** e regras de depósito/saque (PIX e crypto) com webhooks.  
Já operando em live.  
Interessados, entre em contato por [https://api.whatsapp.com/send?phone=5511977476664] ou em [https://t.me/reactdavicastro]

---

# BUNISESS — Broker White Label (BO)
IMAGENS NO FIM  
Plataforma de **opções binárias (BO)** com painel do trader, conta **DEMO/REAL**, **KYC**, **depósitos PIX/saques** (XGate), **admin** (ativos/payouts/usuários/transações), **preços em tempo-real** e **módulo de afiliados integrado**.


---

## 🔥 Principais recursos

### 💹 Trading BO
- Compra **CALL/PUT** com duração configurável (1m, 5m, 15m, 1h).
- Payout por timeframe (M1 / M5 / M15)
- Conta **DEMO** e **REAL** alternáveis no app.
- Fechamento automático por **worker**.

---

### 🕒 Mercado & Preços
- Feed de candles via integração de mercado.
- Auditoria completa: candle de **abertura e fechamento** armazenado junto à posição.

---

### 🧾 KYC e Perfil
- Upload de documento (frente) + selfie (opcional).
- Status: `none | submitted | approved | rejected` + nota personalizada do admin.

---

### 💰 Pagamentos (XGate)
- **Depósito PIX**: cria ordem e retorna EMV (qrcode/copia-e-cola).
- **Webhook depósito**: credita saldo automaticamente no `Profile`.
- **Saque PIX** e **Saque Crypto** (suporte a múltiplas redes e moedas).
- Webhooks de **withdraw** para baixar saldo com idempotência.
- (O sistema é projetado para operar com **depósitos exclusivamente via PIX**.)

---

### 🧩 Sistema de Afiliados (NOVO)

#### 🎯 Visão geral
Módulo nativo de **afiliados** totalmente integrado ao núcleo da corretora.  
Permite a criação de redes de afiliados, comissão automática, e controle de desempenho em tempo real.

#### ⚙️ Funcionalidades principais
- Geração automática de **links de afiliação únicos** por usuário.
- Painel visual completo:
  - Total de afiliados ativos/inativos.
  - Volume negociado por afiliado.
  - Lucro da corretora por rede.
  - **Comissão pendente / liberada**.
- Relatórios filtráveis por **data, ativo, tipo de conta (DEMO/REAL)**.
- Cálculo baseado em **lucro da corretora (Revenue Share)** ou **volume (Turnover)**.
- Dashboard administrativo com rede hierárquica e gráficos de desempenho.
- Pagamento de comissões via **PIX (XGate)** com webhooks dedicados.

#### 📊 Modelos de comissão
- **Revenue Share** — percentual sobre o lucro líquido da corretora.  
- **Turnover** — percentual sobre o volume total negociado na perda.  
- Configuração dos percentuais feita diretamente pelo **Admin**.


---

### ⚙️ Admin
- Gerenciamento de **ativos** (símbolo, nome, payout M1/M5/M15, ativar/desativar).
- Gerenciamento de **usuários** (aprovação KYC, PnL individual).
- Controle de **transações** (status, totais, últimas entradas/saídas).
- KPIs:
  - Usuários ativos
  - Volume total
  - PnL da corretora
  - Ativos listados
- Módulo **Afiliados**:
  - Totais de comissão e pagamento manual
  - Histórico de transferências e registros de comissão

---

### 🔐 Autenticação
- **Supabase Auth (JWT)** com verificação via `Authorization: Bearer <token>`.
- Sessão segura com tempo de expiração configurável.

---

## ⚡ Stack
**Frontend:** Next.js 14, React, TypeScript, TailwindCSS, shadcn/ui, MobX  
**Backend:** FastAPI, SQLAlchemy, PostgreSQL  
**Auth:** Supabase (JWT)  
**Pagamentos:** XGate (PIX e Crypto)  
**Infraestrutura:** Docker, Nginx, PM2 ou digitalocean e vercel ou qqualquer uma na verdade  


---

### 1️⃣ Systema
- Node 
- Python 
- PostgreSQL 
- Conta **Supabase** (Auth/JWT)
- Conta **XGate** (API Key, PIX habilitado para depósitos e saques)

---

## 🔒 Segurança

- Auth: Supabase JWT no header Authorization.  
- Webhooks: padrão sem autenticação (XGate chama diretamente). Recomenda-se:
  - Validar IPs de origem (XGate).
  - Implementar assinatura HMAC se disponível.
- Idempotência via `provider_ref`.
- CORS: restringir domínios em produção.
- Secrets protegidos (nunca enviados ao frontend).
- 90% das requisições ocorrem **no servidor**, não no front.

---

## 📸 Screenshots

<img width="1919" height="911" alt="Captura de tela 2025-10-08 164642" src="https://github.com/user-attachments/assets/cc90b112-e37a-472f-b417-cae08df80ae2" />
<img width="1917" height="906" alt="Captura de tela 2025-10-08 164607" src="https://github.com/user-attachments/assets/2741b095-c21f-4e29-96ec-b90471ac56ea" />
<img width="1904" height="888" alt="Captura de tela 2025-10-08 164750" src="https://github.com/user-attachments/assets/bf4dc07c-2d6c-4cef-a801-cd595ab29cad" />
<img width="1918" height="909" alt="Captura de tela 2025-10-08 164924" src="https://github.com/user-attachments/assets/3bf828c4-d318-4008-bbd3-5e5798c6f9c2" />
<img width="1918" height="905" alt="Captura de tela 2025-10-08 164910" src="https://github.com/user-attachments/assets/1665d988-f266-44cc-9f81-9947af8263fa" />
<img width="1916" height="899" alt="Captura de tela 2025-10-08 165334" src="https://github.com/user-attachments/assets/d5bb152c-b94a-4023-8df1-e896fde6a677" />
<img width="1912" height="906" alt="Captura de tela 2025-10-08 165318" src="https://github.com/user-attachments/assets/4a502223-fb33-4cce-b2b2-28bc6d8cf70b" />
<img width="1916" height="904" alt="Captura de tela 2025-10-08 165306" src="https://github.com/user-attachments/assets/20ed9ecb-12bc-43a7-8638-7c6f5db1eb97" />
<img width="1010" height="474" alt="Captura de tela 2025-10-28 051501" src="https://github.com/user-attachments/assets/4761c17b-1acf-46f0-8213-ca377df47d41" />
<img width="417" height="339" alt="Captura de tela 2025-10-08 165212" src="https://github.com/user-attachments/assets/42d6352f-be9a-416e-b5ee-afac62747ced" />
<img width="1916" height="895" alt="Captura de tela 2025-10-08 165200" src="https://github.com/user-attachments/assets/8a2f5a9b-8dd7-46c0-8957-0b20bb155f87" />
<img width="1909" height="899" alt="Captura de tela 2025-10-08 165142" src="https://github.com/user-attachments/assets/d3d21178-08ea-488a-a956-b16071b1c440" />
<img width="1918" height="885" alt="Captura de tela 2025-10-08 165119" src="https://github.com/user-attachments/assets/bf09bdc1-b5e8-4304-9a55-182fa191108f" />
<img width="1895" height="941" alt="Captura de tela 2025-10-08 165101" src="https://github.com/user-attachments/assets/7220ddd8-3cf8-4f18-b09d-5172c8f12089" />
<img width="1896" height="820" alt="Captura de tela 2025-10-08 165048" src="https://github.com/user-attachments/assets/0addc95a-91d9-44f0-a481-10cfd36715ae" />
<img width="1739" height="838" alt="Captura de tela 2025-10-08 165023" src="https://github.com/user-attachments/assets/82eafe08-2493-428f-b09e-3aea9596f280" />
<img width="1906" height="898" alt="Captura de tela 2025-10-08 165007" src="https://github.com/user-attachments/assets/dbec74c7-14f0-4039-81c5-b3c06d06f02b" />
<img width="1881" height="880" alt="Captura de tela 2025-10-08 164953" src="https://github.com/user-attachments/assets/47c94d4c-f3f6-4990-a03e-ad7f1967c4b7" />
<img width="1918" height="908" alt="Captura de tela 2025-10-08 164702" src="https://github.com/user-attachments/assets/2696d641-0448-45c6-9790-e53c8b9f2eff" />
<img width="2332" height="874" alt="Captura de tela 2025-10-31 231945" src="https://github.com/user-attachments/assets/d4d851a6-71bf-4076-97fa-f7d56af26603" />
<img width="1886" height="907" alt="Captura de tela 2025-11-01 080625" src="https://github.com/user-attachments/assets/56c871c4-7115-4aa3-89fb-0911a56926f4" />
<img width="648" height="374" alt="Captura de tela 2025-11-01 080620" src="https://github.com/user-attachments/assets/bdefdf67-a25f-409d-ae5d-9185299ed9a3" />
<img width="1902" height="518" alt="Captura de tela 2025-11-01 075604" src="https://github.com/user-attachments/assets/6409e91a-69d2-43bc-b816-3d6f78bdd204" />
<img width="1475" height="286" alt="Captura de tela 2025-11-01 012640 - Copia" src="https://github.com/user-attachments/assets/3682169d-b006-4bf6-a3c4-2e90627e0692" />
<img width="1263" height="877" alt="Captura de tela 2025-11-01 012548" src="https://github.com/user-attachments/assets/6e09de02-446c-420a-b3fe-d3e496878afd" />
<img width="2030" height="831" alt="Captura de tela 2025-10-31 232109" src="https://github.com/user-attachments/assets/38165790-48f7-422c-a7eb-1877e4463132" />
<img width="1800" height="804" alt="Captura de tela 2025-10-31 232055 - Copia" src="https://github.com/user-attachments/assets/926fe034-5796-40e9-a614-c5eff6b7be50" />
<img width="1454" height="734" alt="Captura de tela 2025-10-31 232007 - Copia" src="https://github.com/user-attachments/assets/49debe28-7c0f-4b63-8dc9-34830e9f116a" />




---

## 🧩 Tags

binary-options  
digital-options  
options-trading  
quotex  
iq-option  
olymp-trade  
deriv  
binomo  
pocket-option  
white-label-broker  
trading-platform  
broker-engine  
trading-engine  
payout  
fixed-time-trade  
otc-market  
ohlcv  
candles  
price-feed  
websocket  
fastapi  
python  
sqlalchemy  
postgresql  
nextjs  
react  
typescript  
tailwindcss  
shadcn-ui  
mobx  
kyc  
aml  
pix-payments  
deposits  
withdrawals  
webhooks  
risk-management  
copy-trading  
trading-bot  
admin-dashboard  
white-label  
broker  
realtime-data  
ohclv-candles  
charting  
supabase  
xgate  
affiliate-system  
revenue-share  
turnover-model  
affiliate-dashboard  
