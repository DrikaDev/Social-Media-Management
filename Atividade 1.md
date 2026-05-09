## 🦈 Atividade 1 - Criação da aplicação e das tabelas

Nesta atividade, desenvolvemos uma aplicação funcional no ServiceNow, criando tabelas customizadas e relacionamentos entre dados, aplicando boas práticas de modelagem e configuração da plataforma.

## 1. Criação da Aplicação

Utilizando o App Engine Studio, criamos uma nova aplicação escopada chamada **Social Media Management**

<img width="1434" height="245" alt="image" src="https://github.com/user-attachments/assets/ff40fce0-0028-4841-90d3-0af350117ba2" />

## 2. Criação das Tabelas

<img width="1075" height="225" alt="image" src="https://github.com/user-attachments/assets/b05fff01-52dd-4e23-8075-a2e0af06b758" />

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

<img width="1418" height="574" alt="image" src="https://github.com/user-attachments/assets/c6247081-199a-489b-8dd9-f73f07f23102" />

### 🔹 Tabela: Post

Tabela estendida da tabela **Task**.  
Apenas os **campos abaixo foram criados como exclusivos**. Os demais campos são herdados da **Task**.  

**Campos exclusivos:**
-   `Channel` (Reference: Channel)
-   `Total of Clicks` (Choice: -500, 500 to 1000, 1000 to 5000, +5000)
-   `Content` (HTML)
-   `End follow-up` (True/False. Default value: False)

<img width="1424" height="470" alt="image" src="https://github.com/user-attachments/assets/db8f94f7-62ca-454f-b93b-d11ef5b368dd" />

### 🔄 Choices configurados do campo State:
-   Draft (Default: value 1)
-   Published
-   Follow-up
-   Closed

<img width="1389" height="286" alt="image" src="https://github.com/user-attachments/assets/5ac7c27e-57fe-4dc5-b3b6-8f8d1c8792e1" />

<img width="794" height="482" alt="image" src="https://github.com/user-attachments/assets/ad9b4d5d-7243-465f-b8fd-534c59c44e16" />

> As opções padrão da Task foram desativadas.  

## 3. Configuração de Auto-number

Em **System Definition / Tables**, habilitar o **auto-numbering** nas tabelas Channel e Post:

-   Prefixo personalizado
-   Número inicial definido
-   Número de digitos

<img width="1409" height="584" alt="image" src="https://github.com/user-attachments/assets/accba7fc-e68b-4883-8346-fc996b1748c2" />

<img width="1410" height="585" alt="image" src="https://github.com/user-attachments/assets/6a27c0bd-b95b-4ee0-ae78-7afb41e50cc6" />

## 4. Form & List Layout - Tabela Post

### ✔️ Form Layout

-   Remoção de campos desnecessários
-   Inclusão do Activities (Formatter) abaixo de Work Notes
-   Campo State com default: Draft

<img width="1101" height="393" alt="image" src="https://github.com/user-attachments/assets/70545cf7-a4cc-4183-aaba-da8f585e961a" />

### ✔️ List Layout

-   Ajustado conforme imagem
-   Exibição apenas dos campos relevantes

<img width="1117" height="110" alt="image" src="https://github.com/user-attachments/assets/a56e4290-5df8-4c1f-9fca-cd1c930095b3" />

## 5. Form & List Layout - Tabela Channel

- Remoção de campos desnecessários
- Form Layout personalizado conforme imagem

<img width="1120" height="302" alt="image" src="https://github.com/user-attachments/assets/91cf003d-0eb4-4d3e-8d97-cf7df97002e4" />

- List Layout ajustado conforme imagem

<img width="1117" height="115" alt="image" src="https://github.com/user-attachments/assets/c4ab87d7-7010-4dbb-965a-b1e99a26ce9d" />

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

## 8. Application Menus e Modules

Criar um **Application Menus** com módulos identados para:
-   Visualizar Channels: Criar e Listar
-   Visualizar Posts: Criar e Listar

<img width="309" height="282" alt="image" src="https://github.com/user-attachments/assets/9876602e-eee8-4db5-aabf-1cb462d76cc0" />

Em **System Definition / Application Menus** - clique na sua aplicação, e faça as devidas alterações em **Order** e em **Link type**.  

<img width="1410" height="585" alt="image" src="https://github.com/user-attachments/assets/9a133831-2dfa-4a08-96e6-462bf53088ce" />

> Pode-se utilizar o ícone de edição (lápis) à direita de cada submenu para editar.

---
👉🏻 [Clique aqui para voltar ao Readme](https://github.com/DrikaDev/Social-Media-Management/blob/main/README.md)📒
