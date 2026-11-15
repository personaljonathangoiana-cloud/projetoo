# PROJETO: JONATHAN GOIANA FINANCE CENTER — SISTEMA COMPLETO DE GESTÃO FINANCEIRA PESSOAL

## 1. VISÃO GERAL DO PROJETO

Desenvolva uma aplicação web completa, moderna, profissional e responsiva para gestão financeira pessoal, chamada **JONATHAN GOIANA FINANCE CENTER**. Esse é o nome oficial e definitivo do produto. Aplique a identidade nominal em toda a interface: tela de login, dashboard, cabeçalho, menus, título da página do navegador, metadados e documentos/relatórios gerados. Use **JONATHAN GOIANA FINANCE CENTER** por extenso na marca principal.

O sistema deverá funcionar como um centro de controle financeiro pessoal, integrando:

- Gestão de receitas e múltiplas fontes de renda.
- Gestão de despesas.
- Contas bancárias e carteiras.
- Transferências entre contas.
- Cartões de crédito e faturas.
- Compras parceladas.
- Cadastro de alunos e controle de aulas.
- Check-in de aulas e consumo de pacotes.
- Gestão de investimentos em ações e FIIs.
- Controle de dividendos.
- Patrimônio líquido.
- Metas financeiras.
- Planejamento financeiro.
- Dashboards e relatórios gerenciais.

O objetivo é permitir que o usuário acompanhe toda sua vida financeira em um único lugar.

O sistema deve ser funcional, com banco de dados real, autenticação, persistência, relacionamentos entre módulos e cálculos financeiros consistentes.

Não desenvolver apenas um protótipo visual. Todos os botões, formulários, filtros, lançamentos e funcionalidades devem funcionar.

## 2. TECNOLOGIAS E ARQUITETURA

Utilizar:

- React com TypeScript.
- Interface moderna e responsiva.
- Supabase como backend.
- PostgreSQL como banco de dados.
- Supabase Auth para autenticação.
- Row Level Security (RLS) para proteção dos dados.
- Componentes reutilizáveis.
- Gráficos interativos.
- Formatação monetária brasileira.

Configurações regionais:

- Idioma: Português do Brasil.
- Moeda: Real brasileiro (BRL).
- Formato de valores: R$ 1.234,56.
- Datas: DD/MM/AAAA.
- Fuso horário: America/Sao_Paulo.
- Semana iniciando na segunda-feira.

Toda a aplicação deverá ser organizada por módulos, mantendo uma arquitetura escalável.

Criar tabelas relacionais e evitar duplicidade de informações.

As operações financeiras que alteram múltiplos registros devem utilizar transações no banco de dados ou funções RPC apropriadas, garantindo consistência.

Nunca armazenar informações financeiras somente no localStorage.

## 3. IDENTIDADE VISUAL E EXPERIÊNCIA

Criar uma interface premium, sofisticada e minimalista, inspirada em dashboards modernos de fintechs e softwares profissionais de gestão financeira.

Características:

- Layout limpo e organizado.
- Sidebar lateral com navegação.
- Dashboard com cards financeiros.
- Gráficos modernos.
- Ícones intuitivos.
- Boa hierarquia visual.
- Espaçamento consistente.
- Animações discretas.
- Feedback visual nas operações.
- Excelente experiência tanto no computador quanto no celular.

Implementar alternância entre:

1. Modo escuro: fundo grafite ou azul-marinho, superfícies em tons de cinza escuro, textos claros e detalhes em verde.
2. Modo claro: fundo branco ou cinza muito claro, superfícies suaves e textos escuros.

A escolha do tema deve ficar salva nas preferências do usuário.

Evitar aparência de template genérico. A interface deve parecer um produto SaaS profissional.

## 4. ESTRUTURA DE NAVEGAÇÃO

Criar menu lateral com:

1. Dashboard
2. Receitas
3. Despesas
4. Contas bancárias
5. Cartões de crédito
6. Alunos e aulas
7. Investimentos
8. Patrimônio
9. Metas financeiras
10. Planejamento
11. Relatórios
12. Configurações

No topo da aplicação, incluir:

- Seletor de período.
- Busca global.
- Notificações.
- Alternância de tema.
- Perfil do usuário.

## 5. DASHBOARD PRINCIPAL

Esta será a tela mais importante do sistema.

Criar um dashboard completo, com informações atualizadas automaticamente a partir dos dados cadastrados.

### 5.1 Indicadores financeiros

Exibir cards com:

- Saldo total das contas.
- Receitas do mês.
- Despesas do mês.
- Resultado líquido do mês.
- Total a receber.
- Total a pagar.
- Faturas de cartão em aberto.
- Patrimônio líquido.
- Total investido.
- Dividendos recebidos no mês.
- Renda passiva mensal.

Permitir clicar nos indicadores para acessar os respectivos lançamentos.

### 5.2 Gráficos

Criar:

- Gráfico de receitas versus despesas.
- Gráfico de evolução do saldo.
- Gráfico de despesas por categoria.
- Gráfico de receitas por fonte de renda.
- Gráfico de evolução patrimonial.
- Gráfico de renda passiva.
- Gráfico de evolução dos investimentos.

Permitir visualizar períodos mensais, trimestrais, semestrais e anuais.

### 5.3 Atalhos rápidos

Na parte superior do dashboard, disponibilizar quatro atalhos de fácil acesso:

- Nova receita.
- Nova despesa.
- Check-in de aula.
- Nova meta financeira.

Os atalhos devem abrir modais ou formulários rápidos, evitando navegação desnecessária.

### 5.4 Informações adicionais

Criar seções para:

- Últimas movimentações.
- Próximas contas a pagar.
- Próximas faturas.
- Alunos com poucas aulas restantes.
- Próximos vencimentos de pacotes.
- Últimos dividendos recebidos.
- Progresso das metas.
- Alertas financeiros.

### 5.5 Filtro global

O usuário deverá conseguir filtrar o dashboard por mês, ano e intervalo personalizado.

Todos os indicadores e gráficos devem respeitar o período selecionado.

## 6. MÓDULO DE RECEITAS

Criar um módulo completo para registrar e gerenciar todas as entradas financeiras.

### 6.1 Fontes de renda dinâmicas

As fontes de renda não podem ser fixas no código.

Criar um cadastro independente de fontes de renda, permitindo adicionar, editar, desativar e reativar fontes.

Cadastrar inicialmente:

**Serviços:**
- Personal.
- Eletroestimulação.

**Aplicativos:**
- iFood.
- 99.
- Keeta.

**Investimentos:**
- Dividendos de FIIs.
- Dividendos de ações.

Permitir cadastrar novas fontes livremente.

Cada fonte deverá possuir:

- Nome.
- Categoria.
- Descrição.
- Cor de identificação.
- Ícone.
- Status ativo/inativo.

As fontes cadastradas deverão aparecer automaticamente nos formulários, filtros, gráficos e relatórios.

### 6.2 Cadastro de receitas

Campos:

- Descrição.
- Valor.
- Fonte de renda.
- Categoria.
- Data de competência.
- Data de recebimento.
- Conta de destino.
- Status: recebido ou pendente.
- Observações.

Permitir:

- Lançamento de receitas recebidas.
- Lançamento de receitas futuras.
- Receitas recorrentes.
- Edição.
- Exclusão com confirmação.
- Busca e filtros.

### 6.3 Dashboard de fontes de renda

Exibir:

- Total recebido por fonte.
- Participação percentual de cada fonte.
- Comparativo mensal.
- Evolução de cada atividade.
- Fonte de maior faturamento.
- Crescimento ou redução em relação ao mês anterior.

O usuário deverá conseguir identificar facilmente quanto ganhou com Personal, Eletro, iFood, 99, Keeta e investimentos.

## 7. MÓDULO DE DESPESAS

Criar um módulo completo para controle de despesas.

### 7.1 Categorias dinâmicas

Criar categorias iniciais:

- Moradia.
- Alimentação.
- Transporte.
- Saúde.
- Educação.
- Lazer.
- Assinaturas.
- Academia.
- Compras.
- Investimentos.
- Impostos.
- Outros.

Permitir criar categorias e subcategorias personalizadas.

### 7.2 Cadastro de despesas

Campos:

- Descrição.
- Valor.
- Categoria.
- Subcategoria.
- Data da compra.
- Data de vencimento.
- Data de pagamento.
- Conta ou cartão utilizado.
- Tipo de despesa.
- Status.
- Observações.

Tipos:

- Despesa fixa.
- Despesa variável.
- Despesa recorrente.
- Compra parcelada.
- Despesa eventual.

### 7.3 Parcelamento de despesas

Implementar um sistema completo de parcelamento.

Exemplo:

Compra de R$ 1.000,00 dividida em 10 parcelas.

O sistema deverá gerar automaticamente:

- Valor total: R$ 1.000,00.
- Quantidade: 10 parcelas.
- Valor individual: R$ 100,00.
- Primeira parcela.
- Demais parcelas.
- Datas de vencimento.
- Cartão utilizado.
- Faturas correspondentes.

Permitir escolher:

- Quantidade de parcelas.
- Data da compra.
- Primeiro vencimento.
- Cartão.
- Descrição.
- Categoria.

As parcelas deverão aparecer automaticamente nas respectivas faturas e no planejamento financeiro futuro.

Permitir consultar todas as parcelas de uma compra e o saldo ainda comprometido.

Permitir editar ou cancelar parcelas futuras com recálculo consistente, sem apagar pagamentos históricos.

### 7.4 Regras contra duplicidade

Uma compra de R$ 1.000,00 em dez parcelas não pode gerar uma despesa de R$ 1.000,00 mais dez despesas adicionais de R$ 100,00.

O pagamento da fatura também não pode ser contabilizado como uma segunda despesa.

Separar claramente:

- Compra.
- Parcelas.
- Fatura.
- Pagamento da fatura.
- Saída efetiva de dinheiro da conta.

Os relatórios deverão permitir visualizar despesas por competência e fluxo de caixa por data de pagamento.

## 8. MÓDULO DE CONTAS BANCÁRIAS

Criar um módulo para controlar várias contas e carteiras.

Permitir cadastrar:

- Bancos.
- Contas correntes.
- Contas digitais.
- Carteiras de dinheiro.
- Contas de investimento.

Cada conta deverá possuir:

- Nome.
- Instituição.
- Tipo.
- Saldo inicial.
- Data do saldo inicial.
- Cor.
- Status.

### Funcionalidades

- Visualização individual dos saldos.
- Saldo consolidado.
- Histórico de movimentações.
- Entradas e saídas.
- Transferências entre contas.
- Filtros por período.

### Transferências

Permitir transferir dinheiro entre contas próprias.

Uma transferência de R$ 500,00 da conta A para a conta B deve:

- Debitar R$ 500,00 da conta A.
- Creditar R$ 500,00 na conta B.
- Registrar a movimentação nas duas contas.
- Não ser contabilizada como receita.
- Não ser contabilizada como despesa.

Criar identificação única para vincular as duas movimentações.

## 9. MÓDULO DE CARTÕES DE CRÉDITO

Criar módulo completo de gerenciamento de cartões.

### Cadastro de cartões

Campos:

- Nome do cartão.
- Banco ou instituição.
- Bandeira.
- Limite total.
- Limite utilizado.
- Limite disponível.
- Dia de fechamento.
- Dia de vencimento.
- Conta utilizada para pagamento.
- Status.

Permitir cadastrar vários cartões.

### Controle de faturas

Criar visualização das faturas:

- Atual.
- Fechadas.
- Futuras.
- Pagas.
- Em aberto.
- Vencidas.

Cada fatura deverá apresentar:

- Cartão.
- Mês de referência.
- Data de fechamento.
- Data de vencimento.
- Valor total.
- Valor pago.
- Saldo restante.
- Status.

### Compras

Todas as compras feitas no cartão deverão ser vinculadas ao cartão correspondente.

As compras parceladas deverão gerar parcelas nas faturas corretas, respeitando fechamento e vencimento.

### Pagamento de fatura

Permitir pagamento integral ou parcial.

Ao pagar:

- Debitar o valor da conta bancária selecionada.
- Atualizar o saldo da fatura.
- Atualizar o limite disponível conforme a regra de pagamento.
- Registrar data e valor do pagamento.
- Atualizar o status da fatura.

O pagamento não poderá criar uma nova despesa nos relatórios, pois as compras já foram registradas como despesas.

Permitir também identificar juros, multas, encargos e estornos.

## 10. MÓDULO DE ALUNOS E AULAS

Este módulo deverá ter funcionamento próprio, integrado ao financeiro.

É fundamental que seja simples, rápido e confiável.

### 10.1 Cadastro de alunos

Campos:

- Nome completo.
- Telefone.
- E-mail.
- Modalidade.
- Valor por aula.
- Data de cadastro.
- Observações.
- Status.

Modalidades iniciais:

- Personal.
- Eletroestimulação.

Permitir adicionar novas modalidades.

### 10.2 Pacotes de aulas

Permitir cadastrar pacotes com:

- Aluno.
- Modalidade.
- Quantidade contratada.
- Valor total.
- Valor por aula.
- Data de contratação.
- Data de início.
- Validade.
- Quantidade consumida.
- Quantidade restante.
- Status.

Exemplo:

Aluno contrata 20 aulas por R$ 1.000,00.

O sistema deverá registrar:

- 20 aulas contratadas.
- 0 aulas consumidas.
- 20 aulas disponíveis.
- R$ 50,00 por aula.

### 10.3 Check-in

Criar funcionalidade de check-in de aulas.

O processo deverá ser extremamente rápido.

O usuário deverá conseguir:

1. Selecionar o aluno.
2. Selecionar a modalidade.
3. Confirmar a aula.
4. Registrar o check-in.

Ao confirmar:

- Registrar data e horário.
- Debitar uma aula do pacote.
- Atualizar o saldo disponível.
- Atualizar o histórico.
- Atualizar o dashboard.

Impedir saldo negativo e check-ins duplicados acidentais.

Permitir cancelar um check-in, devolvendo o crédito ao pacote e preservando o histórico da operação.

### 10.4 Controle de aulas avulsas

Permitir aulas sem pacote.

Cada aula avulsa deverá possuir:

- Valor.
- Aluno.
- Modalidade.
- Data.
- Status de cobrança.
- Status de pagamento.

O check-in poderá gerar uma cobrança pendente, que poderá ser associada a uma receita quando recebida.

Não registrar automaticamente uma receita recebida apenas porque o check-in foi realizado.

### 10.5 Controle financeiro dos pacotes

Quando um pacote for pago antecipadamente:

- Registrar uma única receita.
- Vincular a receita ao aluno e ao pacote.
- Registrar a conta que recebeu o dinheiro.
- Permitir identificar o saldo de aulas contratado.

O consumo de uma aula não poderá gerar outra receita.

Permitir pacotes parcialmente pagos, quando necessário, com controle do valor pendente.

### 10.6 Alertas

Criar alertas automáticos para:

- 3 aulas restantes.
- 2 aulas restantes.
- 1 aula restante.
- Pacotes próximos do vencimento.
- Pacotes vencidos.
- Pagamentos pendentes.

### 10.7 Dashboard de aulas

Exibir:

- Alunos ativos.
- Total de aulas realizadas no mês.
- Aulas restantes por aluno.
- Pacotes ativos.
- Receita recebida com Personal.
- Receita recebida com Eletro.
- Aulas avulsas pendentes.
- Histórico de check-ins.

Criar calendário de aulas com visualização diária, semanal e mensal.

## 11. MÓDULO DE INVESTIMENTOS

Criar módulo completo para controle de carteira de investimentos em ações e fundos imobiliários.

### 11.1 Cadastro de ativos

Permitir cadastrar ativos manualmente.

Separar:

- Ações.
- FIIs.

Campos:

- Ticker.
- Nome.
- Tipo.
- Quantidade.
- Preço médio.
- Preço atual.
- Valor investido.
- Valor de mercado.
- Instituição ou corretora.
- Observações.

### 11.2 Compras e vendas

Permitir registrar operações de:

- Compra.
- Venda.

Campos:

- Ativo.
- Data.
- Quantidade.
- Preço unitário.
- Taxas.
- Valor total.
- Corretora.
- Conta de origem ou destino.

Atualizar automaticamente:

- Quantidade em carteira.
- Custo médio.
- Capital investido.
- Histórico de operações.
- Posição atual.

Utilizar cálculo de preço médio ponderado para compras.

Controlar separadamente lucro ou prejuízo realizado nas vendas e variação não realizada da carteira.

### 11.3 Atualização de cotações

Preparar arquitetura para integração futura com provedores de cotações.

Permitir atualização manual dos preços.

Não inventar cotações nem apresentar valores desatualizados como preços em tempo real.

Mostrar data e origem da última atualização.

### 11.4 Dividendos

Criar controle de:

- Dividendos de FIIs.
- Dividendos de ações.
- Rendimentos recebidos.
- Valores previstos.
- Data-com.
- Data de pagamento.
- Quantidade de cotas ou ações na data relevante.
- Ativo pagador.
- Conta de destino.
- Status: previsto ou recebido.

Ao registrar o recebimento:

- Criar receita vinculada à fonte correspondente.
- Atualizar o histórico de rendimentos.
- Atualizar os indicadores de renda passiva.
- Atualizar o saldo da conta de destino.

Impedir duplicidade entre o lançamento do dividendo e o recebimento financeiro.

### 11.5 Dashboard de investimentos

Exibir:

- Patrimônio investido.
- Valor atual da carteira.
- Resultado acumulado.
- Rentabilidade.
- Dividendos mensais.
- Dividendos anuais.
- Renda passiva média.
- Evolução da carteira.
- Distribuição entre ações e FIIs.
- Participação de cada ativo.

Permitir visualizar histórico mensal e anual.

## 12. MÓDULO DE PATRIMÔNIO

Criar uma visão consolidada do patrimônio pessoal.

Ativos:

- Saldo bancário.
- Dinheiro em carteira.
- Investimentos.
- Outros bens cadastrados manualmente.

Passivos:

- Faturas de cartão.
- Empréstimos.
- Financiamentos.
- Outras dívidas cadastradas.

Calcular:

Patrimônio líquido = Total de ativos - Total de passivos.

Permitir cadastrar bens e passivos adicionais.

Criar gráfico de evolução patrimonial mensal.

Evitar contabilizar duas vezes ativos que já estejam registrados nos módulos de contas e investimentos.

## 13. MÓDULO DE METAS FINANCEIRAS

Permitir criar metas personalizadas.

Exemplos:

- Reserva de emergência.
- Patrimônio de R$ 100.000.
- Renda passiva de R$ 1.000 mensais.
- Investir determinado valor por mês.
- Economizar determinada quantia.
- Quitar dívidas.

Cada meta deverá possuir:

- Nome.
- Descrição.
- Valor objetivo.
- Valor atual.
- Data inicial.
- Prazo.
- Categoria.
- Status.

Exibir:

- Progresso percentual.
- Valor restante.
- Prazo.
- Evolução.
- Histórico de contribuições.

Permitir vincular metas a contas ou investimentos, sem duplicar o patrimônio contabilizado.

Atualizar automaticamente os valores quando houver movimentações vinculadas.

## 14. MÓDULO DE PLANEJAMENTO FINANCEIRO

Criar planejamento mensal e anual.

Permitir:

- Planejar receitas.
- Planejar despesas.
- Definir orçamento por categoria.
- Projetar saldo futuro.
- Visualizar parcelas futuras.
- Visualizar faturas futuras.
- Prever compromissos recorrentes.
- Comparar planejado versus realizado.

Criar projeção financeira para os próximos 3, 6 e 12 meses.

Deixar claro o que é valor confirmado, previsto ou estimado.

## 15. MÓDULO DE RELATÓRIOS

Criar relatórios com filtros por período, categoria, conta, fonte de renda, aluno e ativo.

Relatórios necessários:

- Receitas mensais.
- Despesas mensais.
- Resultado financeiro.
- Despesas por categoria.
- Receitas por fonte.
- Desempenho de cada atividade.
- Histórico de investimentos.
- Dividendos recebidos.
- Evolução patrimonial.
- Despesas parceladas.
- Compromissos futuros.
- Histórico de aulas.
- Receita por aluno.
- Receita por modalidade.

Permitir exportar dados em CSV e Excel.

## 16. REGRAS FINANCEIRAS GERAIS

Estas regras são obrigatórias para garantir integridade.

1. Uma transferência entre contas próprias não é receita nem despesa.
2. O pagamento de uma fatura não pode duplicar as despesas das compras.
3. Uma compra parcelada precisa gerar parcelas vinculadas a uma única compra.
4. O check-in de uma aula de pacote não gera nova receita.
5. Uma aula avulsa pode gerar uma cobrança pendente, mas só se torna recebimento quando paga.
6. O recebimento de dividendos deve ser registrado uma única vez.
7. Compras de investimentos não devem ser tratadas como despesas de consumo.
8. Vendas de investimentos devem separar movimentação de capital e resultado realizado.
9. O patrimônio deve consolidar os módulos sem duplicidade.
10. Toda movimentação deve possuir histórico e rastreabilidade.
11. Valores financeiros devem utilizar tipos numéricos adequados, como NUMERIC no PostgreSQL, nunca ponto flutuante impreciso.
12. Todas as operações relevantes devem registrar data de criação e atualização.
13. Exclusões de operações já liquidadas devem ser controladas, utilizando cancelamento ou estorno quando apropriado.
14. Valores futuros devem ser separados dos valores efetivamente recebidos ou pagos.
15. Não misturar saldo disponível, limite de crédito e patrimônio líquido.

## 17. ESTRUTURA DO BANCO DE DADOS

Planejar e implementar banco relacional no Supabase.

Criar entidades para:

- profiles
- accounts
- account_transactions
- transfers
- income_sources
- income_categories
- income_transactions
- expense_categories
- expenses
- expense_installments
- credit_cards
- credit_card_purchases
- credit_card_installments
- credit_card_invoices
- credit_card_payments
- students
- class_modalities
- class_packages
- class_checkins
- class_charges
- investment_assets
- investment_transactions
- investment_positions
- investment_dividends
- patrimonial_assets
- liabilities
- financial_goals
- goal_contributions
- budgets
- recurring_transactions
- notifications
- user_preferences

Todas as entidades deverão possuir relacionamentos adequados e, quando aplicável:

- UUID como identificador.
- user_id.
- created_at.
- updated_at.
- Status.
- Índices para consultas frequentes.
- Restrições de integridade.

Utilizar chaves estrangeiras e regras de exclusão adequadas.

Todas as tabelas que contêm informações pessoais ou financeiras devem ter RLS habilitado e políticas que impeçam qualquer usuário de consultar ou modificar dados de outro usuário.

Criar migrations versionadas e funções de banco para operações que exigem atomicidade, como check-in, pagamento de fatura e transferência.

Não permitir alterações inconsistentes em saldos e quantidades por atualizações concorrentes.

## 18. USABILIDADE E AUTOMAÇÕES INTERNAS

Criar:

- Formulários rápidos.
- Modais de lançamento.
- Busca global.
- Filtros persistentes.
- Paginação.
- Ordenação.
- Confirmação de operações críticas.
- Notificações de sucesso e erro.
- Estados de carregamento.
- Estados vazios bem elaborados.
- Alertas de vencimento.
- Alertas de pacote de aulas.
- Lembretes financeiros.

Todos os formulários deverão validar dados obrigatórios e valores.

Não permitir salvar operações incompletas ou inconsistentes.

## 19. SEGURANÇA E PRIVACIDADE

Implementar autenticação segura.

Cada usuário deverá visualizar exclusivamente seus próprios dados.

Não deixar chaves administrativas ou service role no frontend.

Utilizar variáveis de ambiente para credenciais.

Aplicar validações no backend, além das validações visuais no frontend.

Proteger operações financeiras contra duplicidade de requisições.

Manter logs das operações relevantes.

## 20. ORDEM DE IMPLEMENTAÇÃO

Não tentar desenvolver todos os módulos de uma só vez sem validar a estrutura.

Dividir a implementação em etapas:

**ETAPA 1 — Fundação**
- Estrutura visual.
- Autenticação.
- Supabase.
- Banco de dados.
- RLS.
- Layout responsivo.
- Preferências de tema.

**ETAPA 2 — Núcleo financeiro**
- Contas.
- Receitas.
- Fontes de renda.
- Despesas.
- Categorias.
- Transferências.

**ETAPA 3 — Cartões**
- Cadastro de cartões.
- Compras.
- Parcelamentos.
- Faturas.
- Pagamentos.
- Integração com contas e despesas.

**ETAPA 4 — Aulas**
- Alunos.
- Modalidades.
- Pacotes.
- Check-ins.
- Aulas avulsas.
- Integração financeira.

**ETAPA 5 — Investimentos**
- Ativos.
- Compras e vendas.
- Posições.
- Dividendos.
- Rentabilidade.

**ETAPA 6 — Patrimônio e metas**
- Patrimônio líquido.
- Passivos.
- Metas.
- Contribuições.
- Planejamento.

**ETAPA 7 — Dashboard e relatórios**
- Indicadores consolidados.
- Gráficos.
- Relatórios.
- Filtros.
- Exportações.

**ETAPA 8 — Testes e acabamento**
- Testes de integridade financeira.
- Testes de permissões.
- Testes de responsividade.
- Testes de formulários.
- Testes de integração entre módulos.
- Correção de erros.

## 21. CRITÉRIOS DE ACEITAÇÃO

Considerar o sistema funcional somente depois de validar os seguintes cenários:

1. Criar uma nova fonte de renda e verificar se ela aparece nos formulários e dashboards.
2. Registrar uma receita e verificar se o saldo da conta aumenta.
3. Registrar uma despesa paga e verificar se o saldo diminui.
4. Fazer uma transferência e verificar os dois saldos sem gerar receita ou despesa.
5. Registrar uma compra de R$ 1.000 em 10 parcelas e verificar a geração de dez parcelas de R$ 100.
6. Verificar se as parcelas aparecem nas faturas futuras corretas.