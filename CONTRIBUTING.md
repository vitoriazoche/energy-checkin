# Como contribuir

Obrigada por querer ajudar! O projeto é um único `index.html`, então é fácil começar.

## Rodando localmente

1. Faça um fork e clone o repositório.
2. Abra o `index.html` no navegador. Não precisa de instalação nem de build.
3. Para testar o `localStorage` do zero, apague a chave `checkin-energeticos-v1` nas ferramentas do navegador.

## Fluxo

1. Crie uma branch a partir da `main`: `feat/nome-da-mudanca` ou `fix/nome-do-bug`.
2. Faça a mudança.
3. Abra um Pull Request explicando o que mudou e por quê. Se mexeu no visual, anexe um print do tema claro e do escuro.

## Commits

Use Conventional Commits:

- `feat: adiciona meta semanal`
- `fix: corrige cálculo da semana na virada do ano`
- `docs: atualiza checklist de validação`

## Regras do projeto

- Tudo em português do Brasil, incluindo textos da interface, commits e documentação.
- Sem dependências externas, sem frameworks e sem build.
- Sem login e sem enviar dados para servidor. O `localStorage` é o único armazenamento.
- Mantenha o layout responsivo e o dark mode funcionando.
- Todo texto digitado pelo usuário deve passar pela função `esc()` antes de entrar no HTML.

## Antes de abrir o PR

- [ ] Testei em tela pequena (360px) e em desktop
- [ ] Testei no tema claro e no escuro
- [ ] Recarreguei a página e os dados continuaram corretos
- [ ] Atualizei o README se a mudança alterou o comportamento

## Encontrou um bug?

Abra uma issue com o navegador e o aparelho usados, os passos para reproduzir e o que você esperava que acontecesse.
