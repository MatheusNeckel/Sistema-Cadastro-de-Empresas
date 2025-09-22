# Sistema de Cadastro de Empresas 🏢

Sistema desktop em **Java (Swing)** com **MySQL** para **cadastro, edição e relatório de empresas**.  
Projeto acadêmico com foco em **POO**, **DAO/MVC** e integração JDBC.

<p align="left">
  <img alt="Java" src="https://img.shields.io/badge/Java-8%2B-orange">
  <img alt="Build" src="https://img.shields.io/badge/build-Ant%20%7C%20Maven-blue">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-success">
</p>

---

## ✨ Funcionalidades
- Cadastro, edição e exclusão de empresas
- Consulta/listagem com filtros
- Relatório simples de empresas
- Persistência em MySQL via DAO

---

## 🧰 Tecnologias
- Java 8+ (Swing, POO)
- MySQL (JDBC)
- NetBeans/Ant (ou Maven, se aplicável)
- Padrões: DAO, MVC

---

## ⚙️ Como executar

### 1) Pré-requisitos
- **Java 8+**
- **MySQL** em execução (`localhost`)
- IDE (recomendado: **NetBeans**)

### 2) Banco de dados
Crie um banco (ex.: `empresas_db`) e execute o script SQL fornecido no projeto (ex.: `sql/empresas.sql` ou `banco de dados.txt`).

### 3) Configuração JDBC
Abra `src/conexao/Conexao.java` e ajuste as credenciais:
```java
String url = "jdbc:mysql://localhost:3306/empresas_db";
String user = "root";
String password = "sua_senha";
```

### 4) Executar
- **NetBeans/Ant**: abra o projeto e rode a classe principal (ex.: `FormEmpresa.java`).  
- **Maven** (se houver `pom.xml`):  
  ```bash
  mvn clean package
  java -jar target/<artefato>.jar
  ```

> Dica: publique os artefatos (`.jar`, `.zip`) em **Releases** em vez de versioná-los no repositório.

---

## 📁 Estrutura sugerida
```
/README.md
/LICENSE
/.gitignore
/.github/workflows/build.yml
/src/
  /beans/Empresa.java
  /dao/EmpresaDAO.java
  /conexao/Conexao.java
  /forms/FormEmpresa.java
/sql/empresas.sql
/docs/prints/...
nbproject/            # se NetBeans/Ant
pom.xml               # se Maven
```
> Mantenha apenas **código-fonte e configs** no versionamento. Binários e zips devem ir nas **Releases**.

---

## 🧪 CI (GitHub Actions)
Este repositório inclui um workflow de exemplo para compilar o projeto com **Ant** (se `build.xml` existir) ou **Maven** (se `pom.xml` existir).

---

## 📜 Licença
Distribuído sob a licença **MIT**. Veja `LICENSE` para mais detalhes.
