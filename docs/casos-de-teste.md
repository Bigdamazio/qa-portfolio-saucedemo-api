# Casos de Teste

## CT-001 - Login com credenciais válidas
**Objetivo:** Validar acesso com usuário e senha corretos.  
**Pré-condição:** Usuário está na tela de login do SauceDemo.  

**Passos:**
1. Acessar o site SauceDemo
2. Informar o usuário `standard_user`
3. Informar a senha `secret_sauce`
4. Clicar no botão de login

**Resultado esperado:** Usuário acessa a página de produtos com sucesso.  
**Resultado obtido:** Login realizado com sucesso e página de produtos carregada corretamente.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/login-sucesso.png`

---

## CT-002 - Login com senha inválida
**Objetivo:** Validar mensagem de erro ao informar senha incorreta.  
**Pré-condição:** Usuário está na tela de login do SauceDemo.  

**Passos:**
1. Acessar o site SauceDemo
2. Informar o usuário `standard_user`
3. Informar uma senha inválida
4. Clicar no botão de login

**Resultado esperado:** Sistema deve impedir o acesso e exibir mensagem de erro.  
**Resultado obtido:** O sistema bloqueou o login e exibiu mensagem de erro corretamente.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/login-senha-invalida.png`

---

## CT-003 - Login com campos vazios
**Objetivo:** Validar comportamento ao tentar login sem preencher os campos.  
**Pré-condição:** Usuário está na tela de login do SauceDemo.  

**Passos:**
1. Acessar o site SauceDemo
2. Deixar o campo de usuário vazio
3. Deixar o campo de senha vazio
4. Clicar no botão de login

**Resultado esperado:** Sistema deve exibir mensagem orientando o preenchimento dos campos obrigatórios.  
**Resultado obtido:** O sistema exibiu mensagem de erro ao tentar prosseguir sem preencher os campos.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/login-campos-vazios.png`

---

## CT-004 - Adicionar produto ao carrinho
**Objetivo:** Validar adição de item ao carrinho.  
**Pré-condição:** Usuário autenticado no sistema.  

**Passos:**
1. Realizar login com credenciais válidas
2. Selecionar um produto na listagem
3. Clicar em **Add to cart**
4. Acessar o carrinho

**Resultado esperado:** Produto deve aparecer no carrinho com sucesso.  
**Resultado obtido:** O produto foi adicionado ao carrinho corretamente e ficou visível na tela do carrinho.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/produto-adicionado-carrinho1.png`

---

## CT-005 - Remover produto do carrinho
**Objetivo:** Validar remoção de item do carrinho.  
**Pré-condição:** Carrinho contém pelo menos um item adicionado anteriormente.  

**Passos:**
1. Acessar o carrinho
2. Localizar o item adicionado
3. Clicar em **Remove**

**Resultado esperado:** Produto deve ser removido do carrinho.  
**Resultado obtido:** O produto foi removido do carrinho com sucesso e não ficou mais visível na listagem.  
**Status:** Aprovado  
**Evidência:** `evidencias/screenshots/produto-removido-carrinho.png`

---

## CT-006 - Finalizar compra com dados válidos
**Objetivo:** Validar fluxo de checkout com dados corretos.  
**Pré-condição:** Carrinho contém pelo menos um item.  

**Passos:**
1. Acessar o carrinho
2. Clicar em **Checkout**
3. Preencher nome, sobrenome e CEP
4. Avançar no fluxo
5. Confirmar a compra

**Resultado esperado:** Compra deve ser finalizada com sucesso.  
**Status:** Não executado
