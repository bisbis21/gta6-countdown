# GTA VI — Contagem Regressiva Global

Página estática para usar como Browser Source no OBS/Streamlabs.

## Arquivos
- `index.html`: aplicação completa; não exige instalação, banco de dados ou servidor.
- Layout horizontal: `index.html?layout=horizontal`
- Layout vertical: `index.html?layout=vertical`

## Publicar gratuitamente no GitHub Pages
1. Entre em https://github.com e crie um repositório público, por exemplo `gta6-countdown`.
2. Envie o arquivo `index.html` para a raiz do repositório.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione `main` e `/ (root)`, depois **Save**.
6. Aguarde a publicação. O endereço ficará parecido com `https://SEU-USUARIO.github.io/gta6-countdown/`.

Use no Streamlabs/OBS como fonte de navegador:
- Horizontal: `https://SEU-USUARIO.github.io/gta6-countdown/?layout=horizontal`
- Vertical: `https://SEU-USUARIO.github.io/gta6-countdown/?layout=vertical`

Sugestão de dimensões:
- Horizontal: 1920 × 1080
- Vertical: 1080 × 1920

## Como funciona
- O relógio é calculado com `Date.now()` e fuso IANA via `Intl.DateTimeFormat`.
- A referência principal é 19/11/2026 às 00:00 no fuso `America/Sao_Paulo`.
- Os relógios regionais usam 00:00 de 19/11/2026 em cada fuso local.
- **Atenção:** a Rockstar confirma a data de 19/11/2026, mas não necessariamente a hora de desbloqueio de cada região. Os horários regionais desta página são referências estimadas para apresentação, não horários oficiais confirmados.
- As perguntas são embaralhadas e mudam a cada 90 segundos. Não há repetição até esgotar o ciclo.

## Ajustes rápidos
No fim do arquivo, procure `const questions = [...]` para editar as perguntas.
Procure `const RELEASE_DATE` para alterar a data.
Procure `setInterval(nextQuestion, 90000)` para alterar o intervalo (90.000 ms = 90 segundos).

## Observações
- A página é independente: não usa API, login, banco de dados, fontes externas ou imagens externas.
- O modo vertical é a mesma página com composição responsiva específica.
- A página não controla o OBS. A troca para a captura HDMI será feita pela mudança de cena/fonte no OBS ou Streamlabs.
- Projeto de fã, sem afiliação ou endosso da Rockstar Games.
