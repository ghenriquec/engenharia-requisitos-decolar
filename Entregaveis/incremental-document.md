# Minimundo: Sistema de Gestão de Reservas da Companhia Aérea "Decolar"

A Companhia Aérea "Decolar" deseja um sistema de informação para apoiar a gestão das reservas de voos realizadas por seus clientes. Este sistema não é responsável por coordenar as operações diárias dos voos ou de gerenciamento de aeronaves.

Dentro da companhia, existem diversos atendentes e agentes de reservas, dos quais se deseja obter informações como: nome, endereço, telefones e, se aplicável, sua especialização em rotas ou destinos. De uma rota, é importante saber a origem, destino, e duração.

Clientes reservam seus voos através do sistema. De um cliente, é crucial obter: nome, endereço e telefones. Quando um cliente decide fazer uma reserva, um atendente verifica a disponibilidade e indica os voos e assentos disponíveis. A data em que essa reserva foi feita precisa ser registrada. Por exemplo, uma reserva pode incluir o assento 14A, que é um assento à janela próximo à asa. Cada voo tem um código específico e detalhes como origem, destino e duração. Também é importante identificar quais atendentes estão habilitados a gerenciar determinados voos ou rotas.

O atendente que realiza a reserva inicial é considerado o principal responsável por ela. No entanto, outros agentes podem ser designados para modificar detalhes específicos, se necessário. Cada reserva tem um ou mais serviços associados, como seleção de assentos ou solicitações de refeição. Cada detalhe da reserva é gerenciado por um agente específico. Esse agente é responsável por indicar os valores adicionais (se houver) e por atualizar qualquer alteração no sistema. A exclusão de detalhes de uma reserva ou a adição de novos serviços só pode ser feita pelo atendente principal responsável pela reserva. Se uma reserva já foi confirmada, não é permitido excluir nenhum dos seus detalhes.

Após a confirmação de todos os serviços e detalhes, a reserva é considerada concluída. Se uma reserva não for confirmada em até 48 horas, ela é automaticamente cancelada pelo sistema. Finalmente, o cadastro de atendentes, voos e rotas é de responsabilidade dos administradores da "Decolar", enquanto o registro de clientes é tarefa dos atendentes.

