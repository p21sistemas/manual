# Download e Consulta

**REMESSA:**

* Informar o parâmetro “user\_arq” ( Nome do arquivo no no formato FEBRABAN)
* Informar o parâmetro “downloadImagem”, opcionalmente, para baixar as imagens dos títulos na remessa ou para consultar se os títulos possuem imagem.  Preencha o parâmetro com “1" caso seja necessário o download das imagens ou “2" para que o sistema informe se os títulos possuem imagens para serem baixadas. Caso contrário, ele não deve ser informado.
* Serão retornadas todas as remessas da data informada e as pendentes de download das datas anteriores.
* Será validado o inicio do nome do arquivo, B, e a data informada. O código do apresentante não é considerado para o download.
* Por exemplo, ao requisitar a REMESSA com o nome do arquivo B0002401.141, será retornada a REMESSA de 24/01/2014 tendo como base a data de envio da remessa pelo apresentante. Serão retornadas remessas de todos apresentantes na data informada e as pendentes das datas anteriores.

**REMESSA PENDENTE:**

* Informar o parâmetro “user\_arq” ( Nome do arquivo no no formato FEBRABAN)
* Informar o parâmetro “downloadImagem”, opcionalmente, para baixar as imagens dos títulos na remessa ou para consultar se os títulos possuem imagem. Preencha o parâmetro com “1" caso seja necessário o download das imagens ou “2" para que o sistema informe se os títulos possuem imagens para serem baixadas. Caso contrário, ele não deve ser informado.
* Serão retornadas todas as remessas  pendentes de download.
* Será validado o inicio do nome do arquivo, B, e a data informada. O código do apresentante não é considerado para o download.
  * Por exemplo, ao requisitar a REMESSA com o nome do arquivo B0002401.141, serão retornadas as REMESSAS pendentes de download independente do apresentante ou data.

**DESISTENCIA:**

* Informar o parâmetro “user\_arq” ( Nome do arquivo no no formato FEBRABAN)
* Serão retornadas todas as desistências  da data informada e as pendentes de download das datas anteriores.
* Será validado o inicio do nome do arquivo, DP, e a data informada. O código do apresentante não é considerado para o download.
* Por exemplo, ao requisitar a DESISTENCIA com o nome do arquivo DP0002401.141, será retornada a DESISTÊNCIA de 24/01/2014 tendo como base a data de envio da DESISTENCIA pelo apresentante. Serão retornadas desistências de todos apresentantes na data informada e os pendentes das datas anteriores.

**CANCELAMENTO:**

* Informar o parâmetro “user\_arq” ( Nome do arquivo no no formato FEBRABAN)
* Informar o parâmetro “downloadImagem”, opcionalmente, para baixar as imagens das solicitações de cancelamento. Preencha o parâmetro com 1 caso seja necessário o download das imagens, caso contrário, ele não deve ser informado.
* Serão retornados todos os cancelamentos da data informada e os pendentes de download das datas anteriores.
* Será validado o inicio do nome do arquivo, CP, e a data informada. O código do apresentante não é considerado para o download.
* Por exemplo, ao requisitar o CANCELAMENTO com o nome do arquivo CP0002401.141, será retornado o CANCELAMENTO de 24/01/2014 tendo como base a data de envio do cancelamento pelo apresentante. Serão retornados cancelamentos de todos apresentantes na data informada e os pendentes das datas anteriores.

**AUTORIZAÇÃO:**



* Ao requisitar o download do arquivo de autorização, serão retornadas todas as autorizações de desistência e cancelamento referente a data informada e as que estão pendentes de download de datas anteriores.
* A requisição pode ser feita usando AC ou AD na sigla do nome do arquivo
* Informar o parâmetro “downloadImagem”, opcionalmente, para baixar as imagens das autorizações. Preencha o parâmetro com “1" caso seja necessário o download das imagens, caso contrário, informe “0".
* O conteúdo da carta de anuência estará disponível no atributo t10 ()
* A imagem é compactada e convertida em base64. Se houver arquivo assinado, o ZIP conterá um arquivo PDF e outro P7S.
* A atributo “t07" indicará o tipo da autorização

&#x20;         t07="C" – CANCELAMENTO          t07="S" – DESISTENCIA **CONSULTA AUTORIZAÇÃO:**

* Informar o parâmetro “user\_arq” ( Nome do arquivo no no formato FEBRABAN), “numeroProtocolo","dataProtocolo" e “marcarBaixado".
* Quando informo “0” ou “false” no parâmetro marcarBaixado o serviço retorna os dados sem marcar a autorização como baixada.
* Quando informo qualquer outra string ou não informo nada no parâmetro, a consulta marca a autorização como baixada.
