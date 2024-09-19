# Centrais De Atendimento

Grafo de respostas de telemarketing

## Bradesco

```mermaid
graph LR
    Ligacao[Ligação Inicial]
    DadosBase_CartCPF[Número de cartão ou CPF Titular]
    DadosBase_Agencia[Agência e dígito]
    DadosBase_Conta[Conta e dígito]
    DadosBase_Senha[Senha 4 dígitos]

    MenuPrincipal[Menu Principal]

    MenuPrincipal_RepetirSaldo[Repetir saldo, Limite extrato]
    MenuPrincipal_CodigoBarras[Código de barras para pagamento da fatura]
    MenuPrincipal_ProgramaRecompensas[Programa de recompensas]
    MenuPrincipal_ComprasNaoReconhecidas[Compras não reconhecidas]
    MenuPrincipal_InformacaoSenha[Informação da senha do Cartão de crédito]
    MenuPrincipal_OutraSolicitacao[Outra solicitação]
    MenuPrincipal_OutroCartao[Outro cartão]

    MenuPrincipal_OutraSolicitacao_Servicos[Serviços Celular ou internet banking]
    MenuPrincipal_OutraSolicitacao_Taxas[Taxas e cotações]
    MenuPrincipal_OutraSolicitacao_4[4]
    MenuPrincipal_OutraSolicitacao_Cancelamento[Cancelamento por desinteresse]
    MenuPrincipal_OutraSolicitacao_Protecao[Proteção cartão]
    MenuPrincipal_OutraSolicitacao_Alteracoes[Alterações cadastrais]
    MenuPrincipal_OutraSolicitacao_Atendente[Atendente]
    MenuPrincipal_OutraSolicitacao_MenuAnterior[Menu anterior]

    Ligacao --> DadosBase_CartCPF
    DadosBase_CartCPF --> DadosBase_Agencia
    DadosBase_Agencia --> DadosBase_Conta
    DadosBase_Conta --> DadosBase_Senha
    DadosBase_Senha --> MenuPrincipal

    MenuPrincipal -->|2| MenuPrincipal_RepetirSaldo
    MenuPrincipal -->|5| MenuPrincipal_CodigoBarras
    MenuPrincipal -->|6| MenuPrincipal_ProgramaRecompensas
    MenuPrincipal -->|7| MenuPrincipal_ComprasNaoReconhecidas
    MenuPrincipal -->|8| MenuPrincipal_InformacaoSenha
    MenuPrincipal -->|9| MenuPrincipal_OutraSolicitacao
    MenuPrincipal -->|0| MenuPrincipal_OutroCartao

    MenuPrincipal_OutraSolicitacao -->|2| MenuPrincipal_OutraSolicitacao_Servicos
    MenuPrincipal_OutraSolicitacao -->|3| MenuPrincipal_OutraSolicitacao_Taxas
    MenuPrincipal_OutraSolicitacao -->|4| MenuPrincipal_OutraSolicitacao_4
    MenuPrincipal_OutraSolicitacao -->|5| MenuPrincipal_OutraSolicitacao_Cancelamento
    MenuPrincipal_OutraSolicitacao -->|6| MenuPrincipal_OutraSolicitacao_Protecao
    MenuPrincipal_OutraSolicitacao -->|8| MenuPrincipal_OutraSolicitacao_Alteracoes
    MenuPrincipal_OutraSolicitacao -->|9| MenuPrincipal_OutraSolicitacao_Atendente
    MenuPrincipal_OutraSolicitacao -->|0| MenuPrincipal_OutraSolicitacao_MenuAnterior
```
