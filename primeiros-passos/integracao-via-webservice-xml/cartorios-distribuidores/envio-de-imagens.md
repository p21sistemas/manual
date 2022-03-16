# Envio de imagens



**Retorno**

* As imagens podem ser assinadas **opcionalmente**.
* Compactar os arquivos de imagens para a extensão _**\*.zip**_
* Converter o arquivo compactado para **base64**
* Inserir o código gerado no atributo _**t51**_ da tag **>** do XML.
* O restante do conteúdo do arquivo deve estar de acordo com o Layout pré-estabelecido.&#x20;

**Envio de instrumento eletrônico**

* As imagens podem ser assinadas **opcionalmente**.
* Nome do arquivo **INNNDDMM.AAS**
* Compactar os arquivos de imagens para a extensão _**\*.zip**_
* Converter o arquivo compactado para **base64**
* Inserir o código gerado no conteúdo da tag do XML.
* O restante do conteúdo do arquivo deve estar de acordo com o Layout pré-estabelecido. Exemplo

```xml
<?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?>
<retorno>
<imagem>
<protocolo>0003550308</protocolo>
<data_protocolo>18/10/2017</data_protocolo>
<base64>UEsDBBQAAAAIAL1gNT6UEsDBBQAAAAIAL1gNT6AAAIAL1gNT6UEsDBBQAAAAIAL1gNT="</base64>
</imagem>
</retorno>
```
