# RESPOSTAS.md

## Parte A — Escopo do produto e escopo do projeto

### A1. Classificação e Justificativa dos Itens
* **a) Tela de registro de empréstimo:** Escopo do produto, pois é a interface funcional com que o usuário vai interagir no dia a dia.
* **b) Migração dos 12.000 títulos do sistema antigo:** Escopo do projeto, já que é um trabalho essencial para deixar tudo pronto, mas não é um código novo sendo criado do zero.
* **c) Compra de leitores de código de barras:** Exclusão. Aquisição de hardware fica totalmente fora do desenvolvimento do software.
* **d) Treinamento das 3 servidoras:** Escopo do projeto, visto que é um serviço de capacitação essencial para garantir que o pessoal saiba usar a ferramenta.
* **e) Relatório de obras em atraso:** Escopo do produto, pois trata-se de um recurso de informação entregue diretamente pelas funcionalidades do sistema.
* **f) Manutenção do sistema no ano seguinte à entrega:** Exclusão. Esse tipo de suporte contínuo pós-garantia pertence à operação rotineira, e não ao projeto em si.
* **g) Etiquetagem física dos 12.000 exemplares:** Exclusão. É um trabalho manual e físico que cabe unicamente à equipe interna da biblioteca.
* **h) Cálculo de multa por atraso:** Escopo do produto, afinal é uma regra de negócio automatizada integrada ao coração do software.
* **i) Contratação de uma quarta servidora:** Exclusão. Trata-se de uma questão burocrática de gestão de pessoas e RH da instituição.
* **j) Backup automatizado da base:** Escopo do projeto. É um requisito técnico de infraestrutura pensado para blindar a integridade dos dados.

### A2. Decisões Pendentes
Os itens **c** (compra de leitores) e **i** (contratação de nova servidora) dependem diretamente de verba, orçamento e de um sinal verde da Diretoria Administrativa da instituição.

---

## Parte B — Declaração de Escopo (Item B2)

### B2. Diálogo sobre a exclusão da etiquetagem física
* **Sem a exclusão registrada (gerando confusão no terceiro mês):**
  — *Gerente de Projeto:* "O sistema tá pronto, mas agora precisamos colar as etiquetas de código de barras nos 12.000 livros para poder inaugurar."
  — *Chefe da Biblioteca:* "Espera aí! Isso era papel da equipe de vocês de desenvolvimento. A gente não tem gente para fazer isso."
  — *Gerente de Projeto:* "Isso nunca foi combinado, o contrato fala só do software."
  — *Chefe da Biblioteca:* "Pois sem as etiquetas o sistema não roda na prática. Assim o projeto falhou!"

* **Com a exclusão já registrada e alinhada:**
  — *Gerente de Projeto:* "Lembrando da nossa exclusão E3, a etiquetagem física dos exemplares é responsabilidade total da equipe da biblioteca."
  — *Chefe da Biblioteca:* "Tranquilo, nossa equipe de bolsistas já está finalizando essa parte em paralelo para sincronizar com a entrega do módulo."

---

## Parte C — EAP e Dicionário (Item C3)

### C3. Verificação da EAP
1. **Atribuição de Responsável:** Sim, cada pacotinho de trabalho tem um dono bem definido (seja um desenvolvedor, analista ou técnico de infra).
2. **Critério de Conclusão Concreto:** Sim, dá para olhar para algo físico ou digital e cravar se terminou (código rodando, testes passando, documento assinado).

---

## Parte D — Escopo crescente

### D1. Cálculo do Esforço Não Planejado
* Somando as horas dos pedidos que foram entrando: $3 + 10 + 14 + 8 + 22 + 26 + 12 = 95\text{ horas}$.
* Convertendo isso para semanas de trabalho (considerando uma média de 30 horas semanais produtivas):
  $$\frac{95\text{ horas}}{30\text{ horas/semana}} \approx 3,16\text{ semanas de trabalho}$$

### D2. Análise do Acúmulo de Mudanças
Nenhum dos sete pedidos, olhado de forma isolada, parecia um monstro que justificasse parar o projeto ou brigar por prazo. O problema é que, como iam sendo aprovados "na hora" sem burocracia, esse gotejamento constante foi consumindo silenciosamente mais de três semanas inteiras de fôlego da equipe. Quando a conta chegou na semana 18, o estrago no cronograma já estava feito de forma invisível.

### D3. Registro de Mudanças
| Semana | Pedido | Esforço | Impacto Acumulado | Status |
| :--- | :--- | :--- | :--- | :--- |
| 3 | Campo de observação | 3 h | 3 h | Aprovado |
| 5 | Exportar lista em Excel | 10 h | 13 h | Aprovado |
| 7 | Filtro por área | 14 h | 27 h | Aprovado |
| 9 | Etiqueta com logo | 8 h | 35 h | Aprovado |
| 11 | Histórico de empréstimos | 22 h | 57 h | Aprovado |
| 13 | Aviso por e-mail | 26 h | 83 h | Aprovado |
| 16 | Relatório semestral | 12 h | 95 h | Aprovado |

**Como a conversa da semana 18 teria sido diferente:** Com esse histórico na mão, a equipe poderia mostrar com dados concretos que o atraso não foi corpo mole, mas sim o reflexo de quase 100 horas de melhorias extras que foram aceitas ao longo do caminho.

---

## Parte E — Solicitação de Mudança

### E1. Formulário de Mudança
* **Data:** 31/08/2026
* **Solicitante:** Coordenação de Pós-Graduação
* **Descrição:** Permitir o controle de empréstimos integrados entre bibliotecas de outras instituições parceiras, com prazos e regrinhas próprias.
* **Justificativa:** Dar mais acesso a acervos externos para os pesquisadores da pós-graduação.
* **Item de Escopo Afetado:** Módulo de Circulação e Empréstimos.
* **Análise de Impacto:**
  * **Esforço:** Cerca de 45 horas extras de código.
  * **Prazo:** Aumento de aproximadamente 1,5 semanas no cronograma.
  * **Custo:** Custo proporcional pelo tempo a mais da equipe alocada.
  * **Outros Itens:** Exige alterações estruturais no banco de dados.
  * **Riscos Introduzidos:** Instabilidade na comunicação com servidores de fora e falhas de sincronia.
  * **Requisitos Afetados:** Lógicas de multa e tempo limite de retenção de livros.
* **Recomendação da Equipe:** Sugerimos recusar para este momento ou negociar mais prazo e corte de outra funcionalidade equivalente.

### E2. Instância Decisória
Quem deve bater o martelo é o **Comitê de Controle de Mudanças (ou a Gerência junto com o Patrocinador)**, pois mexe diretamente com prazo e custo além da nossa autonomia. Como o impacto é alto, essa mudança exige reabrir o termo de abertura do projeto.

---

## Parte F — Investigação de EAP Real

Analisando um documento de termo de referência de um sistema acadêmico público encontrado em portais de compras, percebi que a estrutura deles costuma se basear mais em **fases do ciclo de vida** (como desenvolvimento, testes e homologação) do que em entregas diretas de valor, o que costuma gerar uma certa confusão na hora de cobrar resultados parciais. Vi que eles incluem sim itens que não são software puro, a exemplo de treinamentos e confecção de manuais, com a gerência de projeto aparecendo como uma atividade transversal de apoio. O maior gargalo desse tipo de EAP pública é que ela foca demais em etapas burocráticas de engenharia em vez de se dividir em pedaços menores que o usuário possa testar de forma independente.
