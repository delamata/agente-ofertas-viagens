# ✈️ Agente de Ofertas de Viagem

Monitora automaticamente **Melhores Destinos** e **Passagens Imperdíveis**, extrai ofertas com IA e exporta para Excel — tudo direto no browser, sem backend.

---

## 🚀 Como publicar no GitHub Pages

### 1. Criar o repositório

1. Acesse [github.com/new](https://github.com/new)
2. Nome sugerido: `agente-ofertas-viagem`
3. Deixe como **Public**
4. Clique em **Create repository**

### 2. Fazer upload dos arquivos

1. Na página do repositório, clique em **Add file → Upload files**
2. Arraste os arquivos `index.html` e `README.md`
3. Clique em **Commit changes**

### 3. Ativar GitHub Pages

1. Vá em **Settings** (aba do repositório)
2. No menu lateral, clique em **Pages**
3. Em **Source**, selecione **Deploy from a branch**
4. Branch: `main` | Folder: `/ (root)`
5. Clique em **Save**
6. Aguarde ~1 minuto e acesse:

```
https://<seu-usuario>.github.io/agente-ofertas-viagem/
```

---

## 🔑 Configurar a chave API

1. Acesse [console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys)
2. Crie uma nova API Key
3. Cole no campo **🔑 Chave da API Anthropic** na página
4. Clique em **Salvar** — fica armazenada apenas no seu navegador (localStorage)

---

## 📋 Funcionalidades

| Recurso | Descrição |
|---|---|
| 🤖 Agente IA | Usa Claude + Web Search para navegar e extrair ofertas |
| 🌐 2 fontes | melhoresdestinos.com.br e passagensimperdiveis.com.br |
| 🔁 Coleta diária | Dispara automaticamente se passaram 24h desde a última coleta |
| 📊 Dashboard | Cards de estatísticas em tempo real |
| 🔍 Filtros | Busca por destino, fornecedor, valor ou fonte |
| 📥 Export Excel | Gera arquivo `.xlsx` completo com todas as ofertas |
| 💾 Persistência | Resultados salvos no localStorage do navegador |

---

## 🛡️ Segurança

- A chave API **nunca sai do seu navegador**
- Requisições vão direto para `api.anthropic.com` (sem servidor intermediário)
- Configure um limite de uso na chave em [console.anthropic.com](https://console.anthropic.com)

---

## 📁 Estrutura

```
agente-ofertas-viagem/
├── index.html    ← aplicação completa
└── README.md     ← instruções
```

## 🔧 Dependências

- **JSZip** via CDN (Cloudflare) — geração do `.xlsx`
- Resto: vanilla JS puro, zero frameworks, zero build step
