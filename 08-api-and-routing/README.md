# 📁 08-api-routing-engine

## 📖 Descrição / Description

**PT-BR:** Esta camada é o controlador de tráfego do sistema. Ela interpreta as requisições HTTP que chegam ao servidor e as direciona (despacha) para o Controller adequado. É aqui que definimos a estrutura das URLs e as regras de segurança iniciais (Middlewares).
**EN-US:** This layer is the system's traffic controller. It interprets incoming HTTP requests and directs (dispatches) them to the appropriate Controller. This is where we define URL structures and initial security rules (Middlewares).

---

## 🛠️ Funcionalidades / Features

### 1. Request Matcher (Mapeamento)
**PT-BR:** Analisa a URI e o método HTTP (GET, POST, etc.) para encontrar a rota correspondente.
**EN-US:** Analyzes the URI and HTTP method (GET, POST, etc.) to find the corresponding route.

### 2. Middlewares (Filtros)
**PT-BR:** Camadas de inspeção que executam antes da lógica principal. Úteis para verificação de autenticação (Auth Check), logs de acesso e manutenção.
**EN-US:** Inspection layers that run before the main logic. Useful for authentication checks, access logs, and maintenance mode.

### 3. RESTful Standards
**PT-BR:** Suporte completo aos verbos HTTP, garantindo que a API siga os padrões da indústria para arquiteturas REST.
**EN-US:** Full support for HTTP verbs, ensuring the API follows industry standards for REST architectures.

---

## 📂 Estrutura de Pastas / Directory Structure



* **`Router/`**: 
    * **PT-BR:** O motor principal que registra e resolve as rotas.
    * **EN-US:** The core engine that registers and resolves routes.
* **`Middlewares/`**: 
    * **PT-BR:** Filtros de requisição (ex: `AuthMiddleware.php`, `GuestMiddleware.php`).
    * **EN-US:** Request filters (e.g., `AuthMiddleware.php`, `GuestMiddleware.php`).
* **`Collections/`**: 
    * **PT-BR:** Grupos de rotas organizados por versão ou contexto (ex: `ApiRoutes.php`).
    * **EN-US:** Route groups organized by version or context (e.g., `ApiRoutes.php`).

---

## 🚀 Por que usar um Routing Engine? / Why use a Routing Engine?

* **Desacoplamento:** O seu código não depende da estrutura de pastas do servidor; você define URLs amigáveis livremente.
* **Segurança Centralizada:** Você pode proteger centenas de rotas com uma única linha de código usando um Middleware.
* **Padronização:** Garante que todos os métodos (PUT, DELETE, PATCH) sejam tratados corretamente, algo difícil de fazer com arquivos PHP soltos.

---

## 🧪 Como Testar / How to Test

**PT-BR:** Tente acessar uma rota protegida sem um token de acesso. Se o **Middleware** funcionar, você deve receber um erro `401 Unauthorized` antes mesmo de chegar ao Controller.
**EN-US:** Try accessing a protected route without an access token. If the **Middleware** works, you should receive a `401 Unauthorized` error before even reaching the Controller.
