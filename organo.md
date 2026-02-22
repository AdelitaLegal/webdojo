# Documentação de Fluxos de Boletos

Este documento descreve as funcionalidades de gestão de boletos e seus serviços compartilhados.

## Organograma Funcional

```mermaid
graph TD
    %% Funcionalidades
    F1[1. Pesquisar Próximo Boleto]
    F2[2. Criar Boleto Residual]
    F3[3. Baixar Boleto]
    F4[4. Enviar por E-mail]
    F5[5. Enviar Boleto + Carta]

    %% Serviços Comuns
    S1((Serviço de Busca))
    S2((Motor de Registro))
    S3((Gerador de PDF))
    S4((Serviço de Carta Acordo))

    %% Conexões
    F1 --> S2
    F2 --> S2
    F3 --> S1
    F4 --> S1
    F5 --> S1
    F5 --> S4
