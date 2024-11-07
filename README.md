# Reconhecimento de Comando de Voz com ESP-EYE e TensorFlow Lite

Este projeto implementa um sistema de reconhecimento de comando de voz para microcontroladores utilizando a biblioteca TensorFlow Lite para Microcontroladores. A aplicação está configurada para detectar palavras-chave específicas ("on" e "off") e responde com ações apropriadas.

## Visão Geral

Este código usa um modelo de aprendizado de máquina treinado para identificar comandos de voz específicos em tempo real, funcionando no ESP-EYE. O modelo foi treinado com o [Speech Commands Dataset](https://www.tensorflow.org/datasets/catalog/speech_commands), que contém gravações de áudio de várias palavras.

## Pré-requisitos

- **Placa ESP-EYE** com microfone embutido.
- **TensorFlow Lite para Microcontroladores**.
- **Google Colab** para treinamento do modelo (link para notebook abaixo).

## Estrutura do Código

- `main_functions.h` e `main_functions.cc`: Configurações principais para inicializar e executar o modelo de reconhecimento de voz no ESP-EYE.
- `audio_provider.h`: Fornece amostras de áudio do microfone para processamento.
- `command_responder.h`: Função personalizada para responder aos comandos detectados.
- `model.cc`: Contém o modelo treinado em formato TFLite.
- `micro_model_settings.h`: Define as palavras-chave que o modelo deve reconhecer.

## Como Treinar o Modelo

Para treinar o modelo com novas palavras-chave ou ajustar as configurações, acesse o [notebook de treinamento no Google Colab](https://colab.research.google.com/drive/11Lquu1coeWABdEYawaOWI_9TYlaYlP_M?usp=sharing). O notebook contém instruções para treinar um modelo com as palavras "on" e "off".

## Como Usar

1. Grave o modelo treinado na memória da ESP-EYE.
2. Execute o código na placa e abra o monitor serial.
3. O sistema detectará comandos de voz e responderá exibindo "LIGAR" ou "DESLIGAR" com base nos comandos reconhecidos.

## Licença

Este projeto está licenciado sob a Licença MIT

 

