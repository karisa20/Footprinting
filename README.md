# Footprinting
Repositório com o objetivo de compartilhar conhecimento.

# O que é Footprinting?

Mais comumente conhecido, como coleta de informações, o Footprinting é a **primeira etapa que ocorre em um teste de pentetração (pentest).**

Consiste em obter **TODAS** as informações possíveis a respeito do alvo (*rede, mapeamento, servidores, funcionários, empresas parceiras ou terceirizadas, e-mails, redes sociais, telefones, informações no lixo, etc*). Essas informações podem auxiliar no processo e quanto mais informações maior a probabilidade de acesso.

A **engenharia social** contribui para o aumento das informações coletadas. Além de pelo Google, Yahoo e outros mecanismos de busca, conseguimos informações relevantes.

## 1 - Início:

**Obter o máximo de informações possíveis**

1.1 - Começar pesquisando no site alvo, lendo o site, vendo os domínios associados, e-mails de contato, nomes relacionados a administração e outras informações.

Com essas informações pode-se criar uma lista de palavras que servirá para ataques (como quebra de sistemas de login - HTTP, SMTP, WPA2, etc). Sites revelam muito sobre o sistema auditado.

1.2 - Buscar informações do site em repositórios como:

* https://archive.org/ - armazena o histórico de sites da internet (desde sua primeira versão)

* https://censys.io/

## 2 - Coletar informações sobre o domínio:

Com as informações básicas enumeradas, a próxima etapa para montar o plano de ataque é coletar informações sobre o domínio.

O domínio irá exibir dados públicos que podem ser de interesse do atacante (pentester). Com uma busca pelo domínio, obtemos informações como e-mail do responsável, servidores DNS (utilizados para enumeração de DNS e transferência de zona), país, etc.

O comando *'whois'* do linux pode ser usado para buscar e enumerar informações de um domínio em órgãos regulamentadores.

O *whois* pode ser usado para determinar qual é a faixa de endereços IPs um determinado IP faz parte. Em organizações que tem faixas de IP próprias essa técnica mostrará os IPs pertencentes à organização.

## Como funciona a estrutura de domínios na internet

Cada país tem seu órgão regulamentador. No Brasil, o responsável é o *registro.br*. Cada órgão é controlado por uma entidade superior, por exemplo o *registro.br* é controlado pela Lacnic (Entidade responsável pelo gerenciamento de domínios da América Latina). O órgão responsável pelo gerenciamento de todos os continentes é o IANA.

Cuidado ao auditar a faixa de IP fornecidos via terminal *whois IP*. Pode ocorrer de a faixa pertencer a um fornecedor do cliente e não ser próprio do cliente. Portanto, audite somente o que for solicitado no escopo do pentest contratado.

Após essa coleta, vamos precisar enumerar o DNS.

# O que é DNS?

O Domain Name System (Sistema de Nomes de Domínio), **traduz os nomes de domínios em endereços IPs** e o contrário também pode ocorrer.












Referências:

MORENO, Daniel. **Introdução ao Pentest**. Editora novatec, 2ª edição atualizada e ampliada. São Paulo, 2019.