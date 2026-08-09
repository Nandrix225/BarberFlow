# Requisitos do Sistema

## Nome do Produto

BarberFlow

---

# Objetivo

Desenvolver um CRM simples, moderno e intuitivo para pequenas barbearias.

O sistema deve ajudar no gerenciamento de clientes, agendamentos e histórico de atendimentos sem exigir conhecimento técnico do usuário.

---

# Público-Alvo

Pequenas barbearias com:

- 1 a 3 barbeiros
- Até 500 clientes cadastrados
- Operação baseada em WhatsApp, agenda física ou planilhas

---

# Problemas que o Sistema Resolve

- Perda de informações de clientes
- Dificuldade para localizar histórico de atendimentos
- Falta de organização dos agendamentos
- Esquecimento de horários marcados
- Falta de visão geral do negócio

---

# Requisitos Funcionais

## RF01 - Gestão de Clientes

O sistema deve permitir:

- Cadastrar clientes
- Editar clientes
- Excluir clientes
- Pesquisar clientes
- Visualizar histórico do cliente

### Dados do Cliente

- ID
- Nome
- Telefone
- Data de nascimento
- Observações
- Data de cadastro

---

## RF02 - Gestão de Agendamentos

O sistema deve permitir:

- Criar agendamentos
- Editar agendamentos
- Cancelar agendamentos
- Filtrar por data

### Dados do Agendamento

- ID
- Cliente
- Serviço
- Data
- Horário
- Observações
- Data de criação

---

## RF03 - Dashboard

O sistema deve exibir:

- Total de clientes
- Agendamentos do dia
- Próximos atendimentos
- Clientes recentes

---

## RF04 - Histórico

O sistema deve exibir:

- Quantidade de atendimentos
- Último atendimento
- Serviços realizados

---

## RF05 - Backup

O sistema deve permitir:

- Exportar dados para JSON
- Importar dados de JSON

---

# Requisitos Não Funcionais

## RNF01 - Facilidade de Uso

O sistema deve ser utilizável por pessoas com pouca experiência em tecnologia.

---

## RNF02 - Responsividade

O sistema deve funcionar corretamente em:

- Desktop
- Tablet
- Smartphone

---

## RNF03 - Performance

As principais telas devem carregar instantaneamente.

---

## RNF04 - Armazenamento

Todos os dados devem ser armazenados inicialmente em LocalStorage.

---

## RNF05 - Escalabilidade

A arquitetura deve permitir futura migração para:

- API REST
- Banco de Dados
- SaaS multiusuário

Sem necessidade de reescrever completamente o sistema.

---

# Fora do Escopo da V1

As funcionalidades abaixo não fazem parte da primeira versão:

- Login
- Multiusuário
- Banco de dados online
- Integração WhatsApp
- Controle financeiro
- Controle de estoque
- Pagamentos
- Relatórios avançados
- Inteligência artificial

---

# Critério de Sucesso

O sistema será considerado pronto quando:

- Permitir cadastro e gestão de clientes
- Permitir gestão de agendamentos
- Possuir dashboard funcional
- Permitir backup e restauração
- Funcionar offline
- Possuir aparência profissional
- Estiver pronto para demonstração a clientes reais
