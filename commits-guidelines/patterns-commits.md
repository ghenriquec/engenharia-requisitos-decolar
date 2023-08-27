# Padronização de Commits para o Projeto.
## Estrutura Básica do Commit:

```
<tipo>(<escopo>): <mensagem curta>
<linha em branco>
<descrição detalhada (opcional)>
```

## Tipos:
- **docs**: Alterações na documentação
- **update**: Atualizações ou adições a um documento
- **fix**: Correções em um documento

## Escopo:
Indica a seção ou tópico específico da documentação que a alteração afeta, como "requisitos", "diagrama", "definição", etc.

## Mensagem Curta:
- Deve ser direta e clara.
- Use o presente do indicativo: "update" em vez de "updated" ou "updates".
- Não use ponto no final.

## Descrição Detalhada (opcional):
- Fornece uma justificação mais detalhada do commit.
- Use "-" para listar várias justificações ou detalhes.

## Exemplos:

1. Adicionando um novo tópico à documentação de requisitos:
```
docs(requisitos): add tópico sobre reserva
- Detalha o processo de reserva.
- Descreve critérios de elegibilidade.
```

2. Corrigindo erros na seção de Diagrama de Atividade:
```
fix(diagrama): correção de erros no Diagrama de Atividade
- Ajusta fluxo incorreto entre atividades.
- Corrige nomeações inconsistentes.
```

3. Atualizando a descrição na seção de Minimundo:
```
update(minimundo): melhoria na descrição dos agentes de reserva
- Fornece mais detalhes sobre as responsabilidades dos agentes.
```
