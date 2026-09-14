<div align="center">
  
# 🎮 PET-EP Gamifica

![License](https://img.shields.io/badge/license-GPL--3.0-blue)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)
![Firebase](https://img.shields.io/badge/Firebase-Firestore-FFCA28?logo=firebase)

Sistema de Gamificação Automatizado para o Programa de Educação Tutorial da Engenharia de Produção (UFC)

**Palavras-chave:** `gamificação` `gestão acadêmica` `leaderboard` `PET` `engenharia de produção` `automação` `pontuação`

</div>

---

## 📑 Índice
 
- [Sobre](#-sobre)
- [Equipe](#-equipe)
- [Tecnologias](#-tecnologias)
- [Licença](#-licença)
- [Requisitos Funcionais](#-requisitos-funcionais)

---

## 📋 Sobre
 
O **PET-EP Gamifica** é uma plataforma desenvolvida para automatizar, centralizar e gamificar o controle de pontos acumulados pelos membros do PET Engenharia de Produção da UFC (os "PETianos").
 
Atualmente, o controle de pontos do grupo é feito de forma manual e descentralizada, através de planilhas eletrônicas e tabelas de referência físicas, o que gera atrasos, erros de preenchimento e falta de transparência no acompanhamento do desempenho dos membros.
 
O sistema resolve esse problema centralizando as tabelas de equivalência de pontos em um banco de dados único, permitindo que coordenadores registrem tarefas realizadas de forma rápida e simples. Com isso, o sistema calcula automaticamente as pontuações, atualiza o extrato individual de cada membro, envia notificações em tempo real e mantém um **Painel de Líderes (Leaderboard)** sempre atualizado, aumentando o engajamento e a transparência no processo de gamificação do grupo.

---

## 👥 Equipe
 
| Nome | Função |
|---|---|
| Jonata Monteiro Alves | Product Owner /  UX/UI Designer  |
| Antonio Pedro Martins Alves | Desenvolvedor Full-Stack |
| Pedro Roger Silva Peixoto | Desenvolvedor Full-Stack |
| Joel Soares Silva | Desenvolvedor Full-Stack |
| Davi Vasconcelos Viana | UX/UI Designer |
| Danilo Everton Vaz de Sousa | QA / Testes |
 
---

## 🛠 Tecnologias
 
**Frontend**
- React 18
- TailwindCSS

**Backend, Banco de Dados e Autenticação**
- Firebase
  - **Firestore** — banco de dados NoSQL em tempo real (armazenamento de membros, atividades, pontuações e semestres)
  - **Firebase Authentication** — autenticação de coordenadores e membros
  - **Cloud Functions** — lógica de servidor (cálculo de pontos, envio de notificações, regras de negócio)
 
**Infraestrutura**
- Firebase Hosting

---

## 📄 Licença
 
Este projeto está licenciado sob os termos da **GNU General Public License v3.0 (GPL-3.0)**.
 
Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
 
---

## ✅ Requisitos Funcionais
 
| ID | Descrição | Prioridade | Depende de |
|---|---|---|---|
| RF01 | Permitir autenticação segura de usuários (membros e coordenadores) usando e-mail institucional da UFC e senha. | Alta | Nenhum |
| RF02 | Permitir aos coordenadores cadastrar, editar, listar e inativar membros (PETianos) do projeto. | Alta | Nenhum |
| RF03 | Permitir aos coordenadores gerenciar tipos de atividades e eventos, com suas respectivas tabelas de pontuação padrão. | Alta | Nenhum |
| RF04 | Permitir que coordenadores realizem o lançamento de pontuação individual, selecionando o membro, a atividade e a data. | Alta | RF02, RF03 |
| RF05 | Permitir que coordenadores realizem lançamentos de pontuação em lote (múltiplos membros simultaneamente) para atividades em grupo. | Média | RF04 |
| RF06 | Permitir que cada membro consulte seu extrato individual de pontos, detalhado por data, tipo de atividade e pontuação ganha. | Alta | RF01, RF04 |
| RF07 | Exibir o Painel de Líderes (Leaderboard) em tempo real, apresentando a lista de membros ordenada por pontuação semestral decrescente. | Alta | RF04 |
| RF08 | Permitir o filtro temporal do painel de líderes por período específico (mês atual, semestre corrente e semestres anteriores). | Média | RF07 |
| RF09 | Gerenciar e atribuir conquistas e medalhas digitais (badges) aos membros de forma automática após atingirem metas de pontos. | Média | RF04 |
| RF10 | Enviar notificações automáticas (via e-mail) ao membro do PET-EP sempre que novos pontos forem creditados. | Baixa | RF04 |
| RF11 | Permitir que os membros abram uma solicitação de ajuste de pontos caso identifiquem divergências no extrato. | Média | RF06 |
| RF12 | Permitir aos coordenadores visualizar, aprovar ou rejeitar solicitações de ajuste de pontos enviadas pelos membros. | Média | RF11 |
| RF13 | Permitir aos coordenadores configurar semestres letivos, definindo datas de início, término e zeramento automático do leaderboard. | Alta | Nenhum |
| RF14 | Permitir aos coordenadores excluir ou editar lançamentos de pontuação efetuados com erros de digitação. | Alta | RF04 |
| RF15 | Exibir uma interface em destaque para o Pódio do Semestre, oficializando os vencedores (1º, 2º e 3º lugares) no encerramento letivo. | Alta | RF07, RF13 |
