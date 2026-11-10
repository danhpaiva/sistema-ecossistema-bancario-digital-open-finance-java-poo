# Exercício Prático: <br>Sistema de Ecossistema Bancário Digital e <br>Open Finance (POO em Java)

**Disciplina:** Algoritmos e Programação

**Professor / Desenvolvedor:** Prof. Daniel Paiva

**Objetivo:** Consolidar conceitos de Programação Orientada a Objetos (POO) em Java — incluindo hierarquias complexas, <br>classes abstratas, interfaces de transação, polimorfismo, tratamento de exceções customizadas, coleções e modelagem de regras financeiras rígidas — aplicados ao segmento bancário moderno e engajado em finanças sustentáveis (alinhado indiretamente à **ODS 8: Trabalho Decente e Crescimento Econômico**).

## 💳 Contextualização do Problema

Você foi contratado como Arquiteto de Software Líder por uma Fintech em franca expansão para projetar a nova geração do seu Core Bancário. <br>O sistema precisa suportar múltiplos tipos de contas, cartões de crédito e débito, investimentos em fundos verdes, empréstimos com análise de crédito automatizada, auditorias de segurança e o padrão de compartilhamento de dados do *Open Finance*.

Para dar conta dessa complexidade regulatória e transacional, o seu projeto deverá ser arquitetado utilizando **no mínimo 14 (quatorze) classes**, perfeitamente estruturadas e integradas a partir da classe principal `Programa.java`.

## 🛠️ Requisitos de Implementação

Sua aplicação deverá conter as seguintes classes e estruturas modulares:

### 1. Módulo de Clientes e Perfis de Acesso (Mínimo de 3 classes)

1. **`Cliente`** (Classe Abstrata Base): Contém dados cadastrais genéricos como identificador único, nome completo, documento (CPF/CNPJ), endereço e nível de conformidade KYC (*Know Your Customer*).

2. **`ClientePessoaFisica`** (Herda de `Cliente`): Atributos específicos como data de nascimento, renda mensal declarada e estado civil.

3. **`ClientePessoaJuridica`** (Herda de `Cliente`): Atributos específicos como faturamento anual, nome fantasia e ramo de atividade empresarial.

### 2. Módulo de Contas e Gestão de Saldo (Mínimo de 4 classes)

4. **`ContaBancaria`** (Classe Abstrata Base): Contém número da agência, número da conta, saldo atual, senha de acesso e referência ao titular (`Cliente`).

5. **`ContaCorrente`** (Herda de `ContaBancaria`): Atributos e regras específicas como limite de cheque especial e taxa de manutenção mensal.

6. **`ContaPoupanca`** (Herda de `ContaBancaria`): Atributos e regras específicas como taxa de rendimento diário e aniversário da poupança.

7. **`ContaInvestimento`** (Herda de `ContaBancaria`): Atributos e regras específicas como perfil de risco do investidor (Conservador, Moderado, Arrojado) e taxa de corretagem.

### 3. Módulo de Cartões e Meios de Pagamento (Mínimo de 3 classes)

8. **`Cartao`** (Classe Abstrata Base): Contém número do cartão, nome impresso, código CVV, data de validade e status (Bloqueado/Ativo).

9. **`CartaoDebito`** (Herda de `Cartao`): Vinculado diretamente a uma conta bancária para liquidação instantânea.

10. **`CartaoCredito`** (Herda de `Cartao`): Atributos específicos como limite total, limite disponível, fatura atual e melhor dia de compra.

### 4. Módulo de Transações, Crédito e Auditoria (Mínimo de 4 classes)

11. **`Transacao`** (Classe Auxiliar/Registro): Representa o histórico de movimentações (código da transação, data/hora, valor monetário e descrição).

12. **`EmprestimoFinanciamento`** (Classe de Negócio): Gerencia solicitações de crédito (valor solicitado, taxa de juros aplicada, quantidade de parcelas e status de aprovação baseado na renda do cliente).

13. **`AuditoriaSeguranca`** (Classe Auxiliar): Responsável por registrar tentativas de acesso suspeitas, bloqueios de segurança e logs de conformidade regulatória do Banco Central.

14. **`BancoSistemaCentral`** (Classe Gerenciadora/Sistema): Classe central que abriga todas as coleções globais (`List<Cliente>`, `List<ContaBancaria>`, `List<Cartao>`, etc.) e centraliza as operações de transferência, abertura de contas e consolidação de balanços.

### 🚀 A Classe Principal (`Programa.java`)

A classe `Programa.java` deve conter o método `public static void main(String[] args)` e simular o ecossistema financeiro em pleno funcionamento:

1. Instanciar a classe gerenciadora central (`BancoSistemaCentral`).

2. Cadastrar clientes pessoas físicas e jurídicas.

3. Abrir diferentes tipos de contas (Corrente, Poupança, Investimento) atreladas aos clientes cadastrados.

4. Emitir cartões de débito e crédito, simulando compras e limites.

5. Realizar operações entre contas (depósitos, saques, transferências via PIX/TED) e simular uma análise de empréstimo.

6. Exibir o extrato consolidado e relatórios gerenciais de auditoria no console.

## 📋 Critérios de Avaliação

* **Modelagem e Abstração:** Emprego correto de classes abstratas e polimorfismo para diferenciar o comportamento de contas e cartões.

* **Encapsulamento e Segurança:** Proteção rigorosa de dados sensíveis (saldos, senhas, documentos) utilizando modificadores de acesso adequados.

* **Organização Estrutural:** Cumprimento estrito do requisito mínimo de 14 classes coesas e bem distribuídas.

* **Coerência de Regras de Negócio:** Validações financeiras lógicas (ex: impedir saques ou compras sem saldo/limite disponível).

* **Simulação Prática:** Execução fluida, clara e organizada na classe `Programa.java`.

Bom desenvolvimento e excelente projeto para consolidar a sua arquitetura de software orientada a objetos! 🏦💼
