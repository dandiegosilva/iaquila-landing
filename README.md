# iAquila — Landing Page

Site institucional da **iAquila**, plataforma forense de detecção de adulteração de chassi com IA pericial.

🔗 **Em produção:** [iaquila.suporteleiloes.com.br](https://iaquila.suporteleiloes.com.br)

---

## Stack

| | |
|---|---|
| **HTML5** + **CSS3** | Sem framework, build zero |
| **Vanilla JS** | IntersectionObserver pra fade-in on scroll |
| **Inter** | Tipografia (Google Fonts) |
| **Cloudflare CDN** | Cache global + SSL |
| **Nginx** | Reverse proxy + serve static |

### Por que HTML estático?

Landing pages institucionais não precisam de framework. Stack moderna pesada (React/Next/Astro) seria over-engineering pra um site de marketing que só precisa carregar rápido.

**Métricas atuais:**
- ⚡ **First Contentful Paint:** ~180ms
- 📦 **Tamanho total:** ~25 KB (HTML + CSS embutido + 1 PNG da logo)
- 🌍 **Servido via Cloudflare** (HTTP/2, gzip, edge-cached)
- 🎯 **Lighthouse Performance:** 100/100

Mesmo Linear.app, Stripe.com e Vercel.com servem HTML estático em produção — só usam framework no buildtime.

---

## Estrutura

```
iaquila-landing/
├── index.html       # markup + estrutura semantica
├── styles.css       # estilos (cacheaveis separadamente)
└── README.md        # este arquivo
```

HTML + CSS separados. Zero dependencias de runtime, zero build step.

---

## Deploy

```bash
# Servir localmente
python3 -m http.server 8080
# Abrir http://localhost:8080

# Deploy pra VPS
rsync -av index.html styles.css iaquila:/var/www/iaquila-landing/
```

---

## Seções

- **Hero** — proposta de valor + mockup de resultado de análise
- **Como funciona** — 3 passos (Capture / Análise / Laudo)
- **Recursos** — 6 features-chave do produto
- **Highlight** — diferencial competitivo + estatísticas
- **Pricing** — 3 planos comerciais (Starter / Pro / Business)
- **FAQ** — 5 perguntas frequentes
- **CTA final** — agendamento de demo via WhatsApp
- **Footer** — navegação + contato

---

## Licença

Proprietária — © 2026 iAquila. Todos os direitos reservados.
