# 📱 QR Code Generator Service

![Java](https://img.shields.io/badge/Java-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.2-green)
![AWS S3](https://img.shields.io/badge/AWS-S3-yellow)
![Docker](https://img.shields.io/badge/Docker-Enabled-blue)

## 📖 Sobre o Projeto

Este projeto é uma **API RESTful** desenvolvida para gerar **QR Codes** dinamicamente e armazená-los na nuvem. 

A aplicação recebe dados (URL ou texto), customizações de cor e tamanho, gera a imagem utilizando a biblioteca **ZXing**, faz o upload automático para um bucket no **Amazon S3** e retorna a URL pública da imagem gerada.

### 🚀 Tecnologias Utilizadas

* **Java 21** (Modern features)
* **Spring Boot 3** (Web, DevTools)
* **Google ZXing** (Geração e processamento de imagens)
* **AWS SDK v2** (Integração com Amazon S3)
* **Docker** (Containerização da aplicação)
* **Maven** (Gerenciamento de dependências)


⚙️ Arquitetura e Funcionalidades

O sistema segue uma arquitetura limpa, separando responsabilidades entre Controllers, Services e Adapters para AWS.

* ✅ Geração de QR Codes em formato PNG.
* ✅ Customização de cores (Foreground/Background).
* ✅ Definição de tamanho (pixels).
* ✅ Armazenamento seguro e escalável no AWS S3.

## 📷 Demonstração

![Demonstração](.github/images/demo-qrcode.gif)

🛠️ Como Executar o Projeto

### Pré-requisitos
* Java 21 instalado
* Maven instalado
* Docker (Opcional)
* Conta na AWS com um Bucket S3 criado e credenciais de acesso (Access Key e Secret Key).

### 1. Configuração de Variáveis de Ambiente

Por segurança, as credenciais da AWS não ficam no código. Crie as variáveis de ambiente no seu sistema ou passe via IDE/Docker:

| Variável | Descrição | Exemplo |
| --- | --- | --- |
| `AWS_ACCESS_KEY_ID` | Sua chave de acesso AWS | "AKIA..." |
| `AWS_SECRET_ACCESS_KEY` | Sua senha secreta AWS | "wJalr..." |
| `AWS_REGION` | Região do seu Bucket | "us-east-1" |

### 2. Rodando Localmente (IntelliJ/Terminal)

1. Clone o repositório:
   bash
   git clone [https://github.com/SEU-USUARIO/qrcode-generator.git](https://github.com/SEU-USUARIO/qrcode-generator.git)
