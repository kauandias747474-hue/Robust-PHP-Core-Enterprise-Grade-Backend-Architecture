# 📁 02-service-abstraction-and-di

## 📖 Descrição / Description

**PT-BR:** Esta camada é responsável pelo gerenciamento de dependências e inversão de controle (IoC). Em vez de instanciar classes manualmente em todo o projeto, utilizamos um **Service Container** que resolve e injeta as dependências necessárias. Isso garante que o sistema seja testável, flexível e siga o princípio da inversão de dependência (D do SOLID).

**EN-US:** This layer is responsible for dependency management and Inversion of Control (IoC). Instead of manually instantiating classes throughout the project, we use a **Service Container** that resolves and injects the required dependencies. This ensures the system is testable, flexible, and follows the Dependency Inversion Principle (D in SOLID).

---

## 🛠️ Componentes Principais / Key Components

### 1. Service Container
**PT-BR:** O coração da pasta. Um objeto central que armazena a "receita" de como criar cada serviço da aplicação. Permite o uso de **Singletons** para economizar memória.
**EN-US:** The heart of the folder. A central object that stores the "recipe" on how to create each application service. It allows the use of **Singletons** to save memory.

### 2. Dependency Injection (DI)
**PT-BR:** Mecanismo que entrega as instâncias necessárias para os construtores, eliminando o acoplamento rígido (*hard-coding*).
**EN-US:** Mechanism that delivers the required instances to constructors, eliminating hard-coded coupling.

### 3. Service Contracts (Interfaces)
**PT-BR:** Definição de interfaces que servem como "contratos". A lógica de negócio depende da interface, não da implementação real.
**EN-US:** Definition of interfaces that serve as "contracts". Business logic depends on the interface, not the actual implementation.

---

## 📂 Estrutura de Pastas / Directory Structure

**PT-BR:** A organização abaixo demonstra como separar a definição da execução:
**EN-US:** The organization below demonstrates how to separate definition from execution:

* **`contracts/`**: 
    * **PT-BR:** Contém as interfaces (ex: `ILogger.ts`). Define **o que** o serviço faz.
    * **EN-US:** Contains interfaces (e.g., `ILogger.ts`). Defines **what** the service does.
* **`implementations/`**: 
    * **PT-BR:** Contém as classes concretas (ex: `ConsoleLogger.ts`). Define **como** o serviço faz.
    * **EN-US:** Contains concrete classes (e.g., `ConsoleLogger.ts`). Defines **how** the service does it.
* **`container/`**: 
    * **PT-BR:** Onde reside a lógica do **Service Container**, mapeando contratos para suas implementações.
    * **EN-US:** Where the **Service Container** logic resides, mapping contracts to their implementations.

---

## 🚀 Benefícios de Engenharia / Engineering Benefits

* **Testabilidade / Testability:** * **PT-BR:** Facilita a substituição de serviços reais por "Mocks" em testes unitários.
    * **EN-US:** Facilitates replacing real services with "Mocks" during unit tests.
* **Desacoplamento / Decoupling:** * **PT-BR:** A lógica de negócio não precisa saber como os serviços de infraestrutura são criados.
    * **EN-US:** Business logic doesn't need to know how infrastructure services are created.
* **Manutenibilidade / Maintainability:** * **PT-BR:** Alterações na construção de objetos são feitas em um único lugar (no Container).
    * **EN-US:** Changes in object construction are made in a single place (in the Container).

---

## 🧪 Como Testar / How to Test

**PT-BR:** Para validar esta camada, você pode realizar dois testes conceituais:
**EN-US:** To validate this layer, you can perform two conceptual tests:

1.  **Troca Dinâmica (Hot Swap):** No arquivo do `container`, altere o registro de `EmailService` para `SmsService`. Se o sistema passar a enviar SMS sem alterar a lógica de negócio, a abstração está correta.
    *(In the container file, change the registration from EmailService to SmsService. If the system starts sending SMS without changing business logic, the abstraction is correct.)*

2.  **Verificação de Singleton:** Solicite a mesma instância do container duas vezes. Se ambas forem o mesmo objeto em memória, o gerenciamento de ciclo de vida está funcionando.
    *(Request the same instance from the container twice. If both are the same object in memory, lifecycle management is working.)*

---

> *Este módulo serve como a fundação para que as camadas superiores consumam recursos de infraestrutura sem criar dependências diretas.*
