### Matriz de Rastreabilidade de Requisitos

#### 1. Requisitos de Alto Nível → Requisitos Detalhados

| ID  | Descrição  | Fonte | ID Requisito Detalhado(s) | Entrega da EAP | Prioridade | Responsável | Comentários |
|-----|------------|-------|---------------------------|----------------|------------|-------------|-------------|
| RAL001 | Registro de clientes | Documento | RF1 | Registro de Clientes | Alta | João Gabriel | - |
| RAL002 | Verificação de disponibilidade de voos e assentos | Documento | RF2, RF4, RF5 | Reservas | Alta | Rafael Farreira | - |
| RAL003 | Registro da data da reserva | Documento | RF3 | Data de Reserva | Alta | Guilherme Henrique | - |
| RAL004 | Gerenciamento de serviços adicionais | Documento | RF5, RF6, RF7 | Serviços Adicionais | Média | Isabela Gontijo | - |
| RAL005 | Cancelamento de reservas | Documento | RF8 | Cancelamento | Média | Arthur Azalim | - |
| RAL006 | Cadastro de atendentes e voos | Documento | RF9 | Administração | Alta | João Gabriel | - |
| RAL007 | Associação de atendentes a reservas | Documento | RF10 | Atendente de Reserva | Alta | Rafael Farreira | - |

#### 2. Requisitos Detalhados → Testes

| ID  | Descrição  | ID Teste(s) | Entrega da EAP | Prioridade | Responsável | Status | Comentários |
|-----|------------|-------------|----------------|------------|-------------|--------|-------------|
| RF1 | Permitir o registro de clientes... | T001 | Registro de Clientes | Alta | Guilherme Henrique | Em andamento | - |
| RF2 | Permitir que atendentes verifiquem... | T002 | Reservas | Alta | Isabela Gontijo | Em andamento | - |
| RF3 | Registrar a data da reserva. | T003 | Data de Reserva | Alta | Arthur Azalim | Em andamento | - |
| RF4 | Mostrar os detalhes dos voos... | T004 | Reservas | Alta | João Gabriel | Em andamento | - |
| RF5 | Permitir a seleção de serviços adicionais... | T005 | Serviços Adicionais | Média | Rafael Farreira | Em andamento | - |
| RF6 | Atualizar valores adicionais... | T006 | Serviços Adicionais | Média | Guilherme Henrique | Em andamento | - |
| RF7 | Restringir a exclusão ou adição de serviços... | T007 | Serviços Adicionais | Média | Isabela Gontijo | Em andamento | - |
| RF8 | Cancelar automaticamente reservas... | T008 | Cancelamento | Média | Arthur Azalim | Em andamento | - |
| RF9 | Permitir que administradores cadastrem... | T009 | Administração | Alta | João Gabriel | Em andamento | - |
| RF10 | Identificar e associar atendentes... | T010 | Atendente de Reserva | Alta | Rafael Farreira | Em andamento | - |

#### 3. Requisitos Não Funcionais → Testes

| ID  | Descrição  | ID Teste(s) | Entrega da EAP | Prioridade | Responsável | Status | Comentários |
|-----|------------|-------------|----------------|------------|-------------|--------|-------------|
| RNF1 | O sistema deve garantir a privacidade... | TNF001 | Segurança | Alta | Guilherme Henrique | Em andamento | - |
| RNF2 | A interface do sistema deve ser intuitiva... | TNF002 | Interface | Alta | Isabela Gontijo | Em andamento | - |
| RNF3 | O sistema deve ser capaz de suportar... | TNF003 | Performance | Alta | Arthur Azalim | Em andamento | - |
| RNF4 | Todos os dados do sistema devem ser armazenados... | TNF004 | Segurança e Backup | Alta | João Gabriel | Em andamento | - |
| RNF5 | O tempo de resposta para verificação... | TNF005 | Performance | Média | Rafael Farreira | Em andamento | RF2 |
| RNF6 | Deve haver um suporte 24/7... | TNF006 | Suporte | Média | Guilher

me Henrique | Em andamento | - |
| RNF7 | O sistema deve garantir uma disponibilidade... | TNF007 | Disponibilidade | Alta | Isabela Gontijo | Em andamento | - |
| RNF8 | Todos os processos críticos devem ser auditáveis. | TNF008 | Auditoria | Média | Arthur Azalim | Em andamento | - |
| RNF9 | O sistema deve ser compatível com os principais... | TNF009 | Compatibilidade | Média | João Gabriel | Em andamento | - |
| RNF10 | O sistema deve ser escalável... | TNF010 | Escalabilidade | Média | Rafael Farreira | Em andamento | - |

Os nomes dos responsáveis foram atribuídos aleatoriamente conforme instruído.