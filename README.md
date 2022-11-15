# 📖 Bem Vindos(a)
* Olá, me chamo chamo Arthur e tenho 16 anos. Sou focado em fazer prejetos legais para o discord.
* No momento, estou praticado e reconhecimento de linguagens da programação, como: javascript.
* Estou Desenvolvendo a [Olia](https://discord.com/api/oauth2/authorize?client_id=1037029929390460979&permissions=8&scope=bot), ela é um bot focado em ajuda pessoas que não estão conseguindo crescer seu servidor.

  <div>
    <h6>Linguagens</h6>
    <img alt="JavaScript" src="https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E"/>

  </div>

### ⭐ ``Auth``
* Uma demonstração do comando Auth ( colocar pessoas no seu servidor )

```
  if (cmd === "users") {
    if (db.get(`wl_${ctx.author.id}`) !== true && !kalash.owners.includes(ctx.author.id)) return;
    fs.readFile('./object.json', async function(err, data) {
      let msg = await ctx.channel.send({
        content: `${emoji.user} **Localizei os users** (\`0\`/${JSON.parse(data).length > 1 ? `\`${JSON.parse(data).length}\`` : `\`${JSON.parse(data).length}\``})`
```
