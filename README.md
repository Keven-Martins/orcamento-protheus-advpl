# Orçamentos e Pedidos de Venda — ADVPL / Protheus

Customização da impressão de orçamentos e pedidos de venda no **TOTVS Protheus**, desenvolvida em **ADVPL com TMSPrinter**, para adaptar o documento às regras comerciais e melhorar a coerência entre unidades, quantidades e preços.

**Desenvolvido por [Keven Sena Martins](https://github.com/Keven-Martins)**

## O problema

A apresentação comercial precisava tratar vendas por peso ou peça, produtos com duas unidades de medida, descontos e informações de clientes e filiais. Divergências entre a quantidade exibida e a utilizada no cálculo podiam dificultar a conferência do documento.

## Minha atuação

Atuei na customização do relatório, no tratamento das informações do pedido e na implementação das regras de apresentação, preservando comportamentos específicos já utilizados pela empresa.

## Melhorias desenvolvidas

| Desafio | Solução implementada |
| --- | --- |
| Vendas por peso ou peça | Escolha do layout conforme o tipo de venda e os itens do pedido |
| Produtos com duas unidades de medida | Análise da unidade comercial e da segunda unidade, respeitando as exceções existentes |
| Itens com características diferentes | Validação do pedido completo antes de definir as colunas de quantidade |
| Preço da segunda unidade desatualizado após desconto | Cálculo do preço apresentado a partir do valor final do item e da quantidade exibida |
| Quantidade exibida diferente da base do preço | Uso da mesma quantidade de apresentação no cálculo do preço unitário |
| Precisão comercial | Apresentação do preço unitário com quatro casas decimais |
| Identificação de cliente e avalista | Correspondência entre código, loja e nome apresentados no cabeçalho |
| Documentos de identificação | Aplicação de máscaras de CPF ou CNPJ conforme o documento cadastrado |
| Pedidos de diferentes filiais | Cabeçalho com informações da filial responsável, em um relatório centralizado |

## Exemplo ilustrativo

Na apresentação pela segunda unidade comercial, o preço unitário utiliza a quantidade que o cliente visualiza no documento:

**Preço unitário apresentado = valor final do item / quantidade apresentada**

O valor final registrado no pedido permanece como referência oficial do item. A apresentação do preço considera os descontos refletidos nesse valor e utiliza quatro casas decimais.

## Fluxo da impressão

1. Identificar pedido, filial, cliente e tipo de venda.
2. Analisar as unidades de medida de todos os itens e as exceções comerciais.
3. Definir o layout compatível com o pedido completo.
4. Preparar as quantidades e os preços de apresentação.
5. Montar o cabeçalho e imprimir o documento com TMSPrinter.

## Tecnologias e conhecimentos aplicados

- **ADVPL** e **TOTVS Protheus**.
- **TMSPrinter** para impressão do relatório.
- Dados de pedidos e itens de venda: **SC5 e SC6**.
- Cadastros de produtos, clientes, fornecedores e vendedores: **SB1, SA1, SA2 e SA3**.
- Parametrização no **SX6**.
- Regras de vendas, unidades de medida, descontos e identificação por filial.

## Resultado funcional

O relatório passou a adaptar a apresentação ao contexto comercial do pedido, reunindo diferentes regras em um único layout. O trabalho busca facilitar a leitura e a conferência comercial e reduzir divergências entre os dados do ERP e o documento entregue ao cliente.

## Sobre esta apresentação

Este repositório documenta o projeto para portfólio. Não inclui fontes corporativos, dados de clientes ou configurações do ambiente da empresa. O conteúdo descreve a atuação e as funcionalidades desenvolvidas, sem atribuir métricas de desempenho ou de economia não medidas.

## Contato

[Perfil profissional](https://github.com/Keven-Martins) · [Contato para oportunidades PJ](mailto:kevenoab2023@gmail.com)
