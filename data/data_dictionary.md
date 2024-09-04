# Dicionário de Dados

## Tabela: `Users`
Armazena informações básicas sobre os usuários.

| Campo              | Tipo de Dado   | Descrição                                           | Exemplo           |
|--------------------|----------------|-----------------------------------------------------|-------------------|
| `user_id`          | INTEGER         | Identificação única do usuário.                    | 12345             |
| `signup_date`      | DATE            | Data de cadastro do usuário.                        | 2023-01-15        |
| `last_active_date` | DATE            | Data da última atividade do usuário.                | 2024-08-30        |
| `subscription_type`| VARCHAR(50)     | Tipo de assinatura do usuário (free, premium, etc.).| premium           |

## Tabela: `Usage`
Histórico de uso do aplicativo pelos usuários.

| Campo            | Tipo de Dado   | Descrição                                        | Exemplo           |
|------------------|----------------|--------------------------------------------------|-------------------|
| `user_id`        | INTEGER         | Identificação única do usuário.                 | 12345             |
| `activity_date`  | DATE            | Data da atividade registrada.                   | 2024-08-01        |
| `activity_type`  | VARCHAR(50)     | Tipo de atividade (login, contratação, avaliação, etc.).| login         |

## Tabela: `Transactions`
Registros de transações realizadas na plataforma.

| Campo            | Tipo de Dado   | Descrição                                        | Exemplo           |
|------------------|----------------|--------------------------------------------------|-------------------|
| `user_id`        | INTEGER         | Identificação única do usuário.                 | 12345             |
| `transaction_date`| DATE           | Data da transação realizada.                    | 2024-08-15        |
| `amount`         | DECIMAL(10,2)   | Valor da transação.                             | 49.99             |

## Notas Adicionais:

- **Tipos de Dados**:
  - `INTEGER`: Números inteiros.
  - `DATE`: Datas no formato YYYY-MM-DD.
  - `VARCHAR(n)`: Texto com até `n` caracteres.
  - `DECIMAL(p,s)`: Números decimais com `p` dígitos no total e `s` dígitos após o ponto decimal.

- **Relacionamentos**:
  - `user_id` nas tabelas `Usage` e `Transactions` refere-se ao `user_id` na tabela `Users`.
