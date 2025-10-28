  # broker-white-label-opcoes-binarias
Plataforma white-label de opções binárias (BO): Next.js + FastAPI, autenticação Supabase. Conta DEMO/REAL, KYC com upload, preços em tempo real, abertura/fechamento de posições e painel admin. Pagamentos via XGate (depósito PIX e saques PIX/crypto) com webhooks. Pronta para deploy.


Plataforma BO white-label pronta para venda. CORE sólido: captura de candles em tempo real, motor de compra/venda e regras de depósito/saque (PIX e crypto) com webhooks. Já operando em live. Interessados, entre em contato por Issues ou em [https://t.me/reactdavicastro]

# BUNISESS — Broker White Label (BO)
IMAGENS NO FIM
Plataforma de **opções binárias (BO)** com painel do trader, conta **DEMO/REAL**, **KYC**, **depósitos PIX/saques** (XGate), **admin** (ativos/payouts/usuários/transações) e **preços em tempo-real**.

> Monorepo: **Next.js (frontend)** + **FastAPI (backend)** + **worker de fechamento**.

---

## 🔥 Principais recursos

- **Trading BO**
  - Compra **CALL/PUT** com duração configurável (1m, 5m, 15m, 1h).
  - Payout por timeframe (M1 / M5 / …).
  - Conta **DEMO** e **REAL** alternáveis no app.
  - Fechamento automático por **worker**.

- **Mercado & Preços**
  - Feed de candles via (integração de mercado).
  - Auditoria: candle da abertura/fechamento guardado na posição.

- **KYC e Perfil**
  - Upload de documento (frente) + selfie (opcional).
  - Status: `none | submitted | approved | rejected` + nota.

- **Pagamentos (XGate)**
  - **Depósito PIX**: cria ordem e retorna EMV (qrcode/copia-e-cola).
  - **Webhook depósito**: credita saldo no `Profile`.
  - **Saque PIX** e **Saque Crypto** (suporte a redes/moedas).
  - Webhooks de **withdraw** para baixar saldo com idempotência.
  (AQUI SE DEVE TERMINAR TODO O PROCESSO POIS VOCE PODE ESCOLHER OUTRA - DEPOSITO SO PIX)

- **Admin**
  - Ativos (símbolo, nome, payout M1/M5, ativar/desativar).
  - Usuários (KYC aprovar/reprovar + PnL por usuário).
  - Transações (últimas, status, totais).
  - KPI: usuários, volume, PnL da empresa, ativos listados.

- **Autenticação**
  - **Supabase Auth** (JWT). O backend valida `Authorization: Bearer <token>`.

---

**Stack**: Next.js 14, React, TypeScript, shadcn/ui, MobX • FastAPI, SQLAlchemy, PostgreSQL • Supabase (auth) • XGate (pagamentos PIX/crypto).

--

### 1) SYSTEMA
- Node 18+ (recomendado 20)
- Python 3.11/3.12
- PostgreSQL 14+
- Conta **Supabase** (Auth/JWT)
- Conta **XGate** (API Key, PIX habilitado). Para **saques**.


🔐 Segurança

Auth: Supabase JWT no header Authorization.

Webhooks: por padrão sem auth (XGate chama diretamente). Recomendo:

Validar IPs de origem (XGate).

Assinatura/HMAC (se disponível).


Idempotência via provider_ref.

CORS: restringir domínios em produção.

Secrets: nunca enviar keys ao frontend.

90% REQUISIÇÔES FEITAS EM SERVER FRONT NÃO VER.


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

