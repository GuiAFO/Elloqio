[README.md](https://github.com/user-attachments/files/29443349/README.md)
# Elloqio — Landing de validação + protótipo

Página de **pesquisa de intenção** do Elloqio, um conceito de app para treinar **inglês voltado ao mercado de trabalho internacional**, por nicho de profissão (começando por tecnologia). O objetivo deste site **não é vender**, e sim medir o interesse real antes de construir o produto.

O repositório contém duas páginas estáticas: a landing com a pesquisa e um protótipo offline (amostra) para a pessoa experimentar a ideia.

> **Status:** fase de validação. O protótipo é ilustrativo e funciona offline — no produto completo a IA conversa e corrige em tempo real.

---

## ✨ O que tem aqui

- **Landing de pesquisa** (`index.html`): apresentação do conceito, três cards que abrem o protótipo e um formulário curto de intenção (nível de inglês, interesse, disposição a pagar).
- **Protótipo offline** (`tech-pronto.html`): amostra interativa com três modos —
  - **Vocabulário** — flashcards de termos de tech (programação, dados, time ágil) com frase de exemplo e áudio (Web Speech API);
  - **Quiz** — tradução com pontuação;
  - **Entrevista** — exemplo ilustrativo de entrevista técnica em inglês, com tradução e áudio.

## 🗂 Estrutura

```
.
├── index.html        # landing + formulário de pesquisa
├── tech-pronto.html  # protótipo offline (amostra)
└── README.md
```

> ⚠️ Os dois arquivos devem ficar **na mesma pasta** (a raiz do repositório). Os botões "Experimentar" usam links relativos (`tech-pronto.html#vocab`, `#quiz`, `#entrevista`) e o protótipo tem um link de volta para o formulário.

## 🛠 Tecnologia

- **HTML, CSS e JavaScript puros** — sem framework e sem etapa de build.
- CSS com variáveis (`:root`), layout responsivo e **modo escuro** via `prefers-color-scheme`.
- Tipografia [Sora](https://fonts.google.com/specimen/Sora) + [Inter](https://fonts.google.com/specimen/Inter) (Google Fonts).
- **[Formspree](https://formspree.io/)** como backend do formulário.
- **Web Speech API** (`speechSynthesis`) para a pronúncia no protótipo.

## 🚀 Publicar no GitHub Pages

1. Suba `index.html` e `tech-pronto.html` na raiz do repositório.
2. Vá em **Settings → Pages**.
3. Em *Source*, escolha **Deploy from a branch**; em *Branch*, selecione **main** e a pasta **/ (root)**; clique em **Save**.
4. Em ~1 minuto o site fica disponível em `https://SEU-USUARIO.github.io/SEU-REPOSITORIO/`.

## 💻 Rodar localmente

Para apenas navegar, basta abrir o `index.html` no navegador. Para **testar o envio do formulário**, publique primeiro (o envio depende de uma origem `http(s)`, não de `file://`). No primeiro envio, o Formspree manda um e-mail para confirmar o formulário — é só uma vez.

## ⚙️ Configuração

- **Endpoint do formulário:** a constante `ENDPOINT`, no início do `<script>` do `index.html`. Aponte para o seu formulário do Formspree.
- **E-mail de contato:** usado no aviso de privacidade do `index.html` (link `mailto:`).
- **Conteúdo do protótipo:** o objeto `VOCAB` e a lista `IV` (entrevista), no `<script>` do `tech-pronto.html`.

## 🔒 Privacidade (LGPD)

O formulário coleta as respostas da pesquisa e, **opcionalmente**, nome e contato (este último só é solicitado a quem demonstra alto interesse). Os dados servem apenas para entender o interesse no projeto e, caso a pessoa deixe contato, avisar sobre novidades. Não são vendidos nem compartilhados com terceiros, e a remoção pode ser solicitada pelo e-mail informado na página. O consentimento é obrigatório no envio.

## ♿ Acessibilidade

- Link "pular para o conteúdo" e estrutura semântica (`header`, `main`).
- Foco visível, foco gerenciado ao trocar de tela e respeito a `prefers-reduced-motion`.
- `aria-required`, `aria-live` para mensagens de erro, `aria-invalid` nos campos e rótulos `aria` nos controles.
- Alvos de toque de 44px e suporte a modo escuro.

## 🛡 Segurança

- **Content-Security-Policy** via `<meta>`.
- Campo **honeypot** anti-spam (descartado pelo Formspree).
- Trava de **um envio por sessão** para evitar duplicidade.
- A tela de "obrigado" só aparece quando o envio é confirmado com sucesso.

## 🎨 Marca

Marinho `#0B2D4D` · Turquesa `#2DE2C5` · Âmbar `#FFB84D`.

---

© 2026 Elloqio — projeto em validação. Uso pessoal; sem licença aberta definida.
