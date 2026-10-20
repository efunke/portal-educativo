---
status: Modelo para preenchimento
subtitle: Template educacional para documentação da arquitetura de
  sistemas
title: Modelo de System Design
version: 1.0
---

# System Design --- \[Nome do sistema\]

> **Orientação aos estudantes:** use este documento para registrar as
> decisões de arquitetura do sistema proposto. Substitua os textos entre
> colchetes pelas informações do projeto. Quando uma decisão ainda não
> estiver definida, registre-a como **Pendente** e explique o que
> precisa ser investigado. Não escolha tecnologias apenas por
> familiaridade: justifique-as com base nos requisitos e nas restrições.

## Controle do documento

  Campo                        Preenchimento
  ---------------------------- --------------------------------------
  Projeto                      \[Nome do projeto\]
  Disciplina / turma           \[Disciplina e turma\]
  Autor(es)                    \[Nomes dos integrantes\]
  Professor(a)                 \[Nome\]
  Versão                       \[0.1\]
  Data da última atualização   \[AAAA-MM-DD\]
  Situação                     \[Rascunho / Em revisão / Aprovado\]

## 1. Resumo executivo

**Objetivo:** explicar o sistema em linguagem clara para alguém que
ainda não conhece o projeto.

\[Descreva em um ou dois parágrafos o problema, quem será atendido, a
solução proposta e o principal benefício.\]

## 2. Problema e contexto

### 2.1 Problema a resolver

\[Qual dificuldade, necessidade ou oportunidade motivou o sistema? Como
esse problema é tratado atualmente?\]

### 2.2 Contexto de uso

\[Onde e em que situações o sistema será utilizado? Há sistemas
existentes com os quais deverá interagir?\]

### 2.3 Objetivos

-   **Objetivo geral:** \[Resultado principal esperado.\]
-   **Objetivos específicos:** \[Liste resultados verificáveis.\]

### 2.4 Fora do escopo

\[Registre o que o sistema não pretende resolver nesta versão. Isso
ajuda a controlar o tamanho do projeto.\]

## 3. Stakeholders e usuários

  Perfil                   Necessidades / responsabilidades   Permissões principais
  ------------------------ ---------------------------------- -----------------------
  \[Ex.: estudante\]       \[O que precisa realizar\]         \[Ações permitidas\]
  \[Ex.: professor\]       \[O que precisa realizar\]         \[Ações permitidas\]
  \[Ex.: administrador\]   \[O que precisa realizar\]         \[Ações permitidas\]

## 4. Requisitos

### 4.1 Requisitos funcionais (RF)

Descreva **o que** o sistema deve fazer. Use identificadores únicos e
critérios verificáveis.

  ----------------------------------------------------------------------------
  ID                Requisito         Prioridade             Critério de
                                                             aceitação
  ----------------- ----------------- ---------------------- -----------------
  RF-001            \[O sistema deve  \[Alta/Média/Baixa\]   \[Como comprovar
                    permitir...\]                            que foi
                                                             atendido\]

  RF-002            \[O sistema       \[Alta/Média/Baixa\]   \[Condição
                    deve...\]                                objetiva de
                                                             sucesso\]
  ----------------------------------------------------------------------------

### 4.2 Requisitos não funcionais (RNF)

Descreva qualidades e restrições, preferencialmente de forma mensurável.

  ---------------------------------------------------------------------------
  ID                Categoria          Requisito / meta  Como verificar
  ----------------- ------------------ ----------------- --------------------
  RNF-001           Segurança          \[Ex.: senhas     \[Teste ou
                                       armazenadas com   inspeção\]
                                       hash seguro\]     

  RNF-002           Desempenho         \[Ex.: resposta   \[Teste de
                                       em até X segundos carga/medição\]
                                       para cenário      
                                       definido\]        

  RNF-003           Acessibilidade     \[Meta e padrão   \[Verificação\]
                                       aplicável\]       

  RNF-004           Disponibilidade    \[Meta, se        \[Medição\]
                                       aplicável\]       

  RNF-005           Manutenibilidade   \[Critério        \[Revisão/testes\]
                                       adotado\]         
  ---------------------------------------------------------------------------

### 4.3 Restrições e premissas

-   **Restrições:** \[Tecnologias obrigatórias, orçamento, prazo,
    ambiente, regras institucionais.\]
-   **Premissas:** \[Condições consideradas verdadeiras para planejar a
    solução.\]
-   **Dependências:** \[Serviços, APIs, infraestrutura ou equipes
    externas.\]

## 5. Casos de uso e fluxos principais

Para cada fluxo importante, informe o ator, as condições iniciais, o
caminho normal e as exceções.

### UC-001 --- \[Nome do caso de uso\]

-   **Ator:** \[Quem inicia o fluxo.\]
-   **Pré-condições:** \[O que precisa ser verdadeiro antes.\]
-   **Fluxo principal:**
    1.  \[Ação do usuário.\]
    2.  \[Resposta do sistema.\]
    3.  \[Resultado esperado.\]
-   **Exceções / alternativas:** \[Erros, validações ou caminhos
    alternativos.\]
-   **Pós-condições:** \[Estado final esperado.\]

**Diagrama sugerido:** caso de uso UML ou diagrama de atividade, quando
ajudar a esclarecer o fluxo.

## 6. Visão arquitetural

### 6.1 Estilo arquitetural escolhido

\[Ex.: monólito modular, cliente-servidor, arquitetura em camadas,
microsserviços ou arquitetura orientada a eventos.\]

**Justificativa:** \[Explique por que o estilo atende ao porte do
projeto, aos requisitos, à equipe e às restrições. Compare ao menos uma
alternativa.\]

### 6.2 Diagrama de contexto

Insira um diagrama que mostre o sistema, os usuários e os sistemas
externos com os quais ele se comunica.

\[Inserir diagrama de contexto --- por exemplo, C4 nível 1.\]

### 6.3 Diagrama de contêineres / componentes

Mostre os principais blocos executáveis e responsabilidades, como
interface web, API, banco de dados e serviços externos.

\[Inserir diagrama de contêineres --- por exemplo, C4 nível 2 --- ou
diagrama de componentes.\]

### 6.4 Descrição dos componentes

  -----------------------------------------------------------------------------
  Componente         Responsabilidade       Tecnologia        Comunicação
                                            candidata         
  ------------------ ---------------------- ----------------- -----------------
  \[Interface\]      \[Responsabilidade\]   \[Tecnologia e    \[HTTP, eventos
                                            justificativa\]   etc.\]

  \[API / backend\]  \[Responsabilidade\]   \[Tecnologia e    \[Protocolo\]
                                            justificativa\]   

  \[Persistência\]   \[Armazenamento e      \[Tecnologia e    \[Driver /
                     consultas\]            justificativa\]   protocolo\]

  \[Serviço          \[Responsabilidade, se \[Fornecedor /    \[API etc.\]
  externo\]          houver\]               tecnologia\]      
  -----------------------------------------------------------------------------

## 7. Modelo e fluxo de dados

### 7.1 Entidades principais

\[Liste entidades centrais, seus atributos relevantes e relações. Evite
listar cada campo antes de compreender o domínio.\]

  Entidade         Finalidade             Relações importantes
  ---------------- ---------------------- ----------------------
  \[Entidade A\]   \[O que representa\]   \[Relacionamentos\]
  \[Entidade B\]   \[O que representa\]   \[Relacionamentos\]

### 7.2 Modelo de dados

\[Inserir diagrama entidade-relacionamento ou modelo equivalente.
Identifique chaves, cardinalidades e restrições relevantes.\]

### 7.3 Fluxo de dados principal

Descreva como os dados passam do usuário pelos componentes e retornam
como resultado.

1.  \[Origem / evento inicial.\]
2.  \[Validação e processamento.\]
3.  \[Consulta ou gravação.\]
4.  \[Resposta e tratamento de falhas.\]

\[Inserir diagrama de sequência ou fluxo de dados, se útil.\]

### 7.4 Dados sensíveis e ciclo de vida

\[Identifique dados pessoais ou sensíveis, finalidade de uso, retenção,
exclusão, controle de acesso e medidas de proteção aplicáveis. Colete
apenas o necessário.\]

## 8. Interfaces e contratos de API

Preencha esta seção se o sistema expuser ou consumir APIs.

  ----------------------------------------------------------------------------------
  Método         Endpoint           Finalidade         Autenticação   Respostas /
                                                                      erros
                                                                      principais
  -------------- ------------------ ------------------ -------------- --------------
  \[GET\]        \[/api/recurso\]   \[Consultar...\]   \[Sim/Não e    \[200, 401,
                                                       mecanismo\]    404...\]

  \[POST\]       \[/api/recurso\]   \[Criar...\]       \[Sim/Não e    \[201, 400,
                                                       mecanismo\]    409...\]
  ----------------------------------------------------------------------------------

Para cada endpoint relevante, documente: - Parâmetros, corpo da
requisição e formato da resposta. - Validações e regras de negócio. -
Códigos de sucesso e de erro. - Autorização exigida, limites de uso e
versionamento, se necessário.

**Contrato sugerido:** OpenAPI para APIs HTTP.

## 9. Segurança, privacidade e conformidade

-   **Autenticação:** \[Como a identidade será verificada.\]
-   **Autorização:** \[Como serão controladas as permissões.\]
-   **Proteção de dados:** \[Criptografia em trânsito e em repouso,
    quando aplicável.\]
-   **Segredos:** \[Como serão armazenadas chaves, tokens e credenciais;
    nunca incluí-los no repositório.\]
-   **Validação de entrada:** \[Como reduzir entradas inválidas e
    ataques comuns.\]
-   **Auditoria:** \[Eventos que precisam ser registrados, evitando
    registrar segredos.\]
-   **Privacidade:** \[Finalidade, minimização, retenção e descarte de
    dados.\]
-   **Riscos conhecidos:** \[Risco, impacto, mitigação e risco
    residual.\]

Considere a LGPD e as políticas institucionais quando houver tratamento
de dados pessoais. Não declare conformidade sem verificar os requisitos
aplicáveis.

## 10. Implantação e infraestrutura

### 10.1 Ambientes

  Ambiente               Finalidade                   Configurações / serviços
  ---------------------- ---------------------------- --------------------------
  Desenvolvimento        \[Construção local\]         \[Serviços\]
  Testes / homologação   \[Validação\]                \[Serviços\]
  Produção               \[Uso real, se aplicável\]   \[Serviços\]

### 10.2 Diagrama de implantação

\[Mostre onde os componentes serão executados, as conexões, os limites
de confiança e os serviços externos.\]

### 10.3 Configuração e entrega

-   **Empacotamento:** \[Ex.: processo ou contêineres.\]
-   **Configuração:** \[Variáveis de ambiente e configurações por
    ambiente.\]
-   **CI/CD:** \[Etapas de validação, testes e publicação.\]
-   **Migrações de banco:** \[Como serão aplicadas e revertidas.\]
-   **Gestão de segredos:** \[Mecanismo adotado.\]

## 11. Observabilidade e operação

-   **Logs:** \[O que registrar, formato e acesso.\]
-   **Métricas:** \[Indicadores técnicos e de negócio relevantes.\]
-   **Rastreamento:** \[Como acompanhar requisições entre componentes,
    se necessário.\]
-   **Alertas:** \[Condições que exigem atenção.\]
-   **Backup e recuperação:** \[O que será copiado, frequência, retenção
    e teste de restauração.\]
-   **Manutenção:** \[Atualizações, dependências e resposta a
    incidentes.\]

Para projetos acadêmicos pequenos, explique quais itens serão
implementados agora e quais são apenas recomendações futuras.

## 12. Estratégia de testes

  -----------------------------------------------------------------------
  Tipo de teste           O que verifica          Evidência / ferramenta
  ----------------------- ----------------------- -----------------------
  Unitário                \[Unidade isolada\]     \[Testes\]

  Integração              \[Comunicação entre     \[Testes\]
                          componentes\]           

  API / contrato          \[Contratos e           \[Testes\]
                          respostas\]             

  Ponta a ponta           \[Fluxo do usuário\]    \[Testes\]

  Segurança               \[Riscos prioritários\] \[Verificações\]

  Desempenho              \[Metas relevantes\]    \[Medições, se
                                                  aplicável\]

  Acessibilidade /        \[Uso por públicos      \[Avaliação\]
  usabilidade             diversos\]              
  -----------------------------------------------------------------------

**Critérios de conclusão:** \[Defina condições para considerar a versão
pronta, incluindo requisitos atendidos, defeitos conhecidos e
documentação.\]

## 13. Decisões arquiteturais (ADR)

Registre decisões importantes para que outras pessoas compreendam o
motivo e as consequências.

### ADR-001 --- \[Título da decisão\]

-   **Status:** \[Proposta / Aceita / Substituída / Rejeitada\]
-   **Contexto:** \[Qual problema ou necessidade motivou a decisão?\]
-   **Decisão:** \[O que foi escolhido?\]
-   **Alternativas consideradas:** \[Quais opções foram comparadas?\]
-   **Consequências positivas:** \[Benefícios.\]
-   **Consequências negativas / riscos:** \[Custos, limitações e
    compromissos.\]
-   **Data e responsáveis:** \[Data e autores.\]

Repita este bloco para cada decisão relevante.

## 14. Trade-offs e alternativas

  -------------------------------------------------------------------------
  Questão           Alternativa       Alternativas      Motivo /
                    escolhida         consideradas      compromisso
                                                        assumido
  ----------------- ----------------- ----------------- -------------------
  \[Ex.: banco de   \[Escolha\]       \[Outras opções\] \[Justificativa
  dados\]                                               baseada nos
                                                        requisitos\]

  \[Ex.:            \[Escolha\]       \[Outras opções\] \[Justificativa\]
  arquitetura\]                                         
  -------------------------------------------------------------------------

Explique não apenas por que a escolha parece boa, mas também em quais
condições outra opção poderia ser melhor.

## 15. Riscos, limitações e evolução

  ---------------------------------------------------------------------------------
  Risco / limitação Probabilidade          Impacto                Mitigação /
                                                                  próximo passo
  ----------------- ---------------------- ---------------------- -----------------
  \[Descrição\]     \[Baixa/Média/Alta\]   \[Baixo/Médio/Alto\]   \[Ação\]

  ---------------------------------------------------------------------------------

### Evolução prevista

-   **MVP / primeira versão:** \[Capacidades mínimas.\]
-   **Próxima versão:** \[Melhorias priorizadas.\]
-   **Fora do planejamento atual:** \[Ideias que não serão executadas
    agora.\]

## 16. Plano de implementação

  -------------------------------------------------------------------------
  Etapa             Entregável          Dependências      Critério de
                                                          conclusão
  ----------------- ------------------- ----------------- -----------------
  1\. Descoberta    \[Problema,         \[Nenhuma /       \[Critério\]
                    usuários e          outras\]          
                    requisitos\]                          

  2\. Projeto       \[Diagramas e       \[Etapa 1\]       \[Critério\]
                    decisões\]                            

  3\. MVP           \[Funcionalidades   \[Projeto\]       \[Critério\]
                    essenciais\]                          

  4\. Validação     \[Testes e          \[MVP\]           \[Critério\]
                    avaliação\]                           

  5\. Entrega       \[Documentação e    \[Validação\]     \[Critério\]
                    demonstração\]                        
  -------------------------------------------------------------------------

## 17. Referências e glossário

### Referências

-   \[Documentação técnica, padrões, artigos ou materiais consultados.\]
-   \[Inclua título, autoria/organização, data e URL quando
    disponível.\]

### Glossário

  Termo / sigla   Definição no contexto do projeto
  --------------- ----------------------------------
  \[API\]         \[Definição\]
  \[MVP\]         \[Definição\]
  \[Outro\]       \[Definição\]

## 18. Checklist de revisão

Antes da entrega, verifique:

-   [ ] O problema e os usuários estão claramente definidos.
-   [ ] Os requisitos funcionais têm critérios de aceitação
    verificáveis.
-   [ ] Os requisitos não funcionais são mensuráveis quando possível.
-   [ ] A arquitetura está representada em diagramas legíveis.
-   [ ] Cada componente tem responsabilidade definida.
-   [ ] O fluxo e o modelo de dados são coerentes com os requisitos.
-   [ ] APIs e integrações têm contratos descritos.
-   [ ] Segurança, privacidade e dados sensíveis foram considerados.
-   [ ] As decisões principais incluem alternativas e justificativas.
-   [ ] Os riscos e as limitações estão explícitos.
-   [ ] O plano de testes cobre os fluxos essenciais.
-   [ ] Não há senhas, tokens ou dados pessoais reais no documento.
-   [ ] Os diagramas e textos estão atualizados e têm legendas.
-   [ ] As referências utilizadas foram registradas.

------------------------------------------------------------------------

## Orientação final ao estudante

Um bom System Design não é uma lista de tecnologias nem precisa ser
excessivamente complexo. Ele deve demonstrar que você compreendeu o
problema, identificou requisitos e restrições, propôs uma arquitetura
coerente e consegue justificar as principais decisões. Adapte a
profundidade do documento ao tamanho e aos riscos do sistema. Registre
incertezas honestamente em vez de inventar informações.
