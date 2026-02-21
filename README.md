## 🦈 Desafio Bootcamp Shark Evolution – Aoop / NTT Data

Este desafio teve como objetivo validar os conhecimento adquiridos ao longo da 3º temporada do Shark Evolution.  
A atividade consistia em desenvolver uma aplicação escopada no ServiceNow para gestão de mídias sociais, permitindo que o time de Marketing registre, acompanhe e controle o ciclo de vida das postagens de clientes, garantindo governança, segurança e automação do processo.  

## 📊 Resultado da Avaliação
A minha colocação no range de notas foi: 
- Abaixo de 5 pontos
- Entre 5 e 8,4 pontos ✅ 
- Acima de 8,5 pontos

## 🔎 Feedback Técnico Recebido
- O Auto Number do Channel não estava funcional no formulário.
- O layout do formulário Post não estava totalmente conforme o esperado.
- Não foi possível validar a exibição correta da Related List solicitada.
- O Record Producer não estava aparecendo no Employee Center.
- Existiam duas roles com o mesmo nome, gerando possível inconsistência.
- Os grupos não foram apresentados para validação.
- Não houve evidência clara de funcionamento do User Criteria.

## 🔄 Evolução Após o Feedback
Após receber o feedback técnico, realizei os ajustes necessários e revisei conceitos importantes da plataforma reforçando:  
- Configuração correta de Auto Number
- Organização de formulários e Related Lists
- Estrutura adequada de Roles e Groups
- Implementação e validação de User Criteria
- Publicação correta do Record Producer no Portal

Esse processo foi essencial para consolidar meu entendimento prático na plataforma.

## 🧩 Conhecimentos Avaliados no Desafio

- **Desenvolvimento e configuração da aplicação:**  
  Criação de um ambiente isolado (escopado) no *App Engine Studio* para resolver uma necessidade de negócio.
- **Modelagem de dados e formulários:**  
  - Criação da tabela *Channel* do zero (from scratch) com campos específicos
  - Criação da tabela *Post* estendendo da tabela *Task*, herdando funcionalidades padrão e adicionando campos personalizados para a gestão dos posts, assim como a configuração de formulários e campos personalizados.
- **Segurança e Governança RBAC (Role-Based Access Control):**  
  - Criação das roles `social_analyst` e `social_manager`
  - Configuração de ACL´s com condições específicas
  - Aplicação de User Criteria no Employee Center para restringir o acesso a visibilidade do menu "New Post" e ao item de catálogo.
- **Conceitos de ITSM:**  
  Tratando cada post como uma Task que possui ciclo de vida com estados: Draft -> Published -> Follow-up -> Closed.
- **Desenvolvimento low-code/no-code:**  
  - Com a utilização do UI Policies condicionais tornando o campo "Channel" obrigatório e ocultando/mostrando o campo "End follow-up" com base no estado do post
  - Organização do layout do portal para os utilizadores finais
  - Automação com Flow Designer

## 💡Etapas do desafio
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

Em suma, este desafio demonstrou minha capacidade de:
- Construir uma solução completa de ponta a ponta
- Aplicar boas práticas de segurança
- Trabalhar com modelagem de dados e automação
- Receber feedback técnico e evoluir com base nele

## 🚀 Considerações Finais

Participar da 3º temporada do **Shark Academy da Aoop/NTT Data** foi uma experiência extremamente enriquecedora.  
Além do aprendizado técnico, reforçou minha capacidade de análise crítica, revisão e melhoria contínua, habilidades essenciais para atuar com *ServiceNow* em ambientes corporativos.    
Agradeço pela oportunidade de participar do programa e de demonstrar meu comprometimento, dedicação, esforço e constante vontade de evoluir na plataforma.

---
✨ Desenvolvido com dedicação por **Adriana G.**
