# 🛡️ Security & Cryptography Module

Este módulo é o escudo do sistema. Ele implementa padrões de segurança proativa (Deny-by-Default).

### 🛠️ Funcionalidades:
- **AES-256-GCM Wrapper:** Criptografia autenticada para dados sensíveis.
- **Input Sanitization:** Filtros contra XSS e injeção de caracteres maliciosos.
- **CSRF Protection:** Gerenciamento de tokens para validar requisições de formulários.
- **Password Hashing:** Implementação segura usando `password_hash()` com Argon2ID ou Bcrypt.

> **Pilar:** Integridade e Confidencialidade.
> 
