# ═══════════════════════════════════════════════════════════
# PDR DE MISSÃO — ANTIGRAVITY
# Projeto: VELLA · Landing Page GitHub Pages
# Data: 2026-03-22 · Gerado por: Claude Sonnet 4.6
# ═══════════════════════════════════════════════════════════

## ESTADO ATUAL — LER PRIMEIRO

O repositório D:\VELLA já está 100% preparado:

- git init ✅ feito
- git add . ✅ feito  
- git commit ✅ feito → hash: 32b2025
- git branch -M main ✅ feito
- git remote add origin ✅ feito → aponta para github.com/Araken13/Vella.git
- MISSAO_ANTIGRAVITY.md ✅ existe mas ainda não foi commitado

O push falhou por bloqueio de rede no ambiente Claude.
**Só falta o push.** Nada mais.

---

## MISSÃO ÚNICA — EXECUTAR AGORA

Abrir PowerShell e executar EXATAMENTE estes comandos na ordem:

### PASSO 1 — Entrar na pasta

```powershell
cd D:\VELLA
```

### PASSO 2 — Adicionar arquivo novo que ficou de fora

```powershell
git add MISSAO_ANTIGRAVITY.md
git commit -m "docs: adiciona PDR de missão Antigravity"
```

### PASSO 3 — Trocar a URL do remote pelo token novo

```powershell
git remote set-url origin https://TOKEN_NOVO@github.com/Araken13/Vella.git
```

> Substituir TOKEN_NOVO pelo Personal Access Token do Araken13
> com escopo `repo`. Gerar em: github.com/settings/tokens

### PASSO 4 — Push

```powershell
git push -u origin main
```

**Resposta esperada:**
```
Enumerating objects: 13, done.
...
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

### PASSO 5 — Ativar GitHub Pages

1. Acessar: https://github.com/Araken13/Vella/settings/pages
2. Source → `Deploy from a branch`
3. Branch: `main` · Folder: `/ (root)`
4. Clicar em **Save**
5. Aguardar 60 segundos

### PASSO 6 — Verificar

```powershell
curl -I https://araken13.github.io/Vella/
```

Resposta esperada: `HTTP/2 200`

---

## ESTRUTURA DO REPOSITÓRIO QUE SERÁ PUBLICADO

```
D:\VELLA\
├── index.html              ← Landing page completa (54 KB)
├── README.md               ← Documentação
├── MISSAO_ANTIGRAVITY.md   ← Este arquivo
├── .nojekyll               ← GitHub Pages sem Jekyll
├── _config.yml             ← Config GitHub Pages
├── .gitignore
├── CNAME.example           ← Modelo para domínio customizado
└── assets\
    ├── favicon.svg         ← Ícone vetorial
    ├── favicon.ico         ← Ícone 16/32/48px
    └── og-image.png        ← Preview social 1200x630
```

---

## TROUBLESHOOTING

| Erro | Solução |
|------|---------|
| `403 Forbidden` | Token sem escopo `repo` → gerar novo em github.com/settings/tokens |
| `rejected - non-fast-forward` | `git pull origin main --allow-unrelated-histories --no-edit` depois push |
| `remote origin already exists` | Já existe — usar `git remote set-url` não `git remote add` |
| Pages retorna 404 | Aguardar 2-5 min após ativar Pages |

---

## RESULTADO ESPERADO AO FINAL

```
✅ Repositório: https://github.com/Araken13/Vella
✅ Site ao vivo: https://araken13.github.io/Vella/
✅ Favicon:      assets/favicon.svg + favicon.ico
✅ OG Image:     assets/og-image.png (1200x630)
✅ Meta tags:    og:title, og:image, twitter:card, description
```

---

## REPORTAR CONCLUSÃO

Após concluir, reportar para o Claude:

```
MISSÃO CONCLUÍDA
commit: 32b2025 + novo commit docs
push: OK
pages: ATIVO
url: https://araken13.github.io/Vella/
```

---

# CONTEXTO COMPLETO DO PROJETO VELLA

## O que é a Vella

Motor local OLLAMA + Qdrant com servidor MCP nativo.
100% local, zero nuvem, zero custo por token.

Stack: Rust 1.75+ · OLLAMA · Qdrant · FastEmbed + ONNX ·
MCP Protocol v2024-11-05 · Sled · XXHash3 · Ratatui

Repositório do motor: https://github.com/Araken13/MPC-RUST-LEARNING-CONTEXT
Conta GitHub: Araken13
Licença: MIT
Autor: Araken Carmo Neto

## O que foi construído hoje

1. Identidade visual completa (logo SVG, paleta, tagline)
2. Landing page HTML (54 KB, 9 seções, dark theme náutico)
3. Favicon SVG + ICO (16/32/48px)
4. OG Image 1200x630 para redes sociais
5. Estrutura GitHub Pages (.nojekyll, _config.yml, CNAME.example)
6. Mini-App vella_status (Python, verifica 9 arquivos + 6 meta tags)
7. Módulo Bridge Rust (antigravity_bridge.rs — orquestrador bidirecional)
8. Spec de integração do Bridge no motor pdr
9. Missão JSON para push orquestrado via Bridge

## Arquitetura do Bridge (fase futura)

Claude → bridge_send (MCP tool) →
BridgeOrchestrator (Rust) →
stdin do antigravity.exe →
aguarda stdout →
captura resposta →
devolve para Claude →
loop até missão concluída

Arquivo: src/bridge/antigravity.rs
Ferramentas MCP: bridge_start, bridge_send, bridge_mission,
                 bridge_history, bridge_stop

---
PDR gerado por Claude Sonnet 4.6 · project-context-rs · 2026-03-22
Hyper-Agent Alliance — Onde código encontra consciência.
