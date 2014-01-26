Bom primeiramente você sabe o que são [Altcoins](http://altcoins.com/)?

Altcoins são cryptomoedas alternativas ao [Bitcoin](http://bitcoin.org/) que funcionam de forma semelhante, descentralizada, criptográfica, ponto-a-ponto, etc. O que muda normalmente é o algoritmo de criptografia que em vez do [SHA-256](http://en.wikipedia.org/wiki/SHA-2) é usado [scrypt](http://en.wikipedia.org/wiki/Scrypt) ou algum outra criptografia híbrida. Bom nesse post ainda não comentarei entre as diferenças entre essas 2 criptografias, o foco é como comprar e vender em um só lugar e para isso eu uso 2 sistemas: [Cryptsy]((https://www.cryptsy.com/users/register?refid=49274) e [CoinedUp](https://coinedup.com/).

#[Cryptsy]((https://www.cryptsy.com/users/register?refid=49274)

O sistema é bem interessante pois pelo que percebi é uma [Single Page Application](http://en.wikipedia.org/wiki/Single-page_application) usando fortemente jquery e acredito que Node.js também pois ele usa Socket.io:
  
  <script src="/js/socket.io/socket.io.min.js"></script>

[view-source:https://www.cryptsy.com/users/balances](view-source:https://www.cryptsy.com/users/balances)

Antes precisamos entender o conceito de Market(mercado) onde cada moeda tem seu mercado específico podendo ser referente ao Bitcoin ou ao Litecoin.

Já dentro do sistema, no menu superior possuímos 5 itens:

- Dashboard
- Trade
- Balances
- Open Orders
- Trade History

![Menu superior](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_5_53_58_PM.png)

###Dashboard
Sessão onde vc tem suas principais informações como: 

- Your Top Account Balances
- Trade Key
- Your Stats
- Your Referrals

###Trade
Em Trade é a sessão que mostra todas as altcoins suportadas e qual seu valor referente ao Bitcoin/BTC e Litecoin/LTC, a tabela é separada em:

- Market: lista as moedas ativas
- Currency: nome da moeda
- Volume: 
- Last Trade: último valor vendido
- 24hr High: maior valor vendido em 24 horas
- 24hr Low: menor valor vendido em 24 horas

![Dados listados](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_01_44_PM.png)

###Balances
Aqui é listada todas as moedas ativas e em quais e quanto você possui em cada. Os dados listados são:

- Currency Name: nome da moeda
- Code: código utilizado, ex.: BTC
- Available Balance: saldo disponível
- Pending Deposit: Depósito pendente
- Held for Orders: Ordens realizadas
- Actions: Acões


![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_29_32_PM.png)

###Open Orders
Nessa área nos mostra a listagem das suas ordens de compra e venda abertas. Mostrando os seguintes dados:

- Date/Action/Market: data, se comprou ou vendeu e em qual mercado.
- Price: preço por cada moeda
- Quantity: quantidade total
- Total: valor total
- Action: link para cancelar

![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_28_41_PM.png)

###Trade History
Mostra suas últimas 200 transações, listando elas com os seguintes dados:

- Date/Action/Market: data, se comprou ou vendeu e em qual mercado.
- Price: preço por cada moeda
- Quantity: quantidade total
- Fee: valor total pago ao Cryptsy como taxa
- Net Total: Total comprado/vendido + Fee

![Dados listados no Trade History](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_27_46_PM.png)

##Como comprar/vender?
Para iniciarmos nosso investimentos em altcoins precisamos enviar ou Litecoins ou Bitcoins para a carteira gerada pelo Cryptsy, para lá no sistema poder ter saldo e começar o jogo.

Para fazer isso EU fiz o seguinte:

  Depositei em dinheiro no [MercadoBitcoin](http://www.mercadobitcoin.com.br/) e no [Bitcoin2you](https://www.bitcointoyou.com/) e de lá transferi meus Bitcoins para o Cryptsy.

Depois que suas moedas tenham entrado no sistema você pode vai clickar no botão na coluna de Actions, na linha da moeda que você quer comprar, no nosso caso será na linha dos Bitcoins, clickando no botão BTC Actions irá abrir um menu de contexto como esse:

![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_37_23_PM.png)

Para depositarmos click em **Deposit / Autosell BTC** nisso abrirá uma modal com o endereço da sua carteira de Bitcoins dentro do Cryptsy, é esse endereço que vc usará para transferir seus Bitcoins.

Depois de copiar seu endereço vá até o sistema onde você possui seus Bitcoins ou na sua carteira offline, nesse exemplo mostrarei como fazer no MercadoBitcoin. 

Faça o login no MercadoBitcoin e vá em Retirada.

![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_41_09_PM.png)

Depois de clickar em Retirar é só aguardar alguns minutos até a rede Bitcoin validar a transação.

Após sua espera volte no Cryptsy e veja em Balances se caiu suas moedas.

![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_43_43_PM.png)

*sim eu coloquei pouco lá ainda porque estava sem tempo, mas já comprei mais BTCs para enviar para lá*

Agora que você já possui saldo no Cryptsy pode inciar a compra de diversas moedas listadas. Para isso vá em Trade e click no Market desejado, nesse exemplo mostrarei utilizando o [DogeCoin](http://dogecoin.com/). Logo abaixo do gráfico existem 2 boxes dividios em: Buy e Sell.

![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_6_47_50_PM.png)


- Ammount Doge: quantidade de moedas, mínimo de 100 pois o valor é muito baixo.
- Price Per DOGE é o valor que você quer pagar/vender por Dogecoin 
- Total (BTC): custo total em BTCs
- 0.20% Fee (BTC): valor da taxa cobrada
- Net Total (BTC): valor total da ordem

###Comprando
Caso você queira saber o valor que o pessoal está pagando em cada moeda, coloca em Ammount o valor **1** para que automagicamente, via [Javascript](http://makeameme.org/media/created/javascript-everywhere.jpg), mas claro que se você esta comprando tem que tentar comprar por um valor menor.

ps: analise o gráfico antes para ver se ela não está subindo desenfreadamente, pois uma hora ela vai cair, o ideal é tentar comprar na baixa, mas você precisa conhecer bem a moeda para tentar prever se ela subirá logo.


###Vendendo
Para vender é o mesmo esquema de comprar, mas qual a ideia, como você pode criar ordens com o valor que quiser, você pode tentar colocar uma parte para venda bem mais caro que o valor atual, pois você não precisa se preocupar, quando ela atingir aquele valor você venderá.

Caso você não tenha acesso direto à internet ou não tenha tanto tempo para ficar comprando/vendendo direto essa é a melhor forma de fazer.

Caso você tenha bastante tempo, vários amigos meus fazem isso, você compra valor x e ja coloca para vender com uns 20% a 30% caso ela tenha uma boa movimentação como o Dogecoin não é difícil de vender no mesmo dia.

**Dica**
  Para especular escolha as moedas que mais flutuam, pois você terá mais chance de vender ganhando lucro no mesmo dia. 

Exemplo:
Comprei 10.000 a 129 cada
![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_7_17_19_PM.png)

E vendi no mesmo dia 220 cada
![](http://nomadev.com.br/content/images/2014/Jan/Screen_Shot_2014_01_26_at_7_17_29_PM.png)

#[CoinedUp](https://coinedup.com/)
Já ganha pontos pois seu login é via OAuth, mas eu me inscrevi nele hoje então ainda não posso falar muita coisa, mas o post será atualizado quando eu já estiver utilizando-o.

Grupo de Investimento em Altcoins no Facebook: https://www.facebook.com/groups/635650459823972/


##Experiências

> colocar aqui a sua experiencia com eus investimentos em altcoins
