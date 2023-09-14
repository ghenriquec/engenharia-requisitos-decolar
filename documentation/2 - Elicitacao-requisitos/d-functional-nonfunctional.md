# Requisitos Funcionais e Não Funcionais
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

---