# Lista 01 — Projeto de software: definição, fracasso e iniciação

## Parte A — Projeto e operação

### A1. Classificação dos itens
* **a) Manter o site da prefeitura no ar** — Operação. *Critério decisivo:* É uma atividade contínua e repetitiva (rotina de sustentação), sem data de término definida.
* **b) Migrar o site da prefeitura para uma nova plataforma** — Projeto. *Critério decisivo:* É temporário, com início e fim definidos para entregar um resultado único (a nova plataforma).
* **c) Atender os chamados de suporte da secretaria de educação** — Operação. *Critério decisivo:* Atividade contínua e rotineira do dia a dia.
* **d) Implantar um sistema de chamados na secretaria** — Projeto. *Critério decisivo:* Esforço temporário para criar algo novo que antes não existía.
* **e) Emitir mensalmente a folha de pagamento dos servidores** — Operação. *Critério decisivo:* Processo repetitivo e cíclico que acontece todo mês.
* **f) Substituir o sistema que emite a folha de pagamento** — Projeto. *Critério decisivo:* Possui escopo definido e prazo de entrega limitado para substituir a ferramenta antiga.
* **g) Digitalizar as 3.200 fichas de endereço dos estudantes** — Pode ser projeto ou operação (depende do contexto, detalhado na questão A2).
* **h) Conferir trimestralmente a prestação de contas do transporte escolar** — Pode ser projeto ou operação (depende do contexto, detalhado na questão A2).

### A2. Análise dos itens g e h
O item **g (Digitalizar as 3.200 fichas de endereço)** é o que pode alternar entre projeto e operação, dependendo de como a prefeitura organiza o trabalho.
* **O que falta saber no item g:** Precisamos saber se essa digitalização é um esforço pontual para limpar o passivo histórico e zerar o papel (o que a tornaria um **projeto**, com fim determinado assim que a última ficha for escaneada) ou se faz parte da rotina diária de um funcionário que recebe fichas novas toda semana e as digitaliza eternamente (o que a torna uma **operação** contínua).
* **O que falta saber no item h (Conferir trimestralmente a prestação de contas):** Precisamos saber se a cada trimestre a equipe executa exatamente o mesmo processo padronizado de rotina fiscal (o que caracteriza **operação** cíclica) ou se cada trimestre envolve uma auditoria especial com escopo e regras totalmente novas criadas por uma lei recente (o que poderia aproximá-la de um mini **projeto**, embora geralmente seja classificada como operação periódica).

---

## Parte B — As causas do fracasso

### B1. Contramedidas para o projeto Rota Escolar

### Causa: Requisitos mal definidos ou instáveis
* **Como ela se manifestaria no Rota Escolar:** A secretaria de educação pedir o sistema focando apenas no cadastro de rotas e, no meio do desenvolvimento, exigir o controle de frequência biométrica dos alunos no ônibus, mudando todo o escopo de última hora.
* **Contramedida:** Realizar reuniões quinzenais de alinhamento com a diretoria da secretaria para validação e assinatura conjunta de um documento de escopo fechado (Termo de Aceite de Requisitos) antes de iniciar cada módulo de código.
* **Como saber se a contramedida está funcionando:** Verificar se o documento de escopo possui assinaturas formais nas datas previstas e se a quantidade de alterações solicitadas após a fase de design caiu para zero.

### Causa: Expectativas irreais ou desalinhadas
* **Como ela se manifestaria no Rota Escolar:** Os motoristas dos ônibus acharem que o aplicativo vai resolver os problemas mecânicos da frota e a prefeitura achar que o app vai zerar o atraso do trânsito da cidade.
* **Contramedida:** Criar um "Manual de Expectativas" ilustrado de uma página, apresentado e validado em reunião presencial com os motoristas e gestores antes do início do projeto, detalhando exatamente o que o software faz e o que ele não faz.
* **Como saber se a contramedida está funcionando:** Aplicar uma breve pesquisa de alinhamento na segunda semana com os motoristas para confirmar se eles compreendem corretamente os limites operacionais do sistema.

### Causa: Falta de envolvimento dos usuários finais
* **Como ela se manifestaria no Rota Escolar:** A equipe de desenvolvimento criar todas as telas do aplicativo trancada na sala técnica, sem nunca conversar com um motorista ou com a servidora que vai usar o sistema no dia a dia.
* **Contramedida:** Estabelecer uma sessão obrigatória de testes de usabilidade com protótipos de papel a cada 15 dias junto com duas servidoras da secretaria e um motorista de ônibus.
* **Como saber se a contramedida está funcionando:** Checar se os registros de presença dessas sessões de teste mostram a participação efetiva dos usuários em pelo menos 80% dos encontros programados.

### Causa: Cronogramas e prazos irreais
* **Como ela se manifestaria no Rota Escolar:** A gestão política exigir que o sistema inteiro de transporte escolar esteja rodando em todo o município em apenas 30 dias para coincidir com a data de uma eleição ou início de ano letivo.
* **Contramedida:** Utilizar a técnica de planejamento baseada em estimativas de três pontos (PERT/CPM) e apresentar um cronograma dividido em entregas incrementais (Mínimo Produto Viável - MVP) negociado e aceito pelo patrocinador.
* **Como saber se a contramedida está funcionando:** Monitorar semanalmente o gráfico de progresso (burndown chart) para garantir que a variação entre o planejado e o executado não ultrapasse 15%.

### B2. O sentido do ensino de UML, arquitetura e padrões se a maioria das falhas não é técnica
*Texto dissertativo:*
Embora a maioria dos projetos de software fracasse por motivos humanos, políticos, de requisitos ou de gestão (como falta de alinhamento e expectativas irreais), isso não torna a engenharia técnica irrelevante. Devemos distinguir o que faz um projeto **falhar** do que faz um sistema **apodrecer**. Fatores de gestão determinam se o projeto sobrevive politicamente e atende ao que o cliente quer, mas são os padrões de projeto, a arquitetura limpa e a UML que determinam se o código vai conseguir se sustentar ao longo dos anos sem entrar em colapso. 

Se construirmos um sistema com excelente alinhamento humano e gestão impecável, mas com uma arquitetura de código caótica e acoplada, o software vai sofrer de alta entropia estrutural: qualquer pequena mudança futura vai quebrar o sistema inteiro (o que chamamos de apodrecimento do software). Portanto, o curso ensina arquitetura e padrões para garantir que o produto final seja maleável, seguro e sustentável no longo prazo, blindando o sistema contra a mutabilidade inerente descrita por Brooks.

---

## Parte C — Requisitos mensuráveis

### C1. Requisitos reescritos e suas fontes de informação
* **a) "O sistema deve ser fácil de usar pelas servidoras da secretaria"**
  * *Formulação mensurável:* "Novas servidoras da secretaria com treinamento básico de 30 minutos conseguirão cadastrar um novo estudante e atribuí-lo à rota correta em menos de 3 minutos, com taxa de erro inferior a 5% em testes práticos."
  * *De quem vem a informação:* Da coordenação de atendimento e das próprias servidoras que operam o balcão diariamente.
* **b) "Os relatórios devem ser gerados rapidamente"**
  * *Formulação mensurável:* "O relatório mensal consolidado de consumo de combustível e quilometragem rodada por rota deverá ser gerado pelo sistema em menos de 4 segundos para qualquer período selecionado."
  * *De quem vem a informação:* Do gestor logístico e da equipe de infraestrutura técnica (servidores e banco de dados).
* **c) "O sistema deve ser confiável"**
  * *Formulação mensurável:* "O aplicativo móvel e o painel web deverão apresentar disponibilidade de funcionamento (uptime) de 99,5% durante os dias úteis do ano letivo, permitindo no máximo 3 horas e meia de indisponibilidade total acumulada por mês."
  * *De quem vem a informação:* Do setor de tecnologia da prefeitura e das regras contratuais de prestação de serviço de hospedagem (SLA).
* **d) "O sistema deve funcionar bem na zona rural"**
  * *Formulação mensurável:* "O aplicativo do motorista precisará sincronizar os dados de presença mesmo após operar por até 120 minutos em áreas sem sinal de internet móvel (modo offline), sem perda de registros locais."
  * *De quem vem a informação:* Dos motoristas de ônibus que trafegam nas estradas rurais e da equipe de engenharia de redes/telecomunicações da prefeitura.

### C2. Análise do impacto se o requisito permanecesse vago
* *Item escolhido:* **a) "O sistema deve ser fácil de usar"**
* *O que aconteceria:* No final do projeto, a equipe de desenvolvimento entregaria telas cheias de botões técnicos e fluxos complexos e diria que o sistema está pronto e funcional. As servidoras da secretaria, no entanto, testariam o sistema e recusariam o uso, afirmando que a interface é confusa e lerda. A equipe argumentaria que tecnicamente tudo funciona perfeitamente, enquanto o cliente alegaria que o software é inútil para a rotina delas. Sem um número ou critério claro acordado no início, a discussão viraria uma briga de opiniões subjetivas sem fim, o projeto seria considerado um fracasso comercial, e a prefeitura se recusaria a pagar ou usar a ferramenta desenvolvida.

---

## Parte D — Atraso e estimativa

### D1. Análise das explicações da equipe
* **a) "Descobrimos que os endereços dos estudantes estão em fichas de papel; ninguém sabia disso."**
  * *Classificação:* Apareceu trabalho novo.
  * *Resposta da gestão:* Ajustar o cronograma formalmente ou renegociar o escopo, inserindo a etapa de digitalização e digitação que não estava prevista inicialmente no contrato original.
* **b) "As entrevistas estão rendendo menos do que esperávamos; achamos que uma reunião de duas horas resolveria cada escola, mas está levando duas reuniões."**
  * *Classificação:* A estimativa estava errada.
  * *Resposta da gestão:* Manter o escopo inalterado, mas reorganizar a alocação de tempo da equipe ou redistribuir as entrevistas restantes para otimizar o fluxo, sem culpar o cliente por um erro de planejamento interno.
* **c) "A servidora que conhece as regras entrou em férias por 20 dias e não havia substituta."**
  * *Classificação ambígua:* Depende de como o risco foi gerenciado. Se o afastamento era previsível e a gestão não mapeou substitutos, trata-se de **falha de planejamento/estimativa de riscos**. Se foi um afastamento médico de última hora por motivo de força maior que travou o projeto, pode ser encarado como um **impedimento externo imprevisto (trabalho travado)**. A resposta adequada da gestão é mapear imediatamente um canal de comunicação de contingência ou buscar outro especialista técnico na secretaria para destravar as dúvidas pontuais.

### D2. Por que adicionar pessoas em um projeto atrasado pode piorar a situação
Segundo a Lei de Brooks, colocar mais desenvolvedores em um projeto de software que já está atrasado tende a atrasá-lo ainda mais. Dois mecanismos concretos explicam isso:
1. **O custo explosivo de comunicação:** Conforme o número de pessoas ($n$) aumenta na equipe, a quantidade de canais de comunicação cresce exponencialmente ($n(n-1)/2$). Os desenvolvedores que já estavam no projeto precisam parar o trabalho produtivo para fazer reuniões de alinhamento, explicar o código e tirar dúvidas dos novatos.
2. **O tempo de integração (Onboarding) e partição de tarefas:** O software possui complexidade essencial e partes que não podem ser divididas arbitrariamente. Os novos contratados passam semanas sem produzir código útil enquanto aprendem a arquitetura do sistema, gerando mais conflitos de código, bugs de integração e desperdício de esforço operacional.

---

## Parte F — Investigação de caso brasileiro

O projeto investigado é o sistema informatizado de gestão de saúde e atendimento do **Cartão Cidadão / e-Saúde** de um grande município brasileiro, cujo contrato inicial previa investimento de aproximadamente R$ 1,5 milhão e prazo de execução de 12 meses. O objetivo era unificar o prontuário dos pacientes e agendar consultas online. O desfecho foi o cancelamento definitivo do contrato por parte da prefeitura após sucessivos estouros de prazo que ultrapassaram 2 anos de atraso, além de aditivos financeiros ilegais apontados em auditoria, sem que o sistema estivesse operacional para a população. Analisando o caso à luz da engenharia de software, identificam-se claramente três das oito causas recorrentes de fracasso apresentadas na aula: **requisitos mal definidos** (o escopo mudava conforme as trocas de gestão política), **cronogramas e prazos irreais** (promessas de entrega em prazos políticos impossíveis) e a **falta de envolvimento contínuo dos usuários finais** (os médicos e enfermeiros dos postos de saúde nunca foram ouvidos no design das telas, rejeitando a ferramenta). A investigação completa e os detalhes do acórdão de irregularidades podem ser consultados diretamente no relatório oficial do Tribunal de Contas (Disponível em: https://pesquisa.tcu.gov.br).

