# 📁 06-infrastructure-services

## 📖 Descrição / Description

**PT-BR:** Este módulo é responsável pela integração com serviços de suporte e o mundo externo. Ele implementa as capacidades técnicas do sistema que não envolvem a regra de negócio principal, como envio de mensagens, armazenamento de arquivos e auditoria (logs).
**EN-US:** This module is responsible for integrating support services and the outside world. It implements the system's technical capabilities that do not involve core business rules, such as messaging, file storage, and auditing (logs).

---

## 🛠️ Funcionalidades / Features

### 1. Logger (Registro de Eventos)
**PT-BR:** Centraliza o registro de erros e atividades do sistema. Pode ser configurado para gravar em arquivos locais ou enviar para serviços de monitoramento na nuvem.
**EN-US:** Centralizes the recording of system errors and activities. It can be configured to write to local files or send to cloud monitoring services.

### 2. Mailer (Serviço de E-mail)
**PT-BR:** Interface para envio de e-mails transacionais (boas-vindas, recuperação de senha). Abstrai o uso de bibliotecas como PHPMailer ou APIs como SendGrid.
**EN-US:** Interface for sending transactional emails (welcome, password recovery). Abstraction for using libraries like PHPMailer or APIs like SendGrid.

### 3. File Storage (Armazenamento)
**PT-BR:** Abstração para manipulação de arquivos. Permite trocar facilmente o armazenamento entre o disco local (Local Storage) e serviços de nuvem (como AWS S3).
**EN-US:** Abstraction for file manipulation. Allows easy switching between local disk storage and cloud services (like AWS S3).

---

## 📂 Estrutura de Pastas / Directory Structure



* **`Logging/`**: 
    * **PT-BR:** Ex: `SystemLogger.php`. Implementa a gravação de logs em arquivos `.log`.
    * **EN-US:** E.g., `SystemLogger.php`. Implements logging to `.log` files.
* **`Messaging/`**: 
    * **PT-BR:** Ex: `SmtpMailer.php`. Lógica de conexão e envio de e-mail via SMTP.
    * **EN-US:** E.g., `SmtpMailer.php`. Connection logic and email sending via SMTP.
* **`Storage/`**: 
    * **PT-BR:** Ex: `LocalStorage.php`. Gerencia uploads e permissões de arquivos no servidor.
    * **EN-US:** E.g., `LocalStorage.php`. Manages file uploads and permissions on the server.

---

## 🚀 Por que isolar estes serviços? / Why isolate these services?

* **Substituibilidade:** Você pode mudar de um provedor de e-mail para outro alterando apenas uma classe nesta camada.
* **Segurança:** Centraliza a validação de uploads e a segurança de credenciais de APIs externas.
* **Organização:** Evita que classes de negócio fiquem "sujas" com detalhes técnicos de bibliotecas de terceiros.

---

## 🧪 Como Testar / How to Test

**PT-BR:** Para testar o Logger, execute uma ação e verifique se o arquivo na pasta `/logs` foi atualizado. Para o Mailer, utilize ferramentas como o Mailtrap para capturar o envio sem precisar de um e-mail real.
**EN-US:** To test the Logger, perform an action and check if the file in the `/logs` folder has been updated. For the Mailer, use tools like Mailtrap to capture the send without needing a real email.
