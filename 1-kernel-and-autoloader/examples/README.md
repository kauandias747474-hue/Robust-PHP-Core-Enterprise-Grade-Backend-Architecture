# 🚀 Kernel Examples | Exemplos do Kernel

[English](#english) | [Português](#portugues)

---

<a name="english"></a>
## 🇺🇸 English: Core Implementation
This directory contains the integration tests for the three main pillars of the architecture.

### 🛠️ Components:
- **Config Echo (49 lines):** Environment variable injector.
- **Security Error (39 lines):** Global exception shield.
- **Autoloader (120 lines):** PSR-4 compliant dependency resolution.

### 🖥️ How to Run:
1. Ensure your `.env` is configured.
2. Run `php bootstrap.php` to see the kernel initialization.
3. Check the `storage/logs/` for any intercepted exceptions.

---

<a name="portugues"></a>
## 🇧🇷 Português: Implementação do Core
Este diretório contém os testes de integração para os três pilares principais da arquitetura.

### 🛠️ Componentes:
- **Config Echo (49 linhas):** Injetor de variáveis de ambiente.
- **Security Error (39 linhas):** Escudo global de exceções.
- **Autoloader (120 linhas):** Resolução de dependências compatível com PSR-4.

### 🖥️ Como Executar:
1. Certifique-se de que seu `.env` está configurado.
2. Execute `php bootstrap.php` para ver a inicialização do kernel.
3. Verifique a pasta `storage/logs/` para ver exceções interceptadas.

4. 
---

### 🔧 Framework Compatibility | Compatibilidade de Frameworks

My **Vanilla Core** is designed to be the "Engine Under the Hood." It provides the low-level infrastructure that can power or integrate with:

- **Laravel / Symfony:** Since the Autoloader (120 lines) follows PSR-4, it can manage custom local packages outside of `vendor/`.
- **Slim Framework / Micro-services:** Perfect for ultra-lightweight APIs where you need the **Security Shield (39 lines)** but don't want the overhead of a full framework.
- **Legacy Systems (PHP 8.0+):** The **Config Echo (49 lines)** can be dropped into older projects to modernize environment variable management without breaking existing logic.

---

### 🇧🇷 Em Português:

Meu **Vanilla Core** foi desenhado para ser o "Motor sob o Capô". Ele fornece a infraestrutura de baixo nível que pode alimentar ou se integrar com:

- **Laravel / Symfony:** Como o Autoloader (120 linhas) segue a PSR-4, ele pode gerenciar pacotes locais customizados fora da pasta `vendor/`.
- **Slim Framework / Micro-serviços:** Perfeito para APIs ultra-leves onde você precisa do **Escudo de Segurança (39 linhas)** mas não quer o peso de um framework completo.
- **Sistemas Legados (PHP 8.0+):** O **Config Echo (49 linhas)** pode ser inserido em projetos antigos para modernizar a gestão de variáveis de ambiente sem quebrar a lógica existente.
