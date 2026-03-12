# 📁 05-utility-and-helpers

## 📖 Descrição / Description

**PT-BR:** Esta camada contém ferramentas de uso geral que dão suporte a todas as outras partes do sistema. Aqui residem funções puras e classes utilitárias que resolvem problemas comuns (como formatação e validação técnica), mas que não pertencem a uma regra de negócio específica.
**EN-US:** This layer contains general-purpose tools that support all other parts of the system. Here reside pure functions and utility classes that solve common problems (such as formatting and technical validation) but do not belong to a specific business rule.

---

## 🛠️ Ferramentas Disponíveis / Available Tools

### 1. Formatters (Formatadores)
**PT-BR:** Classes para transformar dados brutos em formatos legíveis (ex: transformar `2023-10-25` em `25/10/2023`).
**EN-US:** Classes to transform raw data into readable formats (e.g., transforming `2023-10-25` into `10/25/2023`).

### 2. Technical Validators (Validadores Técnicos)
**PT-BR:** Helpers que verificam estruturas de dados, como checar se uma string é um UUID válido ou se um JSON está bem formado.
**EN-US:** Helpers that verify data structures, such as checking if a string is a valid UUID or if a JSON is well-formed.

### 3. Text & Array Support
**PT-BR:** Manipulação de strings (limpeza de caracteres, geração de slugs) e utilitários para busca em arrays complexos.
**EN-US:** String manipulation (sanitizing characters, slug generation) and utilities for searching in complex arrays.

---

## 📂 Estrutura de Pastas / Directory Structure

* **`Formatters/`**: 
    * **PT-BR:** Ex: `CurrencyFormatter.php`. Transforma números em valores monetários.
    * **EN-US:** E.g., `CurrencyFormatter.php`. Transforms numbers into monetary values.
* **`Validators/`**: 
    * **PT-BR:** Ex: `StringValidator.php`. Verifica se campos técnicos atendem requisitos básicos.
    * **EN-US:** E.g., `StringValidator.php`. Checks if technical fields meet basic requirements.
* **`Support/`**: 
    * **PT-BR:** Funções globais e helpers de sistema (ex: `EnvHelper.php`).
    * **EN-US:** Global functions and system helpers (e.g., `EnvHelper.php`).

---

## 🚀 Benefícios de Engenharia / Engineering Benefits

* **Reutilização (Reuse):** Evita a duplicação de lógica simples em diferentes camadas do projeto.
* **Pureza (Purity):** Por serem funções "puras" (sem estado), não causam efeitos colaterais no restante do sistema.
* **Manutenibilidade:** Se a forma de formatar datas mudar, você altera apenas um arquivo central.

---

## 🧪 Como Testar / How to Test

**PT-BR:** Testar esta camada é simples: basta passar uma entrada e validar a saída. Exemplo: Enviar `ola mundo` para um gerador de slug e esperar `ola-mundo`. Se o retorno for idêntico, a ferramenta está pronta.
**EN-US:** Testing this layer is simple: just pass an input and validate the output. Example: Send `hello world` to a slug generator and expect `hello-world`. If the return is identical, the tool is ready.
