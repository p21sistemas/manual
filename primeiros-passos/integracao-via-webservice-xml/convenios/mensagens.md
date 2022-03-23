# Mensagens

### Estrutura da resposta do serviço

| **Atributo**     | **Descrição**                                        |
| ---------------- | ---------------------------------------------------- |
| nome\_arquivo    | Nome do arquivo no processamento                     |
| datahora         | Data e hora do processamento no WebService           |
| dataoperacao     | Data do movimento considerada pelo sistema da CRA    |
| codigo           | Código da mensagem                                   |
| ocorrencia       | Descrição da mensagem                                |
| registro         | Linha do registro do arquivo com erro                |
| total\_registros | Total de registros que foram processados com sucesso |

### Exemplos de respostas

**Envio de remessa com sucesso**

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <nome_arquivo>B9901308.121</nome_arquivo>
    <comarca codmun="3550308">
        <datahora>201208131020</datahora>
        <dataoperacao>20120814</dataoperacao>
        <codigo>0000</codigo>
        <ocorrencia>REGISTROS OK</ocorrencia>
        <total_registros>10</total_registros>
    </comarca>
</relatorio>
```

#### **Envio de remessa com exceção**

Como um arquivo de remessa pode conter títulos para várias comarcas, o serviço de upload pode recusar uma remessa parcialmente ou completamente, em caso de erros no preenchimento do XML.

* Envio com recusa parcial

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <nome_arquivo>B9901308.121</nome_arquivo>
    <comarca codmun="3550308">
        <datahora>201208131020</datahora>
        <codigo>0000</codigo>
        <ocorrencia>REGISTROS OK</ocorrencia>
        <total_registros>10</total_registros>
    </comarca>
    <comarca codmun="3509502">
        <datahora>201208101020</datahora>
        <dataoperacao>20120814</dataoperacao>
        <registro>10</registro>
        <codigo>1217</codigo>
        <ocorrencia>APRESENTANTE NÃO AUTORIZADO A ENVIAR TÍTULOS PARA O MUNICÍPIO (3509502 - PIRACURUCA)</ocorrencia>
        <total_registros>0</total_registros>
    </comarca>
</relatorio>
```

* Envio com recusa completa

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <nome_arquivo>B9901008.121</nome_arquivo>
    <comarca codmun="3550308">
        <datahora>201804181559</datahora>
        <total_registros>0</total_registros>
    </comarca>
    <comarca codmun="3509502">
        <datahora>201208101020</datahora>
        <registro>10</registro>
        <codigo>1217</codigo>
        <ocorrencia>Campo 17 TRANSAÇÃO - VALOR DO TITULO DEVE SER NUMERICO</ocorrencia>
        <total_registros>0</total_registros>
    </comarca>
</relatorio>
```

* Envio com erro no arquivo

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo> B9901008.121</nome_arquivo>
    <codigo>1001</codigo>
    <ocorrencia>ARQUIVO JA TRANSMITIDO</ocorrencia>
</relatorio>
```

**Envio de remessa com imagem**

Esse modo de mensagem é ativado por parâmetro interno do sistema devido ao impacto no tempo da resposta. A mensagem considera as imagens no registro do primeiro devedor.

```xml
<relatorio>
    <nome_arquivo>B9991001.186</nome_arquivo>
    <comarca codmun="2200202">
        <datahora>201901101714</datahora>
        <dataoperacao>20190110</dataoperacao>
        <total_registros>10</total_registros>
        <titulos>
            <titulo>
                <nome_devedor>SR. AARON CORTS</nome_devedor>
                <documento_devedor>28891000141</documento_devedor>
                <saldo>692.91</saldo>
                <numero_titulo>35468930037</numero_titulo>
                <nosso_numero>802150541451059</nosso_numero>
                <imagem>Corrompida</imagem>
            </titulo>
            <titulo>
                <nome_devedor>RICARDO CALDEIRA</nome_devedor>
                <documento_devedor>06572000199</documento_devedor>
                <saldo>60.23</saldo>
                <numero_titulo>33922734313</numero_titulo>
                <nosso_numero>426048244534158</nosso_numero>
                <imagem>Sem imagem</imagem>
            </titulo>
            <titulo>
                <nome_devedor>DR. ZIRALDO PACHECO COLAO FILHO</nome_devedor>
                <documento_devedor>37015000185</documento_devedor>
                <saldo>766.11</saldo>
                <numero_titulo>89975829217</numero_titulo>
                <nosso_numero>741775808168472</nosso_numero>
                <imagem>Gravada</imagem>
            </titulo>
        </titulos>
        <codigo>0000</codigo>
        <ocorrencia>REGISTROS OK</ocorrencia>
    </comarca>
</relatorio>
```

**Envio de imagem do título após envio da remessa**

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<remessas>
    <remessa>
        <sequencial>33</sequencial>
        <titulos>
            <titulo>
                <documento_devedor>39346889187</documento_devedor>
                <nosso_numero>2087753600052</nosso_numero>
                <numero_titulo>1412650</numero_titulo>
                <saldo>2442.86</saldo>
                <mensagem>
                    <codigo>2196</codigo>
                    <descricao>Título não encontrado.</descricao>
                </mensagem>
            </titulo>
        </titulos>
    </remessa>
</remessas>
```

**Download retorno**

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <datahora>201208151509</datahora>
    <codigo>0003</codigo>
    <ocorrencia>NÃO HÁ REGISTROS DE RETORNO NESTA DATA</ocorrencia>
</relatorio>
```

#### **Envio de Desistência/Cancelamento/Autorização**

* Envio com sucesso

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <nome_arquivo>DP9901308.121</nome_arquivo>
    <titulo>
        <datahora>201208101020</datahora>
        <numero_cartorio>01</numero_cartorio>
        <numero_titulo>00345468</numero_titulo>
        <numero_protocolo>1234</numero_protocolo>
        <data_protocolo>13082012</data_protocolo>
        <codigo>0000</codigo>
        <ocorrencia> SOLICITAÇÃO RECEBIDA COM SUCESSO </ocorrencia>
    </titulo>
</relatorio>
```

* Envio com erro

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <nome_arquivo>DP9901008.121</nome_arquivo>
    <titulo>
        <datahora>201208101020</datahora>
        <numero_cartorio>01</numero_cartorio>
        <numero_titulo>003454689</numero_titulo>
        <numero_protocolo>12345</numero_protocolo>
        <data_protocolo>14082012</data_protocolo>
        <codigo>2007</codigo>
        <ocorrencia>DATA DO PROTOCOLO (DDMMAAAA) INVÁLIDA</ocorrencia>
    </titulo>
</relatorio>
```

#### **Download confirmação**

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <nome_arquivo>C9901308.111</nome_arquivo>
    <datahora>201208131430</datahora>
    <codigo>0002</codigo>
    <ocorrencia>NOME DO ARQUIVO INVÁLIDO</ocorrencia>
</relatorio>
```

#### **Download retorno**

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<relatorio>
    <nome_arquivo>R9901508.121</nome_arquivo>
    <datahora>201208151509</datahora>
    <codigo>0003</codigo>
    <ocorrencia>NÃO HÁ REGISTROS DE RETORNO NESTA DATA</ocorrencia>
</relatorio>
```

#### **Consulta título**

* Quando o título não for encontrado

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<consulta>
    <data_consulta>30/09/2016</data_consulta>
</consulta>
```

### Mensagens retornadas

#### **Remessa**

| **CÓDIGO** | **RECUSA** | **DESCRIÇÃO**                                                                                                                                      |
| ---------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0000       |            | REGISTROS OK                                                                                                                                       |
| 0001       | COMPLETO   | FALHA NA AUTENTICAÇÃO                                                                                                                              |
| 0002       | COMPLETO   | NOME DO ARQUIVO INVÁLIDO                                                                                                                           |
| 2139       | COMPLETO   | JÁ PASSOU DO HORÁRIO LIMITE PARA ENVIO DA REMESSA                                                                                                  |
| 0004       | COMPLETO   | ARQUIVO XML INVÁLIDO. (Caracteres inválidos, erros na estrutura do XML, etc.)                                                                      |
| 0009       | COMPLETO   | A INSTITUIÇÃO (XXX) DO USUÁRIO ESTÁ INATIVA                                                                                                        |
| 2117       | PARCIAL    | MUNICÍPIO: XXXXX – XXXXX. SEQUENCIAL (XXX) JÁ ENVIADO: ÚLTIMO SEQUENCIAL: (XXX).                                                                   |
| 1001       | COMPLETO   | ARQUIVO JA TRANSMITIDO                                                                                                                             |
| 1101       | COMPLETO   | Campo 01 HEADER – FALTOU HEADER (TRANSACAO)                                                                                                        |
| 1102       | PARCIAL    | Campo 02 HEADER – CODIGO DO APRESENTANTE INVALIDO                                                                                                  |
| 1105       | COMPLETO   | Campo 05 HEADER – CONTEUDO PERMITIDO: ‘BFO’                                                                                                        |
| 1106       | COMPLETO   | Campo 06 HEADER – CONTEUDO PERMITIDO: ‘SDT’                                                                                                        |
| 1107       | COMPLETO   | Campo 07 HEADER – CONTEUDO PERMITIDO: ‘TPR’                                                                                                        |
| 1109       | COMPLETO   | Campo 09 HEADER – QUANTIDADE DE REGISTROS INVALIDA                                                                                                 |
| 1305       | COMPLETO   | Campo 10 HEADER – TRAILLER – SOM.SEGURANCA-QTDE – INFORMADO Y / CALCULADO X                                                                        |
| 1305       | COMPLETO   | Campo 11 HEADER – TRAILLER – SOM.SEGURANCA-QTDE – INFORMADO Y / CALCULADO X                                                                        |
| 1305       | COMPLETO   | Campo 12 HEADER – TRAILLER – SOM.SEGURANCA-QTDE – INFORMADO Y / CALCULADO X                                                                        |
| 2103       | PARCIAL    | Campo 15 HEADER – Município: (XXX) não cadastrado na CRA.                                                                                          |
| 1102       | COMPLETO   | Campo 16 HEADER – CAMPO 02 HEADER – CODIGO DO APRESENTANTE INVALIDO                                                                                |
| 1117       | COMPLETO   | Campo 17 HEADER – ARQUIVO FORA DE SEQUENCIA                                                                                                        |
| 1201       | COMPLETO   | Campo 01 TRANSAÇÃO – CONTEUDO PERMITIDO: 1 – ATRIBUTO T01                                                                                          |
| 1202       | COMPLETO   | Campo 02 TRANSAÇÃO- CODIGO DO APRESENTANTE INVALIDO                                                                                                |
| 2137       | COMPLETO   | Campo 04 TRANSAÇÃO – CAMPO (NOME DO CEDENTE) INVÁLIDO                                                                                              |
| 1211       | COMPLETO   | Campo 11 TRANSAÇÃO – NOSSO NUMERO EM BRANCO                                                                                                        |
| 1212       | COMPLETO   | Campo 12 TRANSAÇÃO – ESPECIE DO TITULO EM BRANCO                                                                                                   |
| 2137       | COMPLETO   | Campo 14 TRANSAÇÃO – CAMPO (DATA DE EMISSÃO) INVÁLIDO                                                                                              |
| 2137       | COMPLETO   | Campo 15 TRANSAÇÃO – CAMPO (DATA DE VENCIMENTO) INVÁLIDO                                                                                           |
| 1217       | COMPLETO   | Campo 17 TRANSAÇÃO – VALOR DO TITULO DEVE SER NUMERICO                                                                                             |
| 1218       | COMPLETO   | Campo 18 TRANSAÇÃO – VALOR DO SALDO DEVE SER NUMERICO                                                                                              |
| 2111       | COMPLETO   | Campo 22 TRANSAÇÃO – SEQUENCIAL DO DEVEDOR INVÁLIDO                                                                                                |
| 2112       | COMPLETO   | Campo 23 TRANSAÇÃO – INFORMAR O NOME DO DEVEDOR.                                                                                                   |
| 2113       | COMPLETO   | Campo 25 TRANSAÇÃO – INFORMAR O DOCUMENTO DO DEVEDOR                                                                                               |
| 1238       | COMPLETO   | Campo 38 TRANSAÇÃO – CONTEUDO PERMITIDO: BRANCO                                                                                                    |
| 1252       | COMPLETO   | Campo 52 TRANSAÇÃO – NUM. SEQUENCIAL DO REGISTRO INVALIDO                                                                                          |
| 1301       | COMPLETO   | Campo 01 TRAILLER – CONTEUDO PERMITIDO: 9                                                                                                          |
| 1302       | COMPLETO   | Campo 02 TRAILLER – CODIGO DO APRESENTANTE INVALIDO                                                                                                |
| 1305       | COMPLETO   | Campo 05 TRAILLER – SOM.SEGURANCA-QTDE – INFORMADO Y / CALCULADO X                                                                                 |
| 1306       | COMPLETO   | Campo 06 TRAILLER – SOM.SEGURANCA-VLR.REMESSA – INFORMADO Y / CALCULADO X                                                                          |
| 1308       | COMPLETO   | Campo 08 TRAILLER – NUM. SEQUENCIAL DO REGISTRO INVALIDO                                                                                           |
| 2105       | PARCIAL    | Apresentante não autorizado a enviar títulos para o município (XXX – XXX).                                                                         |
| 2110       | COMPLETO   | Arquivo corrompido. Soma de originais existentes no arquivo (XX) não confere com total informado no header (XX).                                   |
| 2160       | COMPLETO   | REMESSA NÃO PODE SER ENVIADA APÓS O DIA LIMITE                                                                                                     |
| 2181       | PARCIAL    | REMESSAS DE XXX (XXX) DEVEM SER ENVIADAS PARA XXX (XXX).                                                                                           |
| 2182       | COMPLETO   | ARQUIVO CORROMPIDO. TIPO DO REGISTRO NÃO ENCONTRADO.                                                                                               |
| 2101       | PARCIAL    | Arquivo contém caractere que não está no padrão ASCII. Linha: XXXX – COLUNA(s): XXXX.                                                              |
| 2102       | PARCIAL    | Arquivo corrompido. Tamanho da linha inválido. Tamanho: XXXX – Linha: XXXX.                                                                        |
| 2104       | PARCIAL    | Município: XXXX – XXXX não possui cartório na CRA.                                                                                                 |
| 2106       | PARCIAL    | Município: XXXX – XXXX não está ativo                                                                                                              |
| 2107       | PARCIAL    | Sequencial do devedor inválido (XXXX)                                                                                                              |
| 2108       | COMPLETO   | Arquivo corrompido. Soma de títulos existentes no arquivo (XXXX) não confere com total informado no header (XXXX).                                 |
| 2109       | COMPLETO   | Arquivo corrompido. Soma de indicações existentes no arquivo (XXXX) não confere com total informado no header (XXXX).                              |
| 1253       | COMPLETO   | TÍTULO NÃO PODE SER ENVIADO COM SALDO (X) SUPERIOR AO PERMITIDO (Y) PARA O APRESENTANTE.                                                           |
| 2200       | COMPLETO   | TÍTULOS APRESENTADOS EXCEDEM A QUANTIDADE MÁXIMA PERMITIDA NO MÊS PARA O MUNICÍPIO (XXXXXXX – XXXXXXX). ENVIADOS: XXXX – LIMITE: XXXX LINHA: XXXX. |
| 2201       | COMPLETO   | TÍTULOS APRESENTADOS EXCEDEM A QUANTIDADE MÁXIMA PERMITIDA NO DIA PARA O MUNICÍPIO (XXXXXXX – XXXXXXX). ENVIADOS: XXXX – LIMITE: XXXX LINHA: XXXX  |
| 2222       | COMPLETO   | TÍTULOS APRESENTADOS EXCEDEM A QUANTIDADE MÁXIMA PERMITIDA NO MÊS. ENVIADOS: XXXX – LIMITE: XXXX.                                                  |
| 2212       | COMPLETO   | REMESSA POSSUI DEVEDOR QUE NÃO PODE SER PROTESTADO. DOCUMENTO: XXXX.                                                                               |
| 2219       | COMPLETO   | O SALDO DO TÍTULO É MENOR QUE O MÍNIMO PERMITIDO XXXX PARA APRESENTAR A ESPÉCIE XXXX. SALDO: XXXX. NÚMERO: XXXX. LINHA: XXXX.                      |
| 2220       | COMPLETO   | A DATA DE VENCIMENTO DO TÍTULO É SUPERIOR AO PRAZO MÁXIMO PREMITIDO PARA APRESENTAR A ESPÉCIE XXXX. NÚMERO: XXXX. LINHA: XXXX.                     |
| 2231       | COMPLETO   | A ÚLTIMA LINHA PRECISA SER UM TRAILLER (9)                                                                                                         |
| 2229       | COMPLETO   | A LINHA QUE ANTECEDE O TRAILLER PRECISA SER UMA TRANSAÇÃO (1)                                                                                      |
| 2305       | COMPLETO   | Documento do devedor inválido. (999.999.999-99)                                                                                                    |
| 2316       | COMPLETO   | Custas do cartório/distribuidor não podem ser informadas para títulos sem pedido de desistência. Protocolo: XXX.                                   |
| 10000      | COMPLETO   | 1.5 ARQUIVO XML CORROMPIDO.                                                                                                                        |

#### **Imagem no arquivo de remessa**

| **DESCRIÇÃO** |
| ------------- |
| Gravada       |
| Sem imagem    |
| Corrompida    |

**Imagem do título após envio da remessa**

| **CÓDIGO** | **DESCRIÇÃO**                                                                                     |
| ---------- | ------------------------------------------------------------------------------------------------- |
| 2225       | CAMPOS OBRIGATÓRIOS NÃO PREENCHIDOS (xxxxxx).                                                     |
| 2226       | ARQUIVO INVÁLIDO. EXISTEM ERROS NA ESTRUTURA DO XML.                                              |
| 2232       | EXTENSÃO DO ARQUIVO INVÁLIDO. SÃO PERMITIDOS APENAS ARQUIVOS NO FORMATO (.PDF, .JPG, .PNG E .P7S) |

**Desistência/Cancelamento/Autorização**

| **CÓDIGO** | **DESCRIÇÃO**                                                                               |
| ---------- | ------------------------------------------------------------------------------------------- |
| 0000       | SOLICITAÇÃO RECEBIDA COM SUCESSO                                                            |
| 0001       | FALHA NA AUTENTICAÇÃO                                                                       |
| 0009       | A INSTITUIÇÃO (XXX) DO USUÁRIO ESTÁ INATIVA                                                 |
| 0002       | NOME DO ARQUIVO INVÁLIDO                                                                    |
| 2141       | JÁ PASSOU DO HORÁRIO LIMITE PARA ENVIO DE DESISTÊNCIA                                       |
| 2140       | JÁ PASSOU DO HORÁRIO LIMITE PARA ENVIO DE CANCELAMENTO                                      |
| 2024       | FALTOU INFORMAR A TAG: DESISTENCIA                                                          |
| 2023       | FALTOU INFORMAR A TAG: CANCELAMENTO                                                         |
| 0007       | FALTA A TAG: COMARCA NO XML                                                                 |
| 2001       | COMARCA NÃO CONVENIADA                                                                      |
| 2002       | CARTORIO XX INVÁLIDO / NÃO EXISTE                                                           |
| 2004       | NUMERO DO PROTOCOLO EM BRANCO                                                               |
| 2005       | NUMERO DO PROTOCOLO INVÁLIDO                                                                |
| 2006       | NUMERO DO PROTOCOLO DEVE CONTER NO MAXIMO 10 DIGITOS                                        |
| 2007       | DATA DO PROTOCOLO (DDMMAAAA) INVÁLIDA                                                       |
| 2008       | NUMERO DO TITULO EM BRANCO                                                                  |
| 2008       | NUMERO DO TITULO DEVE CONTER NO MAXIMO 11 DIGITOS                                           |
| 2009       | NOME DO DEVEDOR EM BRANCO                                                                   |
| 2010       | VALOR DO TITULO INVÁLIDO                                                                    |
| 2159       | APRESENTANTE NÃO AUTORIZADO A ENVIAR PEDIDO DE CANCELAMENTO                                 |
| 2012       | TITULO NAO ENCONTRADO                                                                       |
| 2013       | TITULO NAO FOI PROTESTADO                                                                   |
| 2014       | AUTORIZAÇÃO EM DUPLICIDADE                                                                  |
| 2015       | TÍTULO PERTENCE A OUTRO APRESENTANTE                                                        |
| 2016       | O TÍTULO JÁ POSSUI CANCELAMENTO. PROTOCOLO: (XX)                                            |
| 2017       | O TITULO JÁ POSSUI AUTORIZACAO DE CANCELAMENTO                                              |
| 2018       | IMAGEM INVÁLIDA OU ASSINADA INCORRETAMENTE                                                  |
| 2019       | FALTOU INFORMAR A TAG: CODMUN                                                               |
| 2020       | FALTOU INFORMAR A TAG: NUMERO\_CARTORIO                                                     |
| 2021       | FALTOU INFORMAR A TAG: TITULO                                                               |
| 2022       | FALTOU INFORMAR A TAG: CARTORIO                                                             |
| 2023       | FALTOU INFORMAR A TAG: CANCELAMENTO                                                         |
| 2024       | FALTOU INFORMAR A TAG: DESISTENCIA                                                          |
| 2025       | FALTOU INFORMAR A TAG: AUTORIZACAO                                                          |
| 2026       | FALTOU INFORMAR A TAG: AUTORIZA\_DESISTENCIA                                                |
| 2027       | TAG NUMERO\_CARTORIO INFORMADA EM DUPLICIDADE                                               |
| 2028       | TÍTULO JÁ POSSUI RETORNO                                                                    |
| 2191       | NÃO CONSTA PEDIDO DE CANCELAMENTO EM ARQUIVO ASSINADO COM CERTIFICADO DIGITAL PARA O TÍTULO |

**Confirmação**

| **CÓDIGO** | **DESCRIÇÃO**                               |
| ---------- | ------------------------------------------- |
| 0001       | FALHA NA AUTENTICAÇÃO                       |
| 0002       | NOME DO ARQUIVO INVÁLIDO                    |
| 0005       | NÃO EXISTE CONFIRMAÇÃO NA DATA INFORMADA.   |
| 0009       | A INSTITUIÇÃO (XXX) DO USUÁRIO ESTÁ INATIVA |

**Retorno**

| **CÓDIGO** | **DESCRIÇÃO**                                                                             |
| ---------- | ----------------------------------------------------------------------------------------- |
| 0001       | FALHA NA AUTENTICAÇÃO                                                                     |
| 0002       | NOME DO ARQUIVO INVÁLIDO                                                                  |
| 0004       | NÃO EXISTE RETORNO NA DATA INFORMADA.                                                     |
| 0009       | A INSTITUIÇÃO (XXX) DO USUÁRIO ESTÁ INATIVA                                               |
| 2163       | Já foi enviado arquivo de retorno com o sequencial (XXXX) para o apresentante XXXX (XXXX) |

**Consulta slip**

| **CÓDIGO** | **DESCRIÇÃO**                           |
| ---------- | --------------------------------------- |
| 2183       | CÓDIGO DO MUNICÍPIO NÃO INFORMADO.      |
| 2184       | CÓDIGO DO CARTÓRIO NÃO INFORMADO.       |
| 2185       | DATA INVÁLIDA.                          |
| 2187       | PROTOCOLO NÃO INFORMADO.                |
| 2188       | TÍTULO NÃO ENCONTRADO OU NÃO RETORNADO. |
