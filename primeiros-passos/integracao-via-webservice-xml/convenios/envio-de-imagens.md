# Envio de Imagens

**Imagem do título no arquivo de remessa**

* As imagens podem ser assinadas **opcionalmente**.
* **Compactar** os arquivos de imagens para a extensão _**\*.zip.**_
* Converter o arquivo compactado para **base64.**
* Inserir o código gerado no atributo **t51** da tag **< tr / >** do XML.
* O restante do conteúdo do arquivo deve estar de acordo com o Layout pré-estabelecido. Exemplo:

```xml
<remessa>
	<hd .../>
	<tr ... t51="YBIFAEZ0BQAcA==".../>
	<tl .../>
</remessa>
```

**Imagem do título em arquivo de imagem**

* As imagens podem ser assinadas **opcionalmente**.
* **Compactar** os arquivos de imagens para a extensão _**\*.zip.**_
* Converter o arquivo compactado para **base64.**
* Inserir o código gerado na tag **< imagem >** do XML:
* O restante do conteúdo do arquivo deve corresponder com o Layout pré-estabelecido. Exemplo:

```xml
<?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?>
<remessas>
    <remessa>
        <sequencial>000249</sequencial>
        <municipio>3100203</municipio>
        <titulos>
            <titulo>
                <documento_devedor>10964681668</documento_devedor>
                <nosso_numero>1350100099999</nosso_numero>
                <numero_titulo>13501000999</numero_titulo>
                <saldo>5114.85</saldo>
                <imagem>UEsDBBQAAAAIALdVXVMk==</imagem>
            </titulo>
        </titulos>
    </remessa>
</remessas>
```



**Cancelamento/Desistência**

* As imagens podem ser assinadas **opcionalmente**.
* Compactar os arquivos de imagens para a extensão _**\*.zip.**_
* Converter o arquivo compactado para **base64.**
* Inserir o código gerado na tag **< imagem >** do XML:

```xml
<?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?>
<desistencia>
    <comarca>
        <cartorio>
            <titulo>
                <imagem>YBIFAEZ0BQAcA==</imagem>
            </titulo>
        </cartorio>
    </comarca>
</desistencia>
```

**Autorização**

* **IMPORTANTE:** Ao enviar imagens pelo serviço, a aplicação não gerará a carta de autorização, ou seja, o apresentante deverá gerar e enviar a carta de autorização.
* As imagens devem ser assinadas **se o parâmetro “exige autorização assinada” estiver cadastrado na CRA**.
* Converter o arquivo PDF ou assinado para **base64.**
* Inserir o código gerado na tag **< imagem >** do XML:

```xml
<!--?xml version="1.0" encoding="ISO-8859-1" standalone="no" ?-->
<autoriza_cancelamento>
    <comarca>
        <cartorio>
            <titulo>
               <imagem>YBIFAEZ0BQAcA==</imagem>
            </titulo>
        </cartorio>
    </comarca>
</autoriza_cancelamento>
```
