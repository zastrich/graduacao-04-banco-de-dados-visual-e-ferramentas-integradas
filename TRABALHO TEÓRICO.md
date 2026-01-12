## Graduação em IA e Automação Digital – 1º Semestre

### Solução No-Code para Gestão de Eventos e Beneficiários de uma ONG

## 1\. Introdução

Este trabalho descreve a concepção teórica de uma solução de banco de dados visual voltada à gestão de eventos e beneficiários de uma Organização Não Governamental (ONG). A proposta está alinhada ao uso de ferramentas No-Code, permitindo organização de dados, automações e visualizações sem a necessidade de programação tradicional.  
A solução foi desenvolvida considerando o crescimento das atividades da ONG e a necessidade de maior controle, rastreabilidade e comunicação com os beneficiários.

## 2\. Levantamento de Requisitos

O levantamento de requisitos foi realizado a partir da análise do contexto operacional da ONG, que atualmente utiliza planilhas e grupos de mensagens para controle de eventos. A ausência de uma equipe técnica motivou a escolha de uma solução visual, intuitiva e de baixo custo.

Os principais requisitos identificados foram:

- Cadastro e consulta de beneficiários.  
- Criação e gerenciamento de eventos.  
- Inscrição de beneficiários em múltiplos eventos, mantendo histórico.  
- Automação de notificações (novos eventos, cancelamentos, lembretes e confirmação de presença).  
- Disponibilização de relatórios e logs.  
- Atenção à organização, ética e segurança dos dados.

## 3\. Modelagem do Banco de Dados Visual

A modelagem conceitual foi elaborada com a ferramenta BR Modelo Web, utilizando o diagrama Entidade-Relacionamento (ER). O modelo foi projetado para representar de forma clara as entidades, seus atributos e relacionamentos, priorizando simplicidade e aderência ao contexto No-Code.

O diagrama ER está disponível publicamente em:  
[https://app.brmodeloweb.com/\#\!/publicview/695f0201318718d742587c40](https://app.brmodeloweb.com/#!/publicview/695f0201318718d742587c40)

## 4\. Estrutura Relacional

A base de dados foi estruturada em quatro tabelas principais:

- Eventos: armazena dados dos eventos, incluindo datas, status, categoria, indicadores de notificação e campos calculados.  
- Peoples: contém os dados dos beneficiários, como informações pessoais, contato, endereço e preferências de notificação.  
- Registrations: tabela associativa que representa a inscrição de beneficiários em eventos, permitindo múltiplas participações.  
- Notifications Log: registra informações sobre notificações enviadas, sem armazenar o conteúdo das mensagens.

Essa estrutura garante organização, rastreabilidade e flexibilidade para expansão futura.

## 5\. Justificativa da Ferramenta Utilizada

A ferramenta escolhida foi o Airtable, por ter sido apresentada em disciplinas do curso e oferecer recursos adequados no plano gratuito. Entre os principais motivos da escolha destacam-se:

- Interface visual intuitiva.  
- Suporte a relacionamentos entre tabelas.  
- Campos calculados e automações integradas.  
- Criação de formulários, dashboards e visualizações.


Mesmo com limitações na versão gratuita, a ferramenta atendeu bem às necessidades do projeto.

## 6\. Automações e Integrações

Foram implementadas automações para:

- Notificação de novos eventos.  
- Aviso de cancelamento.  
- Confirmação de inscrição.  
- Lembrete de eventos próximos.  
- Solicitação de confirmação de presença.

Uma automação adicional identifica quando um evento está próximo do início. Para simular integrações externas, como envio de mensagens, foi utilizada uma planilha no Google Sheets apenas para fins de consulta e validação, sem uso produtivo. (Link da planilha: [Integração Whatsapp](https://docs.google.com/spreadsheets/d/1pnh1yvBrvObXx9qH_IbfIemXwBBd39zL5vS7oem0BIw/edit?usp=sharing))

## 7\. Interfaces da Aplicação (para colaboradores)

A solução foi organizada em quatro menus principais:

- Relatórios (Dashboard e Log de Notificações)  
- Eventos (Visualização e Criação)  
- Beneficiários (Consulta e Cadastro) \+ Formulário externo ([Link para cadastro](https://airtable.com/appYPltRo0QQiAMT0/pagQf669kwlTMiqNf/form))  
- Inscrições (Consulta e Validação) \+ Formulário externo ([Link para inscrição em eventos](https://airtable.com/appYPltRo0QQiAMT0/pagJwbgBRLWYwK5cc/form))

Essas interfaces permitem uma navegação clara e facilitam o uso por colaboradores sem conhecimento técnico.

## 8\. Ética e Segurança da Informação

Durante o desenvolvimento, foram considerados princípios de ética e segurança da informação, como:

- Não armazenamento do conteúdo das mensagens enviadas.  
- Uso de campos de auditoria para rastreabilidade.  
- Controle e organização dos dados sensíveis dos beneficiários.

Essas práticas contribuem para a proteção dos dados e o uso responsável da informação.

## 9\. Conclusão

A solução proposta demonstra a viabilidade do uso de bancos de dados visuais e ferramentas No-Code para atender às necessidades de uma ONG. O modelo desenvolvido organiza informações, automatiza processos e melhora a comunicação, promovendo eficiência e transparência na gestão dos eventos e beneficiários.