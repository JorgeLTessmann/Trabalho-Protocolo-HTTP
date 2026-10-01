# Nome: Jorge Luiz Tessmann
## Sites Escolhidos
- https://www.youtube.com/
- https://www.instagram.com/
- https://g1.com.br/
  
# Comandos Usados

### Codigo Usado:

```
nslookup -type=NS br.
```
### Resultado
```
Servidor:  ADACAD.acad.redes-ienh.com.br
Address:  192.168.0.4

Não é resposta autoritativa:
br      nameserver = a.dns.br
br      nameserver = c.dns.br
br      nameserver = e.dns.br
br      nameserver = d.dns.br
br      nameserver = b.dns.br
br      nameserver = f.dns.br

a.dns.br        internet address = 200.219.148.10
```

## Youtube

### 1. Codigo Usado:

```
nslookup -type=NS youtube.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
youtube.com     nameserver = ns3.google.com
youtube.com     nameserver = ns2.google.com
youtube.com     nameserver = ns4.google.com
youtube.com     nameserver = ns1.google.com
```

### 2. Codigo Usado:

```
nslookup -type=A youtube.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
Nome:    youtube.com
Address:  172.217.30.46
```

### 3. Codigo Usado:

```
nslookup -type=AAAA youtube.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
Nome:    youtube.com
Address:  2800:3f0:4001:837::200e
```

### 4. Codigo Usado:

```
nslookup -type=MX youtube.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
Nome:    youtube.com
Address:  2800:3f0:4001:837::200e

PS C:\WINDOWS\System32> nslookup -type=MX youtube.com
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
youtube.com     MX preference = 0, mail exchanger = smtp.google.com
```

## Instagram

### 1. Codigo Usado:

```
nslookup -type=NS instagram.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
instagram.com   nameserver = d.ns.instagram.com
instagram.com   nameserver = b.ns.instagram.com
instagram.com   nameserver = a.ns.instagram.com
instagram.com   nameserver = c.ns.instagram.com
```

### 2. Codigo Usado:

```
nslookup -type=A instagram.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
Nome:    instagram.com
Address:  157.240.226.174
```

### 3. Codigo Usado:

```
nslookup -type=AAAA instagram.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
Nome:    instagram.com
Address:  2a03:2880:f359:22:face:b00c:0:4420

```

### 4. Codigo Usado:

```
nslookup -type=MX instagram.com
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
instagram.com   MX preference = 20, mail exchanger = mx0a-00082601.pphosted.com
instagram.com   MX preference = 10, mail exchanger = mxa-00082601.gslb.pphosted.com
instagram.com   MX preference = 10, mail exchanger = mxb-00082601.gslb.pphosted.com
instagram.com   MX preference = 20, mail exchanger = mx0b-00082601.pphosted.com
```

## G1

### 1. Codigo Usado:

```
nslookup -type=NS g1.com.br
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
g1.com.br       nameserver = ns03.oghost.com.br
g1.com.br       nameserver = ns02.oghost.com.br
g1.com.br       nameserver = ns01.oghost.com.br
g1.com.br       nameserver = ns04.oghost.com.br
```

### 2. Codigo Usado:

```
nslookup -type=A g1.com.br
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
g1.com.br       nameserver = ns03.oghost.com.br
g1.com.br       nameserver = ns02.oghost.com.br
g1.com.br       nameserver = ns01.oghost.com.br
g1.com.br       nameserver = ns04.oghost.com.br
PS C:\WINDOWS\System32> nslookup -type=A g1.com.br
Servidor:  one.one.one.one
Address:  1.1.1.1

Não é resposta autoritativa:
Nome:    g1.com.br
Address:  186.192.83.12
```

### 3. Codigo Usado:

```
nslookup -type=AAAA g1.com.br
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

Nome:    g1.com.br

```

### 4. Codigo Usado:

```
nslookup -type=MX g1.com.br
```
### Resultado
```
Servidor:  one.one.one.one
Address:  1.1.1.1

g1.com.br
        primary name server = ns01.oghost.com.br
        responsible mail addr = fapesp.corp.globo.com
        serial  = 2026091600
        refresh = 10800 (3 hours)
        retry   = 3600 (1 hour)
        expire  = 604800 (7 days)
        default TTL = 86400 (1 day)
```

# Ficha de Cada Site

## Youtube

 <font size="7">Item</font> | <font size="5">O que Descobri</font> |
| :--- | :--- |
| Endereço | O site é o youtube.com, usa o protocolo https://, não tem subdomínio e o TLD é .com. |
| TLD | O .com é administrado pela empresa Verisign, que gerencia os servidores raiz desse final de endereço. |
| Dono | O dono é a Google LLC, mas os dados pessoais de contato ficam ocultos por privacidade. |
| Autoritativos | Quem responde oficialmente pelo DNS do site são os servidores da própria Google (ns1.google.com até ns4.google.com). |
| Destinos | O endereço aponta para o IP IPv4 172.217.30.46 e para o IPv6 2800:3f0:4001:837::200e. |
| E-mail | Os e-mails do YouTube passam pelos servidores do próprio ecossistema do Google, com smtp.google.com. |
| Não descoberto | Os dados de contato pessoal de quem registrou o domínio não aparecem porque estão ocultos por privacidade. |

## Instagram

 <font size="7">Item</font> | <font size="5">O que Descobri</font> |
| :--- | :--- |
| Endereço | O site é o instagram.com, usa https://, sem subdomínio, com TLD .com. |
| TLD | Também administrado pela Verisign. |
| Dono | O dono é a empresa Meta Platforms, Inc. |
| Autoritativos | Quem responde pelo DNS são os servidores da própria Meta (a.ns.instagram.com até d.ns.instagram.com). |
| Destinos | O IP IPv4 é 157.240.226.174 e o IPv6 é 2a03:2880:f359:22:face:b00c:0:4420. |
| E-mail | O e-mail usa um serviço terceirizado de segurança e hospedagem de mensagens, o pphosted.com. |
| Não descoberto | Informações de contato direto da pessoa responsável pelo registro estão ocultas. |

## G1

 <font size="7">Item</font> | <font size="5">O que Descobri</font> |
| :--- | :--- |
| Endereço | O site é o g1.com.br, com https://, domínio g1 e TLD .br. |
| TLD | O .br é administrado pelo NIC.br/Registro.br aqui no Brasil. |
| Dono | O titular é o Grupo Globo, como Infoglobo. |
| Autoritativos | Os servidores de DNS são operados pela própria infraestrutura da Globo (ns01.oghost.com.br a ns04.oghost.com.br). |
| Destinos | O IP IPv4 retornado foi 186.192.83.12 (sem IPv6 direto mapeado no teste). |
| E-mail | Os e-mails ficam na rede corporativa da empresa, fapesp.corp.globo.com. |
| Não descoberto | Alguns detalhes internos de caixas postais específicas não aparecem publicamente por motivos de segurança. |

# Perguntas

## 1. **"Em algum dos sites, o dono do domínio e quem opera o DNS são organizações diferentes? Qual?"**

Não. Nos três sites, youtube.com, instagram.com e g1.com.br, o DNS é operado pelas próprias empresas donas dos domínios (Google, Meta e Globo).

## 2. **"Onde ficam os servidores de e-mail de cada site: no próprio domínio ou em outro?"**

O YouTube usa a estrutura do Google e o G1 usa a da Globo, enquanto o Instagram usa um serviço de e-mail terceirizado especializado em segurança, o pphosted.com.

## 3. **"O que foi mais difícil de descobrir, e por quê?"**

O mais difícil foi achar alguns registros de e-mail específicos e dados de dono, porque as grandes empresas escondem essas informações por privacidade e segurança.

