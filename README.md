# 🛡️ Hardened PHP Core: Secure Backend Engineering

> **"Security is not a feature; it is the fundamental state of digital matter."**
> *"Segurança não é um recurso; é o estado fundamental da matéria digital."*

![PHP](https://img.shields.io/badge/Language-PHP_8.x-777bb3?style=for-the-badge&logo=php)
![Security](https://img.shields.io/badge/Focus-Offensive_&_Defensive-red?style=for-the-badge)
![Compliance](https://img.shields.io/badge/Standard-OWASP_Top_10_Mitigation-blue?style=for-the-badge)
![Framework](https://img.shields.io/badge/Dependency-Zero_Framework-green?style=for-the-badge)

---

## 📖 Resumo / Overview

**PT-BR:** O `hardened-php-core` é uma implementação de referência para arquiteturas de backend onde a segurança é tratada como requisito primário. Este projeto foca na mitigação de vetores de ataque do **OWASP Top 10** diretamente no motor da aplicação, utilizando PHP puro para garantir controle total sobre o fluxo de dados.

**EN-US:** `hardened-php-core` is a reference implementation for backend architectures where security is a primary requirement. This project focuses on mitigating **OWASP Top 10** attack vectors directly at the application engine level, using Vanilla PHP to ensure total control over data flow.

---

## 🎯 Proposta de Valor / Value Proposition

### 🎓 Pesquisa & Academia (Academic Research)
Um estudo prático sobre a anatomia das vulnerabilidades web. Este repositório expõe como falhas de injeção ocorrem no nível do interpretador e demonstra técnicas de filtragem determinística.
*A practical study on web vulnerability anatomy, demonstrating deterministic filtering and Defense in Depth.*

### 💼 Portfólio de Engenharia (Recruiters)
A prova de um desenvolvedor que domina os fundamentos. Proteção de **sistemas legados** e aplicações críticas, reduzindo a dívida técnica de segurança em infraestruturas de alta confiabilidade.
*Proof of fundamental mastery. Securing legacy systems and critical apps, reducing technical debt in high-reliability infrastructures.*

### 🚀 Consultoria & Freelance (Business Focus)
Foco em **Continuidade de Negócio**. Transformo aplicações vulneráveis em fortalezas digitais, eliminando a dependência exclusiva de WAFs externos e blindando o código-fonte.
*Focus on Business Continuity. Transforming vulnerable apps into digital fortresses by shielding the source code directly.*

---

## 🛠️ Implementações de Blindagem / Hardening Features

| Feature | Technical Description (EN) | Descrição Técnica (PT) | Vector Mitigated |
| :--- | :--- | :--- | :--- |
| **SQLi Prevention** | Strict PDO Prepared Statements with strong typing. | Implementação rigorosa de Prepared Statements via PDO. | SQL Injection |
| **Session Hardening** | `HttpOnly`, `Secure`, `SameSite=Strict` & ID Regeneration. | Gestão de estado ultra-segura com regeneração de IDs. | Session Hijacking |
| **Input Sanitization** | Type-based Whitelisting (Mathematical conformity). | Filtros baseados em lógica de tipos (Whitelist-only). | XSS / RCE |
| **Active Defense** | Dynamic Security Headers (CSP, HSTS, XSS-Protection). | Injeção granular de cabeçalhos de segurança ativos. | Clickjacking / MITM |
| **Atomic Crypto** | AES-256-GCM wrapper for sensitive data at rest. | Wrapper AES-256-GCM para proteção de dados sensíveis. | Data Exposure |

---

## 📐 Metodologia "Vanilla Security" (Anti-Erro)

Para assegurar que nenhum erro de lógica comprometa a aplicação, adoto um fluxo de desenvolvimento rigoroso baseado em princípios matemáticos:

1.  **Zero-Framework Dependency:** Controle total. Sem vulnerabilidades ocultas em dependências de terceiros. (*Total control. No hidden vulnerabilities in 3rd party libs.*)
2.  **Mathematical Validation:** Se o dado não corresponde exatamente ao modelo matemático/tipo definido, ele é descartado (**Deny by Default**). (*If data doesn't match the math model, it's discarded.*)
3.  **Offensive Validation:** Cada defesa é validada contra scripts de ataque (PoCs) reais antes do commit. (*Every defense is validated against real exploit PoCs.*)

---

## 📂 Estrutura do Ecossistema / Project Structure

* 📁 **[`/core/security`](./core/security):**
    * `Sanitizer.php`: Engine de limpeza de inputs.
    * `Crypto.php`: Criptografia simétrica de alta performance.
    * `Guard.php`: Middleware de proteção de cabeçalhos.
* 📁 **[`/lab/exploits`](./lab/exploits):**
    * Laboratório de ataques controlados para demonstração de vulnerabilidades (PoC).
* 📁 **[`/docs/hardening-guide`](./docs/hardening-guide):**
    * Guia técnico de implementação para sistemas legados.

---

## ⚠️ Aviso de Ética / Ethical Warning

**PT-BR:** Este repositório foi criado para fins educacionais e fortalecimento de sistemas. O uso de técnicas ofensivas sem autorização é ilegal.
**EN-US:** This repository is for educational and defensive purposes. Using offensive techniques without authorization is illegal and unethical.

---

## 📩 Contato & Consultoria / Contact

**Precisa blindar seu sistema ou de uma auditoria de segurança?**
**Need to harden your system or a security audit?**

* 🛡️ **Bug Bounty Portfolio:** [HackerOne/Profile](#)
* 💼 **Freelance Inquiries:** [Consultancy/Email](#)
* 📊 **Mathematics & Logic:** *All core logic is validated via mathematical models.*

---
developed by Kauan Oliveira- 2026
