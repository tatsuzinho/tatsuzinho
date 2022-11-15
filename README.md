# 📖 Bem Vindos(a)
* Olá, me chamo chamo Arthir e tenho 18 anos. Sou focado em fazer prejetos legais para o discord.
* No momento, estou praticado e reconhecimento de linguagens da programação, como: javascript.
* Estou Desenvolvendo a [Olia](https://discord.com/api/oauth2/authorize?client_id=1037029929390460979&permissions=8&scope=bot), ela é um bot focado em ajuda pessoas que não estão conseguindo crescer seu servidor.

  <div>
    <h6>Linguagens</h6>
    <img alt="JavaScript" src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E"/>

  </div>


### ⭐ ``Discord Boost``

* Não use cartão clonado, não irá funcionar!
* Veja abaixo a api que gera cartões virtuais.
* Cóigo abaixo é só api, o resto você tem que fazer - [Créditos](https://github.com/ppolar0)

```js
const json = require("./config.json")
const colors = require("colors")

function card(a,b,c) {

    const fetch = require('sync-fetch')
    const criar = fetch(`https://yours-api.yoursbank.com.br/api/card/createvirtualcard`, {
        method: "POST",
        headers: json
    }).json()

    if (criar && criar.message === "not defined") return a("Erro, a api caiu, vamos resolver em breve!")
    else {

        const desblock = criar.numeroCartao.split("")
        const iddocartão = criar.idCartao
      
        fetch(`https://yours-api.yoursbank.com.br/api/card/${iddocartão}/unblock`, {
            method: "POST",
            body: JSON.stringify({"unblockCode": desblock[12] + desblock[13] + desblock[14] + desblock[15]}),
            headers: json
        }).json()

        console.log("Sucesso, cartão virtual foi criado, já pode usar.".green)

        return criar
    }
    

}

module.exports = card;
```

