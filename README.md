# Teste para candidatos à vaga de Desenvolvedor Full Stack.

Olá, caro desenvolvedor, nesse teste analisaremos seu conhecimento geral e velocidade de desenvolvimento. Abaixo explicaremos tudo o que será necessário.

# Instruções
- Você deve desenvolver uma API, utilizando `Laravel`, `Lumen` ou `Node`.
A escolha das bibliotecas, banco de dados, arquitetura, etc, fica a seu critério.

- O código precisa rodar em múltiplas plataformas, utilizando a Docker.
Altere o arquivo README explicando o que é preciso para rodar sua aplicação.

# O teste

**Back-End**

A primeira etapa será o desenvolvimento do backend.

**Descrição**:

Você será responsável por criar uma 'mini api' que permita a execução de transações de venda de produtos. 
Além disso, será essencial elaborar um relatório baseado nessas transações. 
Para simplificar o processo, a criação de um relatório no formato .csv é uma opção aceitável.

**O cadastro do cliente e vendedor deverá possuir** :
- ID
- Nome
- Documento (CPF/CNPJ)
- Telefone

**O cadastro do produto deverá possuir** :
- ID
- Descrição
- Preço
- Quantidade disponível

**Cada venda deverá possuir** :
- ID
- Cliente
- Vendedor
- Observação
- Condição de Pagamento (Apenas uma descrição é suficiente)
- Produtos (Pode conter um ou mais produtos vinculados a mesma venda)
- Status (Pendente, Encerrada ou Cancelada)

**Recursos
- Toda transação de venda deve inicialmente ser registrada com o status "Pendente".
- Criar recurso para "Faturar", 'Estornar" e "Cancelar" Venda.
- Ao "Faturar" uma venda, deve-se decrementar a quantidade disponível dos produtos relacionados.
- Ao "Estornar" uma venda, deve-se incrementar a quantidade disponível dos produtos relacionados.
- O "Cancelamento" de vendas é permitido exclusivamente para transações com status "Pendente".
- O "Cancelamento" não deve movimentar as quantidades disponíveis dos produtos relacionados.
- Permitir a exclusão de vendas apenas quando o status está "Pendente".
- Não permitir alterar informações das vendas com status "Faturada" e "Cancelada".
- O recurso de listagem de vendas deve oferecer filtragem por "Data de Cadastro, Status, Cliente e Vendedor".
- Desenvolver uma funcionalidade que possibilite o registro em massa de pedidos de venda, marcando-os como "Pendente". Criar uma estratégia para que seja performático.
- Criar relatório de vendas com opções de filtro: "Data de Cadastro, Status, Cliente e Vendedor".

# Front-End
**Para a segunda etapa do teste, você deverá desenvolver uma SPA (Single Page Application) com `Vue.js` e nela deve ser possível:**
> - Gerenciar operações de listagem, cadastro, atualização e exclusão para clientes, vendedores, produtos e vendas.
> - Em vendas, criar listagem do dados conforme definição no backend, utilizar os filtros definidos.
> - Em vendas, criar recurso para "Faturar", "Estornar" ou "Cancelar".
> - Em vendas, criar recurso para extração do relatório.
> - Em vendas, criar recurso que envia um lote de pedidos de venda para o backend. O Conteúdo do lote de pedidos não será digitado pelo usuário. Elabore uma estratégia de dados aleatórios para enviar para o backend. Cuidado com chaves estrangeiras.

**Condições**:
> - A página deve ser responsiva.
> - A página deve funcionar 100% via AJAX, sem outros carregamentos de páginas.
> - Os dados das requisições deverão ser gerenciados pelo VUEX.
> - Ao criar/editar um livro, o campo "categoria" deverá ser um SELECT.
> - A definição de peso ou tamanho do arquivo deverá ser realizada pela função `watch`, verificando o tipo do arquivo: *arquivo digital ou físico*

**Dicas**:
> - Você pode usar frameworks, tanto para o front-end (Vuejs) e tanto para o back-end.
> - Você pode usar ferramentas de automação (Grunt, Gulp), mas deverá informar o uso completo para funcionamento do teste.
> - Será considerado ponto positivo no teste a utilização de orientação a objetos, design patterns e rotinas para testes.

**Entrega**

Para iniciar o teste, faça um fork deste repositório, crie uma branch com o seu nome completo e depois envie-nos o pull request. Se você apenas clonar o repositório não vai conseguir fazer push e depois vai ser mais complicado fazer o pull request.
Nossa análise
Organização do código, legibilidade e comentários, uso de padrões.
Histórico de commits.

**Dúvidas?**
Quaisquer dúvidas que você venha a ter, abra você mesmo uma nova issue, ou mande um e-mail.
Boa sorte!
