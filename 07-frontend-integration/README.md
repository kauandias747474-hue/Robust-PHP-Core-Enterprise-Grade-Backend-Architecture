# 📁 07-frontend-integration-layer

## 📖 Descrição / Description

**PT-BR:** Esta camada é a ponte entre a lógica do servidor (PHP) e a interface do usuário (Browser). Ela é responsável por transformar os dados processados pelo sistema em uma resposta que o cliente entenda, seja ela um JSON estruturado para uma API ou um HTML renderizado via Template Engine.
**EN-US:** This layer is the bridge between server logic (PHP) and the user interface (Browser). It is responsible for transforming the data processed by the system into a response the client understands, whether it is a structured JSON for an API or an HTML rendered via a Template Engine.

---

## 🛠️ Funcionalidades / Features

### 1. Response Factory
**PT-BR:** Centraliza a criação de respostas. Garante que todos os JSONs tenham o mesmo formato (ex: `status`, `data`, `errors`) e define os headers HTTP corretos.
**EN-US:** Centralizes response creation. Ensures all JSONs have the same format (e.g., `status`, `data`, `errors`) and sets the correct HTTP headers.

### 2. Asset Manager (Gestão de Ativos)
**PT-BR:** Um facilitador para gerenciar caminhos de arquivos CSS, JavaScript e imagens, evitando caminhos quebrados ao mudar o projeto de servidor.
**EN-US:** A helper to manage CSS, JavaScript, and image file paths, preventing broken links when moving the project between servers.

### 3. Simple Template Engine
**PT-BR:** Sistema de renderização de views que separa o HTML do código PHP e garante o "escape" de dados para evitar ataques de XSS (Cross-Site Scripting).
**EN-US:** View rendering system that separates HTML from PHP code and ensures data "escaping" to prevent XSS (Cross-Site Scripting) attacks.

---

## 📂 Estrutura de Pastas / Directory Structure



* **`Presenters/`**: 
    * **PT-BR:** Classes que formatam dados especificamente para a visualização (ex: `UserPresenter.php`).
    * **EN-US:** Classes that format data specifically for display (e.g., `UserPresenter.php`).
* **`Responses/`**: 
    * **PT-BR:** Ex: `JsonResponse.php`. Padroniza o retorno das APIs.
    * **EN-US:** E.g., `JsonResponse.php`. Standardizes API returns.
* **`Views/`**: 
    * **PT-BR:** Arquivos de template (HTML/PHP) que definem o layout do sistema.
    * **EN-US:** Template files (HTML/PHP) defining the system layout.

---

## 🚀 Por que essa camada é importante? / Why is this layer important?

* **Segurança:** Ao centralizar a saída de dados, garantimos que qualquer texto enviado ao HTML seja limpo contra scripts maliciosos.
* **Consistência de API:** O front-end sempre receberá a mesma estrutura de resposta, facilitando o desenvolvimento de SPAs (Vue, React).
* **Organização:** Impede que códigos `echo` ou tags HTML fiquem espalhados dentro de Controllers ou Regras de Negócio.

---

## 🧪 Como Testar / How to Test

**PT-BR:** O teste aqui consiste em verificar o "Output". Chame uma rota e verifique se o JSON retornado possui a chave `status: success`. No HTML, verifique se as variáveis PHP foram renderizadas corretamente nos lugares certos.
**EN-US:** Testing here consists of checking the "Output". Call a route and verify if the returned JSON has the `status: success` key. In HTML, verify if the PHP variables were correctly rendered in the right places.
