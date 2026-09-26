# Trabalho-Protocolo-HTTP


Invoke-WebRequest -Uri 'https://teste.alievi.com.br/auth' -Method POST -ContentType "application/json" -Body '{"user": "aluno", "password": "123"}'




StatusCode        : 200
StatusDescription : OK
Content           : {"access\_token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJhbHVubyIsImlhdCI6MTc5MDM3NjgxNywiZ
&nbsp;                   XhwIjoxNzkwMzc3NzE3fQ.UqEnPqgBCFPmLlsODRRGA4yPTVXpbB6HKaUMiZ1ccUQ","token\_type":"Bearer","expires\_i
&nbsp;                   n"...
RawContent        : HTTP/1.1 200 OK
&nbsp;                   Connection: keep-alive
&nbsp;                   cf-cache-status: DYNAMIC
&nbsp;                   Nel: {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}
&nbsp;                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=8,cfOrigi...
Forms             : {}                                                                                                  Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Nel,                                                            {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}], \[Server-Timing,                                        cfCacheStatus;desc="DYNAMIC",cfEdge;dur=8,cfOrigin;dur=1962]...}                                    Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 205



-------------------------------------------------------------------------------



$token = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJhbHVubyIsImlhdCI6MTc5MDM3Nzg5NiwiZXhwIjoxNzkwMzc4Nzk2fQ.hLvXIeZnnoxkyj5MiiLGltaH\_QGnzxMNd18PmxUkS0o"

>> $headers = @{Authorization = "Bearer $token"}

>> $url = "https://teste.alievi.com.br/times"



-------------------------------------------------------------------------------



Invoke-WebRequest -Uri $url -Method GET -Headers $headers





StatusCode        : 200
StatusDescription : OK
Content           : \[]
RawContent        : HTTP/1.1 200 OK
&nbsp;                   Connection: keep-alive
&nbsp;                   link: </times?limit=100\&offset=0>; rel="first", </times?limit=100\&offset=0>; rel="last"
&nbsp;                   x-total-count: 0
&nbsp;                   cf-cache-status: DYNAMIC
&nbsp;                   Nel: {"report\_to":"cf-nel"...
Forms             : {}
Headers           : {\[Connection, keep-alive], \[link, </times?limit=100\&offset=0>; rel="first",
&nbsp;                   </times?limit=100\&offset=0>; rel="last"], \[x-total-count, 0], \[cf-cache-status, DYNAMIC]...}
Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 2



-------------------------------------------------------------------------------



$body1 = @{	
nome = "Internacional"
data\_criacao = "1909-04-04"
pais = "Brasil"
} | ConvertTo-Json

curl $url -Method POST -Headers $headers -ContentType "application/json" -Body $body1





StatusCode        : 201
StatusDescription : Created
Content           : {"id":"a14decfc-1f0b-400d-9751-73282a928db5","data\_criacao":"1909-04-04","nome":"Internacional","pa
&nbsp;                   is":"Brasil","\_links":{"self":{"href":"/times/a14decfc-1f0b-400d-9751-73282a928db5"},"collection":{
&nbsp;                   "h...
RawContent        : HTTP/1.1 201 Created
&nbsp;                   Connection: keep-alive
&nbsp;                   cf-cache-status: DYNAMIC
&nbsp;                   Nel: {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}
&nbsp;                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=9,cf...
Forms             : {}
Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Nel,
&nbsp;                   {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}], \[Server-Timing,                                        cfCacheStatus;desc="DYNAMIC",cfEdge;dur=9,cfOrigin;dur=664]...}                                     Images            : {}                                                                                                  InputFields       : {}                                                                                                  Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 216


-------------------------------------------------------------------------------


$body1 = @{
nome = "Gremio"
data\_criacao = "1903-03-15"
pais = "Brasil"
} | ConvertTo-Json

curl $url -Method POST -Headers $headers -ContentType "application/json" -Body $body1




StatusCode        : 201
StatusDescription : Created
Content           : {"id":"3e9925df-986d-45ff-bdeb-93eaabe8f671","data\_criacao":"1903-03-15","nome":"Gremio","pais":"Br
asil","\_links":{"self":{"href":"/times/3e9925df-986d-45ff-bdeb-93eaabe8f671"},"collection":{"href":;                  "/...
RawContent        : HTTP/1.1 201 Created;                   Connection: keep-alive
&nbsp;                   cf-cache-status: DYNAMIC
&nbsp;                   Nel: {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}
&nbsp;                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=9,cf...
Forms             : {}
Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Nel,
&nbsp;                   {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}], \[Server-Timing,
&nbsp;                   cfCacheStatus;desc="DYNAMIC",cfEdge;dur=9,cfOrigin;dur=365]...}
Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 209


-------------------------------------------------------------------------------


curl -Uri "$url/a14decfc-1f0b-400d-9751-73282a928db5" -Method GET -Headers $headers



StatusCode        : 200
StatusDescription : OK
Content           : {"id":"a14decfc-1f0b-400d-9751-73282a928db5","data\_criacao":"1909-04-04","nome":"Internacional","pa
&nbsp;                   is":"Brasil","\_links":{"self":{"href":"/times/a14decfc-1f0b-400d-9751-73282a928db5"},"collection":{
&nbsp;                   "h...
RawContent        : HTTP/1.1 200 OK
&nbsp;                   Connection: keep-alive
&nbsp;                   cf-cache-status: DYNAMIC
&nbsp;                   Nel: {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}
&nbsp;                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=7,cfOrigi...
Forms             : {}
Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Nel,
&nbsp;                   {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}], \[Server-Timing,
&nbsp;                   cfCacheStatus;desc="DYNAMIC",cfEdge;dur=7,cfOrigin;dur=11]...}
Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 216


-------------------------------------------------------------------------------




$bodyPut = @{
nome = "Barcelona"
data\_criacao = "1899-11-29"
pais = "Espanha"
} | ConvertTo-Json

curl "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method PUT -Headers $headers -ContentType "application/json" -Body $bodyPut



StatusCode        : 200
StatusDescription : OK
Content           : {"id":"3e9925df-986d-45ff-bdeb-93eaabe8f671","data\_criacao":"1899-11-29","nome":"Barcelona","pais":
&nbsp;                   "Espanha","\_links":{"self":{"href":"/times/3e9925df-986d-45ff-bdeb-93eaabe8f671"},"collection":{"hr
&nbsp;                   ef...
RawContent        : HTTP/1.1 200 OK
&nbsp;                   Connection: keep-alive
&nbsp;                   cf-cache-status: DYNAMIC
&nbsp;                   Nel: {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}
&nbsp;                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=45,cfOrig...
Forms             : {}
Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Nel,
&nbsp;                   {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}], \[Server-Timing,
&nbsp;                   cfCacheStatus;desc="DYNAMIC",cfEdge;dur=45,cfOrigin;dur=6]...}                                      Images            : {}                                                                                                  InputFields       : {}                                                                                                  Links             : {}                                                                                                  ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 213


-------------------------------------------------------------------------------


$bodyPatch = @{
nome = "Barcelona"
data\_criacao = "1899-11-29"
pais = "Cataluña"
} | ConvertTo-Json

curl "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method PATCH -Headers $headers -ContentType "application/json" -Body $bodyPatch





StatusCode        : 200
StatusDescription : OK
Content           : {"id":"3e9925df-986d-45ff-bdeb-93eaabe8f671","data\_criacao":"1899-11-29","nome":"Barcelona","pais":
&nbsp;                   "Catalu a","\_links":{"self":{"href":"/times/3e9925df-986d-45ff-bdeb-93eaabe8f671"},"collection":{"h
&nbsp;                   re...
RawContent        : HTTP/1.1 200 OK
&nbsp;                   Connection: keep-alive                                                                                                  cf-cache-status: DYNAMIC                                                                                                Nel: {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}                                                     Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=12,cfOrig...                                 Forms             : {}
Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Nel,
&nbsp;                   {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}], \[Server-Timing,
&nbsp;                   cfCacheStatus;desc="DYNAMIC",cfEdge;dur=12,cfOrigin;dur=367]...}
Images            : {}
InputFields       : {}
Links             : {}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 216


-------------------------------------------------------------------------------


curl -Uri "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method Delete -Headers $headers



StatusCode        : 204
StatusDescription : No Content
Content           : {}
RawContent        : HTTP/1.1 204 No Content
                   Connection: keep-alive
                   cf-cache-status: DYNAMIC
                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=8,cfOrigin;dur=365

                   Report-To: {"group":"cf-nel","max\_age":604800,"end...
Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Server-Timing,

                   cfCacheStatus;desc="DYNAMIC",cfEdge;dur=8,cfOrigin;dur=365], \[Report-To, {"group":"cf-nel","max\_age

                   ":604800,"endpoints":\[{"url":"https://a.nel.cloudflare.com/report/v4?s=%2Fq6kZfJsKv%2BxU1ISu4Oe5qm%

&nbsp;                   2BvONyjSVXsW27UHdZBUAXOOFZ3kj8%2BiugdIRfjEGuDtSyopddfsYAGtG%2FyDczu0SOzTZ2TfjOF936VzlaZQ4eAaiAcSw5E
                   AUIHDJfVsVO5oh3r94y"}]}]...}
RawContentLength  : 0


-------------------------------------------------------------------------------


curl -Uri "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method GET -Headers $headers





curl : {"type":"about:blank","title":"Recurso não encontrado","status":404,"detail":"Nenhum item com esse id nessa
coleção."}
No linha:1 caractere:1
\+ curl -Uri "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method GET -He ...
\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) \[Invoke-WebRequest], WebExc
  eption
   + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand



-------------------------------------------------------------------------------


Invoke-WebRequest -Uri $url -Method GET -Headers $headers



StatusCode        : 200
StatusDescription : OK
Content           : \[{"id":"a14decfc-1f0b-400d-9751-73282a928db5","data\_criacao":"1909-04-04","nome":"Internacional","pais":"Brasil","\_links":{"self":{"href":"/times/a14decfc-1f0b-400d-9751-73282a928db5"},"collection":
                   {"...
RawContent        : HTTP/1.1 200 OK
                   Connection: keep-alive
                   link: </times?limit=100\&offset=0>; rel="first", </times?limit=100\&offset=0>; rel="last"
x-total-count: 1
cf-cache-status: DYNAMICNel: {"report\_to":"cf-nel"...

Forms             : {}

Headers           : {\[Connection, keep-alive], \[link, </times?limit=100\&offset=0>; rel="first",

&nbsp;                   </times?limit=100\&offset=0>; rel="last"], \[x-total-count, 1], \[cf-cache-status, DYNAMIC]...}

Images            : {}

InputFields       : {}

Links             : {}

ParsedHtml        : mshtml.HTMLDocumentClass

RawContentLength  : 218



-------------------------------------------------------------------------------





Invoke-WebRequest -Uri $url -Method GET





Invoke-WebRequest : {"type":"about:blank","title":"Não autenticado","status":401,"detail":"Faça POST /auth e envie o

token em Authorization: Bearer ."}

No linha:1 caractere:1

\+ Invoke-WebRequest -Uri $url -Method GET

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

&nbsp;   + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) \[Invoke-WebRequest], WebExc

&nbsp;  eption

&nbsp;   + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand



-------------------------------------------------------------------------------



$headersInvalido = @{Authorization = "Baerer token\_falso"}

Invoke-WebRequest -Uri $url -Method GET -Headers $headersInvalido





Invoke-WebRequest : {"type":"about:blank","title":"Não autenticado","status":401,"detail":"Faça POST /auth e envie o

token em Authorization: Bearer ."}

No linha:1 caractere:1

\+ Invoke-WebRequest -Uri $url -Method GET -Headers $headersInvalido

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

&nbsp;   + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) \[Invoke-WebRequest], WebExc

&nbsp;  eption

&nbsp;   + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand



-------------------------------------------------------------------------------



$bodyPut = @{

>> nome = "Barcelona"

>> data\_criacao = "1899-11-29"

>> pais = "Cataluña"

>> } | ConvertTo-Json

>>

>> curl "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method PUT -Headers $headers -ContentType "application/json" -Body $bodyPut





curl : {"type":"about:blank","title":"Recurso não encontrado","status":404,"detail":"Nenhum item com esse id nessa

coleção."}

No linha:7 caractere:1

\+ curl "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method PUT -Headers ...

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

&nbsp;   + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) \[Invoke-WebRequest], WebExc

&nbsp;  eption

&nbsp;   + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand



-------------------------------------------------------------------------------



curl -Uri "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method Delete -Headers $headers





curl : {"type":"about:blank","title":"Recurso não encontrado","status":404,"detail":"Nenhum item com esse id nessa

coleção."}

No linha:1 caractere:1

\+ curl -Uri "$url/3e9925df-986d-45ff-bdeb-93eaabe8f671" -Method Delete  ...

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

&nbsp;   + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) \[Invoke-WebRequest], WebExc

&nbsp;  eption

&nbsp;   + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeWebRequestCommand



-------------------------------------------------------------------------------



$bodyPut = @{

>> nome = "Internacional"

>> data\_criacao = "1909-04-04"

>> pais = "Brasil"

>> } | ConvertTo-Json

>>

>> curl "$url/a14decfc-1f0b-400d-9751-73282a928db5" -Method PUT -Headers $headers -ContentType "application/json" -Body $bodyPut





StatusCode        : 200

StatusDescription : OK

Content           : {"id":"a14decfc-1f0b-400d-9751-73282a928db5","data\_criacao":"1909-04-04","nome":"Internacional","pa

&nbsp;                   is":"Brasil","\_links":{"self":{"href":"/times/a14decfc-1f0b-400d-9751-73282a928db5"},"collection":{

&nbsp;                   "h...

RawContent        : HTTP/1.1 200 OK

&nbsp;                   Connection: keep-alive

&nbsp;                   cf-cache-status: DYNAMIC

&nbsp;                   Nel: {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}

&nbsp;                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=8,cfOrigi...

Forms             : {}

Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Nel,

&nbsp;                   {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}], \[Server-Timing,

&nbsp;                   cfCacheStatus;desc="DYNAMIC",cfEdge;dur=8,cfOrigin;dur=139]...}

Images            : {}

InputFields       : {}

Links             : {}

ParsedHtml        : mshtml.HTMLDocumentClass

RawContentLength  : 216



-------------------------------------------------------------------------------



curl -Uri "$url/a14decfc-1f0b-400d-9751-73282a928db5" -Method Delete -Headers $headers





StatusCode        : 204

StatusDescription : No Content

Content           : {}

RawContent        : HTTP/1.1 204 No Content

&nbsp;                   Connection: keep-alive

&nbsp;                   cf-cache-status: DYNAMIC

&nbsp;                   Server-Timing: cfCacheStatus;desc="DYNAMIC",cfEdge;dur=6,cfOrigin;dur=626

&nbsp;                   Report-To: {"group":"cf-nel","max\_age":604800,"end...

Headers           : {\[Connection, keep-alive], \[cf-cache-status, DYNAMIC], \[Server-Timing,

&nbsp;                   cfCacheStatus;desc="DYNAMIC",cfEdge;dur=6,cfOrigin;dur=626], \[Report-To, {"group":"cf-nel","max\_age

&nbsp;                   ":604800,"endpoints":\[{"url":"https://a.nel.cloudflare.com/report/v4?s=ivChTBY%2FM4xkZkYh2E8d%2FDzZ

&nbsp;                   LFQnNKVjHpdftpaUH6CIUD9whF65JblqWlSwuAy4wUzU7LO8cSUQlDob68eXELIeRR5wPfPZlw%2F6ptZgZ6kA98YoCM%2BXa1Z

&nbsp;                   SuKoiHfGvLtGGToRI"}]}]...}

RawContentLength  : 0



-------------------------------------------------------------------------------





**"Oque a API devolveu a criar um item?"**

-- A API devolveu um 201 created, junto com o corpo do objeto, que tinha todos os campos enviados.



**"Oque aconteceu ao buscar o item 2 depois de exclui-lo?"**



--  Retornou um 404 not found, indicando que já não existia mais.



**"Qual é a diferença entre o PUT e o PATCH?"**



-- o PUT é utilizado para mudar o recurso por inteiro, sendo necessário enviar todas as infos, já o PATCH permite mudanças parcias, alterando somente o campo especificado.



**"Para que serve o token?"**



-- É um crachá usado para autenticar e autorizar todas as ações realizadas através da API.

