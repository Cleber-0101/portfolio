# Site Portfólio — Cleber Batista

Site estático (HTML/CSS/JS puro, sem build) publicado no **GitHub Pages**.

## CI/CD

| Workflow | Arquivo | Quando roda | O que faz |
|----------|---------|-------------|-----------|
| **CI** | [.github/workflows/ci.yml](.github/workflows/ci.yml) | `push` na `master` e em Pull Requests | Lint do HTML (`htmlhint`) e checagem dos arquivos essenciais |
| **Deploy site** | [.github/workflows/deploy.yml](.github/workflows/deploy.yml) | `push` na `master` (ou manual em *Actions → Run workflow*) | Empacota os arquivos versionados e publica no GitHub Pages |

Ou seja: **todo push na `master` faz deploy automático.**

### Configuração única (só na primeira vez)

No repositório no GitHub: **Settings → Pages → Build and deployment → Source → "GitHub Actions"**.

Sem isso o workflow de deploy falha com erro de permissão de Pages.

## Rodar localmente

Basta abrir `index.html` no navegador, ou servir a pasta:

```bash
npx serve .
```
