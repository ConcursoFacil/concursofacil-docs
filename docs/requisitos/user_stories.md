# Especificação dos Requisitos

## Cenários BDD's

Abaixo estão os cartões e confirmações das histórias selecionadas para o **MVP do ConcursoFácil**.

---

## **Casos de Uso – Acesso e Autenticação**

---

### **US-01 – Criar Conta**

**Cenário 1: Cadastro bem-sucedido**

- **Dado que** um usuário deseja criar uma conta,  
- **Quando** preencher corretamente os campos obrigatórios (*nome, e-mail, senha e confirmação de senha*),  
- **Então** o sistema deve registrar os dados e exibir a mensagem:  
  *“Conta criada com sucesso.”*

**Cenário 2: Campos inválidos ou ausentes**

- **Dado que** o usuário está criando uma conta,  
- **Quando** deixar algum campo obrigatório em branco ou inserir dados inválidos (*ex.: e-mail incorreto ou senhas diferentes*),  
- **Então** o sistema deve exibir mensagens de erro específicas indicando o problema.

**Cenário 3: E-mail já cadastrado**

- **Dado que** o usuário tenta criar uma conta com um e-mail já existente,  
- **Quando** enviar o formulário de cadastro,  
- **Então** o sistema deve impedir o registro e exibir:  
  *“E-mail já cadastrado. Tente outro ou faça login.”*

---

### **US-02 – Fazer Login**

**Cenário 1: Login bem-sucedido**

- **Dado que** um usuário já possui uma conta válida,  
- **Quando** informar corretamente o e-mail e a senha,  
- **Então** o sistema deve autenticar o usuário e redirecioná-lo para a tela inicial logada.

**Cenário 2: Credenciais incorretas**

- **Dado que** o usuário tenta acessar sua conta,  
- **Quando** informar e-mail ou senha incorretos,  
- **Então** o sistema deve exibir:  
  *“E-mail ou senha incorretos.”*

**Cenário 3: Campos não preenchidos**

- **Dado que** o usuário está na tela de login,  
- **Quando** tentar entrar sem preencher todos os campos obrigatórios,  
- **Então** o sistema deve exibir mensagens como:  
  *“Informe seu e-mail.”*  
  *“Informe sua senha.”*

---

### **US-06 – Exibir Mensagens Claras de Erro e Sucesso**

**Cenário 1: Mensagens de sucesso** 

- **Dado que** o usuário conclui uma ação corretamente (*como cadastro ou login*),  
- **Quando** o sistema processar a requisição com êxito,  
- **Então** deve exibir mensagens claras e visuais, como:  
  *“Login realizado com sucesso.”*  
  *“Conta criada com sucesso.”*

**Cenário 2: Mensagens de erro**

- **Dado que** ocorre um erro de validação, credencial ou servidor,  
- **Quando** o sistema detectar o problema,  
- **Então** deve apresentar mensagens explicativas como:  
  *“Não foi possível entrar agora. Tente novamente.”*  
  *“E-mail ou senha incorretos.”*  
  *“Campo obrigatório não preenchido.”*

---

### **US-07 – Navegar entre Login, Cadastro e Recuperação de Senha**

**Cenário 1: Acesso à tela de cadastro**

- **Dado que** o usuário está na tela de login,  
- **Quando** clicar no link *“Cadastre-se”*,  
- **Então** o sistema deve redirecionar o usuário para a tela de Cadastro de Conta.

**Cenário 2: Acesso à tela de recuperação de senha**

- **Dado que** o usuário está na tela de login,  
- **Quando** clicar em *“Esqueci minha senha”*,  
- **Então** o sistema deve redirecioná-lo para a tela de Recuperação de Senha.

**Cenário 3: Retorno para a tela de login**

- **Dado que** o usuário está na tela de cadastro ou recuperação,  
- **Quando** clicar em *“Já tenho uma conta”*,  
- **Então** o sistema deve redirecioná-lo de volta para a tela de Login.

## **Casos de Uso – Sidebar**

---

### **US-08 – Visualizar Sidebar Fixa**

**Cenário 1: Exibição da sidebar após login**

- **Dado que** o usuário está autenticado no sistema,  
- **Quando** acessar qualquer tela principal (*como Questões, Dashboard ou Configurações*),  
- **Então** o sistema deve exibir uma **sidebar fixa** na lateral esquerda com os **botões principais de navegação**.

**Cenário 2: Sidebar ausente antes do login**

- **Dado que** o usuário ainda não está autenticado,  
- **Quando** acessar páginas públicas (*como Login ou Cadastro*),  
- **Então** a **sidebar não deve ser exibida**, garantindo uma **interface limpa e segura**.

---

### **US-10 – Navegação pelos Botões da Sidebar**

**Cenário 1: Redirecionamento entre telas**

- **Dado que** o usuário está autenticado e visualiza a sidebar,  
- **Quando** clicar em um botão de menu (*ex.: Questões, Dashboard, Configurações*),  
- **Então** o sistema deve **redirecionar o usuário** para a **tela correspondente**.

**Cenário 2: Feedback visual no clique**

- **Dado que** o usuário interage com um botão da sidebar,  
- **Quando** clicar em um item,  
- **Então** o botão deve apresentar um **feedback visual de seleção** (*ex.: cor ou destaque leve*) para indicar a interação.

---

### **US-13 – Ocultar Itens para Usuários Não Autenticados**

**Cenário 1: Restrições para usuários não autenticados**

- **Dado que** o usuário não fez login,  
- **Quando** acessar o sistema,  
- **Então** os **botões e menus da sidebar** devem estar **ocultos ou desativados**, impedindo **acesso a áreas restritas**.

**Cenário 2: Exibição após autenticação**

- **Dado que** o usuário está autenticado,  
- **Quando** o login for concluído com sucesso,  
- **Então** o sistema deve **exibir automaticamente todos os itens da sidebar** disponíveis para o **perfil do usuário** (*padrão ou administrador*).

## **Casos de Uso – Perfil**

---

### **US-15 – Acessar Tela de Perfil**

**Cenário 1: Acesso ao perfil autenticado**

- **Dado que** o usuário está autenticado no sistema,  
- **Quando** clicar na opção *“Perfil”* na sidebar ou menu,  
- **Então** o sistema deve **redirecionar para a tela de perfil**, exibindo as **informações básicas do usuário** (*ex.: nome, e-mail e função/cargo, se disponível*).

**Cenário 2: Acesso negado para usuário não autenticado**

- **Dado que** o usuário não realizou login,  
- **Quando** tentar acessar a rota ou URL da tela de perfil,  
- **Então** o sistema deve **redirecionar para a tela de login** e exibir a mensagem:  
  *“Faça login para acessar seu perfil.”*

**Cenário 3: Falha ao carregar dados**

- **Dado que** o usuário está autenticado,  
- **Quando** o sistema não conseguir carregar as informações do perfil (*por erro de conexão ou falha no servidor*),  
- **Então** deve exibir uma mensagem informativa:  
  *“Não foi possível carregar suas informações agora. Tente novamente mais tarde.”*

**Cenário 4: Exibição de informações básicas**

- **Dado que** o usuário acessou com sucesso a tela de perfil,  
- **Quando** a página for carregada,  
- **Então** devem ser exibidos os **campos básicos cadastrados** (*nome, e-mail e, se disponível, função/cargo*) em formato **somente leitura**.

## **Casos de Uso – Configurações**

---

### **US-22 – Acessar Tela de Configurações da Conta**

**Cenário 1: Acesso autorizado**

- **Dado que** o usuário está autenticado no sistema,  
- **Quando** clicar no menu ou botão *“Configurações”*,  
- **Então** o sistema deve **redirecioná-lo para a tela de configurações da conta**, exibindo os **campos disponíveis** (*nome, e-mail e demais informações básicas*).

**Cenário 2: Acesso negado a usuário não autenticado**

- **Dado que** o usuário não realizou login,  
- **Quando** tentar acessar diretamente a tela de configurações via URL,  
- **Então** o sistema deve **redirecionar o usuário para a tela de login**, exibindo a mensagem:  
  *“Você precisa estar logado para acessar as configurações da conta.”*

**Cenário 3: Falha ao carregar dados do usuário**

- **Dado que** o usuário está autenticado,  
- **Quando** o sistema não conseguir carregar suas informações por erro técnico,  
- **Então** deve exibir uma mensagem informativa:  
  *“Não foi possível carregar suas informações. Tente novamente mais tarde.”*

---

### **US-26 – Exibir Mensagens Claras de Sucesso ou Erro**

**Cenário 1: Alteração bem-sucedida**

- **Dado que** o usuário está na tela de configurações,  
- **Quando** preencher e salvar os dados corretamente,  
- **Então** o sistema deve exibir uma mensagem de confirmação:  
  *“Alterações salvas com sucesso.”*

**Cenário 2: Falha na atualização**

- **Dado que** o usuário tenta salvar alterações,  
- **Quando** ocorrer erro de validação (*campo vazio, formato inválido ou problema no servidor*),  
- **Então** o sistema deve exibir uma **mensagem de erro clara e explicativa**, como:  
  *“Não foi possível salvar as alterações. Verifique os dados e tente novamente.”*

**Cenário 3: Problema de conexão ou timeout**

- **Dado que** o usuário tenta atualizar as informações,  
- **Quando** houver falha na comunicação com o servidor,  
- **Então** deve ser exibida uma mensagem genérica de falha:  
  *“Erro ao conectar com o servidor. Por favor, tente novamente mais tarde.”*

## **Casos de Uso – CRUD de Questões (Admin)**

---

### **US-29 – Acessar Tela de Listagem de Questões**

**Cenário 1: Acesso permitido ao administrador**

- **Dado que** o usuário possui perfil de administrador,  
- **Quando** acessar o menu *“CRUD de Questões”*,  
- **Então** o sistema deve **exibir a tela de listagem de questões**, mostrando **todas as questões cadastradas no sistema**.

**Cenário 2: Acesso negado para usuários comuns**

- **Dado que** o usuário não é administrador,  
- **Quando** tentar acessar a rota do CRUD de questões,  
- **Então** o sistema deve **negar o acesso** e exibir a mensagem:  
  *“Acesso restrito. Apenas administradores podem gerenciar as questões.”*

---

### **US-30 – Buscar Questão por Código ou Enunciado**

**Cenário 1: Busca com resultado encontrado**

- **Dado que** o administrador está na tela de listagem,  
- **Quando** digitar um código ou trecho do enunciado no campo de busca e confirmar,  
- **Então** o sistema deve **exibir apenas as questões correspondentes** aos critérios pesquisados.

**Cenário 2: Busca sem resultados**

- **Dado que** o administrador realiza uma busca,  
- **Quando** não houver correspondências,  
- **Então** o sistema deve exibir a mensagem:  
  *“Nenhuma questão encontrada para os critérios informados.”*

---

### **US-31 – Exibir Tabela de Questões**

**Cenário 1: Exibição padrão**

- **Dado que** o administrador acessou a tela de listagem,  
- **Quando** a página for carregada,  
- **Então** o sistema deve exibir uma **tabela com as seguintes colunas**:  
  - Código  
  - Enunciado  
  - Tipo  
  - Dificuldade  
  - Ano  
  - Ações (*ex.: Editar, Excluir*)

**Cenário 2: Nenhuma questão cadastrada**

- **Dado que** o sistema não possui questões registradas,  
- **Quando** o administrador acessar a listagem,  
- **Então** deve ser exibida a mensagem:  
  *“Nenhuma questão cadastrada no momento.”*

---

### **US-32 – Criar Nova Questão**

**Cenário 1: Criação bem-sucedida**

- **Dado que** o administrador está na tela de cadastro de questões,  
- **Quando** preencher todos os campos obrigatórios (*enunciado, alternativas, resposta correta e metadados*),  
- **Então** o sistema deve **salvar a nova questão** e exibir a mensagem:  
  *“Questão cadastrada com sucesso.”*

**Cenário 2: Campos obrigatórios não preenchidos**

- **Dado que** o administrador tenta criar uma questão,  
- **Quando** deixar campos obrigatórios vazios ou inválidos,  
- **Então** o sistema deve exibir **mensagens de erro específicas**, indicando os campos que precisam ser corrigidos.

---

### **US-38 – Exibir Mensagens Informativas**

**Cenário 1: Operação bem-sucedida**

- **Dado que** o administrador executou uma ação (*criar, editar ou excluir*),  
- **Quando** a operação for concluída com sucesso,  
- **Então** o sistema deve exibir uma **mensagem informativa positiva**, como:  
  *“Ação concluída com sucesso.”*

**Cenário 2: Falha na operação**

- **Dado que** o administrador realiza uma ação de gerenciamento,  
- **Quando** ocorrer erro de validação ou falha no servidor,  
- **Então** o sistema deve exibir uma **mensagem de erro clara**:  
  *“Não foi possível concluir a operação. Tente novamente mais tarde.”*

---

### **US-39 – Acesso Restrito ao Administrador**

**Cenário 1: Controle de acesso**

- **Dado que** o sistema possui diferentes perfis de usuário,  
- **Quando** um usuário sem perfil administrativo tentar acessar a área de gestão de questões,  
- **Então** o sistema deve **bloquear o acesso** e **redirecioná-lo à página inicial**, exibindo a mensagem:  
  *“Acesso negado. Essa área é exclusiva para administradores.”*

**Cenário 2: Acesso válido**

- **Dado que** o usuário é administrador,  
- **Quando** acessar o módulo de gerenciamento,  
- **Então** o sistema deve **conceder acesso total** às funcionalidades de **visualização e criação de questões**.


## **Casos de Uso – Questões**

---

### **US-40 – Acessar Tela de Questões de Concurso**

**Cenário 1: Acesso autorizado**

- **Dado que** o usuário está autenticado no sistema,  
- **Quando** clicar na opção *“Questões”* na sidebar,  
- **Então** o sistema deve **carregar a tela de questões de concurso**, exibindo os **filtros** e a **área de listagem**.

**Cenário 2: Acesso negado**

- **Dado que** o usuário não está autenticado,  
- **Quando** tentar acessar a tela de questões,  
- **Então** o sistema deve **redirecionar para a tela de login** e exibir a mensagem:  
  *“Você precisa estar logado para acessar as questões.”*

---

### **US-41 – Filtrar Questões por Parâmetros**

**Cenário 1: Filtro simples aplicado**

- **Dado que** o usuário está na tela de questões,  
- **Quando** selecionar um ou mais filtros (*ex.: disciplina e banca*) e clicar em *Filtrar*,  
- **Então** o sistema deve **exibir apenas as questões** que correspondem aos filtros aplicados.

**Cenário 2: Nenhum filtro aplicado**

- **Dado que** o usuário não selecionou nenhum filtro,  
- **Quando** clicar em *Filtrar*,  
- **Então** o sistema deve **exibir todas as questões disponíveis**.

**Cenário 3: Filtro sem resultados**

- **Dado que** o usuário aplicou filtros,  
- **Quando** não existirem questões compatíveis,  
- **Então** o sistema deve exibir a mensagem:  
  *“Nenhuma questão encontrada para os filtros selecionados.”*

---

### **US-44 – Exibir Lista de Questões Conforme Filtros**

**Cenário 1: Listagem com resultados**

- **Dado que** o usuário aplicou filtros válidos,  
- **Quando** o sistema retornar questões correspondentes,  
- **Então** deve exibi-las em **cards individuais** contendo:  
  - Número da questão  
  - Disciplina e assunto  
  - Ano, banca e órgão  
  - Enunciado  
  - Alternativas de resposta

**Cenário 2: Nenhuma questão encontrada**

- **Dado que** o filtro aplicado não possui resultados,  
- **Quando** a busca for concluída,  
- **Então** deve ser exibida uma **área vazia** ou **mensagem discreta** indicando ausência de resultados.

---

### **US-45 – Marcar Alternativa e Responder Questão**

**Cenário 1: Resposta enviada com sucesso**

- **Dado que** o usuário está visualizando uma questão,  
- **Quando** selecionar uma alternativa e clicar em *Responder*,  
- **Então** o sistema deve **registrar a resposta** e exibir o **resultado da questão** (*acerto ou erro*).

**Cenário 2: Nenhuma alternativa selecionada**

- **Dado que** o usuário não marcou nenhuma alternativa,  
- **Quando** clicar em *Responder*,  
- **Então** o sistema deve exibir a mensagem:  
  *“Selecione uma alternativa antes de enviar sua resposta.”*

---

### **US-46 – Exibir Resposta Correta Após Responder**

**Cenário 1: Exibição de resultado**

- **Dado que** o usuário respondeu a questão,  
- **Quando** o sistema processar a resposta,  
- **Então** deve **exibir a**


## **Casos de Uso – Meu Painel**

---

### **US-51 – Acessar Tela de Painel de Desempenho**

**Cenário 1: Acesso autorizado**

- **Dado que** o usuário está autenticado no sistema,  
- **Quando** clicar na opção *“Meu Painel”* na sidebar,  
- **Então** o sistema deve **redirecioná-lo para a tela de painel de desempenho**, exibindo as **informações de progresso** e os **gráficos disponíveis**.

**Cenário 2: Acesso negado**

- **Dado que** o usuário não está autenticado,  
- **Quando** tentar acessar o painel de desempenho,  
- **Então** o sistema deve **redirecionar o usuário para a tela de login**, exibindo a mensagem:  
  *“Você precisa estar logado para visualizar seu desempenho.”*

---

### **US-52 – Visualizar Gráfico de Pizza com Percentual de Acertos e Erros**

**Cenário 1: Gráfico exibido corretamente**

- **Dado que** o usuário acessou o painel de desempenho,  
- **Quando** houver dados registrados de questões resolvidas,  
- **Então** o sistema deve **exibir um gráfico de pizza** mostrando o **percentual de acertos e erros**.

**Cenário 2: Sem dados para exibir**

- **Dado que** o usuário acessou o painel,  
- **Quando** não houver registros de questões resolvidas,  
- **Então** o sistema deve **exibir uma mensagem informativa**:  
  *“Nenhum dado disponível para exibição.”*

---

### **US-58 – Exibir Mensagens Informativas em Caso de Ausência de Dados**

**Cenário 1: Nenhum registro encontrado**

- **Dado que** o usuário aplicou filtros de tempo (*ex.: últimos 7 dias*) e não há registros,  
- **Quando** o sistema tentar gerar os gráficos,  
- **Então** deve exibir uma **mensagem clara**:  
  *“Nenhum dado disponível para o período selecionado.”*

**Cenário 2: Exibição padrão sem erro**

- **Dado que** o sistema carregou corretamente os dados,  
- **Quando** existirem registros,  
- **Então** as **mensagens informativas** não devem ser exibidas, apenas os **gráficos correspondentes**.

---

### **US-59 – Exibir Mensagens de Erro ao Carregar os Gráficos**

**Cenário 1: Falha na conexão com o servidor**

- **Dado que** o usuário está na tela de painel,  
- **Quando** ocorrer um erro de conexão ou falha na API de dados,  
- **Então** o sistema deve exibir uma **mensagem clara de erro**:  
  *“Não foi possível carregar os gráficos. Tente novamente mais tarde.”*

**Cenário 2: Erro inesperado no carregamento**

- **Dado que** o sistema apresentou um erro interno,  
- **Quando** o gráfico não puder ser renderizado,  
- **Então** deve exibir uma **mensagem genérica**:  
  *“Ocorreu um erro ao carregar as informações de desempenho.”*



---

## Histórico de Versão

| **Data** | **Versão** | **Descrição** | **Autor** |
| :------: | :--------: | :----------:  | :-------: |
| 17/09/2025 | 1.0 | Criação da especificação dos requisitos (MVP) | Breno Fernandes |
| 18/09/2025 | 1.1 | Adição dos cenários BDD das histórias do MVP (Acesso, Sidebar, Perfil, Configurações, CRUD, Questões) | Breno Fernandes |