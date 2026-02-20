## 📚 Atividade 4 – Catálogo de Serviços e Portal

Nesta atividade, criamos um **Record Producer** para permitir que os usuários submetam postagens de forma simplificada por meio do **Catálogo de Serviços**, 
além da configuração de acesso via **Employee Center**.

## 🔹 1. Criação do Record Producer

Foi desenvolvido um **Record Producer** com nome de **New Social Media Post**

<img width="1285" height="508" alt="image" src="https://github.com/user-attachments/assets/072781eb-3680-415e-a85a-60a21d2e2da6" />

- ✅ Em *Record Producer*, clique em *New* 
<img width="1889" height="315" alt="image" src="https://github.com/user-attachments/assets/ffd556c1-6845-4d40-bf7d-6fd0897bd5a1" />

- ✅ Preencha os campos solicitados:
<img width="1415" height="507" alt="image" src="https://github.com/user-attachments/assets/85f52269-9e0c-47ef-ac16-03cca97ce8b3" />

- ✅ No *Short Descrition* e no *Descrition*:
<img width="1419" height="626" alt="image" src="https://github.com/user-attachments/assets/29141543-69da-4e97-a0d7-cd95d68fe980" />

- ✅ Com 3 variáveis obrigatórias (com indicação de *asterisco vermelho*)
<img width="1275" height="428" alt="image" src="https://github.com/user-attachments/assets/a6e4c632-da8b-4c2e-a69d-91f1290f0516" />

<img width="1412" height="745" alt="image" src="https://github.com/user-attachments/assets/f0fa7446-51cb-4490-bd76-29251223ac5f" />

- ✅ Mapeamento (*Map to Field*) de cada variável para campos da tabela **Post** e configuração de obrigatoriedade no preenchimento (*Mandatory*)
<img width="1416" height="513" alt="image" src="https://github.com/user-attachments/assets/cdf69fd4-db7b-47f0-a89f-b09998a2eba8" />

- ✅ Restrição de acesso: 
Em *Avaibalbe for* criamos o grupo *Social Media Users*:   
<img width="1404" height="414" alt="image" src="https://github.com/user-attachments/assets/4cfaf268-1b9d-4468-a270-59e934ccaf8d" />
Que recebe os grupos: `Social Media - Gestores` e `Social Media - Analistas`  
<img width="1439" height="616" alt="image" src="https://github.com/user-attachments/assets/b69ace08-15e5-4bd4-9171-26a24badf86c" />

## 🔹 2. Criação do Menu Item "New Post" no Employee Center

<img width="890" height="95" alt="image" src="https://github.com/user-attachments/assets/14f68522-b28d-446e-b6a6-c2afe5fd70b1" />

Para permitir o acesso ao *Record Producer* **via portal**, foi criado um **Menu Item** (com o nome de **New Post**) na **Header Menu** do **Employee Center Menu**:

<img width="1896" height="367" alt="image" src="https://github.com/user-attachments/assets/6b278be1-6800-41c0-a73d-31f41e97d7b8" />

Com as seguintes configurações:
> precisa **Elevate role** para essa autorização acontecer  

- Clica no **Parent:** `More`  
  (que por sua vez tem como parent o `Employee Center Menu`)

<img width="1418" height="632" alt="image" src="https://github.com/user-attachments/assets/f5fbea9d-dbc9-4b5a-a589-5972f46655df" />

Para editar, clique em **here**:
<img width="1419" height="321" alt="image" src="https://github.com/user-attachments/assets/39fa59a9-2941-470c-89b5-b9a969b5b407" />

Agora clique em **New**:
<img width="1090" height="678" alt="image" src="https://github.com/user-attachments/assets/c13752e9-d90a-4871-a1a2-30b0731b83f4" />

E preencha os campos solicitados:
- **Label:** `New Post`
- **Type:** `Catalog Item`
- **Referência:** Record Producer criado
- **Page:** `sc_cat_item`

<img width="1433" height="450" alt="image" src="https://github.com/user-attachments/assets/a9beebb1-011b-462f-89fc-c59738c1fc99" />

Essa configuração permite que o usuário acesse o formulário diretamente pelo **Employee Center**.

## 🎯 Resultado Final

O usuário consegue:
- Acessar o portal **Employee Center**
- Localizar o Menu Item criado
- Abrir o Record Producer
- Submeter uma nova postagem de forma estruturada e controlada

## 🧠 Aprendizados

Durante esta atividade, praticamos:  
- Criação e configuração de Record Producer
- Uso de *Map to Field*
- Controle de acesso por grupos
- Configuração de Menu Item no portal
- Navegação e estrutura do Employee Center

---

👉🏻 [Clique aqui para voltar ao Readme](https://github.com/DrikaDev/Social-Media-Management/blob/main/README.md)📒
