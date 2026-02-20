## 🦈 Desafio Shark Evolution – Aoop / NTT Data

Este desafio teve como objetivo desenvolver uma aplicação escopada no ServiceNow para gestão de mídias sociais, permitindo que o time de Marketing registre, acompanhe e controle o ciclo de vida das postagens de clientes, garantindo governança, segurança e automação do processo.

## 🛠️ Tecnologias Utilizadas

- **ServiceNow** (Instância de desenvolvimento)
- **App Engine / Studio**
- **Tables & Forms**
- **Roles & ACLs**
- **Application Menu & Modules**
- **Flow Designer** (quando aplicável)

## 📦 Funcionalidades Implementadas

A atividade avaliou conhecimentos práticos na plataforma ServiceNow, incluindo:  

- **Desenvolvimento e configuração de aplicação:**  
  Criação de um ambiente isolado (escopado) no *App Engine Studio* para resolver uma necessidade de negócio.
- **Modelagem de dados e formulários:**  
  Criação da tabela *Channel* do zero (from scratch) com campos específicos, e da tabela *Post* estendendo da tabela *Task*, herdando funcionalidades padrão e adicionando campos personalizados para a gestão dos posts, assim como a configuração de formulários e campos personalizados.
- **Segurança e governança com controle de acesso (Roles e ACLs):**  
  Implementação de controle de acesso baseado em papéis RBAC (Role-Based Access Control) onde definimos quem pode visualizar ou editar dados através da criação das roles `social_analyst` e `social_manager`, além de ACL´s com condições específicas e user criteria para restringir o acesso a visibilidade do menu "New Post" e ao item de catálogo no Employee Center.
- **Conceitos básicos de ITSM:**  
  Tratando cada post como uma tarefa que possui ciclo de vida com estados: Draft, Published, Follow-up e Closed.
- **Desenvolvimento low-code/no-code:**  
  Com a utilização do UI Policies tornando o campo "Channel" obrigatório e ocultando/mostrando o campo "End follow-up" com base no estado do post, assim como foi configurado visualmente o layout do portal para os utilizadores finais.

## 💡Explicação de cada etapa do desafio

- Atividade 1 - [Criação da aplicação e das tabelas](https://github.com/DrikaDev/Social-Media-Management/blob/main/Atividade%201.md)  
- Atividade 2 - [Governança: Segurança e acessos](https://github.com/DrikaDev/Social-Media-Management/blob/main/Atividade%202.md)
- Atividade 3 - [Flow Designer](https://github.com/DrikaDev/Social-Media-Management/blob/main/Atividade%203.md) 
- Atividade 4 - [Record Producer: Catálogo de Serviços e Portal](https://github.com/DrikaDev/ServiceNow-Social-Media-Management/blob/main/Atividade%204.md) 
- Atividade 5 - [Extra: Process Flow / UI Policies](https://github.com/DrikaDev/ServiceNow-Social-Media-Management/blob/main/Atividade%205.md)  

## ▶️ Demonstração

📹 Um vídeo demonstrativo foi gravado apresentando:
- Estrutura da aplicação
- Navegação pelos módulos
- Testes de permissões com diferentes usuários
- Funcionamento geral da solução

## 🧠 Aprendizados

Em suma, o desafio demonstrou a capacidade de construirmos uma solução completa, desde a base de dados até à interface do utilizador, seguindo as melhores práticas de segurança e automação da plataforma ServiceNow.

## 🚀 Considerações Finais

Este desafio foi uma experiência extremamente enriquecedora, permitindo aplicar conceitos técnicos em um cenário próximo ao real, além de reforçar o interesse em seguir evoluindo 
na plataforma **ServiceNow**.  

Agradeço a oportunidade de participar da 3º temporada do **Shark Academy da Aoop / NTT Data** e de demonstrar meu comprometimento, esforço e vontade de aprender.

---
✨ Desenvolvido com dedicação por **Adriana G.**
