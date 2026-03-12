# 📁 09-quality-testing-suite

## 📖 Descrição / Description

**PT-BR:** Esta camada é a rede de segurança do projeto. Ela contém os testes automatizados que garantem que cada funcionalidade se comporte como esperado. Com esta suíte, podemos refatorar o código ou adicionar novos recursos com a confiança de que não quebramos o que já estava funcionando.
**EN-US:** This layer is the project's safety net. It contains automated tests that ensure each feature behaves as expected. With this suite, we can refactor code or add new features with the confidence that we haven't broken what was already working.

---

## 🛠️ Ferramentas de Qualidade / Quality Tools

### 1. Unit Tests (Testes Unitários)
**PT-BR:** Testam a menor unidade de código possível (funções ou métodos) de forma isolada. São extremamente rápidos e não tocam no banco de dados.
**EN-US:** They test the smallest possible unit of code (functions or methods) in isolation. They are extremely fast and do not touch the database.

### 2. Integration Tests (Testes de Integração)
**PT-BR:** Verificam se diferentes partes do sistema funcionam bem juntas (ex: se o Controller consegue salvar um dado no MySQL através do Repositório).
**EN-US:** They verify if different parts of the system work well together (e.g., if the Controller can save data to MySQL through the Repository).

### 3. Mock Objects (Simulações)
**PT-BR:** Objetos "dublês" que simulam serviços externos (como envio de e-mail ou APIs de pagamento) para que os testes não dependam de internet ou custos externos.
**EN-US:** "Double" objects that simulate external services (like email sending or payment APIs) so that tests don't depend on internet or external costs.

---

## 📂 Estrutura de Pastas / Directory Structure



* **`Unit/`**: 
    * **PT-BR:** Testes de lógica pura, como validação de CPF ou cálculos matemáticos.
    * **EN-US:** Pure logic tests, such as tax ID validation or mathematical calculations.
* **`Integration/`**: 
    * **PT-BR:** Testes que envolvem banco de dados, sistema de arquivos e rotas de API.
    * **EN-US:** Tests involving databases, file systems, and API routes.
* **`Mocks/`**: 
    * **PT-BR:** Classes que fingem ser serviços reais para isolar os testes.
    * **EN-US:** Classes that pretend to be real services to isolate tests.

---

## 🚀 O Valor dos Testes / The Value of Testing

* **Prevenção de Regressão:** Garante que um erro corrigido no passado não volte a aparecer.
* **Documentação Viva:** Os testes mostram exatamente como as classes devem ser usadas.
* **Código Limpo:** Se algo é difícil de testar, é porque o código está mal desenhado. Testes forçam uma arquitetura melhor.

---

## 🧪 Como Executar / How to Run

**PT-BR:** Em um ambiente real, usaríamos o **PHPUnit**. Para esta demonstração, cada arquivo de teste pode ser executado via CLI, exibindo `PASSED` ou `FAILED` para cada validação realizada.
**EN-US:** In a real environment, we would use **PHPUnit**. For this demonstration, each test file can be run via CLI, displaying `PASSED` or `FAILED` for each validation performed.
