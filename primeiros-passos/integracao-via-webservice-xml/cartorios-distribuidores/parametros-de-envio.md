# Parâmetros de envio



* **Os dados (parâmetros) devem ser enviados via protocolo SOAP**

Todos os arquivos enviados ou recebidos nos serviços devem estar em conformidade com o padrão FEBRABAN XML.

* **Ao consumir o WebService, em todos os serviços, a autenticação deverá ser realizada utilizando autenticação básica.**
  * Deverão ser passados os parâmetros de _usuário_ e _senha_, fornecidos pela CRA.
  * Após a autenticação serão validados os parâmetros de entrada e por último a crítica do arquivo
* **Serviços disponíveis:**

| **Remessa**             | Download do arquivo de remessa.                                  |
| ----------------------- | ---------------------------------------------------------------- |
| **RemessaPendente**     | Download de arquivo de remessa ainda não baixado.                |
| **Confirmacao**         | Upload do arquivo de confirmação.                                |
| **Retorno**             | Upload do arquivo de retorno.                                    |
| **Desistencia**         | Download do arquivo de desistência.                              |
| **Cancelamento**        | Download do arquivo de cancelamento.                             |
| **Autorizacao**         | Download do arquivo de autorização (desistência e cancelamento). |
| **BuscarApresentante**  | Download de apresentantes ativos no município.                   |
| **SalvarSituacao**      | Salva os dados da situação do título na CRA.                     |
| **BuscarSituacao**      | Busca a situação do título na CRA.                               |
| **Imagem**              | Upload das imagens dos instrumentos de protesto.                 |
| **ConsultaSlip**        | Serviço para consulta do código/nome da agência do cedente.      |
| **ConsultaAutorizacao** | Consulta uma autorização específica de um título.                |
| **ConsultaImagem**      | Consulta os arquivos de imagem de um título.                     |



**Parâmetros dos serviços disponíveis:**\
&#x20;     \
&#x20;        Upload

| **user\_arq**   | Nome do arquivo no formato **FEBRABAN.** |
| --------------- | ---------------------------------------- |
| **user\_dados** | Conteúdo do arquivo XML.                 |

&#x20;       Download

| **user\_arq**      | Nome do arquivo no formato **FEBRABAN.**                                                                                |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **downloadImagem** | Parâmetro opcional utilizado somente no serviço de “Remessa". Indica se a remessa retornará com as imagens dos títulos. |

&#x20;        SalvarSituacao / BuscarSituacao

| **protocoloCartorio** | Informar o código do cartório.       |
| --------------------- | ------------------------------------ |
| **dataOcorrencia**    | Informar a data de ocorrência.       |
| **ocorrência**        | Informar a ocorrência.               |
| **codigoPraca**       | Informar o código IBGE do município. |
| **codigoCartorio**    | Informar o código do cartório.       |

ConsultaSlip

| **protocolo**     | Número do protocolo informado na confirmação. |
| ----------------- | --------------------------------------------- |
| **dataProtocolo** | Data do protocolo informado na confirmação.   |

ConsultaAutorizacao

| **userArq**       | Nome do arquivo no formato FEBRABAN (AD ou AC).                  |
| ----------------- | ---------------------------------------------------------------- |
| **protocolo**     | Número do protocolo informado na confirmação.                    |
| **dataProtocolo** | Data do protocolo informado na confirmação.                      |
| **marcarBaixado** | Parâmetro que define se a autorização será marcada como baixada. |

ConsultaImagem

| **nossoNumero**      | Informar o Nosso Número.                              |
| -------------------- | ----------------------------------------------------- |
| **numeroTitulo**     | Informar o número de identificação do título.         |
| **documentoDevedor** | Informar o número do documento do devedor (CPF/CNPJ). |
| **saldoTitulo**      | Informar o saldo do título. (Opcional)                |
| **vencimento**       | Informar a data de vencimento do título. (Opcional)   |
| **remessa**          | Informar o número sequencial da remessa. (Opcional)   |

* **O encoding do XML deve estar de acordo com ISO-8859-1.**
* **O conteúdo dos arquivos enviados para CRA devem seguir o padrão de codificação ASCII**
* **Assim como no HTML, o XML possui entidades, que devem ser substituídas conforme tabela abaixo:**

| **De** | **Para** |
| ------ | -------- |
| <      | & lt;    |
| >      | & gt;    |
| &      | & amp;   |
| ‘      | & apos;  |
| “      | & quot;  |
