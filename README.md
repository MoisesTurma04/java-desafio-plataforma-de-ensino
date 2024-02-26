# Plataforma de Ensino

Este projeto consiste em uma plataforma de ensino desenvolvida para calcular a duração total de um curso, a partir das informações fornecidas sobre as aulas. O sistema é capaz de processar dados de aulas em vídeo e tarefas, calculando a duração total do curso com base nessas informações.

## Funcionalidades

- **Cadastro de Aulas:** O sistema permite o cadastro de aulas, tanto em formato de vídeo quanto de tarefa, com informações detalhadas sobre cada uma.
  
- **Cálculo da Duração Total:** Utilizando os dados das aulas cadastradas, o sistema realiza o cálculo da duração total do curso, considerando a duração de cada aula.

## Estrutura de Dados

O projeto utiliza uma estrutura de dados baseada em classes para representar as informações das aulas. Cada aula pode ser do tipo vídeo ou tarefa, e possui os seguintes atributos:

- **Vídeo:** título, URL e duração em segundos.
- **Tarefa:** título, descrição e quantidade de questões.

## Implementação

O programa utiliza uma lista do tipo `List<Lesson>` para armazenar todas as aulas do curso. A chamada do método `duration()` é polimórfica, permitindo calcular a duração total do curso de forma dinâmica, conforme o tipo de aula.

## Diagrama de classes
```mermaid
classDiagram
    class Lesson {
        - String title
        + duration(): int 
    }
    class Video {
        - String url
        - int seconds
    }
    class Task {
        - String description
        - int questionCount
    }
    class Program {
        + main(args: String[]): void
    }

    Program --|> Lesson : uses
    Lesson <|-- Video
    Lesson <|-- Task

