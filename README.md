# Blind-Helper

## Introdução
O Blind-Helper é um chatbot que utiliza o Gemini IA, esse projeto tem o objetivo de ajudar os deficientes visuais que possuem dificuldade em conseguir entender as imagens. O Blind-Helper indentifica quais objetos, pessoas e etc, que compõem a imagem, assim descrevendo para a pessoa.

<div align="center">
  <img alt="[Logo Blind Helper" src="https://github.com/rafaelnator/Blind-Helper/blob/main/Imagem-README/Blind_Helper.png" heght="50px"/>
</div>

## Instalação

1. **Instale as dependências:**

   ```bash
   !pip install -q -U google-generativeai
   ```

## Bibliotecas Utilizadas

O Blind Helper utiliza as seguintes bibliotecas:

* `google.generativeai`: Usada para interagir com a API do Google GenerativeAI.
* `os`: Usada para apagar a imagem após a execução.
* `google.colab import files`: Usada para baixar a imagem para o Google Colab.
* `google.colab import userdata`: Usada para codificação e decodificação de dados binários.

## Funções do Código

* **`files.upload()`:** Fazer upload para o computador do Google Colab.
* **`next(iter(uploaded))`:** Para indentificar o nome da imagem.
* **`genai.upload_file(picture)`:** Envia a imagem para o modelo Gemini IA e retorna a resposta do modelo com um texto.
* **`os.remove(picture)`:** remover a imagem após a execução.

## Configuração da API

1. **Crie uma conta do Google Cloud** ([https://cloud.google.com/](https://cloud.google.com/)) e habilite a Key API do Generative AI.
2. **Obtenha a sua chave de API** e armazene-a com segurança usando `google.colab.userdata.set('api_key', 'sua-chave-api')`.
Obs.: Documentação da API em: https://ai.google.dev/gemini-api/docs/system-instructions?hl=pt-br

## Configuração do Modelo

* **`generation_config`:** Define o número de candidatos de resposta (1) e a temperatura (0.5).
* **`safety_settings`:** Define o nível de bloqueio para BLOCK_ONLY_HIGH (Block some, ou seja, ).
* **`model`:** Inicializa o modelo Gemini-1.5-pro-latest com a configuração de geração e os ajustes de segurança.

## Loop do Chat

O código implementa um loop que permite a conversação com o Jarvis. O loop funciona da seguinte maneira:

1. O usuário grava um áudio.
2. O áudio gravado é enviado para o modelo Gemini.
3. O modelo retorna uma resposta textual.
4. A resposta textual é convertida em fala e reproduzida para o usuário.
5. O loop continua até que o usuário diga "fim".

## Executando o Código

1. **Faça upload do código para o Colab** ([https://colab.research.google.com/notebook](https://colab.research.google.com/notebook)).
2. **Substitua `'SUA-CHAVE-API'`** pela sua chave de API real em `api_key = userdata.get('SUA-CHAVE-API')`.
3. **Execute o código** pressionando `Shift + Enter`.
3. **Função deseja** Escolher qual função irá realizar se é a de Descrever uma Imagem ou sair do programa.
4. **Clique no botão "`Escolher Aqruivo`"** para enviar sua imagem e aguarde a resposta.
5. O Blind Helper irá descrever todos os detalhes à sua imagem.

## Exemplo
A um exemplo de como executar o programa logo a baixo terá a imagem que foi utilizada para o test

<div align="center">
  <img alt="[Imagem de exemplo" src="https://github.com/rafaelnator/Blind_Helper/blob/main/Imagem-README/michael_jordan.png" heght="50px"/>
</div>

## Licença

GNU General Public License v3.0
