## 🔐 Atividade 2 - Segurança e acessos

Nesta etapa, implementamos controles de acesso baseados em perfil, utilizando Roles, Groups e ACLs na aplicação **Social Media Management**.

## 1 - Criação de Roles

Foram criadas duas roles customizadas para a aplicação:

### 🔹 Sufix: social_manager
- **Descrição:** Usuários com permissão para criar e atualizar canais e posts.

### 🔹 Sufix: social_analyst
- **Descrição:** Usuários com permissão para criar e atualizar posts.

<img width="1077" height="224" alt="image" src="https://github.com/user-attachments/assets/57580d81-5d6b-4341-9272-5d9911de1318" />

## 2 - Criação de Grupos e Associação de Roles

Foram criados dois grupos:
- **Social Media - Gestores**
- **Social Media - Analistas**

Após a criação:
- Usuários foram adicionados aos respectivos grupos.
  
- Ao grupo **Social Media - Gestores** foi atribuída a role `social_manager`.
  <img width="1422" height="527" alt="image" src="https://github.com/user-attachments/assets/9b96bd9f-a8d8-4259-82b1-d969fe637e20" />

- Ao grupo **Social Media - Analistas** foi atribuída a role `social_analyst`.
  <img width="1422" height="524" alt="image" src="https://github.com/user-attachments/assets/3a959ddc-2ddd-4086-84fb-2a666fe138e4" />

> Os usuários utilizados poderiam já existir na instância ou serem criados especificamente para testes.

## 3 - Configuração de Permissões (CRUD)

O controle de acesso (CRUD) foi configurado conforme a matriz definida no desafio.  

<img width="547" height="238" alt="image" src="https://github.com/user-attachments/assets/9c82c937-bf1a-412f-9801-6fee74da777e" />  

#### **Em System Security - Access Control**, foram incluídas as roles de acordo com a exigência de cada operação:  

**Na tabela Channel:**  
<img width="1407" height="405" alt="image" src="https://github.com/user-attachments/assets/17190ad0-23bc-4832-8845-b9c32e117bac" />

**Na tabela Post:**  
<img width="1401" height="348" alt="image" src="https://github.com/user-attachments/assets/e75365e9-c549-4032-872f-e413dad084a4" />

⚠️ **Observação importante:**
Como a tabela **Post** estende a tabela **Task**, algumas restrições de acesso podem ocorrer devido às ACLs herdadas da tabela pai.  

Por esse motivo, foi necessário criar ou ajustar ACLs na tabela **Post** para permitir a manipulação / autorização dos seguintes campos:
- `Short description - (write)`
- `Additional comments - (read & write)`
- `Work notes - (read & write)`

Em **System Security / Access Control (ACL)** - com **Elevate role**, clica em **New**.

<img width="1425" height="265" alt="image" src="https://github.com/user-attachments/assets/5c258c69-4a19-4047-abc4-c67ff03c4fe0" />

- `Short description - (write)`
<img width="1415" height="461" alt="image" src="https://github.com/user-attachments/assets/0cfcd001-e9f7-4d7a-b872-c976a1b70bb1" />

- `Additional comments - (read & write)`
<img width="1419" height="463" alt="image" src="https://github.com/user-attachments/assets/99193af2-e125-4788-9ebc-80a7086437fd" />

- `Work notes - (read & write)`
<img width="1411" height="461" alt="image" src="https://github.com/user-attachments/assets/5503def3-d0fa-4bcb-a81a-7cba4eb1e753" />

**Resultado**
<img width="1090" height="567" alt="image" src="https://github.com/user-attachments/assets/df17962e-d911-4114-ab29-946ea65f7089" />

> Os campos **work notes** (read & write) e **additional comments** (read & write) são herdados da tabela **TASK**!
> No "Impersonate" de cada um aparece os campos que precisam de ACL.  

### 👉🏼 Roles para Manager & Analistas.  
As ACLs criadas foram associadas às roles `social_manager` e `social_analyst`, conforme regra definida na matriz de permissões.
<img width="1098" height="178" alt="image" src="https://github.com/user-attachments/assets/e279e18d-0254-4777-b266-b80be04bc15b" />

## 4 - Restrição de Acesso ao Application Menu e Modules

As permissões definidas nas tabelas também foram refletidas na navegação da aplicação, garantindo que:
- Apenas usuários autorizados visualizem os módulos correspondentes.
- O acesso ao menu respeite as roles atribuídas.

Ao impersonarmos um manager, vemos que tem acesso ao CRUD completo conforme solicitado na atividade:  
<img width="304" height="287" alt="image" src="https://github.com/user-attachments/assets/4a67a6cb-7a99-4281-a82c-4ae415a13b37" />

Ao impersonarmos um analista, vemos que tem acesso a quase tudo: ele pode criar e listar posts, pode listar Channel, porém, não pode criar um Channel.  
<img width="314" height="260" alt="image" src="https://github.com/user-attachments/assets/8903a961-fb95-48b2-9048-57b8b73c9a9f" />

## ⚠️ Boas Práticas Aplicadas

- Remoção de roles desnecessárias criadas anteriormente.
- Evitar excesso de ACLs sem necessidade.
- Manutenção de uma estrutura de segurança limpa e organizada.

A segurança foi configurada de forma enxuta, respeitando o "princípio do menor privilégio".

---

👉🏻 [Clique aqui para voltar ao Readme](https://github.com/DrikaDev/Social-Media-Management/blob/main/README.md)📒
