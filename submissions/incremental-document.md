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

### Diagrama de Contexto

O Diagrama de Contexto oferece uma visualização de alto nível do sistema e suas interações com entidades externas. Ele nos ajuda a entender a fronteira do sistema e as interfaces com outros sistemas ou atores.

A seguir, é apresentada a representação gráfica do Diagrama de Contexto para o sistema de reservas:

![Diagrama de Contexto](../documentation/5%20-%20DIagrama-contexto/diagrama_contexto.jpeg)

Este diagrama destaca as principais entidades que interagem com o sistema e os fluxos de dados entre eles.

### Diagrama de Classes

O Diagrama de Classes fornece uma representação estática da estrutura do sistema, destacando as classes principais, seus atributos, métodos e os relacionamentos entre elas. É uma ferramenta essencial na modelagem orientada a objetos, oferecendo uma visão clara da arquitetura do sistema.

Abaixo está o Diagrama de Classes para o sistema de reservas:

![Diagrama de Classes](../documentation/7%20-%20Diagrama-classe/diagrama_classes.png)

Neste diagrama, as classes são representadas por retângulos, enquanto os relacionamentos são indicados por linhas conectando essas classes. Os diferentes tipos de relacionamentos (como associação, herança e composição) são denotados por símbolos específicos nas linhas.

Os atributos e métodos de cada classe são detalhados dentro dos respectivos retângulos, e a visibilidade (como público, privado ou protegido) é indicada por símbolos específicos (+, -, #).

### Diagrama de Estado

O diagrama de estado é uma ferramenta útil para modelar o comportamento de um sistema, mostrando como ele se comporta em diferentes estados e como ele muda de um estado para outro. Ele é composto por estados, transições e eventos.

![Diagrama de Estado](../documentation/4%20-%20Diagrama-estado/state_diagram.png)	

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

### Diagrama de Atividade
O diagrama de atividades é um tipo de diagrama comportamental usado na modelagem de processos de negócios e na engenharia de software para representar fluxos de trabalho e processos.

![Diagrama de Atividades](../documentation/3%20-%20Diagrama-atividade/activity-diagram.png)

## Funcionalidades Principais:

1. **Registro de Clientes**: Os atendentes têm a capacidade de registrar clientes no sistema, mantendo todos os seus detalhes relevantes para futuras reservas.
2. **Gestão de Reservas**: Permitir que atendentes verifiquem e registrem novas reservas, além de visualizar os detalhes de vôos e serviços associados a cada reserva.
3. **Serviços Adicionais**: O sistema deve permitir a seleção, adição ou remoção de serviços adicionais para as reservas, como assentos especiais, refeições e outros.
4. **Administração**: Administradores têm a capacidade de cadastrar novos vôos, rotas e detalhes relevantes ao funcionamento do sistema.
5. **Atendente de Reserva**: Cada reserva é associada a um atendente principal que tem a exclusividade de modificar detalhes dessa reserva.

## Requisitos Não Funcionais:

- **Segurança**: Privacidade e proteção dos dados dos usuários são fundamentais, bem como armazenamento seguro e backups periódicos.
- **Interface**: A usabilidade é uma prioridade, e a interface deve ser intuitiva para atendentes e clientes.
- **Performance**: O sistema deve ser rápido, capaz de suportar múltiplos acessos simultâneos e manter um tempo de resposta otimizado.
- **Disponibilidade**: O sistema deve estar disponível pelo menos 99,9% do tempo, garantindo que clientes e atendentes possam acessá-lo sempre que necessário.
- **Auditabilidade e Compatibilidade**: Todos os processos críticos devem ser rastreáveis, e o sistema deve ser compatível com os principais navegadores e dispositivos.

### Diagramas de Sequência

## 1. Registro de Clientes

**Atores**: Cliente, Atendente, Sistema de Reservas.

**Sequência**:
1. O Cliente solicita o registro ao Atendente.
2. O Atendente acessa o Sistema de Reservas e inicia o processo de registro.
3. O Sistema de Reservas solicita informações do cliente.
4. O Atendente obtém e insere as informações do Cliente.
5. O Sistema de Reservas confirma o registro e informa o Atendente.
6. O Atendente confirma o registro bem-sucedido para o Cliente.

![Diagrama de Sequência - Registro de Clientes](../documentation/6%20-%20Diagrama-sequencia/registro_clientes.png)

---

## 2. Gestão de Reservas

**Atores**: Cliente, Atendente, Sistema de Reservas.

**Sequência**:
1. O Cliente solicita uma reserva ao Atendente.
2. O Atendente acessa o Sistema de Reservas para verificar a disponibilidade dos voos.
3. O Sistema de Reservas mostra os voos disponíveis.
4. O Atendente seleciona o voo adequado e informa os detalhes ao Cliente.
5. O Cliente confirma o voo.
6. O Atendente finaliza a reserva no Sistema de Reservas.
7. O Sistema de Reservas confirma a reserva e informa o Atendente.
8. O Atendente informa o Cliente sobre a reserva bem-sucedida.

![Diagrama de Sequência - Gestão de Reservas](../documentation/6%20-%20Diagrama-sequencia/gestao_reservas.png)

---

## 3. Cancelamento de Reservas

**Atores**: Cliente, Atendente, Sistema de Reservas.

**Sequência**:
1. O Cliente solicita o cancelamento de uma reserva ao Atendente.
2. O Atendente acessa o Sistema de Reservas e busca a reserva específica.
3. O Sistema de Reservas mostra os detalhes da reserva.
4. O Atendente confirma com o Cliente os detalhes e solicita confirmação para cancelar.
5. O Cliente confirma o cancelamento.
6. O Atendente prossegue com o cancelamento no Sistema de Reservas.
7. O Sistema de Reservas confirma o cancelamento e informa o Atendente.
8. O Atendente informa o Cliente sobre o cancelamento bem-sucedido.

![Diagrama de Sequência - Cancelamento de Reservas](../documentation/6%20-%20Diagrama-sequencia/cancelamento_reservas.png)

