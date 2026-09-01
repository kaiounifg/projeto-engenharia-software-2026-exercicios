# declaracao-escopo.md

## Declaração de Escopo — Sistema de Biblioteca do Campus

### 1. Inclusões
* **I1:** Módulo de login e permissões separadas para alunos, professores e funcionários.
* **I2:** Módulo para cadastrar e gerenciar livros, títulos e dados do acervo.
* **I3:** Módulo de circulação para controlar retiradas, devoluções e renovações de exemplares.
* **I4:** Sistema automático para calcular multas quando houver atraso na devolução.
* **I5:** Ferramenta para importar os dados antigos do sistema legado.
* **I6:** Rotina automatizada de cópias de segurança (backup) da base de dados.
* **I7:** Relatórios gerenciais para ver livros em atraso e estatísticas de uso.
* **I8:** Configuração inicial dos servidores para hospedar o sistema no ar.

### 2. Exclusões
* **E1:** Compra de leitor de código de barras ou totens de autoatendimento (*Motivo: Equipamentos de hardware são de responsabilidade da instituição, fora do escopo de código*).
* **E2:** Suporte técnico diário ou manutenção corretiva após acabar a garantia da entrega (*Motivo: Atividade de rotina que deve ficar com o setor de TI da própria faculdade*).
* **E3:** Colocar etiquetas físicas nos 12.000 livros (*Motivo: Ajuste da premissa anterior; é um trabalho manual que cabe exclusivamente à equipe da biblioteca*).
* **E4:** Contratar mais funcionários para o balcão (*Motivo: Gestão de pessoas e RH é papel exclusivo da administração da universidade*).
* **E5:** Integrar o sistema com bibliotecas de outras cidades e faculdades (*Motivo: Complexidade muito alta para o prazo inicial, deixando para uma fase futura via mudança*).

### 3. Entregas
* **D1:** Plano inicial do projeto e validação da arquitetura técnica.
* **D2:** Módulo de acervo pronto junto com a importação dos dados antigos.
* **D3:** Módulo de circulação de empréstimos com o cálculo de multas funcionando.
* **D4:** Geração dos relatórios e painéis gerenciais.
* **D5:** Configuração do ambiente de infraestrutura e rotinas de backup.
* **D6:** Treinamento prático da equipe e lançamento oficial do sistema.

### 4. Critérios de Aceitação
| Critério | Como se verifica |
| :--- | :--- |
| **C1. Importação de dados** | Rodar o script de migração e conferir se 100% dos títulos antigos aparecem corretamente na busca. |
| **C2. Registro de empréstimo** | Simular a retirada de um livro por um aluno ativo e checar se o prazo e os bloqueios funcionam. |
| **C3. Cálculo de multa** | Simular a devolução de um livro com 5 dias de atraso e ver se o valor cobrado bate com a regra da faculdade. |
| **C4. Desempenho de relatórios** | Emitir o relatório de atrasos com a base cheia e garantir que a tela abre em menos de 3 segundos. |
