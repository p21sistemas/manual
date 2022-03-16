# Download e Consulta

**CONFIRMAÇÃO E RETORNO**

* Informar somente o parâmetro “**user\_arq**”.
* Serão retornados todos os arquivos de **confirmação/retorno** conforme a data informada no nome do arquivo.

Por exemplo, ao requisitar a **CONFIRMAÇÃO** com o nome do arquivo **C3412401.141** será retornada a **CONFIRMAÇÃO** de 24/01/2014 independente da data de envio da **REMESSA**, tendo como base a data de envio da confirmação pelo cartório.

A mesma regra se aplica para o download de **RETORNO**.

**OBSERVAÇÃO**

Quando há centavos no valor, esses são separados por ponto.\
Então ficaria assim no download do retorno:\
R$ 274,00 = “274"\
R$ 134,80 = “134.8"\
R$ 27,01 = “27.01"

**COMARCAS HOMOLOGADAS**

* Informar os parâmetros:
* “**codapres**” – Serão retornados todos os municípios que estão habilitados para o apresentante informado.
* “**cartorios**” – Informe “**x**" para consultar os dados dos cartórios que o apresentante está habilitado a enviar títulos.

**CONSULTA**

* Informar os parâmetros “nossoNumero" e “numeroTitulo".

**CONSULTA SLIP**

* Informar os parâmetros “**cod\_municipio**“, “**cod\_cartorio**“, “**protocolo**" e “**data\_protocolo**“.
* Informar a “**data\_protocolo**" no padrão brasileiro. Ex.: 02/05/2016.

**INSTRUMENTO**

Informar o parâmetro “**userDados**" com a seguinte estrutura:\


```xml
<instrumento>
    <municipios>
        <municipio>
            <codigoMunicipio>3100203</codigoMunicipio>
            <cartorios>
                <cartorio>
                    <codigoCartorio>01</codigoCartorio>
                    <titulos>
                        <titulo>
                            <protocolo>0000038317</protocolo>
                            <dataProtocolo>28/12/2018</dataProtocolo>
                         </titulo>
                         <titulo>
                            <protocolo>1020304050</protocolo>
                            <dataprotocolo>01/03/2018</dataprotocolo>
                         </titulo>
                     </titulos>
                 </cartorio>
             </cartorios>
         </municipio>
         <municipio>
             <codigomunicipio>3100209</codigomunicipio>
             <cartorios>
                 <cartorio>
                     <codigocartorio>02</codigocartorio>
                     <titulos>
                         <titulo>
                             <protocolo>5040302010</protocolo>
                             <dataprotocolo>28/12/2018</dataprotocolo>
                         </titulo>
                         <titulo>
                             <protocolo>1738544625</protocolo>
                             <dataprotocolo>28/12/2018</dataprotocolo>
                         </titulo>
                     </titulos>
                 </cartorio>
             </cartorios>
         </municipio>
     </municipios>
</instrumento>
```

Dessa forma, o apresentante poderá fazer a consulta de mais de um instrumento por município e cartório.

<mark style="color:green;">**``**</mark>[<mark style="color:green;">**`DOWNLOAD DO ARQUIVO EXEMPLO`**</mark>](https://github.com/p21sistemas/manual-cra-21/blob/main/CONFIRMACAO\_RETORNO\_COMARCAS\_CONSULTA\_SLIP\_XML.zip?raw=true)<mark style="color:green;">**``**</mark>
