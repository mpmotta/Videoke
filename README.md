# 🎤 Videoke Player Web (Pro Operator)

Um sistema de Karaokê baseado em navegador (HTML/CSS/JS) desenvolvido para rodar offline em PCs ou TV Boxes. O sistema conta com uma interface de **Operador Profissional**, permitindo gerenciamento de fila de espera, pontuação automática e controle manual de reprodução.

![Status do Projeto](https://img.shields.io/badge/Status-Finalizado-green)
![Tech](https://img.shields.io/badge/Tech-HTML5%20%7C%20jQuery%20%7C%20Bootstrap-blue)

## ✨ Funcionalidades

* **Dual Resolution:** Suporte nativo para telas 1080p e 720p (HD/Full HD).
* **Fila de Espera (Queue):** Sidebar lateral que mostra as próximas músicas.
* **Modo Operador:** O sistema carrega a próxima música e aguarda o comando do operador para tocar (evita que a música comece enquanto o cantor ainda está subindo no palco).
* **Sistema de Pontuação (Nota):** Ao final da música, uma tela de "Nota" é exibida com animação e comentários baseados na pontuação (randomizada).
* **Automação:**
    1.  Toca a música.
    2.  Exibe nota por 10 segundos.
    3.  Carrega a próxima da fila automaticamente (em *Pause*).
* **Teclado Virtual:** Interface para digitar códigos usando mouse ou touch.
* **Botão Pânico (Parar):** Interrompe a música atual e prepara a próxima da fila imediatamente.

## 📂 Estrutura de Arquivos

Para o sistema funcionar, os arquivos devem estar organizados desta maneira:

```
/
├── index.html          # Splash Screen (Seletor de Resolução)
├── index1080.html      # Player Principal (Full HD)
├── index720.html       # Player Versão Leve (HD)
├── nota1080.html       # Tela de Pontuação
├── lista.js            # Banco de dados das músicas (JSON Object)
│
├── css/                # Estilos (Bootstrap + Custom)
├── js/                 # Scripts (jQuery, Bootstrap, MaskedInput)
│
├── img/
│   ├── wallpaper.jpg   # Fundo padrão
│   ├── wallpaperQR.jpg # Fundo de espera (QR Code ou Logo)
│   └── 00001.jpg       # Capa da música (Mesmo nome do código)
│
├── music/
│   └── NOME_DA_MUSICA.mp4  # Arquivo de vídeo
│
└── audio/
    └── intro.mp3       # Som de abertura da nota
````

## 🚀 Como Usar

1.  Abra o arquivo `index.html` no seu navegador.
2.  Escolha a resolução (**720P** ou **1080P**).
3.  **Para Tocar:**
      * Digite o código da música no teclado virtual ou físico.
      * Clique em **BUSCAR** para confirmar o nome.
      * Clique em **ADD FILA +** para colocar na lista de espera.
      * Clique em **▶ PLAY FILA** para iniciar a festa.
4.  **Fluxo Automático:**
      * Quando a música acaba, a nota aparece.
      * Após 10 segundos, a tela volta para o Player com a próxima música carregada (capa na tela).
      * O operador clica em **▶ PLAY FILA** novamente quando o cantor estiver pronto.

## 🎵 Como Adicionar Músicas

O sistema funciona vinculando um **CÓDIGO** a um **ARQUIVO DE VÍDEO**.

### 1\. Prepare os Arquivos

  * Coloque o vídeo `.mp4` na pasta `music/`. (o arquivo deve ter o nome completo da múscia e o autor. ex: "Bohemian Rhapsody - Queen.mp4")
  * (Opcional) Coloque uma imagem `.jpg` com o **número do código** na pasta `img/` (Ex: `1500.jpg`).

### 2\. Edite o `lista.js`

Abra o arquivo `lista.js` e adicione a entrada no formato JSON:

var musicas = {
    "00001": "Evidencias - Chitaozinho e Xororo",
    "00002": "Anna Julia - Los Hermanos",
    "1500": "Bohemian Rhapsody - Queen"
};


> **Atenção:** O nome do arquivo na pasta `music/` deve ser **exatamente igual** ao valor escrito (sem a extensão .mp4).
>
>   * Código: `00001`
>   * No `lista.js`: `"Evidencias - Chitaozinho e Xororo"`
>   * Arquivo: `music/Evidencias - Chitaozinho e Xororo.mp4`

## 🛠 Tecnologias Utilizadas

  * **HTML5 & CSS3**: Estrutura e animações (Gradientes, Flexbox).
  * **JavaScript (ES5/ES6)**: Lógica do player, manipulação de DOM e Array de Playlist.
  * **jQuery**: Facilitação de seletores e eventos.
  * **Bootstrap 5**: Estilização base de botões e grid.

## 🤝 Contribuição

Sinta-se à vontade para fazer um fork deste projeto e enviar pull requests. Sugestões de melhorias no sistema de pontuação ou layout são bem-vindas\!

## 📝 Licença

Este projeto é de uso pessoal e educacional.


Isso vai fazer seu portfólio no GitHub ficar muito mais atraente!
