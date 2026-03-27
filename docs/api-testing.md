# API Testing - ReqRes

## Objetivo
Registrar testes iniciais de API realizados no Postman, com foco em validação de endpoints, status codes, estrutura de resposta e operações básicas.

## API utilizada
- ReqRes
- Base URL: `https://reqres.in`

## Ferramenta utilizada
- Postman

## Cenários executados

### API-001 - Listar usuários
**Método:** GET  
**Endpoint:** `/api/users?page=2`  

**Headers utilizados:**
- `x-api-key`
- `User-Agent`

**Resultado esperado:** Retornar lista de usuários com status 200.  
**Resultado obtido:** A API retornou a lista de usuários corretamente, com status 200 e estrutura esperada no campo `data`.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/api-get-list-users.png`

---

### API-002 - Consultar usuário único
**Método:** GET  
**Endpoint:** `/api/users/2`  

**Headers utilizados:**
- `x-api-key`
- `User-Agent`

**Resultado esperado:** Retornar dados do usuário com status 200.  
**Resultado obtido:** A API retornou os dados do usuário corretamente, com status 200 e campos compatíveis com a consulta.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/api-get-single-user.png`

---

### API-003 - Criar usuário
**Método:** POST  
**Endpoint:** `/api/users`  

**Headers utilizados:**
- `x-api-key`
- `User-Agent`
- `Content-Type: application/json`

**Body enviado:**

    {
      "name": "Eduardo",
      "job": "QA"
    }

**Resultado esperado:** Criar usuário com status 201.  
**Resultado obtido:** A API retornou os dados enviados, além de um `id` e do campo `createdAt`, indicando criação com sucesso.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/api-post-create-user.png`

---

### API-004 - Atualizar usuário
**Método:** PUT  
**Endpoint:** `/api/users/2`  

**Headers utilizados:**
- `x-api-key`
- `User-Agent`
- `Content-Type: application/json`

**Body enviado:**

    {
      "name": "Eduardo",
      "job": "Senior QA"
    }

**Resultado esperado:** Atualizar usuário com status 200.  
**Resultado obtido:** A API retornou confirmação de atualização com sucesso, incluindo o campo `updatedAt`.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/api-put-update-user.png`

---

### API-005 - Excluir usuário
**Método:** DELETE  
**Endpoint:** `/api/users/2`  

**Headers utilizados:**
- `x-api-key`
- `User-Agent`

**Resultado esperado:** Excluir usuário com status 204.  
**Resultado obtido:** A API retornou status 204, sem conteúdo no body, conforme esperado para exclusão.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/api-delete-user.png`

---

## Validações realizadas
Durante os testes, foram observados principalmente os seguintes pontos:
- retorno de status code esperado
- estrutura básica da resposta
- comportamento dos métodos HTTP
- criação e atualização de recurso com payload JSON
- resposta sem conteúdo no método DELETE
- necessidade de headers para autorização e identificação da requisição

## Conclusão
Os cenários iniciais de API foram executados com sucesso no Postman, cobrindo operações básicas de consulta, criação, atualização e exclusão.

Esta etapa complementa o portfólio com uma frente prática de testes de API, reforçando conhecimentos em:
- métodos HTTP
- análise de respostas
- uso de headers
- validação de status codes
- documentação de testes
