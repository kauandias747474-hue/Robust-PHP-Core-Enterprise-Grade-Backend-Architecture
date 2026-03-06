# 📂 01 - Kernel & Autoloader (Core Engine)

Este repositório contém o **Core Engine** da aplicação, responsável por gerenciar o ciclo de vida inicial e preparar o ambiente para a execução da lógica de negócio. O foco principal é o controle total sobre o *bootstrapping* do sistema, garantindo performance e segurança desde o primeiro segundo de execução.

## 🎯 Objetivo
Gerenciar o ciclo de vida inicial da aplicação, garantindo que o ambiente esteja configurado, as classes sejam carregadas automaticamente e os erros sejam tratados de forma profissional.

## 🛠️ Responsabilidades Técnicas

* **Autoloading (PSR-4 Adaptado):** Implementação manual de carregamento automático de classes. Elimina a necessidade de múltiplos `require` ou `include`, mapeando namespaces para diretórios de forma eficiente e seguindo os padrões modernos da comunidade PHP.
* **Exception Handling (Security Shield):** Um capturador global de erros e exceções. Este componente impede que falhas críticas exponham dados sensíveis do servidor (como caminhos de diretórios, versões de software ou variáveis de ambiente) para o usuário final.
* **Environment Management:** Carregamento de variáveis de configuração via arquivos `.env`. Isso permite a separação estrita entre o código-fonte e as configurações de ambiente (Desenvolvimento vs. Produção), seguindo as boas práticas de *Twelve-Factor App*.

---

## 🚀 Demonstrações Práticas (PoC)

Para validar a robustez do motor, o diretório `/examples` contém scripts que testam cada pilar do Kernel de forma isolada:

1.  **`AutoLoaderTest.php`**: Valida a hierarquia de namespaces e a capacidade do motor de encontrar e instanciar classes em subdiretórios automaticamente.
2.  **`SecurityError.php`**: Demonstra o "Escudo de Segurança". Ao forçar um erro ou exceção, o Kernel intercepta a falha e exibe uma resposta tratada, ocultando detalhes técnicos que poderiam ser usados para exploração de vulnerabilidades.
3.  **`ConfigEcho.php`**: Prova que o Kernel conseguiu ler, processar e injetar as configurações do arquivo de ambiente no sistema de forma segura.

---

## 🏗️ Estrutura do Módulo

```text
├── /src                # Código-fonte do motor (Core)
│   ├── Kernel.php      # Maestro do ciclo de vida
│   ├── Autoloader.php  # Implementação do motor PSR-4
│   └── Handler.php     # Lógica de tratamento de exceções e erros
├── /examples           # Scripts de teste e validação (PoCs)
│   ├── AutoLoaderTest.php
│   ├── SecurityError.php
│   └── ConfigEcho.php
├── .env.example        # Modelo de variáveis de ambiente
└── README.md           # Documentação do módulo
