# Sistema de Prescrição Clínica

Este é um projeto de software para um sistema de prescrição clínica, desenvolvido com o objetivo de aplicar os princípios do Domain-Driven Design (DDD), utilizando o [ContextMapper](https://contextmapper.org/) como ferramenta de modelagem.

## Objetivo

O objetivo deste projeto é fornecer uma implementação prática dos conceitos de Domain-Driven Design (DDD) em um contexto específico da área da saúde, mais precisamente no processo de prescrição médica em ambientes hospitalares.

## Principais Conceitos de DDD

- **Bounded Contexts**: Cada contexto delimitado (Bounded Context) representa um conjunto coeso de conceitos relacionados a uma parte específica do sistema, com sua própria linguagem ubíqua e regras de negócio.
- **Aggregates**: Os Aggregates representam as raízes de agregação em cada Bounded Context, encapsulando entidades relacionadas e garantindo consistência e invariabilidade de suas relações.
- **Eventos de Domínio**: Eventos de Domínio representam acontecimentos importantes dentro do domínio do sistema, que podem desencadear mudanças de estado ou atividades em outros componentes do sistema.

## Modelagem de Domínio

O modelo de domínio é estruturado em diversos Bounded Contexts, cada um contendo Aggregates e Eventos de Domínio relevantes para suas responsabilidades específicas. Os Bounded Contexts incluem:

- **Contexto de Prescrição Médica**: Responsável pela criação, modificação e cancelamento de prescrições médicas, incluindo dosagem de medicamentos, posologia e horários de administração.
- **Contexto de Farmácia Hospitalar**: Gerencia o estoque de medicamentos, recebimento, dispensação e monitoramento de estoque baixo.
- **Contexto de Administração de Medicamentos**: Registra a administração de medicamentos prescritos aos pacientes.
- **Contexto de Sistema de Gestão Hospitalar (ERP)**: Gerencia pacientes, registros médicos, agendamento de consultas, faturamento e estoque hospitalar.
- **Contexto de Faturamento**: Responsável pela geração de faturas para os pacientes com base nas prescrições médicas e serviços hospitalares prestados.
- **Contexto de Gestão de Estoque**: Monitora e controla o estoque de medicamentos, realizando reposição e identificação de medicamentos vencidos.