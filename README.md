# Neuro Bolha

PWA educativo de Neuroanatomia, responsivo, instalável e funcional offline.

## Imagens numeradas

- `assets/img/1.png`: neurônio azul
- `assets/img/2.png`: cérebro vermelho
- `assets/img/3.png`: medula espinal laranja
- `assets/img/4.png`: nervo dourado
- `assets/img/5.png`: monstro da Demência

Você pode substituir qualquer arquivo por outra imagem PNG, mantendo o mesmo nome. Recomenda-se imagem quadrada de 512 × 512 px.

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub.
2. Envie todo o conteúdo desta pasta, mantendo as subpastas.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main`, pasta `/ (root)` e clique em **Save**.

## Como testar no computador

O service worker exige servidor HTTP. Dentro da pasta, execute:

```bash
python -m http.server 8080
```

Depois abra `http://localhost:8080`.

## Sons

- `assets/audio/clique.wav`
- `assets/audio/bomba.wav`
- `assets/audio/vitoria.wav`

Para trocar um som, substitua o arquivo mantendo o mesmo nome.

## Acessibilidade e Libras

O botão **♿** oferece aumento e redução do texto, alto contraste, redução de
movimentos, leitura em voz alta e controles grandes com descrições para leitores
de tela.

O botão **LIBRAS** abre a área sinalizada. Para incluir uma gravação feita por
intérprete, crie a pasta `assets/video` e coloque nela o arquivo `libras.mp4`.
Quando houver internet, o PWA também disponibiliza o tradutor VLibras. A
tradução automática é um recurso de apoio e não substitui intérprete humano em
atividades educacionais.

## GIFs do jogo

- `assets/video/abertura.mp4`: vídeo exibido antes de iniciar a partida;
- `assets/video/abertura-poster.jpg`: capa mostrada enquanto a abertura carrega;
- `assets/video/vitoria.mp4`: vídeo exibido ao vencer cada fase;
- `assets/video/vitoria-poster.jpg`: capa mostrada enquanto o vídeo carrega.

É possível substituir os vídeos mantendo exatamente esses nomes. A derrota
exibe a tela **GAME OVER**, a pontuação final e o botão **JOGAR NOVAMENTE**.

O tabuleiro possui onze linhas e começa com uma grande área vazia entre as
bolhas e o lançador. A linha tracejada avermelhada indica o limite de derrota.

O lançamento usa velocidade de 900 pixels por segundo, calculada pelo tempo
real entre quadros. Assim, permanece rápido e uniforme mesmo em celulares com
taxas de atualização diferentes.
