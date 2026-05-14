# 🛡️ Cylock — Dashboard de Notícias em Cibersegurança

Plataforma pública de monitoramento e visualização de notícias sobre cibersegurança, voltada para estudantes e o público geral da **Universidade Federal de Sergipe**.

---

## 🎯 Objetivo

Centralizar e exibir notícias atualizadas de cibersegurança de forma **organizada, visual e acessível**, facilitando o acompanhamento de tendências e o aprendizado de quem está começando na área.

---

## ⚙️ Funcionalidades Principais

### 📰 Coleta e Exibição de Notícias
- Agregação de notícias via **RSS, APIs e scraping**
- Atualização automática em intervalos configuráveis
- Exibição com: título, resumo, fonte, data e categoria
- Destaque visual para notícias de **alto impacto**

### 🔍 Filtros e Busca
- Filtro por **categoria** (malware, phishing, vulnerabilidades...)
- Filtro por **data** e **fonte**
- Campo de **busca por palavras-chave**

### 📊 Dashboard e Visualizações
- Gráficos de tendências (ex: tipos de ataques mais frequentes)
- Indicadores visuais de **nível de risco**
- Estatísticas simples e didáticas

### 🔔 Alertas e Notificações
- Integração com bot no **Telegram** e **Discord**
- Envio automático de alertas para notícias relevantes

---

## 🏗️ Arquitetura

```
Coletor de Dados → Backend → Banco de Dados → Frontend (Dashboard)
                                                      ↓
                                          Módulo de Notificações
                                         (Telegram / Discord)
```

| Camada | Responsabilidade |
|---|---|
| **Coletor** | Extrai e normaliza notícias de fontes externas |
| **Backend** | Processa, categoriza e prioriza o conteúdo |
| **Banco de Dados** | Armazena notícias, fontes e categorias |
| **Frontend** | Interface web de visualização |
| **Notificações** | Dispara alertas via Telegram/Discord |

---

## 🧰 Stack Tecnológica (Planejada)

**Backend**
- Python · FastAPI · feedparser · SQLAlchemy

**Frontend**
- React · TailwindCSS · Chart.js ou Recharts

**Infraestrutura**
- PostgreSQL · Docker · GitHub Actions · Render / Railway

---

## ⚠️ Riscos Conhecidos

- Mudanças na estrutura de sites externos podem **quebrar o scraping**
- Dependência de fontes externas (instabilidade ou bloqueios)
- Volume de dados pode crescer rapidamente → necessidade de paginação e limpeza periódica

---

## ✅ Critérios de Aceitação

- [ ] Notícias exibidas corretamente e atualizadas
- [ ] Filtros e busca funcionando sem falhas
- [ ] Dashboard com dados claros e compreensíveis
- [ ] Interface utilizável por iniciantes

---

## 📋 Requisitos Não Funcionais

| Requisito | Meta |
|---|---|
| ⚡ Desempenho | Carregamento < 3 segundos |
| 📱 Responsividade | Desktop e mobile |
| 🔒 Segurança | Proteção contra XSS e CSRF |
| 🔁 Disponibilidade | 99% do tempo |
| 📦 Escalabilidade | Arquitetura modular |

---

> 📧 **cylock.ufs@gmail.com** · 📸 **@cylock.ufs**
> *Liga Acadêmica de Cibersegurança — Universidade Federal de Sergipe*
