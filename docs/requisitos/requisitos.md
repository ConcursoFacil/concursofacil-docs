# REQUISITOS DE SOFTWARE

## Requisitos Funcionais

Os requisitos funcionais definem o que o sistema deve fazer para atender às necessidades dos usuários.  

### Acesso e Autenticação
- **RF-01**: Cadastrar usuário.  
- **RF-02**: Realizar login de usuário.  
- **RF-03**: Recuperar senha de usuário.  

### Questões
- **RF-04**: Listar questões disponíveis.  
- **RF-05**: Filtrar questões.  
- **RF-06**: Responder questão e registrar resposta.  
- **RF-07**: Exibir feedback da resposta (certa/errada).  

### Desempenho
- **RF-08**: Exibir estatísticas básicas de acertos e erros.  
- **RF-09**: Acompanhar evolução do usuário ao longo do tempo.  

### Administração (restrito a administradores)
- **RF-10**: Gerenciar usuários (listar, editar, desativar).
- **RF-11**: Gerenciar questões (cadastrar, editar, excluir).

---

## Requisitos Não Funcionais

Os requisitos não funcionais definem restrições e características de qualidade do sistema.  

### Implementação
- **RNF-01**: O sistema deve ser desenvolvido em **Laravel (PHP 8.3)**.  
- **RNF-02**: O front-end deve utilizar **Blade** ou **Vue.js**.  
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
