# 🛒 Mini E-commerce (Arquitetura MVC & PHP Orientado a Objetos)

Este projeto consiste no desenvolvimento de um mini e-commerce estruturado do zero utilizando **PHP Nativo**, focado em boas práticas de desenvolvimento, separação de responsabilidades e conceitos sólidos de Engenharia de Software.

O objetivo foi construir uma aplicação web dinâmica, segura e escalável, aplicando padrões de projeto utilizados no mercado.

---

## 🏗️ Arquitetura e Conceitos Aplicados

### 📂 Padrão MVC (Model-View-Controller)
A aplicação foi dividida em camadas para separar a lógica de negócios da interface visual:
* **View:** Responsável pela interface do usuário (HTML5, CSS3, JavaScript). Utiliza um sistema de *templates* para renderização de conteúdo dinâmico.
* **Model:** Camada de persistência e regras de acesso ao banco de dados (Comandos SQL, conexões e segurança).
* **Controller:** A ponte lógica que recebe as requisições do usuário, processa as regras de negócio junto ao Model e entrega os dados formatados para a View.

### 🛡️ Namespaces & Autoload (Composer)
Para evitar colisão de nomes de classes e organizar a estrutura, o projeto utiliza **Namespaces** mapeados pelo **Autoload do Composer (PSR-4)**. Isso elimina a necessidade de `include` e `require` manuais, tornando o código limpo e moderno.

---

## ⚙️ Funcionamento e Fluxo da Aplicação

* **`index.php` (Front Controller):** Ponto de entrada único da aplicação. Inicializa o Autoload, configurações de ambiente e centraliza as respostas das requisições.
* **`routes.php`:** Centralizador de rotas. Identifica a página solicitada via parâmetros na URL e instancia o respectivo Controlador.
* **`config.php`:** Centralização de variáveis de ambiente e credenciais de conexão com o banco de dados utilizando variáveis globais (`$_ENV`).

### 📁 Estrutura Base (`/app`)

O projeto utiliza o conceito de Herança (`extends`) para reaproveitamento de código e padronização:

* **`ViewPadrao.php`:** Motor de renderização que lê arquivos estáticos `.html` e substitui marcadores dinâmicos (ex: `{{exemplo}}`) por dados processados no Controller.
* **`ModelPadrao.php`:** Abstração de conexão com o Banco de Dados e padronização de operações CRUD (Select, Insert, Update, Delete).
* **`ControllerPadrao.php`:** Orquestrador de ações (Actions) baseado em parâmetros de requisição.

---

## 🚀 Tecnologias Utilizadas
* **Back-end:** PHP 8+ (Programação Orientada a Objetos)
* **Gerenciador de Dependências:** Composer
* **Front-end:** HTML5, CSS3, JavaScript
* **Banco de Dados:** MySQL / PostgreSQL

---
*Este projeto demonstra o domínio de arquitetura de software web tradicional, manipulação de rotas dinâmicas e estruturação de projetos PHP sem dependência de grandes frameworks monolíticos.*
