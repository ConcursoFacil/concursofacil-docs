# Especificação dos Requisitos

## Cenários BDD's

Abaixo estão os cartões e confirmações das histórias selecionadas para o **MVP do ConcursoFácil**.

---

### **US-01 – Criar Conta**

#### Cenário 1: Cadastro bem-sucedido
- **Dado que** um usuário deseja criar uma conta,  
- **Quando** preencher corretamente os campos obrigatórios (nome, e-mail, senha),  
- **Então** o sistema deve registrar os dados e exibir: *"Conta criada com sucesso."*  

#### Cenário 2: Campos inválidos
- **Dado que** um usuário está criando uma conta,  
- **Quando** deixar de preencher algum campo ou inserir dados inválidos,  
- **Então** o sistema deve exibir mensagens de erro específicas.  

---

### **US-02 – Login**

#### Cenário 1: Login válido
- **Dado que** o usuário já possui cadastro,  
- **Quando** inserir e-mail e senha corretos,  
- **Então** o sistema deve autenticar e redirecionar para a página inicial.  

#### Cenário 2: Login inválido
- **Dado que** o usuário já possui cadastro,  
- **Quando** inserir e-mail ou senha incorretos,  
- **Então** o sistema deve exibir: *"Credenciais inválidas."*  

---

### **US-03 – Recuperar Senha**

#### Cenário 1: Solicitação de recuperação
- **Dado que** um usuário esqueceu a senha,  
- **Quando** solicitar recuperação informando seu e-mail,  
- **Então** o sistema deve enviar um link ou código de redefinição.  

---

### **US-06 – Listar Questões**

#### Cenário 1: Listagem inicial
- **Dado que** o usuário acessa a área de questões,  
- **Quando** não aplicar nenhum filtro,  
- **Então** o sistema deve exibir uma lista com questões disponíveis.  

---

### **US-07 – Filtrar Questões**

#### Cenário 1: Aplicar filtros
- **Dado que** o usuário acessa a área de questões,  
- **Quando** aplicar filtros (disciplina, dificuldade, etc.),  
- **Então** o sistema deve exibir apenas as questões compatíveis.  

---

### **US-08 – Responder Questões**

#### Cenário 1: Resposta correta
- **Dado que** o usuário responde uma questão,  
- **Quando** selecionar a alternativa correta,  
- **Então** o sistema deve registrar a resposta e exibir: *"Resposta correta."*  

#### Cenário 2: Resposta incorreta
- **Dado que** o usuário responde uma questão,  
- **Quando** selecionar alternativa incorreta,  
- **Então** o sistema deve registrar a resposta e exibir: *"Resposta incorreta."*  

---

### **US-09 – Revisar Questões Respondidas**

#### Cenário 1: Revisão de histórico
- **Dado que** o usuário já respondeu questões,  
- **Quando** acessar seu histórico,  
- **Então** o sistema deve exibir a lista de questões respondidas e seus resultados.  

---

### **US-12 – Estatísticas Básicas**

#### Cenário 1: Visualizar estatísticas
- **Dado que** o usuário já respondeu questões,  
- **Quando** acessar a área de desempenho,  
- **Então** o sistema deve exibir um resumo de acertos e erros.  

---

### **US-13 – Evolução ao Longo do Tempo**

#### Cenário 1: Visualizar progresso
- **Dado que** o usuário possui histórico de respostas,  
- **Quando** acessar a área de desempenho,  
- **Então** o sistema deve apresentar um gráfico ou lista mostrando sua evolução no tempo.  

---

### **US-16 – Gerenciar Questões (Admin)**

#### Cenário 1: Cadastrar questão
- **Dado que** o administrador acessa o painel,  
- **Quando** preencher os campos obrigatórios de uma nova questão,  
- **Então** o sistema deve salvar e exibir: *"Questão cadastrada com sucesso."*  

#### Cenário 2: Editar questão
- **Dado que** o administrador acessa o painel,  
- **Quando** editar uma questão existente,  
- **Então** o sistema deve atualizar os dados e exibir: *"Questão atualizada com sucesso."*  

#### Cenário 3: Excluir questão
- **Dado que** o administrador acessa o painel,  
- **Quando** remover uma questão,  
- **Então** o sistema deve excluir o registro e exibir: *"Questão removida com sucesso."*  

---

## Histórico de Versão

| **Data** | **Versão** | **Descrição** | **Autor** |
| :------: | :--------: | :----------:  | :-------: |
| 17/09/2025 | 1.0 | Criação da especificação dos requisitos (MVP) | Breno Fernandes |
