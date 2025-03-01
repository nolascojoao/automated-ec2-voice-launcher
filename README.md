# Gerenciamento de EC2 Controlado por Voz 🤖


Automação em Python para gerenciamento de instâncias EC2 via comandos de voz.


Captura o áudio, transcreve com o AWS Transcribe e usa uma função AWS Lambda para interpretar e tomar decisões sobre criar ou terminar instâncias EC2 com base na transcrição.


---


### Colaboradores
- [João Nolasco](https://github.com/nolascojoao)
- [Danniel de Albuquerque](https://github.com/Danniel30)
- [Maria Clara Valotti](https://github.com/MariaClaravalotti)


---


### Como Funciona


1. **Gravar Áudio**: O script Python grava o áudio e o salva como um arquivo `.wav`.


2. **Enviar para o S3**: O arquivo de áudio é enviado para um bucket S3.


3. **Transcrição com AWS Transcribe**: O AWS Transcribe transcreve o áudio e armazena o resultado no mesmo bucket S3.


4. **Acionar Lambda**: O evento do S3 aciona uma função Lambda, que analisa a transcrição.


5. **Gerenciamento do EC2**: Com base nas palavras-chave da transcrição, a função Lambda cria ou termina instâncias EC2.


---


### Vídeo Demo


<p align="center">
  <a href="https://youtu.be/X7NFVisl2SQ">
    <img src="https://img.youtube.com/vi/X7NFVisl2SQ/0.jpg" alt="Assista ao vídeo" />
  </a>
</p>


---


### Guia para Execução do Projeto


Para um passo a passo de execução e configuração, confira o [Guia do Projeto](https://github.com/MariaClaravalotti/transcribe) ✅


---


### Roadmap de Melhorias


- **Transcrição em Tempo Real**: Integrar com o **Real-time transcription** do Amazon Transcribe para acelerar a conversão de áudio em texto, oferecendo respostas mais rápidas.
  

- **Automatizar com Terraform**: Utilizar Terraform para gerenciar a criação e remoção de instâncias EC2, agilizando a infraestrutura.


- **Integrar com IA Generativa**: Permitir interação em linguagem natural para personalizar comandos como tipo de instância, AMI, disco, etc.


- **Integração com Alexa**: Integrar o controle de instâncias EC2 por comandos de voz via Alexa para uma interface mais prática.
