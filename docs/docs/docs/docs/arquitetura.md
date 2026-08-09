# Arquitetura do Sistema

## Visão Geral

O BarberFlow foi projetado utilizando uma arquitetura modular baseada em responsabilidades separadas.

O objetivo é manter o sistema simples para a V1 e permitir crescimento futuro sem necessidade de reescrever todo o projeto.

---

# Tecnologias

## Frontend

- HTML5
- CSS3
- JavaScript ES6+

## Armazenamento

- LocalStorage

## PWA

- Service Worker
- Manifest

---

# Estrutura Geral

```text
UI
↓
Router
↓
Store
↓
Repository
↓
LocalStorage
```

---

# Camadas

## UI

Responsável pela interface do usuário.

Funções:

- Renderização de telas
- Componentes visuais
- Formulários
- Feedback visual

Exemplos:

- Dashboard
- Clientes
- Agendamentos
- Histórico

---

## Router

Responsável pela navegação interna.

Funções:

- Troca de telas
- Rotas dinâmicas
- Gerenciamento de histórico

Exemplos:

```text
/
clientes
clientes/:id
agendamentos
historico
```

---

## Store

Responsável pelo estado da aplicação.

Funções:

- Centralizar dados carregados
- Atualizar componentes
- Notificar alterações

Benefícios:

- Evita duplicação de dados
- Facilita futuras integrações

---

## Repository

Responsável pela persistência.

Funções:

- Salvar dados
- Buscar dados
- Atualizar dados
- Excluir dados

Benefício:

A aplicação não depende diretamente do LocalStorage.

No futuro será possível trocar:

```text
LocalStorage
```

por

```text
API REST
```

sem alterar a interface.

---

## Storage

Camada de armazenamento físico.

Na V1:

```text
LocalStorage
```

No futuro:

```text
PostgreSQL
MySQL
Supabase
Firebase
MongoDB
```

---

# Modelos de Dados

## Cliente

```javascript
{
  id: string,
  nome: string,
  telefone: string,
  dataNascimento: string,
  observacoes: string,
  criadoEm: string
}
```

---

## Agendamento

```javascript
{
  id: string,
  clienteId: string,
  servico: string,
  data: string,
  horario: string,
  observacoes: string,
  criadoEm: string
}
```

---

# Fluxo de Dados

Exemplo:

Cadastro de Cliente

```text
Usuário
↓
Formulário
↓
Store
↓
Repository
↓
LocalStorage
```

Consulta de Cliente

```text
LocalStorage
↓
Repository
↓
Store
↓
UI
↓
Usuário
```

---

# Responsividade

O sistema deve suportar:

- Desktop
- Notebook
- Tablet
- Smartphone

Estratégia:

- Sidebar em telas grandes
- Menu inferior em dispositivos móveis

---

# PWA

Objetivos:

- Instalação na tela inicial
- Funcionamento offline básico
- Experiência semelhante a aplicativo

---

# Evolução Futura

## V2

- Login
- Multiusuário
- Controle de barbeiros

## V3

- Banco de dados online
- Sincronização em nuvem
- Painel administrativo

## V4

- SaaS completo
- Assinaturas
- Integrações externas
- WhatsApp
- Relatórios avançados

---

# Princípios do Projeto

1. Simplicidade antes de complexidade.
2. Experiência do usuário acima de funcionalidades.
3. Entrega rápida.
4. Código organizado.
5. Escalabilidade gradual.
6. Facilidade de manutenção.
