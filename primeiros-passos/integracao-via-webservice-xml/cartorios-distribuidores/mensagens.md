# Mensagens

**Mensagens**

* Download remessa

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>B0001911.141</nome_arquivo>
    <datahora>201411191158</datahora>
    <codigo>0003</codigo>
    <ocorrencia>NÃO EXISTE REMESSA NA DATA INFORMADA.</ocorrencia>
</relatorio>
```

* Download desistência

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>DP0001911.141</nome_arquivo>
    <datahora>201411191201</datahora>
    <codigo>0006</codigo>
    <ocorrencia>NÃO EXISTE DESISTÊNCIA NA DATA INFORMADA.</ocorrencia>
</relatorio>
```

* Download cancelamento

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>CP0001911.141</nome_arquivo>
    <datahora>201411191200</datahora>
    <codigo>0007</codigo>
    <ocorrencia>NÃO EXISTE CANCELAMENTO NA DATA INFORMADA.</ocorrencia>
</relatorio>
```

**Upload confirmação**

* Envio com sucesso

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>C3411811.141</nome_arquivo>
    <comarca codmun="5300108">
        <datahora>201411181628</datahora>
        <dataoperacao>20141118</dataoperacao>
        <total_registros>2</total_registros>
        <codigo>0000</codigo>
        <ocorrencia>APRESENTANTE: ITAÚ (341) - SEQUENCIAL REMESSA: 000353 (2 TÍTULOS).</ocorrencia>
    </comarca>
</relatorio>
```

* Envio com erro

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>C0001811.141</nome_arquivo>
    <comarca codmun="5300108">
        <datahora>201411181708</datahora>
        <dataoperacao>20141118</dataoperacao>
        <total_registros>0</total_registros>
        <codigo>2117</codigo>
        <ocorrencia>JÁ• FOI ENVIADA REMESSA COM O MESMO SEQUENCIAL (000353) PARA O MUNICÍPIO (5300108).</ocorrencia>
    </comarca>
</relatorio>
```

* Envio com erro no arquivo

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>C3411811.141</nome_arquivo>
    <codigo>2116</codigo>
    <ocorrencia>O ARQUIVO C3411811.141 JÁ• FOI ENVIADO EM 18/11/2014.</ocorrencia>
</relatorio>
```

**Upload Retorno**

* Envio com sucesso

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>R0001811.141</nome_arquivo>
    <comarca codmun="5300108">
        <datahora>201411181631</datahora>
        <dataoperacao>20141118</dataoperacao>
        <total_registros>5</total_registros>
        <codigo>0000</codigo>
        <ocorrencia>APRESENTANTE: 341 – ITAÚ (5 TÍTULOS).</ocorrencia>
    </comarca>
</relatorio>
```

* Envio com erro

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>R0001911.141</nome_arquivo>
    <comarca codmun="5500108">
        <datahora>201411191350</datahora>
        <total_registros>0</total_registros>
        <codigo>2142</codigo>
        <ocorrencia>CÓDIGO DO MUNICÍPIO INFORMADO NO ARQUIVO (5500108) NÃO CORRESPONDE AO SEU MUNICÍPIO.</ocorrencia>
        <codigo>2151</codigo>
    </comarca>
</relatorio>
```

* Envio com erro no arquivo

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>R0001811.141</nome_arquivo>
    <codigo>2116</codigo>
    <ocorrencia>O ARQUIVO R0001811.141 JÁ• FOI ENVIADO EM 18/11/2014.</ocorrencia>
</relatorio>
```

* Envio com imagem no arquivo

```xml
<?xml version="1.0" encoding="ISO-8859-1" standalone="no"?>
<relatorio>
  <nome_arquivo>R9992606.181</nome_arquivo>
  <comarca CodMun="1234567">
    <datahora>201806221505</datahora>
    <dataoperacao>20180622</dataoperacao>
    <total_registros>5</total_registros>
    <titulos>
      <titulo>
        <protocolo>0000012345</protocolo>
        <data_protocolo>10052018</data_protocolo>
        <situacao>Não gravado</situacao>
        <imagem>Não gravada</imagem>
      </titulo>
      <titulo>
        <protocolo>0000012346</protocolo>
        <data_protocolo>10052018</data_protocolo>
        <situacao>Gravado</situacao>
        <imagem>Corrompida</imagem>
      </titulo>
      <titulo>
        <protocolo>0000012347</protocolo>
        <data_protocolo>10052018</data_protocolo>
        <situacao>Gravado</situacao>
        <imagem>Gravada</imagem>
      </titulo>
      <titulo>
        <protocolo>0000012348</protocolo>
        <data_protocolo>10052018</data_protocolo>
        <situacao>Gravado</situacao>
        <imagem>Sem imagem</imagem>
      </titulo>
      <titulo>
        <protocolo>0000012349</protocolo>
        <data_protocolo>10052018</data_protocolo>
        <situacao>Não gravado</situacao>
        <imagem>Sem imagem</imagem>
      </titulo>
    </titulos>
    <codigo>0000</codigo>
    <ocorrencia>APRESENTANTE: 999 - TESTE (5 TÍTULOS).</ocorrencia>
  </comarca>
</relatorio>
```

**Mensagens**

* Imagem retorno

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no"?-->
<relatorio>
    <nome_arquivo>I0001810.171</nome_arquivo>
<imagem>
    <protocolo>0011038370</protocolo>
    <data_protocolo>07/02/2017</data_protocolo>
    <codigo>2191</codigo>
    <ocorrencia>IMAGEM SALVA COM SUCESSO.</ocorrencia>
</imagem>
<imagem>
    <protocolo>0003550308</protocolo>
    <data_protocolo>18/10/2017</data_protocolo>
    <codigo>2192</codigo>
    <ocorrencia>RETORNO NÃO ENCONTRADO.</ocorrencia>
</imagem>
<imagem>
    <protocolo>0003550308</protocolo>
    <data_protocolo>18/10/2017</data_protocolo>
    <codigo>2193</codigo>
    <ocorrencia>IMAGEM CORROMPIDA.</ocorrencia>
</imagem>
</relatorio>
```

### **ATRIBUTOS**

| **Atributo**     | **Descrição**                                                                               |
| ---------------- | ------------------------------------------------------------------------------------------- |
| nome\_arquivo    | Nome do arquivo no processamento                                                            |
| datahora         | Data e hora do processamento no WebService                                                  |
| dataoperacao     | Data do movimento considerada pelo sistema da CRA                                           |
| codigo           | Código da mensagem                                                                          |
| ocorrencia       | Descrição da mensagem                                                                       |
| registro         | Linha do registro do arquivo com erro                                                       |
| total\_registros | Total de registros que foram processados com sucesso                                        |
| situacao         | Informa se o retorno foi “Gravado" ou “Não Gravado" na CRA                                  |
| imagem           | No envio de retorno com images, informará se a imagem foi “Gravada" ou se está “Corrompida" |

**Remessa**

| **CÓDIGO** | **DESCRIÇÃO**                               |
| ---------- | ------------------------------------------- |
| 0001       | Falha na autenticação.                      |
| 0009       | A instituição (xxx) do usuário está inativa |
| 0002       | Nome do arquivo inválido.                   |
| 0003       | Não existe remessa na data informada.       |

**Desistência**

| **CÓDIGO** | **DESCRIÇÃO**                               |
| ---------- | ------------------------------------------- |
| 0001       | Falha na autenticação.                      |
| 0009       | A instituição (xxx) do usuário está inativa |
| 0002       | Nome do arquivo inválido.                   |
| 0006       | Não existe desistência na data informada.   |

**Cancelamento**

| **CÓDIGO** | **DESCRIÇÃO**                               |
| ---------- | ------------------------------------------- |
| 0001       | Falha na autenticação.                      |
| 0009       | A instituição (xxx) do usuário está inativa |
| 0002       | Nome do arquivo inválido.                   |
| 0007       | Não existe cancelamento na data informada.  |

**Autorização**

| **CÓDIGO** | **DESCRIÇÃO**                                          |
| ---------- | ------------------------------------------------------ |
| 0001       | Falha na autenticação.                                 |
| 0009       | A instituição (xxx) do usuário está inativa            |
| 0002       | Nome do arquivo inválido.                              |
| 0008       | Não existem autorizações para os parâmetros informados |

**ConsultaAutorizacao**

| **CÓDIGO** | **DESCRIÇÃO**                                          |
| ---------- | ------------------------------------------------------ |
| 0001       | Falha na autenticação.                                 |
| 0009       | A instituição (xxx) do usuário está inativa            |
| 0002       | Nome do arquivo inválido.                              |
| 0008       | Não existem autorizações para os parâmetros informados |

**Confirmação**

| **CÓDIGO** | **DESCRIÇÃO**                                                                                                                     |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------- |
| 0000       | Envio efetuado com sucesso                                                                                                        |
| 9999       | Erro no processamento do arquivo                                                                                                  |
| 0001       | Falha na autenticação.                                                                                                            |
| 0009       | A instituição (xxx) do usuário está inativa                                                                                       |
| 0002       | Nome do arquivo inválido.                                                                                                         |
| 2101       | Arquivo contém caractere que não está no padrão ASCII. Linha: XXX – Coluna(s): XXX.                                               |
| 2102       | Arquivo corrompido. Tamanho da linha inválido. Tamanho: XXX – Linha: XXX.                                                         |
| 2107       | Arquivo corrompido. Número de controle do devedor (XXX) não está contínuo.                                                        |
| 2108       | Arquivo corrompido. Soma de títulos existentes no arquivo (XXX) não confere com total informado no header (XXX).                  |
| 2109       | Arquivo corrompido. Soma de indicações existentes no arquivo (XXX) não confere com total informado no header (XXX).               |
| 2110       | Arquivo corrompido. Soma de originais existentes no arquivo (XXX) não confere com total informado no header (XXX).                |
| 2114       | Arquivo corrompido. Número sequencial do registro no header (XXX) não está contínuo. Faltou registro (XXX).                       |
| 2116       | O arquivo XXX já foi enviado em XXX.                                                                                              |
| 2117       | JÁ FOI ENVIADA REMESSA COM O MESMO SEQUENCIAL (XXXXX) PARA O MUNICÍPIO (XXXXX)                                                    |
| 2120       | Arquivo corrompido. Número sequencial do registro na transação (XXX) não está contínuo. Faltou registro (XXX).                    |
| 2122       | Arquivo corrompido. Soma de registros de transação existentes no arquivo (XXX) não confere com total informado no header (XXX).   |
| 2123       | Arquivo corrompido. Somatório do saldo no trailler (XXX) não confere com somatório dos saldos dos títulos (XXX).                  |
| 2126       | Arquivo corrompido. Número sequencial do registro no trailler do cartório (XXX) não está contínuo. Faltou registro (XXX).         |
| 2134       | Protocolo inválido (XXX).                                                                                                         |
| 2135       | Data do protocolo inválida (XXX).                                                                                                 |
| 2136       | Arquivo corrompido. Somatório de segurança dos registros (XXX) não confere com a soma das quantidades informadas no header (XXX). |
| 2142       | Código do município informado no arquivo (XXX) não corresponde ao seu município.                                                  |
| 2143       | Não existe remessa (XXX) do apresentante (XXX – XXX) para ser confirmada.                                                         |
| 2144       | Arquivo corrompido. Este arquivo não é de confirmação de remessa (tipo CRT).                                                      |
| 2145       | Título: XXX Remessa: XXX Apresentante: XXX Nosso Número: XXX Sequencial Registro: XXX. Não foi encontrado na CRA.                 |
| 2146       | Código de ocorrência inválido (XXX).                                                                                              |
| 2147       | Código de irregularidade inválido (XXX).                                                                                          |
| 2148       | Data de ocorrência inválida (XXX).                                                                                                |
| 2149       | Data do protocolo (XXX) anterior à data da remessa (XXX)                                                                          |
| 2150       | Código de cartório não informado.                                                                                                 |
| 2151       | Código de cartório inválido ou não encontrado no município (XXX).                                                                 |
| 2152       | Código do cartório informado no arquivo deve ser o mesmo do cartório logado.                                                      |
| 2153       | Campo “XXX" diferente do informado no envio da remessa.                                                                           |
| 2154       | Apresentante: XXX – Sequencial Remessa: XXX não foi encontrado na CRA.                                                            |
| 2155       | Já foi enviado título com o Protocolo XXX e Data XXX no dia XXX.                                                                  |
| 2156       | Os dados da devolução devem ser os mesmos para todos os devedores do título.                                                      |
| 2157       | Os dados da confirmação devem ser os mesmos para todos os devedores do título.                                                    |
| 2158       | Apresentante: XXX (XXX) – Sequencial Remessa: XXX (Faltam títulos enviados na remessa).                                           |
| 2161       | Campo demais despesas pode ser informado somete para título liquidado ou protesto. Protocolo XXXXXXXXXX                           |
| 2221       | Custas do cartório não podem ser informadas para títulos com cobrança de emolumentos no cancelamento                              |
| 10000      | 1.5 ARQUIVO XML CORROMPIDO.                                                                                                       |

**Retorno**

| **CÓDIGO** | **DESCRIÇÃO**                                                                                                                                                                                       |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0000       | Envio efetuado com sucesso                                                                                                                                                                          |
| 9999       | Erro no processamento do arquivo                                                                                                                                                                    |
| 0001       | Falha na autenticação.                                                                                                                                                                              |
| 0009       | A instituição (xxx) do usuário está inativa                                                                                                                                                         |
| 0002       | Nome do arquivo inválido.                                                                                                                                                                           |
| 2101       | Arquivo contém caractere que não está no padrão ASCII. Linha: XXX – Coluna(s): XXX.                                                                                                                 |
| 2102       | Arquivo corrompido. Tamanho da linha inválido. Tamanho: XXX – Linha: XXX.                                                                                                                           |
| 2114       | Arquivo corrompido. Número sequencial do registro no header (XXX) não está contínuo. Faltou registro (XXX).                                                                                         |
| 2116       | O arquivo XXX já foi enviado em XXX.                                                                                                                                                                |
| 2120       | Arquivo corrompido. Número sequencial do registro na transação (XXX) não está contínuo. Faltou registro (XXX).                                                                                      |
| 2121       | Arquivo corrompido. Número sequencial do registro no trailler (XXX) não está contínuo. Faltou registro (XXX).                                                                                       |
| 2122       | Arquivo corrompido. Soma de registros de transação existentes no arquivo (XXX) não confere com total informado no header (XXX).                                                                     |
| 2123       | Arquivo corrompido. Somatório do saldo no trailler (XXX) não confere com somatório dos saldos dos títulos (XXX).                                                                                    |
| 2142       | Código do município informado no arquivo (XXX) não corresponde ao seu município.                                                                                                                    |
| 2146       | Código de ocorrência inválido (XXX).                                                                                                                                                                |
| 2147       | Código de irregularidade inválido (XXX).                                                                                                                                                            |
| 2148       | Data de ocorrência inválida (XXX).                                                                                                                                                                  |
| 2135       | Data do protocolo inválida (XXX).                                                                                                                                                                   |
| 2151       | Código de cartório inválido ou não encontrado no município (XXX).                                                                                                                                   |
| 2152       | Código do cartório informado no arquivo deve ser o mesmo do cartório logado.                                                                                                                        |
| 2154       | Apresentante: XXX – Sequencial Remessa: XXX não foi encontrado na CRA.                                                                                                                              |
| 2137       | Campo (XXX) inválido.                                                                                                                                                                               |
| 2161       | Nenhum registro foi gravado.                                                                                                                                                                        |
| 2162       | Arquivo corrompido. Este arquivo não é de retorno de remessa (tipo RTP).                                                                                                                            |
| 2163       | Já foi enviado arquivo de retorno com o sequencial (XXX) para o apresentante XXX (XXX)                                                                                                              |
| 2164       | Arquivo corrompido. Faltou informar o campo Agência Centralizadora.                                                                                                                                 |
| 2165       | Arquivo corrompido. Faltou informar o campo Agência/Código do Cedente.                                                                                                                              |
| 2166       | Arquivo corrompido. Campo Agência Centralizadora inválido (XXX).                                                                                                                                    |
| 2167       | Arquivo corrompido. Campo Agência/Código do Cedente inválido (XXX).                                                                                                                                 |
| 2168       | Arquivo corrompido. Campo Agência/Código do Cedente (XXX) não pode ser menor que 10 posições.                                                                                                       |
| 2169       | Arquivo corrompido. Faltou informar o campo nosso número.                                                                                                                                           |
| 2170       | Valor do saldo do título no retorno (XXX) menor que o valor do saldo na remessa (XXX).                                                                                                              |
| 2171       | Existem títulos no arquivo com o mesmo protocolo (XXX) ou nosso número (XXX) para o cartório (XXX).                                                                                                 |
| 2172       | Arquivo corrompido. Somatório de segurança dos registros (XXX) não confere com a quantidade informada no trailler (XXX).                                                                            |
| 2173       | Custas do cartório não pode ser informada para título pago. Protocolo: XXX.                                                                                                                         |
| 2174       | Título liquidado não pode ser informado com custas de distribuição. Protocolo: XXX.                                                                                                                 |
| 2175       | Valor do título inválido (XXX). É permitido somente caracteres numéricos.                                                                                                                           |
| 2176       | Saldo do título inválido (XXX). É permitido somente caracteres numéricos.                                                                                                                           |
| 2177       | Cartório não autorizado a trabalhar com o apresentante (XXX – XXX).                                                                                                                                 |
| 2178       | Campo Nosso Número do retorno está diferente do informado na remessa.                                                                                                                               |
| 2179       | Título não foi encontrado na remessa.                                                                                                                                                               |
| 2180       | As custas informadas (XXX) não podem ser maior do que o máximo estabelecido (XXX) no cadastro de emolumentos. Protocolo: (XXX).                                                                     |
| 2190       | Valor do saldo informado no arquivo (XXX) menor que o valor mínimo esperado (XXX).                                                                                                                  |
| 2194       | Existe retorno, do apresentante (XXXX) gerado manualmente e não enviado. Verifique na tela gerar retorno ou entre em contato com a CRA e solicite que providencie o envio ou a exclusão do retorno. |
| 2209       | JÁ PASSOU DO HORÁRIO LIMITE PARA ENVIO DO RETORNO                                                                                                                                                   |
| 2210       | SOMA DOS VALORES DE TED/DOC DOS TÍTULOS PAGOS (XXX) MAIOR QUE O PERMITIDO (XXX). APRESENTANTE : XXX – CARTÓRIO: XX                                                                                  |
| 2211       | SOMA DOS VALORES DE SEDEX DOS TÍTULOS PROTESTADOS (XXX) MAIOR QUE O PERMITIDO (XXX). APRESENTANTE : XXX – CARTÓRIO: XX                                                                              |
| 2215       | Não é possível enviar mais de um retorno no mesmo dia com título pago e demais despesas.                                                                                                            |
| 2216       | Arquivo não está assinado corretamente ou foi modificado.                                                                                                                                           |
| 2217       | Informar custas do cartório nos títulos de apresentantes com cobrança na confirmação. Linha: xxx                                                                                                    |
| 2238       | CÓDIGO DO MUNICÍPIO OU CÓDIGO DO CARTÓRIO INVÁLIDOS.                                                                                                                                                |
| 2221       | Custas do cartório não podem ser informadas para títulos com cobrança de emolumentos no cancelamento.                                                                                               |
| 2187       | Protocolo não informado.                                                                                                                                                                            |

**Imagens retorno**

| **CÓDIGO** | **DESCRIÇÃO**                                                              |
| ---------- | -------------------------------------------------------------------------- |
| 2191       | Imagem salva com sucesso.                                                  |
| 2192       | Retorno não encontrado.                                                    |
| 2193       | Imagem corrompida.                                                         |
| 0002       | Nome do arquivo inválido.                                                  |
| 2203       | O nome do arquivo XNNNDDMM.AAS não corresponde ao tipo de arquivo enviado. |
| 2206       | O ARQUIVO INFORMADO ESTÁ CORROMPIDO OU NÃO É DO TIPO ZIP                   |

**Salvar situação / Buscar situação**

| **CÓDIGO** | **DESCRIÇÃO**                      |
| ---------- | ---------------------------------- |
| 0          | Transação efetuada                 |
| 1          | Erro na operação                   |
| 2          | Título não encontrado              |
| 4          | Requisição inválida                |
| 5          | Erro ao atualizar título           |
| 7          | Ocorrência não cadastrada          |
| 11         | Protocolo não informado            |
| 12         | Data de protocolagem não informada |
| 13         | Data da ocorrência não informada   |
| 14         | Ocorrência não informada           |
| 15         | Código do município não informado  |
| 16         | Código do cartório não informado   |

**Consulta slip**

| **CÓDIGO** | **DESCRIÇÃO**                        |
| ---------- | ------------------------------------ |
| 2195       | Título não requer impressão de slip. |
| 2196       | Título não encontrado.               |
| 2197       | Agência não cadastrada.              |
| 2187       | PROTOCOLO NÃO INFORMADO.             |
| 2185       | DATA INVÁLIDA.                       |
