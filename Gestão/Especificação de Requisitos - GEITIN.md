# **Especificação de Requisitos – GEITIN**

## **1\. Introdução**

### **1.1. Propósito**

Este documento tem como objetivo delinear os requisitos funcionais e não funcionais para o desenvolvimento da aplicação **GEITIN**, uma plataforma colaborativa de gestão de projetos com foco em ciclos de entregas, feedback da equipe e visualização do progresso via quadro interativo (QCE). O documento visa garantir que o produto final esteja alinhado aos objetivos dos usuários e às exigências técnicas.

### **1.2. Escopo**

A aplicação **GEITIN** permitirá aos usuários:

* Criar e gerenciar projetos com descrição e equipe associada.

* Dividir projetos em ciclos de trabalho com entregas e responsáveis.

* Registrar feedbacks periódicos via formulário.

* Visualizar progresso por meio do **Quadro de Ciclo de Entregas (QCE)**, com status colorido e percentuais.

* Armazenar e acessar documentos pertinentes ao projeto (TAP, EAP, atas, diagramas), com envio ou link.

* Enviar lembretes via e-mail para preenchimento de feedbacks (integração futura via WhatsApp ou Drive).

### **1.3. Definições**

* **Projeto**: entidade principal contendo suas entregas, ciclos, equipe e documentos.

* **Ciclo**: período de trabalho dentro de um projeto, com entregas específicas.

* **Entrega**: tarefa ou atividade atribuída a um usuário dentro de um ciclo.

* **QCE (Quadro de Ciclo de Entregas)**: interface visual que mostra progresso em forma de grid colorido com percentuais (0, 25, 50, 75, 100%).

* **Feedback**: avaliação periódica da equipe sobre seu desempenho e status da entrega.

* **TAP/EAP**: Termo de Abertura do Projeto / Estrutura Analítica do Projeto — documentos importantes que podem ser enviados ou linkados.

### **1.4. Referências**

* [Documentação oficial do Django](https://docs.djangoproject.com/pt-br/5.2)

* Guias de metodologias ágeis simplificadas. Além disso, a fim de entender melhor os conceitos de gestão, nos baseamos em documentos tais como a [monografia](https://www.dropbox.com/scl/fi/zrsb3giyt6o3ck2u3hpq8/Monografia2014-AnaPaulaFerreiraSoares-Gestao_de_Projetos_de_Pesquisa_Desenvolvimento_e_Inovacao_nos_Laboratorios_da_CoppeUFRJ-MONOGRAFIA_vfinalRevisada.pdf?rlkey=979h5z4wpywpou22g0vntzrc2&dl=0) sobre gestão de projetos  nos laboratórios da Coppe realizada pela Ana Paula Ferreira Soares.

* Aplicação [GerOndApp](https://github.com/lucas-noblat/GerOndApp) produzida anteriormente.

---

## **2\. Descrição Geral**

### **2.1. Perspectiva do Produto**

A aplicação será uma ferramenta de autogestão para equipes acadêmicas ou de inovação, permitindo que visualizem e atualizem juntos o progresso dos projetos de forma intuitiva, leve e visual.

### **2.2. Funções do Produto**

* Registro de projetos com campos descritivos e upload de documentação.

* Criação de ciclos dentro dos projetos.

* Definição de entregas/subentregas com responsáveis, prazos e percentuais.

* Formulário de feedback para capturar indicadores de dedicação, progresso e percepção do prazo.

* QCE visual com sinais de status codificado por cores.

* Upload ou link de documentos associados.

* Envio manual de lembretes por e-mail para preenchimento dos feedbacks.

### **2.3. Características dos Usuários**

Público principal: estudantes, pesquisadores e membros de equipes que buscam acompanhar ciclos de trabalho de forma colaborativa e organizada, sem a complexidade de metodologias formais.

### **2.4. Restrições**

* Implementação com Django \+ Tailwind \+ JS, MySQL ou PostgreSQL.

* Deve funcionar em navegadores modernos (Chrome, Firefox).

* Interface intuitiva e responsiva.

---

## **3\. Requisitos Específicos**

### **3.1. Requisitos Funcionais**

* **RF01**: Permitir criação de projetos com nome, descrição e equipe.

* **RF02**: Dentro do projeto, permitir criação de ciclos com entregas associadas.

* **RF03**: Atribuir a cada entrega: responsável, data prevista, percentual, e possibilidade de edição.

* **RF04**: Registrar feedback via formulário com campos: dedicação (%), sensação do cronograma, status (% concluído), e data prevista de finalização.

* **RF05**: Exibir o **QCE**, com entregas codificadas por cores conforme o progresso (0‑25‑50‑75‑100%).

* **RF06**: Permitir upload ou vinculação de documentos (TAP, EAP, atas, diagramas).

* **RF07**: Enviar lembretes por e-mail (inicialmente) para preenchimento de feedback. (Posteriormente os formulários serão enviados e recebidos via Whatsapp Business API).

### **3.2. Requisitos Não Funcionais**

* **RNF01**: Backend em Django, banco MySQL ou PostgreSQL; frontend com Tailwind e JS.

* **RNF02**: Servir estáticos com WhiteNoise via Gunicorn. (Configuração para programador)

* **RNF03**: Segurança via autenticação Django e roles (admin, gerente, membro).

* **RNF04**: Estrutura modular com apps separados (projects, cycles, feedbacks, documents).

* **RNF05**: Documentos devem ser armazenados de forma segura (limitados por acesso do projeto).

---

## **4\. Modelos**

### **4.1. Diagrama de Casos de Uso**

*Inserir diagrama aqui ilustrando interações de usuário com o sistema (ex: usuário cadastra projeto; usuário cria ciclo; usuário envia feedback; usuário visualiza QCE).*

