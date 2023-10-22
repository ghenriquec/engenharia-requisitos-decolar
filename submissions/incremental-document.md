# Minimundo: Sistema de Gestão de Reservas da Companhia Aérea "Decolar"

A Companhia Aérea "Decolar" deseja um sistema de informação para apoiar a gestão das reservas de voos realizadas por seus clientes. Este sistema não é responsável por coordenar as operações diárias dos voos ou de gerenciamento de aeronaves.

Dentro da companhia, existem diversos atendentes e agentes de reservas, dos quais se deseja obter informações como: nome, endereço, telefones e, se aplicável, sua especialização em rotas ou destinos. De uma rota, é importante saber a origem, destino, e duração.

Clientes reservam seus voos através do sistema. De um cliente, é crucial obter: nome, endereço e telefones. Quando um cliente decide fazer uma reserva, um atendente verifica a disponibilidade e indica os voos e assentos disponíveis. A data em que essa reserva foi feita precisa ser registrada. Por exemplo, uma reserva pode incluir o assento 14A, que é um assento à janela próximo à asa. Cada voo tem um código específico e detalhes como origem, destino e duração. Também é importante identificar quais atendentes estão habilitados a gerenciar determinados voos ou rotas.

O atendente que realiza a reserva inicial é considerado o principal responsável por ela. No entanto, outros agentes podem ser designados para modificar detalhes específicos, se necessário. Cada reserva tem um ou mais serviços associados, como seleção de assentos ou solicitações de refeição. Cada detalhe da reserva é gerenciado por um agente específico. Esse agente é responsável por indicar os valores adicionais (se houver) e por atualizar qualquer alteração no sistema. A exclusão de detalhes de uma reserva ou a adição de novos serviços só pode ser feita pelo atendente principal responsável pela reserva. Se uma reserva já foi confirmada, não é permitido excluir nenhum dos seus detalhes.

Após a confirmação de todos os serviços e detalhes, a reserva é considerada concluída. Se uma reserva não for confirmada em até 48 horas, ela é automaticamente cancelada pelo sistema. Finalmente, o cadastro de atendentes, voos e rotas é de responsabilidade dos administradores da "Decolar", enquanto o registro de clientes é tarefa dos atendentes.

# Elicitação de Requisitos "Decolar"

## Requisitos Funcionais:

| Identificador | Descrição                                                                                                 | Prioridade | Requisitos Relacionados |
|---------------|-----------------------------------------------------------------------------------------------------------|------------|-------------------------|
| RF1           | Permitir o registro de clientes com nome, endereço e telefones.                                          | Alta       |                         |
| RF2           | Permitir que atendentes verifiquem a disponibilidade de voos e assentos.                                 | Alta       | RF4, RF5                |
| RF3           | Registrar a data da reserva.                                                                              | Alta       |                         |
| RF4           | Mostrar os detalhes dos voos, incluindo origem, destino e duração.                                       | Alta       | RF2                     |
| RF5           | Permitir a seleção de serviços adicionais, como seleção de assentos ou solicitações de refeição.         | Média      | RF2, RF6                |
| RF6           | Atualizar valores adicionais com base nos serviços selecionados.                                          | Média      | RF5                     |
| RF7           | Restringir a exclusão ou adição de serviços a reservas confirmadas.                                       | Média      | RF6                     |
| RF8           | Cancelar automaticamente reservas não confirmadas após 48 horas.                                          | Média      | RF3                     |
| RF9           | Permitir que administradores cadastrem atendentes, voos e rotas.                                          | Alta       |                         |
| RF10          | Identificar e associar atendentes a reservas específicas como responsáveis.                               | Alta       | RF1, RF2                |

## Requisitos Não Funcionais:

| Identificador | Descrição                                                                                                 | Prioridade | Requisitos Relacionados |
|---------------|-----------------------------------------------------------------------------------------------------------|------------|-------------------------|
| RNF1          | O sistema deve garantir a privacidade e segurança dos dados pessoais dos clientes.                        | Alta       |                         |
| RNF2          | A interface do sistema deve ser intuitiva e fácil de usar para atendentes e administradores.             | Alta       |                         |
| RNF3          | O sistema deve ser capaz de suportar pelo menos 1.000 usuários simultâneos.                              | Alta       |                         |
| RNF4          | Todos os dados do sistema devem ser armazenados em servidores seguros e com backup regular.              | Alta       |                         |
| RNF5          | O tempo de resposta para verificação de disponibilidade não deve exceder 5 segundos.                      | Média      | RF2                     |
| RNF6          | Deve haver um suporte 24/7 disponível para quaisquer problemas técnicos.                                 | Média      |                         |
| RNF7          | O sistema deve garantir uma disponibilidade de 99,9% do tempo.                                           | Alta       |                         |
| RNF8          | Todos os processos críticos devem ser auditáveis.                                                        | Média      |                         |
| RNF9          | O sistema deve ser compatível com os principais navegadores da web e dispositivos móveis.                | Média      |                         |
| RNF10         | O sistema deve ser escalável, permitindo a adição de novos recursos ou módulos no futuro.                | Média      |                         |

### Priorização dos Requisitos

A priorização foi baseada na importância imediata do requisito para os usuários e no impacto que teria no negócio. Por exemplo, o cadastro de atendentes e rotas é prioritário, pois sem essas informações, o sistema não teria utilidade.

### Verificação e Validação dos Requisitos

Todos os requisitos foram verificados para assegurar que são consistentes, completos, relevantes e realizáveis. A validação foi feita por meio de revisões com as partes interessadas para garantir que os requisitos atendem às suas necessidades e expectativas.

### Requisitos Especiais 
### SR1: Conformidade com Regulamentações Aéreas
- **Descrição**: O sistema deve estar em conformidade com todas as regulamentações aéreas nacionais e internacionais pertinentes.
- **Justificação**: Garantir que a companhia aérea "Decolar" opere de acordo com todas as leis e regulamentações aplicáveis.

### SR2: Acessibilidade
- **Descrição**: O sistema deve ser acessível para usuários com deficiências, seguindo padrões de acessibilidade, como WCAG.
- **Justificação**: Proporcionar uma experiência inclusiva para todos os usuários, além de cumprir possíveis regulamentações de acessibilidade.

### SR3: Multi-idioma
- **Descrição**: O sistema deve oferecer suporte em vários idiomas, incluindo, no mínimo, Português, Inglês e Espanhol.
- **Justificação**: Atender a uma base diversificada de clientes que podem ter preferências linguísticas diferentes.

### SR4: Reservas para Menores Desacompanhados
- **Descrição**: O sistema deve incluir uma opção especial para a reserva de menores que viajam sem a companhia de um adulto.
- **Justificação**: Certos regulamentos e políticas se aplicam a menores desacompanhados, e a companhia aérea precisa garantir que essas reservas sejam tratadas adequadamente.

### SR5: Backup e Recuperação de Desastres
- **Descrição**: O sistema deve ter um plano de backup robusto e capacidades de recuperação de desastres.
- **Justificação**: As informações de reserva são críticas para a operação da companhia aérea. A perda desses dados pode resultar em sérias repercussões financeiras e de reputação.

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
| RNF6 | Deve haver um suporte 24/7... | TNF006 | Suporte | Média | Guilherme Henrique | Em andamento | - |
| RNF7 | O sistema deve garantir uma disponibilidade... | TNF007 | Disponibilidade | Alta | Isabela Gontijo | Em andamento | - |
| RNF8 | Todos os processos críticos devem ser auditáveis. | TNF008 | Auditoria | Média | Arthur Azalim | Em andamento | - |
| RNF9 | O sistema deve ser compatível com os principais... | TNF009 | Compatibilidade | Média | João Gabriel | Em andamento | - |
| RNF10 | O sistema deve ser escalável... | TNF010 | Escalabilidade | Média | Rafael Farreira | Em andamento | - |

