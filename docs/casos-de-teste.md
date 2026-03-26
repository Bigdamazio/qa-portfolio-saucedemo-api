# Casos de Teste

## CT-001 - Login com credenciais válidas
**Objetivo:** Validar acesso com usuário e senha corretos.  
**Pré-condição:** Usuário está na tela de login.  
**Passos:**
1. Informar usuário válido
2. Informar senha válida
3. Clicar em login

**Resultado esperado:** Usuário acessa a página de produtos.

---

## CT-002 - Login com senha inválida
**Objetivo:** Validar mensagem de erro ao informar senha incorreta.  
**Pré-condição:** Usuário está na tela de login.  
**Passos:**
1. Informar usuário válido
2. Informar senha inválida
3. Clicar em login

**Resultado esperado:** Sistema exibe mensagem de erro.

---

## CT-003 - Login com campos vazios
**Objetivo:** Validar comportamento ao tentar login sem preencher os campos.  
**Pré-condição:** Usuário está na tela de login.  
**Passos:**
1. Deixar usuário em branco
2. Deixar senha em branco
3. Clicar em login

**Resultado esperado:** Sistema exibe mensagem orientando preenchimento.

---

## CT-004 - Adicionar produto ao carrinho
**Objetivo:** Validar adição de item ao carrinho.  
**Pré-condição:** Usuário autenticado.  
**Passos:**
1. Selecionar um produto
2. Clicar em adicionar ao carrinho
3. Acessar o carrinho

**Resultado esperado:** Produto aparece no carrinho.

---

## CT-005 - Remover produto do carrinho
**Objetivo:** Validar remoção de item do carrinho.  
**Pré-condição:** Carrinho contém pelo menos um item.  
**Passos:**
1. Acessar carrinho
2. Clicar em remover

**Resultado esperado:** Produto é removido do carrinho.

---

## CT-006 - Finalizar compra com dados válidos
**Objetivo:** Validar fluxo de checkout com dados corretos.  
**Pré-condição:** Carrinho contém item.  
**Passos:**
1. Iniciar checkout
2. Preencher nome, sobrenome e CEP
3. Confirmar compra

**Resultado esperado:** Compra finalizada com sucesso.
