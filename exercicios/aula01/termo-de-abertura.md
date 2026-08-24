# Termo de Abertura do Projeto (Project Charter)
**Projeto:** Sistema de Gestão do Acervo e Empréstimos da Biblioteca Universitária (Opção 1)

## 1. Justificativa
A biblioteca do campus universitário atende 4.000 estudantes e 12.000 títulos de acervo utilizando atualmente um sistema desktop legado desenvolvido em 2009. Esse sistema roda em uma única máquina física, não possui nenhum mecanismo de backup automatizado e o fornecedor original encerrou as atividades há anos. Essa situação gera um risco institucional gravíssimo de perda total do banco de dados bibliográfico em caso de pane física do computador, além de filas presenciais e impossibilidade de consulta remota do acervo pelos estudantes. A modernização é indispensável para garantir a segurança patrimonial da universidade e a agilidade no atendimento acadêmico.

## 2. Objetivo
Desenvolver e implantar um novo sistema web moderno, seguro e centralizado para gestão do acervo e controle de empréstimos da biblioteca, substituindo o software legado até o final do semestre letivo atual, garantindo migração de 100% dos dados históricos e redundância automatizada de backup em nuvem.

## 3. Resultados esperados mensuráveis
* **M1 (Migração):** 100% dos registros de livros e histórico de usuários do sistema legado de 2009 serão migrados para a nova base de dados sem perda de registros até a data de virada de chave.
* **M2 (Desempenho):** O tempo de registro de um empréstimo ou devolução no balcão não ultrapassará 15 segundos por atendimento.
* **M3 (Segurança/Backup):** O sistema executará rotinas automáticas diárias de backup do banco de dados na nuvem, com tempo de recuperação em caso de desastre (RTO) inferior a 2 horas.
* **M4 (Acessibilidade):** Os 4.000 estudantes do campus conseguirão consultar a disponibilidade de títulos remotamente de forma simultânea, suportando picos de até 100 acessos concorrentes sem lentidão perceptível.

## 4. Escopo preliminar e exclusões explícitas
* **O que está incluído no escopo:**
  * Módulo de cadastro e consulta de títulos e exemplares do acervo.
  * Módulo de controle de empréstimos, devoluções e renovações para os 3 servidores e 4.000 estudantes.
  * Painel de controle de multas e prazos de atraso.
  * Ferramenta de migração automatizada dos dados antigos.
* **Exclusões explícitas (O que NÃO será feito neste projeto):**
  * Integração com catálogos de bibliotecas externas de outros campi ou universidades federais de fora da instituição.
  * Sistema de pagamento online de multas via cartão de crédito (as multas serão registradas apenas de forma controlada no sistema para baixa presencial na tesouraria ou balcão).
  * Aplicativo móvel nativo dedicado (o sistema será acessível de forma responsiva via navegador web em smartphones e computadores).

## 5. Marcos previstos
* **Março:** Conclusão do levantamento de requisitos e mapeamento do banco de dados legado de 2009.
* **Abril:** Entrega da primeira versão prototipada para testes das 3 servidoras da biblioteca.
* **Maio:** Conclusão da migração de dados e homologação do sistema em ambiente de testes.
* **Junho:** Treinamento final das servidoras, virada de chave oficial e desativação do sistema antigo de 2009.

## 6. Restrições
* O orçamento técnico é limitado aos recursos de hardware e infraestrutura de servidores já disponíveis na TI do campus.
* O prazo de entrega é estrito e inegociável, devendo coincidir com o período de recesso acadêmico de julho para evitar impacto no fluxo de empréstimos durante as aulas.
* A equipe de desenvolvimento conta apenas com os recursos humanos alocados na disciplina, sem contratação externa de pessoal.

## 7. Premissas
* O computador atual que abriga o sistema de 2009 funcionará de forma estável o suficiente para permitir a exportação completa dos arquivos de dados legados no início do projeto.
* As 3 servidoras da biblioteca terão disponibilidade de pelo menos 2 horas semanais para participar de reuniões de validação de regras de negócio.
* A equipe de TI do campus concederá as permissões de acesso ao servidor de homologação web dentro do prazo previsto no cronograma.

## 8. Riscos iniciais
* **Risco 1:** O formato de exportação de dados do sistema legado de 2009 ser proprietário ou corrompido, impossibilitando a migração automática limpa. (*Mitigação:* Realizar um teste de exportação nas primeiras duas semanas de projeto).
* **Risco 2:** Resistência operacional das 3 servidoras em abandonar a interface antiga à qual estão habituadas há mais de 15 anos. (*Mitigação:* Envolvê-las ativamente desde o design inicial das telas e realizar treinamentos práticos antecipados).
* **Risco 3:** Indisponibilidade de infraestrutura de rede da universidade durante a semana de implantação.

## 9. Interessados (Stakeholders)
* **As 3 servidoras da biblioteca:** Usuárias operacionais cotidianas do sistema de balcão.
* **Os 4.000 estudantes do campus:** Usuários finais que consultam acervos e realizam empréstimos.
* **A Direção do Campus / Reitoria:** Patrocinadores institucionais interessados na modernização tecnológica.
* **O responsável pelo Patrimônio da Instituição:** *[Interessado frequentemente esquecido]* — Responsável legal pela integridade física e inventário dos 12.000 títulos que compõem o patrimônio público da universidade registrado nos livros contábeis.
* **A equipe de Suporte de TI do Campus:** Responsável por manter a infraestrutura de servidores e rede onde o novo sistema vai rodar.

---

## E2. Leitura crítica do termo de abertura

* **Premissa de maior impacto:** A premissa de que *"o computador atual que abriga o sistema de 2009 funcionará de forma estável o suficiente para permitir a exportação completa dos dados"*. Se esta premissa for falsa e o computador queimar de vez antes de exportarmos os arquivos, perderemos todo o histórico de cadastros e o acervo digitalizado, forçando a equipe a redigitar 12.000 títulos manualmente do zero, o que destruiria o cronograma do projeto.
* **Seção com maior dificuldade de escrita:** A seção de **Exclusões Explícitas**, pois exige definir limites claros e admitir o que o sistema *não* vai fazer, o que evidencia que ainda não compreendo completamente se a universidade exigirá obrigatoriamente pagamentos online integrados ou se o escopo enxuto proposto atenderá a todas as normativas de auditoria interna da instituição.
* **Pergunta ao patrocinador:** Se eu tivesse acesso direto ao patrocinador (Direção do Campus), eu perguntaria: *"Existe verba ou previsão institucional para adquirir leitores de código de barras novos para o balcão, ou o sistema precisa obrigatoriamente funcionar integrado apenas com a digitação manual de teclado e mouse que as servidoras usam hoje?"*

