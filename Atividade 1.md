## 🦈 Atividade 1 - Criação da aplicação e tabelas

## 📌 Objetivo

Criar uma aplicação escopada no ServiceNow para gestão de mídias sociais, permitindo que o time de Marketing registre e acompanhe postagens nos perfis da marca.

## 1. Criação da Aplicação

Utilizando o App Engine Studio, criar uma nova aplicação escopada chamada **Social Media Management**

> **Finalidade da Aplicação**:  
> Gerenciar canais de redes sociais e acompanhar postagens realizadas pela equipe de Marketing.

## 2. Criação das Tabelas

### 🔹 Tabela: Channel

Tabela criada do zero (from scratch), sem estender outra tabela.  
**Funcionalidade:** armazenar informações dos perfis das redes sociais.  

**Campos principais:**
- `Profile` (URL)
-   `Type` (Choice)
    -   Facebook
    -   Instagram
    -   LinkedIn
    -   YouTube
-   `Number of Followers` (Integer)
-   `Number of Posts` (Integer)
-   `Username` (String com max length 100)
-   `Password` (String com max length 100)
-   `Observations` (String com max length 100)

### 🔹 Tabela: Post

Tabela estendida da tabela Task.  
Apenas os campos abaixo foram criados como exclusivos. Os demais campos são herdados da Task.  

**Campos exclusivos:**
-   `Channel` (Reference: Channel)
-   `Total of Clicks` (Choice: -500, 500 to 1000, 1000 to 5000, +5000)
-   `Content` (HTML)
-   `End follow-up` (True/False. Default value: Fase)

### 🔄 Estados configurados:
-   Draft (Default)
-   Published
-   Follow-up
-   Closed

> As opções padrão da Task foram desativadas.

## 3. Configuração de Auto-number

Auto-number habilitado em ambas as tabelas:

-   Prefixo personalizado
-   Número inicial definido
-   Incremento automático configurado

## 4. Form & List Layout - Tabela Post

### ✔️ Form Layout

-   Remoção de campos desnecessários
-   Inclusão do Activities (Formatter) abaixo de Work Notes
-   Campo State com:
    -   Default: Draft
    -   Apenas os 4 estados configurados

### ✔️ List Layout

-   Ajustado conforme imagem
-   Exibição apenas dos campos relevantes

## 5. Form & List Layout - Tabela Channel

-   Remoção de campos desnecessários
-   Form Layout personalizado conforme imagem
-   List Layout ajustado conforme imagem

## 6. Related List

Adicionar uma **Related List de Posts** no formulário da tabela Channel.
Dessa forma todas as postagens relacionadas ao canal aparecem automaticamente no registro.

**Clique no menu hamburguer - Configure - Related Lists**
<img width="1424" height="605" alt="image" src="https://github.com/user-attachments/assets/96e891cf-4c36-4ae3-a593-84344bc96176" />

## 7. Layout da Lista de Referência do formulário da tabela "Post"

No formulário da tabela Post, o campo **Channel** deve ser configurado para exibir uma lista personalizada ao selecionar o registro de referência quando os 
canais forem cadastrados, como por exemplo:  

- Facebook: https://www.facebook.com/abc
- Instagram: https://www.instagram.com/abc
- LinkedIn: https://www.linkedin.com/abc
- YouTube: https://www.youtube.com/abc

<img width="1365" height="334" alt="image" src="https://github.com/user-attachments/assets/c59f5037-e97a-48e3-b9da-f34c94decc77" />

## 8. Application Menu e Modules

Criar um **Application Menu** com módulos identados para:

-   Visualizar Channels: Criar e Listar
-   Visualizar Posts: Criar e Listar

<img width="309" height="282" alt="image" src="https://github.com/user-attachments/assets/9876602e-eee8-4db5-aabf-1cb462d76cc0" />

---

