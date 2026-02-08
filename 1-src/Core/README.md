# 🧠 Core System Logic

**PT-BR:** O coração da aplicação. Esta camada é responsável pelo ciclo de vida da requisição, orquestração do Kernel e regras de negócio puras.
**EN-US:** The heart of the application. This layer is responsible for the request lifecycle, Kernel orchestration, and pure business rules.

---

## 🛠️ Componentes de Engenharia / Engineering Components

1. **Dependency Injection Container:** Gestão de instâncias e inversão de controle (PSR-11).
2. **Event Dispatcher:** Desacoplamento de processos via eventos determinísticos.
3. **Command Bus:** Separação entre intenção de ação (Command) e execução (Handler).
4. **Strict Entity Hydrator:** Transformação de inputs brutos em objetos de domínio tipados.
5. **Response Factory:** Padronização rigorosa de saídas (JSON/HTML) e HTTP status codes.

> **Design Note:** Esta camada é agnóstica a drivers externos. Toda lógica aqui é determinística.
