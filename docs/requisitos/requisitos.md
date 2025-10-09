# REQUISITOS DE SOFTWARE

## Requisitos Funcionais

Os requisitos funcionais definem o que o sistema deve fazer para atender às necessidades dos usuários.  

### Acesso e Autenticação  
- **RF-01**: Cadastrar usuário.  
- **RF-02**: Realizar login de usuário.  
- **RF-03**: Recuperar senha de usuário.  
- **RF-04**: Verificar código de recuperação.  
- **RF-05**: Redefinir senha de usuário.  

### Sidebar
- **RF-06**: Ter uma sidebar fixa na lateral do sistema.
- **RF-07**: Na sidebar haverá botões para acesso às telas: Questões, Dashboard, Configurações, Meus Cadernos, CRUD Questões e Meu Painel.
- **RF-08**: Exibir o nome e a foto do usuário logado na parte superior da sidebar.
- **RF-09**: Destacar o botão da tela atual em que o usuário se encontra.
- **RF-10**: Permitir recolher ou expandir a sidebar conforme o tamanho da tela.

### Perfil
- **RF-11**: Ter uma tela de perfil do usuário.
- **RF-12**: Exibir foto, nome completo e cargo/função do usuário.
- **RF-13**: Exibir informações pessoais na aba “Sobre”, como educação, habilidades e notas.
- **RF-14**: Possuir abas “Cadernos” e “Questões”.
- **RF-15**: Na aba “Cadernos”, mostrar a lista de cadernos e a quantidade de questões em cada um.
- **RF-16**: Na aba “Questões”, exibir a quantidade de questões resolvidas e comentadas.
- **RF-17**: Permitir alternar entre as abas “Cadernos” e “Questões”.

### Configurações
- **RF-18**: Ter uma tela de configurações da conta do usuário.
- **RF-19**: Possuir abas “Alterar dados da conta”, “Alterar senha” e “Excluir minha conta”.
- **RF-20**: Permitir que o usuário edite nome, e-mail, educação, habilidades, profissão e notas.
- **RF-21**: Exigir a senha atual para confirmar alterações nos dados da conta.
- **RF-22**: Permitir que o usuário altere sua senha informando a atual, a nova e a confirmação.
- **RF-23**: Exibir mensagem de sucesso ou erro após salvar as alterações.
- **RF-24**: Permitir que o usuário exclua sua conta de forma permanente.
- **RF-25**: Exibir alerta de confirmação antes da exclusão da conta.

### CRUD de Questões (Admin)
- **RF-35**: Ter uma tela para listagem, busca e gerenciamento de questões.
- **RF-36**: Permitir buscar questões por código ou trecho do enunciado.
- **RF-37**: Exibir tabela com colunas: código, enunciado, tipo, dificuldade, ano e ações.
- **RF-38**: Permitir criar, editar e excluir questões.
- **RF-39**: Exibir confirmação antes de excluir uma questão.
- **RF-40**: Atualizar automaticamente a lista após exclusão ou edição.
- **RF-41**: Possuir paginação exibindo até 10 questões por página.
- **RF-42**: Exibir mensagem quando nenhuma questão for encontrada.
- **RF-43**: Permitir criar novas questões informando enunciado, alternativas, resposta correta e dados complementares (disciplina, dificuldade, ano etc.).
- **RF-44**: Exibir mensagem de sucesso ao criar, editar ou excluir uma questão.
- **RF-45**: Restringir o acesso dessa tela apenas a usuários administradores.

### Questões
- **RF-26**: Ter uma tela para exibir e responder questões de concurso.
- **RF-27**: Possuir filtros para buscar questões por disciplina, banca, instituição, ano, cargo, nível, área e dificuldade.
- **RF-28**: Permitir filtrar questões por status (todas, resolvidas, não resolvidas, acertei, errei).
- **RF-29**: Permitir marcar filtros adicionais como inéditas, anuladas, com gabarito comentado ou comentários.
- **RF-30**: Exibir lista de questões conforme os filtros selecionados.
- **RF-31**: Permitir ao usuário marcar uma alternativa e responder à questão.
- **RF-32**: Exibir a resposta correta após o envio da resposta.
- **RF-33**: Permitir visualizar o gabarito comentado e os comentários de cada questão.
- **RF-34**: Permitir adicionar novos comentários sem recarregar a página.

### Meu Painel
- **RF-46**: Ter uma tela de painel para exibir o desempenho do usuário.
- **RF-47**: Exibir gráfico de pizza mostrando o percentual de acertos e erros.
- **RF-48**: Permitir filtrar os dados do gráfico por período (hoje, 7 dias, 30 dias, sempre).
- **RF-49**: Exibir gráfico de área mostrando a quantidade de questões respondidas ao longo do tempo.
- **RF-50**: Permitir filtrar o histórico de resoluções por período (último ano, mês ou semana).
- **RF-51**: Exibir gráfico de barras horizontais mostrando a taxa de acertos por disciplina.
- **RF-52**: Atualizar os gráficos dinamicamente conforme os filtros selecionados.
- **RF-53**: Exibir mensagens informativas caso não haja dados no período selecionado.

### Meus Cadernos (expansão pós-MVP)

- **RF-54**: Ter uma tela para visualização e gerenciamento de cadernos de estudo.
- **RF-55**: Permitir criar novos cadernos informando apenas o nome.
- **RF-56**: Exibir tabela com os cadernos criados, mostrando nome e opções de ação.
- **RF-57**: Permitir excluir cadernos existentes com confirmação.
- **RF-58**: (Planejado) Permitir editar o nome de um caderno.
- **RF-59**: (Planejado) Permitir acessar as questões vinculadas a um caderno.
- **RF-60**: Exibir mensagens de sucesso ou erro ao criar ou excluir um caderno.
- **RF-61**: (Planejado) Integrar com a tela de questões para adicionar questões a um caderno.

### Meus Simulados (expansão pós-MVP)
- **RF-62**: Ter uma tela para visualização e gerenciamento de simulados criados pelo usuário.
- **RF-63**: Permitir criar novos simulados selecionando disciplinas e quantidade de questões por disciplina.
- **RF-64**: Exibir tabela com os simulados criados, mostrando nome, progresso e percentual de acertos.
- **RF-65**: Permitir excluir simulados existentes com confirmação.
- **RF-66**: (Planejado) Permitir editar simulados já criados.
- **RF-67**: (Planejado) Exibir e responder questões de um simulado, uma por vez.
- **RF-68**: (Planejado) Exibir resultado final do simulado com gráficos de desempenho.
- **RF-69**: (Planejado) Permitir revisar as questões após finalizar o simulado.
- **RF-70**: (Planejado) Sortear questões aleatoriamente conforme as disciplinas escolhidas.

---

## Requisitos Não Funcionais

Os requisitos não funcionais definem restrições e características de qualidade do sistema.  

### Implementação
- **RNF-01**: O sistema deve ser desenvolvido em **Laravel 12x (PHP 8.3)**.  
- **RNF-02**: O front-end deve utilizar **Vue.js**.  
- **RNF-03**: O banco de dados deve ser **MySQL/MariaDB**.  

### Usabilidade
- **RNF-04**: A interface deve ser simples, clara e responsiva.  

### Confiabilidade
- **RNF-05**: O sistema deve salvar corretamente as respostas dos usuários e seus simulados.  

---

## Histórico de Versão

| **Data** | **Versão** | **Descrição** | **Autor** |
| :------: | :--------: | :----------:  | :-------: |
| 17/09/2025 | 1.0 | Criação dos requisitos de software | Breno Fernandes |
| 08/10/2025 | 1.1 | Adicionados novos requisitos funcionais e simplificação das seções de cada módulo (Sidebar, Perfil, Configurações, Questões, CRUD, Painel, Cadernos e Simulados) | Breno Fernandes |