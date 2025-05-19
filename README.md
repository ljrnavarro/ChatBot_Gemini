# Exemplo de Uso da API Gemini no Colab

Este repositório contém um exemplo de como utilizar a API Gemini no Google Colab. O código demonstra como interagir com os modelos Gemini para gerar conteúdo e manter conversas.

## Pré-requisitos

Para rodar este código, você precisará:

*   Uma conta Google.
*   Um notebook Google Colab.
*   Uma chave de API para a API Gemini. Você pode obter uma em [Google AI Studio](https://aistudio.google.com/).

## Configuração

1.  **Abra no Google Colab:** Clique no botão "Open in Colab" acima (se houver um, caso contrário, copie e cole o código em um novo notebook).
2.  **Instale a biblioteca:** Rode a célula com `!pip install google-genai` para instalar a biblioteca necessária.
3.  **Configure sua chave de API:**
    *   Armazene sua chave de API como um segredo no Colab. Clique no ícone de chave (🔑) na barra lateral esquerda e adicione um novo segredo com o nome `GOOGLE_API_KEY` e o valor da sua chave de API.
    *   Rode a célula que carrega a chave de API dos segredos do Colab.
4.  **Inicialize o cliente:** Rode a célula que inicializa o cliente da API Gemini.

## Como Usar

O notebook demonstra várias formas de interagir com a API:

*   **Listar modelos disponíveis:** A primeira célula após a configuração lista os modelos Gemini disponíveis.
*   **Gerar conteúdo único:** A célula que utiliza `client.models.generate_content` mostra como obter uma resposta direta para uma pergunta.
*   **Iniciar e interagir com um chat:** As células subsequentes demonstram como criar um chat (`client.chats.create`) e enviar mensagens (`chat.send_message`) para manter uma conversa.
*   **Configurar o comportamento do chat:** A célula que utiliza `types.GenerateContentConfig` mostra como definir instruções para o sistema para influenciar o estilo e o conteúdo das respostas do modelo em um chat.
*   **Acessar o histórico do chat:** A célula que utiliza `chat.get_history()` demonstra como recuperar as interações passadas em um chat.
*   **Loop de interação com o usuário:** O loop `while prompt != "fim"` permite que você interaja continuamente com o modelo através do chat.
*   **Múltiplos chats com configurações diferentes:** A última parte do código mostra como criar um segundo chat com uma configuração de sistema diferente para obter respostas com um tom distinto (neste caso, sarcástico).

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes. (Se você não tiver um arquivo LICENSE, pode remover esta seção ou criar um).
