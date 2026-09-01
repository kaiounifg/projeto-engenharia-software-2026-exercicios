# eap.md

## Estrutura Analítica de Projetos (EAP) — Tabela de Estimativas

| Nó / Pacote | Descrição do Pacote | Estimativa (Horas) |
| :--- | :--- | :--- |
| **1. Biblioteca do Campus** | **Escopo total do projeto** | **232h** |
| **1.1 Gerência do projeto** | **Coordenação e acompanhamento geral** | **40h** |
| 1.1.1 | Plano de projeto e cronograma | 24h |
| 1.1.2 | Controle de andamento e marcos | 16h |
| **1.2 Requisitos e Concepção** | **Alinhamento e levantamento inicial** | **40h** |
| 1.2.1 | Entrevistas com as servidoras | 16h |
| 1.2.2 | Documentação de requisitos | 24h |
| **1.3 Módulo de Acervo** | **Organização de títulos e dados** | **72h** |
| 1.3.1 | Cadastro de títulos e exemplares | 40h |
| 1.3.2 | Importação de dados antigos | 32h |
| **1.4 Módulo de Circulação** | **Controle do fluxo de empréstimos** | **72h** |
| 1.4.1 | Registro de empréstimo e devolução | 48h |
| 1.4.2 | Cálculo e registro de multas | 24h |
| **1.5 Módulo de Relatórios** | **Informações para a gestão** | **16h** |
| 1.5.1 | Relatório de obras em atraso | 16h |
| **1.6 Implantação e Treinamento** | **Entrega final e capacitação** | **44h** |
| 1.6.1 | Configuração de servidores e backup | 20h |
| 1.6.2 | Treinamento dos operadores | 24h |

---

## Dicionário da EAP (4 Pacotes Selecionados)

### 1. Pacote de Maior Estimativa: 1.4.1 Registro de empréstimo e devolução
* **Descrição:** Construção de toda a lógica e telas para emprestar, renovar e devolver livros aos usuários.
* **Entrega:** Módulo de Circulação pronto.
* **Responsável:** Desenvolvedor Sênior Backend.
* **Estimativa:** 48 horas.
* **Predecessor:** 1.2.2 (Especificação de requisitos).
* **Critério de Conclusão:** Tela funcionando perfeitamente, registrando saídas e entradas de livros e bloqueando usuários inadimplentes.
* **Premissas:** Regras da biblioteca já devidamente aprovadas pela coordenação.
* **Exclui:** Cálculo de multas por atraso (que fica isolado no pacote 1.4.2).

### 2. Pacote de Menor Estimativa: 1.5.1 Relatório de obras em atraso
* **Descrição:** Criação da consulta no banco e do layout em tela/PDF listando os livros com devolução vencida.
* **Entrega:** Módulo de Relatórios.
* **Responsável:** Desenvolvedor Fullstack.
* **Estimativa:** 16 horas.
* **Predecessor:** 1.4.1 (Registro de empréstimo e devolução).
* **Critério de Conclusão:** Relatório gerado com sucesso trazendo a listagem correta filtrada por data.
* **Premissas:** Banco de dados de circulação já populado e estável.
* **Exclui:** Envio de e-mails automáticos de cobrança para os usuários.

### 3. Pacote Não-Software: 1.6.2 Treinamento dos operadores
* **Descrição:** Aulas práticas presenciais com as servidoras para ensiná-las a mexer no novo sistema.
* **Entrega:** Implantação e Treinamento.
* **Responsável:** Analista de Qualidade / Suporte.
* **Estimativa:** 24 horas.
* **Predecessor:** 1.6.1 (Configuração de infraestrutura).
* **Critério de Conclusão:** Lista de presença assinada pelas servidoras e entrega do manual básico impresso.
* **Premissas:** Servidoras disponíveis nos dias marcados e ambiente rodando sem bugs críticos.
* **Exclui:** Suporte contínuo de operação após a primeira semana de lançamento.

### 4. Pacote Mais Arriscado: 1.3.2 Importação de dados legados
* **Descrição:** Desenvolvimento de script de extração e carga para puxar os 12.000 títulos do sistema antigo para o novo.
* **Entrega:** Módulo de Acervo.
* **Responsável:** Desenvolvedor Backend / DBA.
* **Estimativa:** 32 horas.
* **Predecessor:** 1.2.2 (Especificação de requisitos).
* **Critério de Conclusão:** Carga rodada no ambiente de testes sem corromper metadados importantes e com o aval da biblioteca.
* **Premissas:** Ter acesso liberado aos arquivos e formatos do banco de dados antigo.
* **Exclui:** Limpeza manual de erros de digitação ou inconsistências herdadas do sistema legado.