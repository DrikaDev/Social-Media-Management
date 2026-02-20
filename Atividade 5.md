## 🧩 Atividade 5 – Process Flow / UI Policies

Nessa atividade, implementamos melhorias funcionais e regras condicionais no formulário da tabela **Post**, dentro da aplicação Social Media Management.

## 1 - Bloco de orientações no formulário

Foi adicionado um bloco informativo no formulário da tabela **Post**, orientando os usuários que:
- A data de publicação deve ser preenchida manualmente para que o campo **State** seja atualizado corretamente; e
- O campo **End follow-up** deve ser marcado para que o fluxo avance para o próximo estado, **Closed**.  

Garantindo assim que os usuários compreendam as regras de transição de estado da aplicação.

<img width="1101" height="162" alt="image" src="https://github.com/user-attachments/assets/07e19a72-288c-495d-8b27-bf049b0419dd" />

### Para incluir o Blue Box, só clicar com o botão direito no cabeçalho cinza, vá em **Configure** e em **Form Builder**:  
<img width="511" height="162" alt="image" src="https://github.com/user-attachments/assets/2c28d197-5199-47c5-a111-87d2d45c9169" />

### Adicione um elemento **Remember** e escolha o **Annotation type** do tipo *Info Box Blue* e preencha as informações no campo **Annotation text**:  
<img width="1428" height="367" alt="image" src="https://github.com/user-attachments/assets/2bae9412-c6a8-4d35-94e3-b5199d800676" />

## 2 - Indicadores visuais de status (State Flow)

Foram implementadas setas indicadoras no formulário da tabela **Post**, representando visualmente as fases do campo **State**.

<img width="1113" height="221" alt="image" src="https://github.com/user-attachments/assets/9ca50426-361b-4355-a02c-ec0ae044977d" />

### 👉🏼 Em System UI / Process Flow, clica em New
Preencher os devidos campos e ordernar eles para manterem nessa ordem:  
<img width="1091" height="55" alt="image" src="https://github.com/user-attachments/assets/82c0cec3-b501-46a8-b4a7-aa6aaf6b82cc" />

- 100 para Draft,
- 200 para Publish,
- 300 para Follow-up e
- 400 para Closed.

<img width="1090" height="397" alt="image" src="https://github.com/user-attachments/assets/b0ba3743-80c7-482a-bc97-8e93e2ce54c5" />  

As transições respeitam as validações e regras definidas na aplicação, proporcionando:
- Melhor experiência do usuário
- Maior clareza sobre o status da postagem
- Acompanhamento visual do ciclo de vida do registro

## 3 - Regras condicionais no formulário (Client-side)

#### ✔ Campo "Channel" obrigatório (Core UI / Classic)
Foi implementado um mecanismo para tornar o campo **Channel** obrigatório no formulário, sem alterar diretamente sua propriedade no dicionário de dados.
Em Configure / Form Builder, aplicamos **Mandatory** no campo:
<img width="1109" height="456" alt="image" src="https://github.com/user-attachments/assets/882a20e1-42a8-4990-a011-daaea7d0b4cf" />

#### ✔ Exibição condicional do campo "End follow-up"
O campo **End follow-up** foi configurado para aparecer somente quando o campo **State** estiver com o valores **Follow-up** ou **Closed**:  

<img width="1113" height="391" alt="image" src="https://github.com/user-attachments/assets/9abd5cc0-ebef-4a79-8e64-2ae6303f540c" />
<img width="1098" height="126" alt="image" src="https://github.com/user-attachments/assets/cc48f7ab-6b60-4286-a501-4818b53bc278" />

**Objetivo:** Garantir maior controle e coerência na jornada do registro.

## 4 - Controle de visibilidade no Employee Center

O menu **"New Post"** foi configurado para ser exibido no *Employee Center* apenas para usuários com perfil *Analista* e *Gestor*.
Ambos vinculados à aplicação Social Media Management.
A regra garante controle de acesso baseado em papéis (roles), mantendo a governança da aplicação.

👉🏼 **Esconder o botão no menu** é apenas uma medida visual chamada de **Segurança por obscuridade**.
Para garantir 100% de segurança, devemos adicionar essas mesmas roles na aba **User Criteria (Available For)** do próprio Catalog Item "New Social Media Post".

Para garantir que o formulário "New Social Media Post" esteja totalmente protegido (impedindo o acesso até por quem descobrir o link direto), 
você deve configurar o User Criteria.  
No ServiceNow, esconder o botão no menu é apenas o primeiro passo; o User Criteria é a segurança real.  

Em Catalog Definitions / Maintain Items, clicamos no **New Social Media Post** para *adicionar o critério de disponibilidade*  
<img width="1428" height="226" alt="image" src="https://github.com/user-attachments/assets/27ee5c2d-e9e9-4b8f-92c6-045d8ade7bc2" />

Rolamos para baixo para encontrar a aba chamada *Available For* e clicamos no *Social Media Users*  
<img width="1091" height="222" alt="image" src="https://github.com/user-attachments/assets/d04c772b-0116-4a0c-ac89-79539249ad64" />

Clicamos em Roles e adicionamos as roles social_analyst e social_manager:  
<img width="496" height="96" alt="image" src="https://github.com/user-attachments/assets/c13e1860-e8b5-4f11-bcaa-cab5b5867a2c" />

## Realizando testes:

### Teste 1
Ao impersonar com o Abraham Lincoln que não faz parte de nenhum dos grupos:  
<img width="1428" height="277" alt="image" src="https://github.com/user-attachments/assets/1e0c930b-1aa3-48c2-a92e-7ff781002744" />
Vemos que o **New Post** automaticamente desaparece:  
<img width="1423" height="136" alt="image" src="https://github.com/user-attachments/assets/7fa30da8-799a-4099-9d29-49449da16e59" />

### Teste 2
Ao copiarmos a URL do **Catalog Item** de um usuário *autorizado* (Analisty ou Manager), e colarmos numa guia anônima para tentarmos acessar via impersonate com algum outro usuário sem as roles necessárias, como por exemplo o Abraham Lincoln que não faz parte de nenhum dos grupos, o sistema bloqueia o acesso exibindo a seguinte mensagem de restrição:  
<img width="1430" height="262" alt="image" src="https://github.com/user-attachments/assets/88c0c08e-9b1e-4714-87ec-6635966b162f" />

---
👉🏻 [Clique aqui para voltar ao Readme](https://github.com/DrikaDev/Social-Media-Management/blob/main/README.md)📒
