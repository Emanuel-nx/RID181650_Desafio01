# 🏛️ Landing Page — Arquitetura

Landing page institucional para empresa de arquitetura, desenvolvida como desafio técnico de portfólio front-end.

---

## 📋 Sobre o Projeto

O projeto consiste em uma landing page responsiva criada com **HTML puro e CSS**, sem frameworks ou dependências externas. O formulário de contato é integrado ao **Google Sheets** via **SheetMonkey**, permitindo capturar leads diretamente em uma planilha.

---

## 🎨 Layout

O design foi baseado no protótipo disponibilizado no Figma:

- **Cores:** `#303030` (escuro), `#F9F9F9` (claro), `#FFFFFF` (branco), `#C8952A` (acento dourado)
- **Tipografia:** [Inter](https://fonts.google.com/specimen/Inter) — Google Fonts
- **Responsivo:** adaptado para telas a partir de 768px

---

## 🗂️ Estrutura do Projeto

```
/
├── index.html    # Página principal (HTML + CSS + JS em arquivo único)
└── README.md     # Documentação do projeto
```

---

## 📄 Seções da Página

| Seção | Descrição |
|---|---|
| **Hero** | Título principal com fundo escuro |
| **Stats** | Números de destaque da empresa (850 empreendimentos, 40 anos, 2M m²) |
| **Sobre** | Texto institucional com imagem de prédio |
| **Formulário** | Captura de nome e e-mail integrada ao Google Sheets |
| **Footer** | Rodapé com copyright |

---

## ⚙️ Integração com SheetMonkey

O formulário envia dados para o **Google Sheets** utilizando o serviço [SheetMonkey](https://sheetmonkey.io).

### Como funciona

1. O usuário preenche **Nome** e **Email** e clica em "Fale Conosco"
2. Os dados são enviados via `fetch` com `mode: 'no-cors'` para a API do SheetMonkey
3. O SheetMonkey registra os dados na planilha vinculada automaticamente

### Campos enviados

| Campo HTML (`name`) | Coluna na Planilha | Descrição |
|---|---|---|
| `Name` | Name | Nome do usuário |
| `Email` | Email | E-mail do usuário |
| `Created` | Created | Data/hora do envio (automático) |

### Endpoint

```
https://api.sheetmonkey.io/form/DW2jBK6mUGV5Xa1f8Pria
```

> ⚠️ Para trocar a planilha de destino, basta substituir o ID no `action` do `<form>` e garantir que os cabeçalhos da nova planilha sejam `Name`, `Email` e `Created`.

---

## 🚀 Como Executar Localmente

Não há dependências ou build necessário. Basta abrir o arquivo no navegador:

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git

# Abra o arquivo no navegador
cd seu-repositorio
open index.html
# ou arraste o arquivo para o navegador
```

---

## ☁️ Deploy

O projeto está hospedado no **Netlify** com deploy contínuo via repositório GitHub.

- 🌐 **Site:** [[https://seu-site.netlify.app](https://ephemeral-pixie-e6715f.netlify.app/)](https://ephemeral-pixie-e6715f.netlify.app/)
- 📊 **Planilha:** [Google Sheets — Respostas do Formulário](https://docs.google.com/spreadsheets/d/seu-id-aqui)

> Atualize os links acima com as URLs reais do seu projeto.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| HTML5 | Estrutura da página |
| CSS3 | Estilização e responsividade |
| JavaScript (ES6+) | Submissão assíncrona do formulário |
| Google Fonts | Tipografia (Inter) |
| Pexels | Imagem de arquitetura |
| SheetMonkey | Integração com Google Sheets |
| Netlify | Hospedagem |

---

## 📱 Responsividade

A página é responsiva com breakpoint em `768px`:

- **Desktop:** layout em duas colunas na seção Sobre, stats em linha
- **Mobile:** colunas empilhadas, padding reduzido, imagem com altura ajustada

---

## 👤 Autor

Desenvolvido como parte de um desafio técnico de desenvolvimento front-end.

---

## 📜 Licença

Este projeto foi desenvolvido para fins educacionais e de portfólio.
