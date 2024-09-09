# Post Mortem

## 1. Resumo do Projeto

**Nome do Projeto:** Calculus  
**Data de Início:** 19/03/2024  
**Data de Conclusão:** 09/09/2024  
**Objetivo:**  
O objetivo do projeto Calculus era desenvolver uma plataforma de aprendizado onde professores pudessem criar conteúdos por meio de um estúdio virtual e hospedá-los na internet. A plataforma deveria ser acessível para alunos, com uma interface que permitisse aos professores gerenciar usuários, estruturar aulas e criar conteúdos facilmente.

---

## 2. Resultados Esperados vs Resultados Alcançados

| Funcionalidade              | Resultado Esperado                                     | Resultado Alcançado                                  | Comentários                                              |
|-----------------------------|--------------------------------------------------------|------------------------------------------------------|----------------------------------------------------------|
| **US01 - Criar Conta**       | Permitir que novos usuários criem contas               | Entregue e validado                                  | Não é possível criar conta via Microsoft na aplicação pois o deployment está em http                         |
| **US02 - Login**             | Login de usuários com autenticação segura              | Entregue e validado                                  | O login via microsoft só funcionará no deploy quando a hospedagem passar de http para https                                    |
| **US03 - Gerenciar Roles**   | Sistema de gerenciamento de papéis de usuários         | Entregue e validado                                  | Atende às expectativas                                    |
| **US04 - Recuperar Conta**   | Recuperação de senhas via e-mail                       | Entregue e validado                                  | Sem problemas                                            |
| **US05 - Estúdio de Criação**| Ambiente virtual para criação de aulas                 | Entregue e validado                                  | Atende as necessidades do produto, porém o PO deixou o comentário de que a interface poderia ser mais bonita, mesmo assim ele aceitou a história de usuário                        |
| **US06 - Gerenciar Jornada** | Permitir que professores criem jornadas de aprendizagem| Entregue e validado                                  | Usabilidade dentro do esperado                           |
| **US07 - Gerenciar Trilha**  | Gestão de trilhas de aprendizagem                     | Entregue e validado                                  | Funcionalidade implementada com sucesso                   |
| **US08 - Visualização de Trilhas**| Alunos visualizarem suas trilhas de aprendizado   | Entregue e validado                                  | Sem falhas encontradas                                    |
| **US09 - Visualizar HomePage**| Página inicial para usuários                          | Entregue e validado                                  | Interface intuitiva                                      |
| **US10 - Visualizar Conteúdo**| Acesso ao conteúdo de aprendizagem                     | Entregue e validado                                  | Todos os recursos funcionais                              |
| **US11 - Gerenciar Pontos de Partida**| Gestão dos pontos de início em jornadas       | Entregue e validado                                  | Implementado corretamente                                |

**Conclusão sobre os Resultados:**  
Todas as funcionalidades planejadas foram entregues e validadas pelo Product Owner (PO). O projeto atendeu às expectativas sem falhas críticas.

---

## 3. Aspectos Positivos

1. **Proatividade da Equipe:**  
   Os membros do time mostraram grande compromisso em relação ao projeto, buscando resolver problemas de forma independente.
   
2. **Melhoria na Comunicação:**  
   Embora a comunicação tenha sido um desafio no início, houve uma evolução significativa durante o projeto, especialmente nas fases finais.
   
3. **Ferramentas Apropriadas:**  
   As tecnologias escolhidas, como Nest.js, Next.js, MongoDB, Docker, e SonarQube, foram eficazes no desenvolvimento da aplicação e controle da qualidade do código.

---

## 4. Aspectos Negativos

1. **Greve Acadêmica:**  
   Uma greve que durou aproximadamente 45 dias impactou gravemente o andamento do projeto, atrasando o cronograma e paralisando os trabalhos por um longo período.

2. **Falta de Engajamento Inicial:**  
   No início, houve uma falta de engajamento por parte de alguns membros da equipe, o que prejudicou a velocidade do desenvolvimento. Este problema foi parcialmente resolvido na fase final.

3. **Atrasos no Escopo:**  
   Alterações no escopo de algumas histórias, especialmente próximo à release MVP, causaram atrasos na entrega. A mudança no escopo da última sprint foi significativa e levou a uma reavaliação das prioridades.

4. **Problemas Técnicos:**  
   Alguns integrantes não tinham equipamentos adequados no início do projeto, o que dificultou o desenvolvimento inicial da aplicação.

5. **Falta de Orçamento:**  
   Muitos recursos utilizados, especialmente os relacionados ao deploy, eram pagos. Como o projeto não tinha orçamento, os custos foram cobertos pelos próprios membros da equipe, o que limitou algumas escolhas tecnológicas.

---

## 5. Lições Aprendidas

1. **Comunicação é Fundamental:**  
   Um dos maiores aprendizados foi que uma comunicação eficaz é crucial para o sucesso de qualquer projeto. Melhorar esse aspecto mais cedo poderia ter evitado vários problemas.
   
2. **Engajamento Antecipado:**  
   O esforço para engajar todos os membros da equipe desde o início é essencial para garantir que o trabalho seja distribuído de forma mais equitativa e que o projeto avance conforme o planejado.

3. **Reuniões Constantes com o PO:**  
   As reuniões frequentes com o Product Owner (PO) foram fundamentais para alinhar as expectativas e garantir que as histórias estivessem bem definidas, além de ajudar a ajustar o escopo quando necessário.

---

## 6. Oportunidades de Melhoria

1. **Escopo de Testes:**  
   Mais atenção poderia ser dada ao planejamento de testes, especialmente testes automatizados, para garantir maior qualidade e evitar problemas na fase de deploy.

2. **Orçamento para o Deploy:**  
   Uma estratégia de deploy mais robusta poderia ser implementada caso houvesse um orçamento alocado para essa parte do projeto, o que tornaria o processo mais eficiente.

3. **Incluir um Especialista em UX/UI:**  
   A adição de um membro focado exclusivamente em UX/UI traria uma experiência de usuário mais refinada e ajudaria a tornar a plataforma mais atraente visualmente.

4.  **US06 - Gerenciar Jornada e US11 - Gerenciar Pontos de Partida**
   Ambas histórias de usuário, em sua interface, existe um espaço que foi designado para se colocar imagens. Hoje, na entrega do projeto, este campo está com uma imagem genérica, não permitindo a mudança pela usuário. Uma oportunidade de melhoria seria adicionar uma funcionalidade para que o usuário possa adicionar qualquer imagem às jornadas e aos pontos de partida.

5. **Troca de protocólo de comunicação**
   A aplicação está sendo entregue com seu deployment feito a partir de uma máquina virtual, hospedada no Microsoft Azure. Dito isso, foi feita uma abertura de rede e exposição dessa máquina na internet, para que usuários externos possam interagir com a aplicação. Esta abertura de portas e rotas para intenet foi executada de tal forma que só é possível se comunicar com a aplicação por meio do protocólo HTTP. Isso abre espaço para adição de um certificado SSL/TLS, o que permitirá comunicação segura com a porta 443 (padrão TCP/IP) e consequentemente o uso do protocólo HTTPS.
   

---

## 7. Conclusão

Apesar dos desafios enfrentados, o projeto Calculus foi considerado um sucesso. Todas as funcionalidades planejadas foram entregues e validadas, e a equipe conseguiu superar problemas técnicos, organizacionais e financeiros. As lições aprendidas durante este processo serão fundamentais para futuros projetos.

---

## 8. Agradecimentos

Gostaríamos de expressar nossa gratidão aos professores **Vinicius Rispolli** e **Hilmer Neri**, que acompanharam o desenvolvimento deste projeto e forneceram orientações valiosas para seu sucesso. Também gostaríamos de agradecer pela participação e comprometimento de todos da equipe de EPS e MDS, responsáveis por desenvolver e gerenciar a aplicação fim-a-fim. Por último, agradecer a Universidade de Brasília por condicionar o ambiente de aprendizado.

## 9. Histórico de Versão
| Data       | Versão | Descrição             | Autor(es)                          |
|------------|--------|-----------------------|------------------------------------|
| 08/09/2024 | 1.0    | Criação do Documento  | Paulo Henrique Gontijo |
