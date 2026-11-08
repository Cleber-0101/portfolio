# Site Portfólio — Cleber Batista

Portfólio pessoal de **Cleber Batista**, Backend Developer Jr (Node.js · TypeScript · APIs REST · SQL).

🔗 **No ar:** https://cleber-0101.github.io/Site-portif-lio/

Site estático (HTML, CSS e JavaScript puros, sem build), responsivo para celular, tablet e desktop,
hospedado de graça no **GitHub Pages**.

## Estrutura

```
.
├── index.html                  # página única do site
├── assets/
│   ├── css/style.css           # estilos (inclui os breakpoints de celular/tablet)
│   ├── js/script.js            # menu mobile, barra de progresso e animações
│   ├── img/foto-perfil.jpg     # foto do perfil (também usada na prévia do link)
│   ├── img/favicon.svg         # ícone da aba
│   └── docs/Cleber-Batista-CV.pdf  # currículo para download
└── .github/workflows/
    ├── ci.yml                  # validação
    └── deploy.yml              # publicação no GitHub Pages
```

## Deploy automático (CI/CD)

| Workflow | Quando roda | O que faz |
|----------|-------------|-----------|
| **CI** ([ci.yml](.github/workflows/ci.yml)) | `push` na `master` e em Pull Requests | Lint do HTML (`htmlhint`) e checa se todo arquivo citado no HTML existe |
| **Deploy site** ([deploy.yml](.github/workflows/deploy.yml)) | `push` na `master` (ou manual em *Actions → Run workflow*) | Publica só `index.html` + `assets/` no GitHub Pages |

**Todo push na `master` atualiza o site sozinho** em 1–2 minutos. O andamento aparece na aba *Actions*.

Configuração (já feita; só precisa repetir se criar outro repositório):
**Settings → Pages → Build and deployment → Source → "GitHub Actions"**.

## Como atualizar

- **Currículo:** substitua `assets/docs/Cleber-Batista-CV.pdf` mantendo o mesmo nome.
- **Foto:** substitua `assets/img/foto-perfil.jpg` (quadrada, ~480×480).
- **Textos, experiências e projetos:** edite `index.html`.

Depois: `git add .`, `git commit -m "..."` e `git push`.

## Rodar localmente

Abra o `index.html` no navegador ou sirva a pasta:

```bash
npx serve .
```
