# Atividade 15: Sistema de Gestão de Matrículas

## Objetivo
Desenvolver uma aplicação em Spring Boot para gerenciar matrículas de alunos em cursos, implementando um relacionamento Many-to-Many entre as entidades Aluno e Curso.

## Cenário
Uma escola deseja um sistema para:
* **Gerenciar** as matrículas de alunos em diversos cursos.
* **Permitir** que um aluno se matricule em vários cursos.
* **Permitir** que um curso tenha vários alunos matriculados.

## Requisitos

### Modelagem do Banco de Dados
* Configurar um relacionamento Many-to-Many entre as entidades Aluno e Curso.
* Utilizar o JPA para criar uma tabela de junção automaticamente.

### Entidades JPA
* **Aluno:**
    * Atributos: id, nome, email.
    * Relacionamento @ManyToMany com Curso.
* **Curso:**
    * Atributos: id, nome, descrição.
    * Relacionamento @ManyToMany com Aluno.

### Repositórios
* Criar repositórios para Aluno e Curso para operações CRUD e consultas.

### Serviço
* **Funcionalidades:**
    * Criar novos alunos e cursos.
    * Matricular e desmatricular alunos em cursos.
    * Listar cursos de um aluno e alunos de um curso.

### Controller
* **Endpoints REST:**
    * POST /alunos: Adicionar um novo aluno.
    * POST /cursos: Adicionar um novo curso.
    * POST /alunos/{id}/cursos/{cursoId}: Matricular um aluno em um curso.
    * DELETE /alunos/{id}/cursos/{cursoId}: Desmatricular um aluno de um curso.
    * GET /alunos/{id}/cursos: Listar cursos de um aluno.
    * GET /cursos/{id}/alunos: Listar alunos de um curso.

## Desafio Adicional
* Implementar pesquisa de cursos por nome e alunos por email utilizando consultas dinâmicas.

