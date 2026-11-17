# Check-in de Energéticos

Landing page simples para registrar o consumo semanal de energéticos. Sem login, sem servidor, sem build. Um único arquivo `index.html`.

## O que foi feito

- Cadastro de usuário com nome e data de nascimento (sem senha)
- Registro de energéticos com marca, tamanho (ml), quantidade e dia da semana
- Opção "Outra..." para marcas que não estão na lista
- Resumo da semana: total de latas, volume em litros, marca mais tomada e dia mais pesado
- Gráfico de barras por dia da semana
- Navegação entre semanas (segunda a domingo) para ver o histórico
- Remoção de registros individuais e botão para apagar todos os dados
- Aviso para menores de 18 anos
- Layout responsivo (mobile first, ajusta a partir de 640px)
- Dark mode: segue o sistema e tem botão para alternar, a escolha fica salva
- Interface toda em português do Brasil (`lang="pt-BR"`)

## Como usar

1. Abra o `index.html` no navegador.
2. Informe nome e data de nascimento.
3. Adicione os energéticos escolhendo marca, tamanho, quantidade e dia.
4. Use as setas no topo para navegar entre as semanas.

## Como os dados são guardados

Tudo fica no `localStorage` do navegador, na chave `checkin-energeticos-v1`. Nada é enviado para fora do aparelho.

```json
{
  "user": { "nome": "Vih", "nasc": "1999-01-31" },
  "entries": [
    { "id": 1731800000000, "week": "2026-11-16", "dia": 0, "marca": "Monster", "ml": 473, "qtd": 2 }
  ]
}
```

- `week`: data da segunda-feira da semana (YYYY-MM-DD)
- `dia`: 0 = segunda, 6 = domingo

Limitações: os dados não sincronizam entre aparelhos, e limpar os dados do navegador apaga tudo.

## O que falta validar

O código ainda não foi testado em navegador. Antes de publicar, confira:

**Funcional**
- [ ] Cadastro bloqueia campos vazios e data de nascimento no futuro
- [ ] Adicionar, remover e recarregar a página mantém os registros
- [ ] "Outra..." exige o nome da marca
- [ ] Navegar entre semanas mostra só os registros de cada semana
- [ ] Virada de semana e de mês/ano (ex.: segunda 28/12 até domingo 03/01)
- [ ] Cálculo de idade perto do aniversário (aviso de menor de 18)
- [ ] "Apagar meus dados" limpa tudo e volta para a tela inicial

**Visual**
- [ ] Layout em 360px, 390px, tablet e desktop
- [ ] Dark mode no sistema claro e no escuro, e o botão de alternar
- [ ] Gráfico com todos os dias zerados e com um dia muito acima dos outros
- [ ] Nomes de marca longos não quebram o layout

**Navegadores**
- [ ] Chrome, Safari (iOS), Firefox
- [ ] Campo de data no Safari e no Firefox
- [ ] Modo anônimo (o `localStorage` pode ser limitado)

**Acessibilidade**
- [ ] Navegação só por teclado
- [ ] Leitor de tela nos botões "Remover" e nas setas de semana
- [ ] Contraste das cores nos dois temas

**Segurança**
- [ ] Marca personalizada com HTML (`<b>teste</b>`) aparece como texto puro

## Ideias para depois

- Meta semanal (contador coletivo, como no grupo "Mil Monsters")
- Estimativa de cafeína por lata
- Exportar e importar dados em CSV ou JSON
- Instalar como PWA e funcionar offline
- Vários usuários no mesmo aparelho

## Licença

Defina antes de publicar.
