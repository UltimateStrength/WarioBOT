# The Old Project was Made with the Discord.js Library, on the Visual Studio Code Platform!!!

---------------------------------------------------------------------------------------------

# .gitignore

node_modules/
package-lock.json/

---------------------------------------------------------------------------------------------

# bot.js

const Discord = require("discord.js");
const client = new Discord.Client(); 
const config = require("./config.json"); 

client.on("ready", () => {
  console.log(``); 
  client.user.setPresence({ game: { name: 'comando', type: 1, url: 'https://www.twitch.tv/ultimatestrength99'} });
    //0 = Jogando
    //  1 = Transmitindo
    //  2 = Ouvindo
    //  3 = Assistindo
});

client.on("guildCreate", guild => {
  console.log(`ATUALIZAÇÃO
  O WarioBOT Acaba de Entrar no Servidor:${guild.name}
  
  Com o Id: ${guild.id}... 
  Com ${guild.memberCount} Membros!!!
  E Com (${guild.channels.cache.size}) Canais/Categorias...
  Assim Estando em ${client.guilds.cache.size} Servidores`);
});

client.on("guildDelete", guild => {
  console.log(`ATUALIZAÇÃO
  O WarioBOT Acaba de Ser Removido do Servidor: ${guild.name}

  Com o Id: (id: ${guild.id})... 
  Com ${guild.memberCount} Membros!!!
  E Com (${guild.channels.cache.size}) Canais/Categorias...
  Assim Estando em ${client.guilds.cache.size} Servidores`);
});

    client.on("message", async message => {

        if(message.author.bot) return;
        if(message.channel.type === "dm") return;
        if(!message.content.startsWith(config.prefix)) return;
    
      const args = message.content.slice(config.prefix.length).trim().split(/ +/g);
      const comando = args.shift().toLowerCase();
      
// comando ping
if(comando === "ping") {
  const m = await message.channel.send("**Ping???**");
m.edit(`**:ping_pong: Pong!**
**:satellite: Latência = ${m.createdTimestamp - message.createdTimestamp}ms.....**
**:zap: Latencia de API = ${Math.round(client.ping)}ms**`);

}

// comando support
if(comando === "support") {
  const m = await message.channel.send(`**:zap:Servidor Suporte do Bot!!!:zap:**
  :arrow_right: **https://top.gg/servers/697931751829274631**
 
**:zap:Site de Suporte do Bot!!!:zap:**
  :arrow_right: **https://migatte-no-ultizin.webnode.com/bot/** 
  
**:zap:Top.gg do Bot!!!:zap:** 
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}

// comando suporte
if(comando === "suporte") {
  const m = await message.channel.send(`**:zap:Servidor Suporte do Bot!!!:zap:**
  :arrow_right: **https://top.gg/servers/697931751829274631**
 
**:zap:Site de Suporte do Bot!!!:zap:**
  :arrow_right: **https://migatte-no-ultizin.webnode.com/bot/** 
  
**:zap:Top.gg do Bot!!!:zap:** 
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}


// comando vote
if(comando === "vote") {
  const m = await message.channel.send(`**:zap:Vote no WarioBOT no Top.gg:zap:**
  
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}

// comando votar
if(comando === "votar") {
  const m = await message.channel.send(`**:zap:Vote no WarioBOT no Top.gg:zap:**
  
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}

// comando invite
if(comando === "invite") {
  const m = await message.channel.send(`**:zap:Link de Invite do Bot!!!:zap:**
  
  :arrow_right: **https://discord.com/oauth2/authorize?client_id=709448420548673536&scope=bot&permissions=8**`);

}

// comando de prefixo
if(comando === "") {
  const m = await message.channel.send("**Parece que Alguém me Chamou... Para Saber meus Comandos, (Digite: w.help)**");

}

  // comando bem-vindo
  if(comando === "bem-vindo") {
    const m = await message.channel.send("Isso Mesmo Seja Bem Vindo https://cdn.discordapp.com/attachments/603568752206020608/713009381981159474/Bem_Vindo.gif");
  
  }

  // comando kira
  if(comando === "kira") {
    const m = await message.channel.send("Ei, Pare de Me Chamar, Vou Escrever seu Nome em Meu Death Note!!! https://cdn.discordapp.com/attachments/603568752206020608/713009392018259989/Kira.gif");
  
  }

// comando serverinfo
if(comando === "serverinfo") {
  const m = await message.channel.send(`:jigsaw:**__Info do Servidor ${message.guild.name}__**:jigsaw:
  :point_right:**Id: (${message.guild.id})...** 
  :point_right:**Numero de Membros (${message.guild.memberCount})...**
  :point_right:**Com (${message.guild.channels.cache.size}) Canais/Categorias...**`);

}

// comando botinfo
if(comando === "botinfo") {
  const m = await message.channel.send(`:jigsaw:**__Info do ${client.user.username}__**:jigsaw:

  :satellite:**Meu Prefixo é (w.)!!!**
  :house:**Estou em ${client.guilds.cache.size} Servidores!!!**
  :sunglasses:**Com ${client.users.cache.size} Usuarios**
  :file_cabinet:**Com ${client.channels.cache.size} Canais**
  :robot:**Meu Id é: ${client.user.id}**`);

}

// comando userinfo
if(comando === "userinfo") {
  const m = await message.channel.send(`**__Info do Usuario ${client.username}__**

  :globe_with_meridians:**Tag do Discord: ${client.tag}**
  :gear:**Id: ${client.id}**`)
  
}

  // comando l
  if(comando === "l") {
    const m = await message.channel.send("Para Começarmos, devo Dizer que Tenho Duas Regras, 1º Eu Nunca Erro, 2º Se eu Errar Volte para a Primeira Regra!!! https://cdn.discordapp.com/attachments/603568752206020608/713009979342192660/L.gif");
  
  }

  // comando ryuk
  if(comando === "ryuk") {
    const m = await message.channel.send("Coloque sua Assinatura em Meu Death Note..... https://cdn.discordapp.com/attachments/603568752206020608/713009978948059136/ryuk.gif");
  
  }

   // comando obito
   if(comando === "obito") {
    const m = await message.channel.send("Kamui!!! https://cdn.discordapp.com/attachments/603568752206020608/713012296514797588/obito.gif");
  
  }

    // comando tobi
    if(comando === "tobi") {
      const m = await message.channel.send("Kamui!!! https://cdn.discordapp.com/attachments/603568752206020608/713012302214987788/tobi.gif");
    
    }
  
      // comando sasuke
   if(comando === "sasuke") {
    const m = await message.channel.send("Narutooooooooo!!! https://cdn.discordapp.com/attachments/603568752206020608/713013250421424168/narutooooooooooooooooooo.gif");
  
  }

    // comando naruto
  if(comando === "naruto") {
    const m = await message.channel.send("Sasukeeeeeeeee!!! https://cdn.discordapp.com/attachments/603568752206020608/713013494370402314/sasukeeeeeeeeeeeeeee.gif");
    
    }

    // comando madara
    if(comando === "madara") {
      const m = await message.channel.send("Hashiramaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713016280139169827/hashiramaaaaaaaaaaaaaaaaaa.gif");
      
      }

      // comando hashirama
      if(comando === "hashirama") {
        const m = await message.channel.send("Madaraaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713016278712975440/madaraaaaaaaaaa.gif");
      
      }

  // comando bem vindo
  if(comando === "bem vindo") {
    const m = await message.channel.send("Isso Mesmo Seja Bem Vindo https://cdn.discordapp.com/attachments/603568752206020608/713009381981159474/Bem_Vindo.gif");
  
  }
  
  // comando saitama
  if(comando === "saitama") {
    const m = await message.channel.send("Hissatsu: Maji Naguri https://cdn.discordapp.com/attachments/603568752206020608/725804171877679194/saitama.gif");
  
  }
  
  // comando gohan
  if(comando === "gohan") {
    const m = await message.channel.send("aaaaaaaaaAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAA** Sintam o Poder da Forma Mistica https://cdn.discordapp.com/attachments/603568752206020608/725806467214737428/gohan.gif");
  
  }
  
// comando trunks
if(comando === "trunks") {
  const m = await message.channel.send("Burning Atack https://cdn.discordapp.com/attachments/603568752206020608/726085011148636341/trunks.gif");

}

// comando kale
if(comando === "kale") {
  const m = await message.channel.send("Sinta a Furia de Um Lendario Super Sayajin https://cdn.discordapp.com/attachments/603568752206020608/726089721570132018/kale.gif");

}

// comando caulifla
if(comando === "caulifla") {
  const m = await message.channel.send("aaaaaaaaaaaaaaaaaaAAAAAAAAAAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAAAA** Esse é o Poder do Super Sayajin 2 https://cdn.discordapp.com/attachments/603568752206020608/726091612899246170/caulifla.gif");

}

// comando kaulifla
if(comando === "kaulifla") {
  const m = await message.channel.send("aaaaaaaaaaaaaaaaaaAAAAAAAAAAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAAAA** Esse é o Poder do Super Sayajin 2 https://cdn.discordapp.com/attachments/603568752206020608/726091612899246170/caulifla.gif");

}

// comando kefla
if(comando === "kefla") {
  const m = await message.channel.send("A Fusão Potara une Kale e Caulifla, com Junto nos Tornamos Kefla https://cdn.discordapp.com/attachments/603568752206020608/726090423541432380/kefla.gif");

}

// comando jiren
if(comando === "jiren") {
  const m = await message.channel.send("Poder Elevado em 100% aaaaaaaaaaaaaaaaAAAAAAAAAAAAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAAAAAA** https://cdn.discordapp.com/attachments/603568752206020608/726088161784233994/overpower.gif");

}

// comando toppo
if(comando === "toppo") {
  const m = await message.channel.send("Hakai https://cdn.discordapp.com/attachments/603568752206020608/726089189552029696/hakai.gif");

}

// comando goten
if(comando === "goten") {
  const m = await message.channel.send("Super Ka-me-ha-me-hahahaaaaaaaaaaaaaaaaaaaaaa https://cdn.discordapp.com/attachments/603568752206020608/726084947068321823/goten.gif");

}

// comando picollo
if(comando === "picollo") {
  const m = await message.channel.send("Makankōsappō https://cdn.discordapp.com/attachments/603568752206020608/726086689826799687/picollo.gif");

}

 7// comando picolo
if(comando === "picolo") {
  const m = await message.channel.send("Makankōsappō https://cdn.discordapp.com/attachments/603568752206020608/726086689826799687/picollo.gif");

}

  // comando goku
  if(comando === "goku") {
    const m = await message.channel.send("Ka - me - ha - me - haaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713017232707420310/kamehameha.gif");
  
  }

 // comando kakaroto
 if(comando === "kakaroto") {
  const m = await message.channel.send("Ka - me - ha - me - haaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713017232707420310/kamehameha.gif");

}

  // comando vegeta
  if(comando === "vegeta") {
    const m = await message.channel.send("Galick Guuuuuuuuuuuuuuuuuuuuuuuuun!!! https://cdn.discordapp.com/attachments/603568752206020608/713017222146293760/galick_gun.gif");
  
  }

  // comando kakashi
  if(comando === "kakashi") {
    const m = await message.channel.send("Raikiri!!! https://cdn.discordapp.com/attachments/603568752206020608/713017901476478997/chidori.gif");
  
  }

  // comando yu-gi-oh
  if(comando === "yu-gi-oh") {
    const m = await message.channel.send("Trading Card..... https://cdn.discordapp.com/attachments/603568752206020608/713018376678801468/trading_card.gif");
  
  }

  // comando yugioh
  if(comando === "yugioh") {
    const m = await message.channel.send("Trading Card..... https://cdn.discordapp.com/attachments/603568752206020608/713018376678801468/trading_card.gif");
  
  }

 // comando frieza
 if(comando === "frieza") {
  const m = await message.channel.send("Cale-Se VERME MIZERAVEL, Vou lhe Tranformar em Pueira Cosmica!!! HA - HA - HA - HA https://cdn.discordapp.com/attachments/603568752206020608/713019382468706334/frezza.gif");

}

// comando freeza
if(comando === "freeza") {
  const m = await message.channel.send("Cale-Se VERME MIZERAVEL, Vou lhe Tranformar em Pueira Cosmica!!! HA - HA - HA - HA https://cdn.discordapp.com/attachments/603568752206020608/713019382468706334/frezza.gif");

}

// comando ben10
if(comando === "ben10") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036652087345242/ben10.gif");

}

// comando ben 10
if(comando === "ben 10") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036704671465524/bendez.gif");

}

// comando bendez
if(comando === "bendez") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036704671465524/bendez.gif");

}

// comando ben dez
if(comando === "ben dez") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036652087345242/ben10.gif");

}

// comando jacan
if(comando === "jacan") {
  const m = await message.channel.send("Você é a Vergonha da Profission!!! https://cdn.discordapp.com/attachments/603568752206020608/713037528206278717/jacan.gif");

}

// comando jacquin
if(comando === "jacquin") {
  const m = await message.channel.send("Você é a Vergonha da Profissão!!! https://cdn.discordapp.com/attachments/603568752206020608/713037561727287357/jacquin.gif");

}

// comando rocklee
if(comando === "rocklee") {
  const m = await message.channel.send("Primeiro Portão, o Portão de Abertura, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040068847075448/primeiroportao.gif");

}

// comando lee
if(comando === "lee") {
  const m = await message.channel.send("Segundo Portão, o Portão do Descanço, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040068889018438/segundoportao.gif");

}

// comando guysensei
if(comando === "guysensei") {
  const m = await message.channel.send("Oitavo Portão, o Portão da Morte, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040028141617182/oitavoportao.gif");

}

// comando gaisensei
if(comando === "gaisensei") {
  const m = await message.channel.send("Oitavo Portão, o Portão da Morte, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040028141617182/oitavoportao.gif");

}

// comando guy
if(comando === "guy") {
  const m = await message.channel.send("Terceiro Portão, o Portão da Vida Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040114422644736/terceiroportao.gif");

}

// comando gai
if(comando === "gai") {
  const m = await message.channel.send("Terceiro Portão, o Portão da Vida Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040114422644736/terceiroportao.gif");

}

// comando luccasneto
if(comando === "luccasneto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando luccas neto
if(comando === "luccas neto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando lucas neto
if(comando === "lucas neto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando lucasneto
if(comando === "lucasneto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando felipeneto
if(comando === "felipeneto") {
  const m = await message.channel.send("Criativo no Mine Galerinha..... https://cdn.discordapp.com/attachments/603568752206020608/713040831770263562/felipeneto.gif");

}

// comando felipe neto
if(comando === "felipe neto") {
  const m = await message.channel.send("Criativo no Mine Galerinha..... https://cdn.discordapp.com/attachments/603568752206020608/713040831770263562/felipeneto.gif");

}

// comando mario
if(comando === "mario") {
  const m = await message.channel.send("It's-a Me Mario https://cdn.discordapp.com/attachments/603568752206020608/713041504159006810/mario.gif");

}

// comando sonic
if(comando === "sonic") {
  const m = await message.channel.send("Eu sou a Velocidade!!! https://cdn.discordapp.com/attachments/603568752206020608/713041523880755280/sonic.gif");

}

// comando fu
if(comando === "fu") {
  const m = await message.channel.send("São, HAAAAA https://cdn.discordapp.com/attachments/603568752206020608/713041911509680178/fusao.gif");

}

// comando fusão
if(comando === "fusão") {
  const m = await message.channel.send("HAAAAA https://cdn.discordapp.com/attachments/603568752206020608/713041911509680178/fusao.gif");

}

// comando ash
if(comando === "ash") {
  const m = await message.channel.send("Ketchum, da Cidade de PALLET!!! https://cdn.discordapp.com/attachments/603568752206020608/713042221452230757/ash.gif");

}

// comando fusao
if(comando === "fusao") {
  const m = await message.channel.send("HAAAAA https://cdn.discordapp.com/attachments/603568752206020608/713041911509680178/fusao.gif");

}

// comando hahaha
if(comando === "hahaha") {
  const m = await message.channel.send("Qual é a graça? Imaginei que você perguntaria, É que eu pensei numa piada, Só que cê não entenderia.... Senhoras e senhores, esse é o Circo dos Horrores, Um show com tantas dores e todos os seus temores, Que alegria! Público, sorria!!! Nossa próxima atração é o Coringa..... https://cdn.discordapp.com/attachments/603568752206020608/713042595512844318/coringa.gif");

}

// comando choji
if(comando === "choji") {
  const m = await message.channel.send("Expanssão Parcial: Ambas as Mãos https://cdn.discordapp.com/attachments/603568752206020608/713043824754163832/choji.gif");

}

// comando ichigo
if(comando === "ichigo") {
  const m = await message.channel.send("Gentsuga Tenshou!!! https://cdn.discordapp.com/attachments/603568752206020608/713044299310301234/ichigo.gif");

}

// comando rukia
if(comando === "rukia") {
  const m = await message.channel.send("Bakudou 61, Rikujukourou!!! https://cdn.discordapp.com/attachments/603568752206020608/713044768091013181/rukia.gif");

}

// comando bills
if(comando === "bills") {
  const m = await message.channel.send("Hakai!!! https://cdn.discordapp.com/attachments/603568752206020608/713045181871423518/bills.gif");

}

// comando beerus
if(comando === "beerus") {
  const m = await message.channel.send("Hakai!!! https://cdn.discordapp.com/attachments/603568752206020608/713045181871423518/bills.gif ");

}

// comando kuririn
if(comando === "kuririn") {
  const m = await message.channel.send("Kienzan!!! https://cdn.discordapp.com/attachments/603568752206020608/713046067867942962/kuririn.gif");

}

// comando krillin
if(comando === "krillin") {
  const m = await message.channel.send("Kienzan!!! https://cdn.discordapp.com/attachments/603568752206020608/713046067867942962/kuririn.gif");

}

// comando tenshinhan
if(comando === "tenshinhan") {
  const m = await message.channel.send("Ki-Ko-Hoooooooooooooo!!! https://cdn.discordapp.com/attachments/603568752206020608/713054797590298635/kikoho.gif");

}

// comando gotenks
if(comando === "gotenks") {
  const m = await message.channel.send("Ataque Kamikaze!!! https://cdn.discordapp.com/attachments/603568752206020608/713055524941463563/gotenks.gif");

}

// comando hiruzen
if(comando === "hiruzen") {
  const m = await message.channel.send("Kuchiyose no Jutsu: Enma!!! https://cdn.discordapp.com/attachments/603568752206020608/746392192184090644/hiruzen.gif");

}

// comando tobirama
if(comando === "tobirama") {
  const m = await message.channel.send("Tenkyū https://cdn.discordapp.com/attachments/603568752206020608/746392098537734144/tobirama.gif");

}

// comando zabuza
if(comando === "zabuza") {
  const m = await message.channel.send("Kirigakure no Jutsu https://cdn.discordapp.com/attachments/603568752206020608/746392465744986255/zabuza.gif");

}

// comando itachi
if(comando === "itachi") {
  const m = await message.channel.send("Você é Fraco, te Falta Odio...... https://cdn.discordapp.com/attachments/603568752206020608/713056574012129380/itachi.gif");

}

// comando hidan
if(comando === "hidan") {
  const m = await message.channel.send("Ohh Deus Poderoso Jashin.... https://cdn.discordapp.com/attachments/603568752206020608/713056885368029294/hidan.gif");

}

// comando kiba
if(comando === "kiba") {
  const m = await message.channel.send("Ataque do Homem Besta, Pressa sobre Pressa!!! https://cdn.discordapp.com/attachments/603568752206020608/713057479952564244/kiba.gif");

}

// comando fuuton
if(comando === "fuuton") {
  const m = await message.channel.send("Raseshuriken.... https://cdn.discordapp.com/attachments/603568752206020608/713057764187963512/rasenshuriken.gif");

}

// comando juukenhou
if(comando === "juukenhou") {
  const m = await message.channel.send("Hakke Nishou, Yon Shou, Hachi Shou, Juuroku Shou, Sanjuu Nishou!!! https://cdn.discordapp.com/attachments/603568752206020608/713058250505060515/juukenhou.gif");

}

// comando suiton
if(comando === "suiton") {
  const m = await message.channel.send("Suiryuudan no Jutsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713058527928778793/zabuza.gif");

}

// comando gaara
if(comando === "gaara") {
  const m = await message.channel.send("Tsuname de Areia https://cdn.discordapp.com/attachments/603568752206020608/713059067601617006/gaara.gif");

}

// comando shikamaru
if(comando === "shikamaru") {
  const m = await message.channel.send("Jutsu Possessão da Sombra!!! https://cdn.discordapp.com/attachments/603568752206020608/713059483546288238/shikamaru.gif");

}

// comando katon
if(comando === "katon") {
  const m = await message.channel.send("Goukakyuu no Jutsu https://cdn.discordapp.com/attachments/603568752206020608/713060187858010273/katon.gif");

}

// comando minato
if(comando === "minato") {
  const m = await message.channel.send("Tecnica do Deus Voador do Trovão https://cdn.discordapp.com/attachments/603568752206020608/713060727060955216/minato.gif");

}

// comando orihime
if(comando === "orihime") {
  const m = await message.channel.send("Santen Kensshun, eu Rejeito!!! https://cdn.discordapp.com/attachments/697931757311492123/713067188684193844/orihime.gif");

}

// comando hinata
if(comando === "hinata") {
  const m = await message.channel.send("Oito Trigramas, Senssenta e Quatro Golpes https://cdn.discordapp.com/attachments/603568752206020608/713069597409935360/hinata.gif");

}

// comando sai
if(comando === "sai") {
  const m = await message.channel.send("Arte Ninja, Pergaminho da Super Bestas!!! https://cdn.discordapp.com/attachments/603568752206020608/713069920954613800/sai.gif");

}

// comando ino
if(comando === "ino") {
  const m = await message.channel.send("Jutsu Transferência de Mente.... https://cdn.discordapp.com/attachments/603568752206020608/713098093683277854/ino.gif");

}

// comando pikachu
if(comando === "pikachu") {
  const m = await message.channel.send("Pika Pikahh!!! Pika-Chuuuuu!!! https://cdn.discordapp.com/attachments/603568752206020608/713074367101272114/pikachu.gif");

}

// comando boruto
if(comando === "boruto") {
  const m = await message.channel.send("Kieru Rasengan https://cdn.discordapp.com/attachments/603568752206020608/713076012774326444/boruto.gif");

}

// comando ganju
if(comando === "ganju") {
  const m = await message.channel.send("Seppa https://cdn.discordapp.com/attachments/603568752206020608/713076738153906186/ganju.gif");

}

// comando jiraya
if(comando === "jiraya") {
  const m = await message.channel.send("Prisão da Boca do Sapo https://cdn.discordapp.com/attachments/603568752206020608/713081510907084850/jiraya.gif");

}

// comando orochimaru
if(comando === "orochimaru") {
  const m = await message.channel.send("Kusanagi!!! https://cdn.discordapp.com/attachments/603568752206020608/713084877867843654/kusanagi.gif");

}

// comando tsunade
if(comando === "tsunade") {
  const m = await message.channel.send("Shōsen Jutsu https://cdn.discordapp.com/attachments/603568752206020608/713088168148074526/tsunade.gif");

}

// comando sarada
if(comando === "sarada") {
  const m = await message.channel.send("Jutsu Bola de Fogo https://cdn.discordapp.com/attachments/603568752206020608/713088885864792124/sarada.gif");

}

// comando help
if(comando === "help") {
  const m = await message.channel.send(`**:star:__Olá, Alguém pediu Ajuda???__:star:**`);
  m.edit(`:diamond_shape_with_a_dot_inside:**Bem eu Sou WarioBOT!!! Sou um Robo Criado por Ultimate Strength#2307!!!**:diamond_shape_with_a_dot_inside:
  
  :gear:**__Informações do Bot__**:gear:
  
:satellite: **Prefixo = "w."**
:house:**Servidores = ${client.guilds.cache.size}**
:sunglasses: **Usuarios = ${client.users.cache.size}**
:file_cabinet: **Canais de Texto/Voz = ${client.channels.cache.size}**
:ping_pong: **Latência = ${m.createdTimestamp - message.createdTimestamp}ms**

              Comandos:
  
:crown:**Adm -**:crown:
***w.serverinfo w.botinfo w.help w.ajuda w.ping w.invite w.support w.suporte w.vote w.votar***
  
:bar_chart:**Status -**:bar_chart:
***w.stats(1 a 13)***
  
:partying_face:**Diversão -**:partying_face:
***w.bem-vindo w.kira w.ryuk w.l w.obito w.tobi w.sasuke w.naruto w.madara w.hashirama w.kakashi w.rocklee w.lee w.guy w.gai w.guysensei w.gaisensei w.choji w.itachi w.hidan w.kiba w.fuuton w.suiton w.katon w.juukenhou w.gaara w.shikamaru w.minato w.hinata w.sai w.ino w.boruto w.jiraya w.orochimaru w.tsunade w.sarada w.sakura w.pain w.kimimaru w.kimimaro w.kakuzu w.konan w.sasori w.nagato w.zetsu w.haku w.kaguya w.hagoromo w.indra w.ashura w.hiruzen w.tobirama w.zabuza w.gohan w.trunks w.kale w.caulifla w.kefla w.jiren w.toppo w.goten w.picollo w.picolo w.goku w.kakaroto w.vegeta w.frieza w.freeza w.fu w.fusão w.bills w.beerus w.kuririn w.krillin w.tenshinhan w.gotenks w.jabami w.yumeko w.ichigo w.rukia w.orihime w.ganju w.ulquiorra w.cifer w.aizen w.bankai w.kenpachi w.zaraki w.yoruichi w.shihoin w.renji w.abarai w.yoshino w.yoshi  w.ugaki w.koga w.sawatari w.mabashi w.utagawa w.kariya w.ichinose w.saitama w.luffy w.monkeudluffy w.roronoa w.zoro w.roronoazoro w.ash w.pikachu w.hahaha w.mario w.sonic w.suicidio w.jacquin w.jacan w.felipeneto w.luccasneto***`)


}

// comando ajuda
if(comando === "ajuda") {
  const m = await message.channel.send(`:diamond_shape_with_a_dot_inside:**Bem eu Sou WarioBOT!!! Sou um Robo Criado por Ultimate Strength#2307!!!**:diamond_shape_with_a_dot_inside:
  
  :gear:**__Informações do Bot__**:gear:
  
:satellite: **Prefixo = "w."**
:house:**Servidores = ${client.guilds.cache.size}**
:sunglasses: **Usuarios = ${client.users.cache.size}**
:file_cabinet: **Canais de Texto/Voz = ${client.channels.cache.size}**
:ping_pong: **Latência = ${m.createdTimestamp - message.createdTimestamp}ms**

              Comandos:
  
:crown:**Adm -**:crown:
***w.serverinfo w.botinfo w.help w.ajuda w.ping w.invite w.support w.suporte w.vote w.votar***
  
:bar_chart:**Status -**:bar_chart:
***w.stats(1 a 13)***
  
:partying_face:**Diversão -**:partying_face:
***w.bem-vindo w.kira w.ryuk w.l w.obito w.tobi w.sasuke w.naruto w.madara w.hashirama w.kakashi w.rocklee w.lee w.guy w.gai w.guysensei w.gaisensei w.choji w.itachi w.hidan w.kiba w.fuuton w.suiton w.katon w.juukenhou w.gaara w.shikamaru w.minato w.hinata w.sai w.ino w.boruto w.jiraya w.orochimaru w.tsunade w.sarada w.sakura w.pain w.kimimaru w.kimimaro w.kakuzu w.konan w.sasori w.nagato w.zetsu w.haku w.kaguya w.hagoromo w.indra w.ashura w.hiruzen w.tobirama w.zabuza w.gohan w.trunks w.kale w.caulifla w.kefla w.jiren w.toppo w.goten w.picollo w.picolo w.goku w.kakaroto w.vegeta w.frieza w.freeza w.fu w.fusão w.bills w.beerus w.kuririn w.krillin w.tenshinhan w.gotenks w.jabami w.yumeko w.ichigo w.rukia w.orihime w.ganju w.ulquiorra w.cifer w.aizen w.bankai w.kenpachi w.zaraki w.yoruichi w.shihoin w.renji w.abarai w.yoshino w.yoshi  w.ugaki w.koga w.sawatari w.mabashi w.utagawa w.kariya w.ichinose w.saitama w.luffy w.monkeudluffy w.roronoa w.zoro w.roronoazoro w.ash w.pikachu w.hahaha w.mario w.sonic w.suicidio w.jacquin w.jacan w.felipeneto w.luccasneto***`)

}

// comando sakura
if(comando === "sakura") {
  const m = await message.channel.send("Impacto da Flor de Cerejeira https://cdn.discordapp.com/attachments/603568752206020608/713089477194678372/sakura.gif");
  
}

// comando yoshino
if(comando === "yoshino") {
  const m = await message.channel.send("Zeige Dich Goethe https://cdn.discordapp.com/attachments/603568752206020608/741642276526227486/yoshino.png");
  
}

// comando yoshi
if(comando === "yoshi") {
  const m = await message.channel.send("Zeige Dich Nieder https://cdn.discordapp.com/attachments/603568752206020608/741642311519174656/yoshi.gif");
  
}

// comando ugaki
if(comando === "ugaki") {
  const m = await message.channel.send("Zeige Dich Gesell https://cdn.discordapp.com/attachments/603568752206020608/741642265168052274/ugaki.png");
  
}

// comando koga
if(comando === "koga") {
  const m = await message.channel.send("Zeige Dich Dalk https://cdn.discordapp.com/attachments/603568752206020608/741642441580609676/koga.png");
  
}

// comando sawatari
if(comando === "sawatari") {
  const m = await message.channel.send("Zeige Dich Baura https://cdn.discordapp.com/attachments/603568752206020608/741642178274787358/sawatari.gif");
  
}
// comando mabashi
if(comando === "mabashi") {
  const m = await message.channel.send("Zeige Dich Ritz https://cdn.discordapp.com/attachments/603568752206020608/741642494529241108/mabashi.gif");
  
}

// comando utagawa
if(comando === "utagawa") {
  const m = await message.channel.send("Zeige Dich Fried https://cdn.discordapp.com/attachments/603568752206020608/741642317378879538/utagawa.gif");
  
}

// comando kariya
if(comando === "kariya") {
  const m = await message.channel.send("Zeige Dich Messer https://cdn.discordapp.com/attachments/603568752206020608/741642390648913980/kariya.gif");
  
}

// comando ichinose
if(comando === "ichinose") {
  const m = await message.channel.send("Nijigasumi https://cdn.discordapp.com/attachments/603568752206020608/741642343354204170/ichinose.gif");
  
}

// comando pain
if(comando === "pain") {
  const m = await message.channel.send("Shinra Tensei.... https://cdn.discordapp.com/attachments/603568752206020608/713089805721796618/pain.gif");
  
}

// comando roronoa
if(comando === "roronoa") {
  const m = await message.channel.send("Ittoryu Iai: Shishi Sonson!!! https://cdn.discordapp.com/attachments/603568752206020608/713090166914285658/roronoa_zoro.gif");
  
}

// comando zoro
if(comando === "zoro") {
  const m = await message.channel.send("Ittoryu Iai: Shishi Sonson!!! https://cdn.discordapp.com/attachments/603568752206020608/713090166914285658/roronoa_zoro.gif");
  
}

// comando roronoazoro
if(comando === "roronoazoro") {
  const m = await message.channel.send("Ittoryu Iai: Shishi Sonson!!! https://cdn.discordapp.com/attachments/603568752206020608/713090166914285658/roronoa_zoro.gif");
  
}

// comando luffy
if(comando === "luffy") {
  const m = await message.channel.send("Gomu Gomu no Pistol!!! https://cdn.discordapp.com/attachments/603568752206020608/713090941283467324/luffy.gif");
  
}

// comando monkeydluffy
if(comando === "monkeydluffy") {
  const m = await message.channel.send("Gomu Gomu no Pistol!!! https://cdn.discordapp.com/attachments/603568752206020608/713090941283467324/luffy.gif");
  
}

// comando ulquiorra
if(comando === "ulquiorra") {
  const m = await message.channel.send("Cerro Negro!!! https://cdn.discordapp.com/attachments/603568752206020608/713092399320268810/cero.gif");
  
}

// comando cifer
if(comando === "cifer") {
  const m = await message.channel.send("Cerro Negro!!! https://cdn.discordapp.com/attachments/603568752206020608/713092399320268810/cero.gif");
  
}

// comando aizen
if(comando === "aizen") {
  const m = await message.channel.send("Hadou 90!!! https://cdn.discordapp.com/attachments/603568752206020608/713094059409014824/aizen.gif");
  
}

// comando bankai
if(comando === "bankai") {
  const m = await message.channel.send("Tensa Zangetsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713094792334016572/bankai.gif");
  
}

// comando kimimaru
if(comando === "kimimaru") {
  const m = await message.channel.send("Dança das Camélias!!! https://cdn.discordapp.com/attachments/603568752206020608/713095448923078746/kimimaro.gif");
  
}

// comando kimimaro
if(comando === "kimimaro") {
  const m = await message.channel.send("Dança das Camélias!!! https://cdn.discordapp.com/attachments/603568752206020608/713095448923078746/kimimaro.gif");
  
}

// comando kabuto
if(comando === "kabuto") {
  const m = await message.channel.send("Edo Tensei https://cdn.discordapp.com/attachments/603568752206020608/713096254837620869/edo_tensei.gif");

}

// comando kisame
if(comando === "kisame") {
  const m = await message.channel.send("Fúria da Samehada!!! https://cdn.discordapp.com/attachments/603568752206020608/713096513148026900/samehada.gif");

}

// comando deidara
if(comando === "deidara") {
  const m = await message.channel.send("A Arte é uma Explossão https://cdn.discordapp.com/attachments/603568752206020608/713096889683148800/deidara.gif");

}

// comando kakuzu
if(comando === "kakuzu") {
  const m = await message.channel.send("Jiongu!!! https://cdn.discordapp.com/attachments/603568752206020608/713097394710904913/kakuzu.gif");

}

// comando konan
if(comando === "konan") {
  const m = await message.channel.send("Dança do Shikigami https://cdn.discordapp.com/attachments/603568752206020608/713098045893640212/konan.gif");

}

// comando sasori
if(comando === "sasori") {
  const m = await message.channel.send("Marionete Preparada: Oito Ondas de Agulhas!!! https://cdn.discordapp.com/attachments/603568752206020608/713098425016778842/sasori.gif");

}

// comando nagato
if(comando === "nagato") {
  const m = await message.channel.send("Banshō Ten'in https://cdn.discordapp.com/attachments/603568752206020608/713098977268072518/nagato.gif");

}

// comando zetsu
if(comando === "zetsu") {
  const m = await message.channel.send("Transferência de Chakra!!! https://cdn.discordapp.com/attachments/603568752206020608/713099576600428606/zetsu.gif");

}

// comando suicidio
if(comando === "suicidio") {
  const m = await message.channel.send("Parabéns, Está Pessoa Acabou de MORRER!!! https://cdn.discordapp.com/attachments/603568752206020608/713100932866637824/suicidio.gif");

}

// comando kenpachi
if(comando === "kenpachi") {
  const m = await message.channel.send("Armadura de Reiatsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713374237276241930/zaraki.gif");

}

// comando zaraki
if(comando === "zaraki") {
  const m = await message.channel.send("Armadura de Reiatsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713374237276241930/zaraki.gif");

}

// comando yoruichi
if(comando === "yoruichi") {
  const m = await message.channel.send("Shunkō: Raijin Senkei https://cdn.discordapp.com/attachments/603568752206020608/713376192023232582/Yoruichi.gif");

}

// comando Shihoin
if(comando === "shihoin") {
  const m = await message.channel.send("Shunkō: Raijin Senkei https://cdn.discordapp.com/attachments/603568752206020608/713376192023232582/Yoruichi.gif");

}

// comando renji
if(comando === "renji") {
  const m = await message.channel.send("Bankai: Hihio Zabimaru https://cdn.discordapp.com/attachments/603568752206020608/713378281096740864/renji.gif");

}

// comando abarai
if(comando === "abarai") {
  const m = await message.channel.send("Bankai: Hihio Zabimaru https://cdn.discordapp.com/attachments/603568752206020608/713378281096740864/renji.gif");

}

// comando haku
if(comando === "haku") {
  const m = await message.channel.send("Espelhos Demoníacos de Cristais de Gelo https://cdn.discordapp.com/attachments/603568752206020608/714585248519815218/haku.gif");

}

// comando haku
if(comando === "haku") {
  const m = await message.channel.send("https://cdn.discordapp.com/attachments/603568752206020608/714585130974576660/haku2.gif");

}

// comando kaguya
if(comando === "kaguya") {
  const m = await message.channel.send("Amenominaka https://cdn.discordapp.com/attachments/603568752206020608/725084785759879248/Kaguya.gif");

}

// comando hagoromo
if(comando === "hagoromo") {
  const m = await message.channel.send("Seis Caminhos, Chibaku Tensei https://cdn.discordapp.com/attachments/603568752206020608/725085492726726809/hagoromo.gif");

}

// comando indra
if(comando === "indra") {
  const m = await message.channel.send("Ashuraaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/729428333762183238/indra.gif");

}

// comando ashura
if(comando === "ashura") {
  const m = await message.channel.send("Indraaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/729428313117950102/ashura.gif");

}

// comando yumeko
if(comando === "yumeko") {
  const m = await message.channel.send("Se Você quer Ganhar Alguma coisa, Você Precisa tentar Alcançá-La!!! https://cdn.discordapp.com/attachments/603568752206020608/729431222601777233/jabami.gif");

}

// comando jabami
if(comando === "jabami") {
  const m = await message.channel.send("Se Você quer Ganhar Alguma coisa, Você Precisa tentar Alcançá-La!!! https://cdn.discordapp.com/attachments/603568752206020608/729431222601777233/jabami.gif");

}

// comando Ajuda Stats
if(comando === "stats") {
  const m = await message.channel.send("**Para Conseguir Alterar o Status do WarioBOT Escreva w.stats E um Numero de 1 à 13 (Tudo Junto)**");

}

// comando Status 1
if(comando === "stats1") {
  const m = await client.user.setActivity(`| CS:GO com Meu Pai Ultimate Strength#2307, Matando os Bot.....`);

}

// comando Status 2
if(comando === "stats2") {
  const m = await client.user.setActivity(`| Meu Joguinho de Waifu....`);

}

// comando Status 3
if(comando === "stats3") {
  const m = await client.user.setActivity(`| Meu Prefixo é "w."`);

}

// comando Status 4
if(comando === "stats4") {
  const m = await client.user.setActivity(`| Minha Loli na Cama`);

}

// comando Status 5
if(comando === "stats5") {
  const m = await client.user.setActivity(`| Entre no Site do Meu Criador https://migatte-no-ultizin.webnode.com/`);

}

// comando Status 6
if(comando === "stats6") {
  const m = await client.user.setActivity(`| Minecraft, Saga Tentando Matar o Ender Dragon`);

}

// comando Status 7
if(comando === "stats7") {
  const m = await client.user.setActivity(`| Brocolis na Cara dos Noob!!!`);

}

// comando Status 8
if(comando === "stats8") {
  const m = await client.user.setActivity(`| Gosto Muito de Cookie AAAAAA`);

}

// comando Status 9
if(comando === "stats9") {
  const m = await client.user.setActivity(`| Estou em ${client.guilds.cache.size} Servidores, ${client.users.cache.size} Usuarios, e ${client.channels.cache.size} Canais!!!`);

}

// comando Status 10
if(comando === "stats10") {
  const m = await client.user.setActivity(`| Meu Criador no Lixo e Sendo Independente!!!`);

}

// comando Status 11
if(comando === "stats11") {
  const m = await client.user.setActivity(`| Pesquise UltiServer of Strength no Seu Navegador e Entre em Top.gg`);

}

// comando Status 12
if(comando === "stats12") {
  const m = await client.user.setActivity(`| Macarronada na Cabeça da Sua Vó`);

}

// comando Status 13
if(comando === "stats13") {
  const m = await client.user.setActivity(`| #AdeEmeTbmÉGente`);

}

});

client.login(config.token);

const Discord = require("discord.js");
const client = new Discord.Client(); 
const config = require("./config.json"); 

client.on("ready", () => {
  console.log(``); 
  client.user.setPresence({ game: { name: 'comando', type: 1, url: 'https://www.twitch.tv/ultimatestrength99'} });
    //0 = Jogando
    //  1 = Transmitindo
    //  2 = Ouvindo
    //  3 = Assistindo
});

client.on("guildCreate", guild => {
  console.log(`ATUALIZAÇÃO
  O WarioBOT Acaba de Entrar no Servidor:${guild.name}
  
  Com o Id: ${guild.id}... 
  Com ${guild.memberCount} Membros!!!
  E Com (${guild.channels.cache.size}) Canais/Categorias...
  Assim Estando em ${client.guilds.cache.size} Servidores`);
});

client.on("guildDelete", guild => {
  console.log(`ATUALIZAÇÃO
  O WarioBOT Acaba de Ser Removido do Servidor: ${guild.name}

  Com o Id: (id: ${guild.id})... 
  Com ${guild.memberCount} Membros!!!
  E Com (${guild.channels.cache.size}) Canais/Categorias...
  Assim Estando em ${client.guilds.cache.size} Servidores`);
});

    client.on("message", async message => {

        if(message.author.bot) return;
        if(message.channel.type === "dm") return;
        if(!message.content.startsWith(config.prefix)) return;
    
      const args = message.content.slice(config.prefix.length).trim().split(/ +/g);
      const comando = args.shift().toLowerCase();
      
// comando ping
if(comando === "ping") {
  const m = await message.channel.send("**Ping???**");
m.edit(`**:ping_pong: Pong!**
**:satellite: Latência = ${m.createdTimestamp - message.createdTimestamp}ms.....**
**:zap: Latencia de API = ${Math.round(client.ping)}ms**`);

}

// comando support
if(comando === "support") {
  const m = await message.channel.send(`**:zap:Servidor Suporte do Bot!!!:zap:**
  :arrow_right: **https://top.gg/servers/697931751829274631**
 
**:zap:Site de Suporte do Bot!!!:zap:**
  :arrow_right: **https://migatte-no-ultizin.webnode.com/bot/** 
  
**:zap:Top.gg do Bot!!!:zap:** 
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}

// comando suporte
if(comando === "suporte") {
  const m = await message.channel.send(`**:zap:Servidor Suporte do Bot!!!:zap:**
  :arrow_right: **https://top.gg/servers/697931751829274631**
 
**:zap:Site de Suporte do Bot!!!:zap:**
  :arrow_right: **https://migatte-no-ultizin.webnode.com/bot/** 
  
**:zap:Top.gg do Bot!!!:zap:** 
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}


// comando vote
if(comando === "vote") {
  const m = await message.channel.send(`**:zap:Vote no WarioBOT no Top.gg:zap:**
  
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}

// comando votar
if(comando === "votar") {
  const m = await message.channel.send(`**:zap:Vote no WarioBOT no Top.gg:zap:**
  
  :arrow_right: **https://top.gg/bot/709448420548673536/vote**`);

}

// comando invite
if(comando === "invite") {
  const m = await message.channel.send(`**:zap:Link de Invite do Bot!!!:zap:**
  
  :arrow_right: **https://discord.com/oauth2/authorize?client_id=709448420548673536&scope=bot&permissions=8**`);

}

// comando de prefixo
if(comando === "") {
  const m = await message.channel.send("**Parece que Alguém me Chamou... Para Saber meus Comandos, (Digite: w.help)**");

}

  // comando bem-vindo
  if(comando === "bem-vindo") {
    const m = await message.channel.send("Isso Mesmo Seja Bem Vindo https://cdn.discordapp.com/attachments/603568752206020608/713009381981159474/Bem_Vindo.gif");
  
  }

  // comando kira
  if(comando === "kira") {
    const m = await message.channel.send("Ei, Pare de Me Chamar, Vou Escrever seu Nome em Meu Death Note!!! https://cdn.discordapp.com/attachments/603568752206020608/713009392018259989/Kira.gif");
  
  }

// comando serverinfo
if(comando === "serverinfo") {
  const m = await message.channel.send(`:jigsaw:**__Info do Servidor ${message.guild.name}__**:jigsaw:
  :point_right:**Id: (${message.guild.id})...** 
  :point_right:**Numero de Membros (${message.guild.memberCount})...**
  :point_right:**Com (${message.guild.channels.cache.size}) Canais/Categorias...**`);

}

// comando botinfo
if(comando === "botinfo") {
  const m = await message.channel.send(`:jigsaw:**__Info do ${client.user.username}__**:jigsaw:

  :satellite:**Meu Prefixo é (w.)!!!**
  :house:**Estou em ${client.guilds.cache.size} Servidores!!!**
  :sunglasses:**Com ${client.users.cache.size} Usuarios**
  :file_cabinet:**Com ${client.channels.cache.size} Canais**
  :robot:**Meu Id é: ${client.user.id}**`);

}

// comando userinfo
if(comando === "userinfo") {
  const m = await message.channel.send(`**__Info do Usuario ${client.username}__**

  :globe_with_meridians:**Tag do Discord: ${client.tag}**
  :gear:**Id: ${client.id}**`)
  
}

  // comando l
  if(comando === "l") {
    const m = await message.channel.send("Para Começarmos, devo Dizer que Tenho Duas Regras, 1º Eu Nunca Erro, 2º Se eu Errar Volte para a Primeira Regra!!! https://cdn.discordapp.com/attachments/603568752206020608/713009979342192660/L.gif");
  
  }

  // comando ryuk
  if(comando === "ryuk") {
    const m = await message.channel.send("Coloque sua Assinatura em Meu Death Note..... https://cdn.discordapp.com/attachments/603568752206020608/713009978948059136/ryuk.gif");
  
  }

   // comando obito
   if(comando === "obito") {
    const m = await message.channel.send("Kamui!!! https://cdn.discordapp.com/attachments/603568752206020608/713012296514797588/obito.gif");
  
  }

    // comando tobi
    if(comando === "tobi") {
      const m = await message.channel.send("Kamui!!! https://cdn.discordapp.com/attachments/603568752206020608/713012302214987788/tobi.gif");
    
    }
  
      // comando sasuke
   if(comando === "sasuke") {
    const m = await message.channel.send("Narutooooooooo!!! https://cdn.discordapp.com/attachments/603568752206020608/713013250421424168/narutooooooooooooooooooo.gif");
  
  }

    // comando naruto
  if(comando === "naruto") {
    const m = await message.channel.send("Sasukeeeeeeeee!!! https://cdn.discordapp.com/attachments/603568752206020608/713013494370402314/sasukeeeeeeeeeeeeeee.gif");
    
    }

    // comando madara
    if(comando === "madara") {
      const m = await message.channel.send("Hashiramaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713016280139169827/hashiramaaaaaaaaaaaaaaaaaa.gif");
      
      }

      // comando hashirama
      if(comando === "hashirama") {
        const m = await message.channel.send("Madaraaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713016278712975440/madaraaaaaaaaaa.gif");
      
      }

  // comando bem vindo
  if(comando === "bem vindo") {
    const m = await message.channel.send("Isso Mesmo Seja Bem Vindo https://cdn.discordapp.com/attachments/603568752206020608/713009381981159474/Bem_Vindo.gif");
  
  }
  
  // comando saitama
  if(comando === "saitama") {
    const m = await message.channel.send("Hissatsu: Maji Naguri https://cdn.discordapp.com/attachments/603568752206020608/725804171877679194/saitama.gif");
  
  }
  
  // comando gohan
  if(comando === "gohan") {
    const m = await message.channel.send("aaaaaaaaaAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAA** Sintam o Poder da Forma Mistica https://cdn.discordapp.com/attachments/603568752206020608/725806467214737428/gohan.gif");
  
  }
  
// comando trunks
if(comando === "trunks") {
  const m = await message.channel.send("Burning Atack https://cdn.discordapp.com/attachments/603568752206020608/726085011148636341/trunks.gif");

}

// comando kale
if(comando === "kale") {
  const m = await message.channel.send("Sinta a Furia de Um Lendario Super Sayajin https://cdn.discordapp.com/attachments/603568752206020608/726089721570132018/kale.gif");

}

// comando caulifla
if(comando === "caulifla") {
  const m = await message.channel.send("aaaaaaaaaaaaaaaaaaAAAAAAAAAAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAAAA** Esse é o Poder do Super Sayajin 2 https://cdn.discordapp.com/attachments/603568752206020608/726091612899246170/caulifla.gif");

}

// comando kaulifla
if(comando === "kaulifla") {
  const m = await message.channel.send("aaaaaaaaaaaaaaaaaaAAAAAAAAAAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAAAA** Esse é o Poder do Super Sayajin 2 https://cdn.discordapp.com/attachments/603568752206020608/726091612899246170/caulifla.gif");

}

// comando kefla
if(comando === "kefla") {
  const m = await message.channel.send("A Fusão Potara une Kale e Caulifla, com Junto nos Tornamos Kefla https://cdn.discordapp.com/attachments/603568752206020608/726090423541432380/kefla.gif");

}

// comando jiren
if(comando === "jiren") {
  const m = await message.channel.send("Poder Elevado em 100% aaaaaaaaaaaaaaaaAAAAAAAAAAAAAAAAAAAAA**AAAAAAAAAAAAAAAAAAAAAAAA** https://cdn.discordapp.com/attachments/603568752206020608/726088161784233994/overpower.gif");

}

// comando toppo
if(comando === "toppo") {
  const m = await message.channel.send("Hakai https://cdn.discordapp.com/attachments/603568752206020608/726089189552029696/hakai.gif");

}

// comando goten
if(comando === "goten") {
  const m = await message.channel.send("Super Ka-me-ha-me-hahahaaaaaaaaaaaaaaaaaaaaaa https://cdn.discordapp.com/attachments/603568752206020608/726084947068321823/goten.gif");

}

// comando picollo
if(comando === "picollo") {
  const m = await message.channel.send("Makankōsappō https://cdn.discordapp.com/attachments/603568752206020608/726086689826799687/picollo.gif");

}

 7// comando picolo
if(comando === "picolo") {
  const m = await message.channel.send("Makankōsappō https://cdn.discordapp.com/attachments/603568752206020608/726086689826799687/picollo.gif");

}

  // comando goku
  if(comando === "goku") {
    const m = await message.channel.send("Ka - me - ha - me - haaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713017232707420310/kamehameha.gif");
  
  }

 // comando kakaroto
 if(comando === "kakaroto") {
  const m = await message.channel.send("Ka - me - ha - me - haaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/713017232707420310/kamehameha.gif");

}

  // comando vegeta
  if(comando === "vegeta") {
    const m = await message.channel.send("Galick Guuuuuuuuuuuuuuuuuuuuuuuuun!!! https://cdn.discordapp.com/attachments/603568752206020608/713017222146293760/galick_gun.gif");
  
  }

  // comando kakashi
  if(comando === "kakashi") {
    const m = await message.channel.send("Raikiri!!! https://cdn.discordapp.com/attachments/603568752206020608/713017901476478997/chidori.gif");
  
  }

  // comando yu-gi-oh
  if(comando === "yu-gi-oh") {
    const m = await message.channel.send("Trading Card..... https://cdn.discordapp.com/attachments/603568752206020608/713018376678801468/trading_card.gif");
  
  }

  // comando yugioh
  if(comando === "yugioh") {
    const m = await message.channel.send("Trading Card..... https://cdn.discordapp.com/attachments/603568752206020608/713018376678801468/trading_card.gif");
  
  }

 // comando frieza
 if(comando === "frieza") {
  const m = await message.channel.send("Cale-Se VERME MIZERAVEL, Vou lhe Tranformar em Pueira Cosmica!!! HA - HA - HA - HA https://cdn.discordapp.com/attachments/603568752206020608/713019382468706334/frezza.gif");

}

// comando freeza
if(comando === "freeza") {
  const m = await message.channel.send("Cale-Se VERME MIZERAVEL, Vou lhe Tranformar em Pueira Cosmica!!! HA - HA - HA - HA https://cdn.discordapp.com/attachments/603568752206020608/713019382468706334/frezza.gif");

}

// comando ben10
if(comando === "ben10") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036652087345242/ben10.gif");

}

// comando ben 10
if(comando === "ben 10") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036704671465524/bendez.gif");

}

// comando bendez
if(comando === "bendez") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036704671465524/bendez.gif");

}

// comando ben dez
if(comando === "ben dez") {
  const m = await message.channel.send("Tá na Hora de Virar Heroi!!! https://cdn.discordapp.com/attachments/603568752206020608/713036652087345242/ben10.gif");

}

// comando jacan
if(comando === "jacan") {
  const m = await message.channel.send("Você é a Vergonha da Profission!!! https://cdn.discordapp.com/attachments/603568752206020608/713037528206278717/jacan.gif");

}

// comando jacquin
if(comando === "jacquin") {
  const m = await message.channel.send("Você é a Vergonha da Profissão!!! https://cdn.discordapp.com/attachments/603568752206020608/713037561727287357/jacquin.gif");

}

// comando rocklee
if(comando === "rocklee") {
  const m = await message.channel.send("Primeiro Portão, o Portão de Abertura, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040068847075448/primeiroportao.gif");

}

// comando lee
if(comando === "lee") {
  const m = await message.channel.send("Segundo Portão, o Portão do Descanço, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040068889018438/segundoportao.gif");

}

// comando guysensei
if(comando === "guysensei") {
  const m = await message.channel.send("Oitavo Portão, o Portão da Morte, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040028141617182/oitavoportao.gif");

}

// comando gaisensei
if(comando === "gaisensei") {
  const m = await message.channel.send("Oitavo Portão, o Portão da Morte, Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040028141617182/oitavoportao.gif");

}

// comando guy
if(comando === "guy") {
  const m = await message.channel.send("Terceiro Portão, o Portão da Vida Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040114422644736/terceiroportao.gif");

}

// comando gai
if(comando === "gai") {
  const m = await message.channel.send("Terceiro Portão, o Portão da Vida Abra!!! https://cdn.discordapp.com/attachments/603568752206020608/713040114422644736/terceiroportao.gif");

}

// comando luccasneto
if(comando === "luccasneto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando luccas neto
if(comando === "luccas neto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando lucas neto
if(comando === "lucas neto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando lucasneto
if(comando === "lucasneto") {
  const m = await message.channel.send("Eu Sou uma FOCA e um IDIOTA!!! https://cdn.discordapp.com/attachments/603568752206020608/713040875936153620/lucasneto.gif");

}

// comando felipeneto
if(comando === "felipeneto") {
  const m = await message.channel.send("Criativo no Mine Galerinha..... https://cdn.discordapp.com/attachments/603568752206020608/713040831770263562/felipeneto.gif");

}

// comando felipe neto
if(comando === "felipe neto") {
  const m = await message.channel.send("Criativo no Mine Galerinha..... https://cdn.discordapp.com/attachments/603568752206020608/713040831770263562/felipeneto.gif");

}

// comando mario
if(comando === "mario") {
  const m = await message.channel.send("It's-a Me Mario https://cdn.discordapp.com/attachments/603568752206020608/713041504159006810/mario.gif");

}

// comando sonic
if(comando === "sonic") {
  const m = await message.channel.send("Eu sou a Velocidade!!! https://cdn.discordapp.com/attachments/603568752206020608/713041523880755280/sonic.gif");

}

// comando fu
if(comando === "fu") {
  const m = await message.channel.send("São, HAAAAA https://cdn.discordapp.com/attachments/603568752206020608/713041911509680178/fusao.gif");

}

// comando fusão
if(comando === "fusão") {
  const m = await message.channel.send("HAAAAA https://cdn.discordapp.com/attachments/603568752206020608/713041911509680178/fusao.gif");

}

// comando ash
if(comando === "ash") {
  const m = await message.channel.send("Ketchum, da Cidade de PALLET!!! https://cdn.discordapp.com/attachments/603568752206020608/713042221452230757/ash.gif");

}

// comando fusao
if(comando === "fusao") {
  const m = await message.channel.send("HAAAAA https://cdn.discordapp.com/attachments/603568752206020608/713041911509680178/fusao.gif");

}

// comando hahaha
if(comando === "hahaha") {
  const m = await message.channel.send("Qual é a graça? Imaginei que você perguntaria, É que eu pensei numa piada, Só que cê não entenderia.... Senhoras e senhores, esse é o Circo dos Horrores, Um show com tantas dores e todos os seus temores, Que alegria! Público, sorria!!! Nossa próxima atração é o Coringa..... https://cdn.discordapp.com/attachments/603568752206020608/713042595512844318/coringa.gif");

}

// comando choji
if(comando === "choji") {
  const m = await message.channel.send("Expanssão Parcial: Ambas as Mãos https://cdn.discordapp.com/attachments/603568752206020608/713043824754163832/choji.gif");

}

// comando ichigo
if(comando === "ichigo") {
  const m = await message.channel.send("Gentsuga Tenshou!!! https://cdn.discordapp.com/attachments/603568752206020608/713044299310301234/ichigo.gif");

}

// comando rukia
if(comando === "rukia") {
  const m = await message.channel.send("Bakudou 61, Rikujukourou!!! https://cdn.discordapp.com/attachments/603568752206020608/713044768091013181/rukia.gif");

}

// comando bills
if(comando === "bills") {
  const m = await message.channel.send("Hakai!!! https://cdn.discordapp.com/attachments/603568752206020608/713045181871423518/bills.gif");

}

// comando beerus
if(comando === "beerus") {
  const m = await message.channel.send("Hakai!!! https://cdn.discordapp.com/attachments/603568752206020608/713045181871423518/bills.gif ");

}

// comando kuririn
if(comando === "kuririn") {
  const m = await message.channel.send("Kienzan!!! https://cdn.discordapp.com/attachments/603568752206020608/713046067867942962/kuririn.gif");

}

// comando krillin
if(comando === "krillin") {
  const m = await message.channel.send("Kienzan!!! https://cdn.discordapp.com/attachments/603568752206020608/713046067867942962/kuririn.gif");

}

// comando tenshinhan
if(comando === "tenshinhan") {
  const m = await message.channel.send("Ki-Ko-Hoooooooooooooo!!! https://cdn.discordapp.com/attachments/603568752206020608/713054797590298635/kikoho.gif");

}

// comando gotenks
if(comando === "gotenks") {
  const m = await message.channel.send("Ataque Kamikaze!!! https://cdn.discordapp.com/attachments/603568752206020608/713055524941463563/gotenks.gif");

}

// comando hiruzen
if(comando === "hiruzen") {
  const m = await message.channel.send("Kuchiyose no Jutsu: Enma!!! https://cdn.discordapp.com/attachments/603568752206020608/746392192184090644/hiruzen.gif");

}

// comando tobirama
if(comando === "tobirama") {
  const m = await message.channel.send("Tenkyū https://cdn.discordapp.com/attachments/603568752206020608/746392098537734144/tobirama.gif");

}

// comando zabuza
if(comando === "zabuza") {
  const m = await message.channel.send("Kirigakure no Jutsu https://cdn.discordapp.com/attachments/603568752206020608/746392465744986255/zabuza.gif");

}

// comando itachi
if(comando === "itachi") {
  const m = await message.channel.send("Você é Fraco, te Falta Odio...... https://cdn.discordapp.com/attachments/603568752206020608/713056574012129380/itachi.gif");

}

// comando hidan
if(comando === "hidan") {
  const m = await message.channel.send("Ohh Deus Poderoso Jashin.... https://cdn.discordapp.com/attachments/603568752206020608/713056885368029294/hidan.gif");

}

// comando kiba
if(comando === "kiba") {
  const m = await message.channel.send("Ataque do Homem Besta, Pressa sobre Pressa!!! https://cdn.discordapp.com/attachments/603568752206020608/713057479952564244/kiba.gif");

}

// comando fuuton
if(comando === "fuuton") {
  const m = await message.channel.send("Raseshuriken.... https://cdn.discordapp.com/attachments/603568752206020608/713057764187963512/rasenshuriken.gif");

}

// comando juukenhou
if(comando === "juukenhou") {
  const m = await message.channel.send("Hakke Nishou, Yon Shou, Hachi Shou, Juuroku Shou, Sanjuu Nishou!!! https://cdn.discordapp.com/attachments/603568752206020608/713058250505060515/juukenhou.gif");

}

// comando suiton
if(comando === "suiton") {
  const m = await message.channel.send("Suiryuudan no Jutsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713058527928778793/zabuza.gif");

}

// comando gaara
if(comando === "gaara") {
  const m = await message.channel.send("Tsuname de Areia https://cdn.discordapp.com/attachments/603568752206020608/713059067601617006/gaara.gif");

}

// comando shikamaru
if(comando === "shikamaru") {
  const m = await message.channel.send("Jutsu Possessão da Sombra!!! https://cdn.discordapp.com/attachments/603568752206020608/713059483546288238/shikamaru.gif");

}

// comando katon
if(comando === "katon") {
  const m = await message.channel.send("Goukakyuu no Jutsu https://cdn.discordapp.com/attachments/603568752206020608/713060187858010273/katon.gif");

}

// comando minato
if(comando === "minato") {
  const m = await message.channel.send("Tecnica do Deus Voador do Trovão https://cdn.discordapp.com/attachments/603568752206020608/713060727060955216/minato.gif");

}

// comando orihime
if(comando === "orihime") {
  const m = await message.channel.send("Santen Kensshun, eu Rejeito!!! https://cdn.discordapp.com/attachments/697931757311492123/713067188684193844/orihime.gif");

}

// comando hinata
if(comando === "hinata") {
  const m = await message.channel.send("Oito Trigramas, Senssenta e Quatro Golpes https://cdn.discordapp.com/attachments/603568752206020608/713069597409935360/hinata.gif");

}

// comando sai
if(comando === "sai") {
  const m = await message.channel.send("Arte Ninja, Pergaminho da Super Bestas!!! https://cdn.discordapp.com/attachments/603568752206020608/713069920954613800/sai.gif");

}

// comando ino
if(comando === "ino") {
  const m = await message.channel.send("Jutsu Transferência de Mente.... https://cdn.discordapp.com/attachments/603568752206020608/713098093683277854/ino.gif");

}

// comando pikachu
if(comando === "pikachu") {
  const m = await message.channel.send("Pika Pikahh!!! Pika-Chuuuuu!!! https://cdn.discordapp.com/attachments/603568752206020608/713074367101272114/pikachu.gif");

}

// comando boruto
if(comando === "boruto") {
  const m = await message.channel.send("Kieru Rasengan https://cdn.discordapp.com/attachments/603568752206020608/713076012774326444/boruto.gif");

}

// comando ganju
if(comando === "ganju") {
  const m = await message.channel.send("Seppa https://cdn.discordapp.com/attachments/603568752206020608/713076738153906186/ganju.gif");

}

// comando jiraya
if(comando === "jiraya") {
  const m = await message.channel.send("Prisão da Boca do Sapo https://cdn.discordapp.com/attachments/603568752206020608/713081510907084850/jiraya.gif");

}

// comando orochimaru
if(comando === "orochimaru") {
  const m = await message.channel.send("Kusanagi!!! https://cdn.discordapp.com/attachments/603568752206020608/713084877867843654/kusanagi.gif");

}

// comando tsunade
if(comando === "tsunade") {
  const m = await message.channel.send("Shōsen Jutsu https://cdn.discordapp.com/attachments/603568752206020608/713088168148074526/tsunade.gif");

}

// comando sarada
if(comando === "sarada") {
  const m = await message.channel.send("Jutsu Bola de Fogo https://cdn.discordapp.com/attachments/603568752206020608/713088885864792124/sarada.gif");

}

// comando help
if(comando === "help") {
  const m = await message.channel.send(`**:star:__Olá, Alguém pediu Ajuda???__:star:**`);
  m.edit(`:diamond_shape_with_a_dot_inside:**Bem eu Sou WarioBOT!!! Sou um Robo Criado por Ultimate Strength#2307!!!**:diamond_shape_with_a_dot_inside:
  
  :gear:**__Informações do Bot__**:gear:
  
:satellite: **Prefixo = "w."**
:house:**Servidores = ${client.guilds.cache.size}**
:sunglasses: **Usuarios = ${client.users.cache.size}**
:file_cabinet: **Canais de Texto/Voz = ${client.channels.cache.size}**
:ping_pong: **Latência = ${m.createdTimestamp - message.createdTimestamp}ms**

              Comandos:
  
:crown:**Adm -**:crown:
***w.serverinfo w.botinfo w.help w.ajuda w.ping w.invite w.support w.suporte w.vote w.votar***
  
:bar_chart:**Status -**:bar_chart:
***w.stats(1 a 13)***
  
:partying_face:**Diversão -**:partying_face:
***w.bem-vindo w.kira w.ryuk w.l w.obito w.tobi w.sasuke w.naruto w.madara w.hashirama w.kakashi w.rocklee w.lee w.guy w.gai w.guysensei w.gaisensei w.choji w.itachi w.hidan w.kiba w.fuuton w.suiton w.katon w.juukenhou w.gaara w.shikamaru w.minato w.hinata w.sai w.ino w.boruto w.jiraya w.orochimaru w.tsunade w.sarada w.sakura w.pain w.kimimaru w.kimimaro w.kakuzu w.konan w.sasori w.nagato w.zetsu w.haku w.kaguya w.hagoromo w.indra w.ashura w.hiruzen w.tobirama w.zabuza w.gohan w.trunks w.kale w.caulifla w.kefla w.jiren w.toppo w.goten w.picollo w.picolo w.goku w.kakaroto w.vegeta w.frieza w.freeza w.fu w.fusão w.bills w.beerus w.kuririn w.krillin w.tenshinhan w.gotenks w.jabami w.yumeko w.ichigo w.rukia w.orihime w.ganju w.ulquiorra w.cifer w.aizen w.bankai w.kenpachi w.zaraki w.yoruichi w.shihoin w.renji w.abarai w.yoshino w.yoshi  w.ugaki w.koga w.sawatari w.mabashi w.utagawa w.kariya w.ichinose w.saitama w.luffy w.monkeudluffy w.roronoa w.zoro w.roronoazoro w.ash w.pikachu w.hahaha w.mario w.sonic w.suicidio w.jacquin w.jacan w.felipeneto w.luccasneto***`)


}

// comando ajuda
if(comando === "ajuda") {
  const m = await message.channel.send(`:diamond_shape_with_a_dot_inside:**Bem eu Sou WarioBOT!!! Sou um Robo Criado por Ultimate Strength#2307!!!**:diamond_shape_with_a_dot_inside:
  
  :gear:**__Informações do Bot__**:gear:
  
:satellite: **Prefixo = "w."**
:house:**Servidores = ${client.guilds.cache.size}**
:sunglasses: **Usuarios = ${client.users.cache.size}**
:file_cabinet: **Canais de Texto/Voz = ${client.channels.cache.size}**
:ping_pong: **Latência = ${m.createdTimestamp - message.createdTimestamp}ms**

              Comandos:
  
:crown:**Adm -**:crown:
***w.serverinfo w.botinfo w.help w.ajuda w.ping w.invite w.support w.suporte w.vote w.votar***
  
:bar_chart:**Status -**:bar_chart:
***w.stats(1 a 13)***
  
:partying_face:**Diversão -**:partying_face:
***w.bem-vindo w.kira w.ryuk w.l w.obito w.tobi w.sasuke w.naruto w.madara w.hashirama w.kakashi w.rocklee w.lee w.guy w.gai w.guysensei w.gaisensei w.choji w.itachi w.hidan w.kiba w.fuuton w.suiton w.katon w.juukenhou w.gaara w.shikamaru w.minato w.hinata w.sai w.ino w.boruto w.jiraya w.orochimaru w.tsunade w.sarada w.sakura w.pain w.kimimaru w.kimimaro w.kakuzu w.konan w.sasori w.nagato w.zetsu w.haku w.kaguya w.hagoromo w.indra w.ashura w.hiruzen w.tobirama w.zabuza w.gohan w.trunks w.kale w.caulifla w.kefla w.jiren w.toppo w.goten w.picollo w.picolo w.goku w.kakaroto w.vegeta w.frieza w.freeza w.fu w.fusão w.bills w.beerus w.kuririn w.krillin w.tenshinhan w.gotenks w.jabami w.yumeko w.ichigo w.rukia w.orihime w.ganju w.ulquiorra w.cifer w.aizen w.bankai w.kenpachi w.zaraki w.yoruichi w.shihoin w.renji w.abarai w.yoshino w.yoshi  w.ugaki w.koga w.sawatari w.mabashi w.utagawa w.kariya w.ichinose w.saitama w.luffy w.monkeudluffy w.roronoa w.zoro w.roronoazoro w.ash w.pikachu w.hahaha w.mario w.sonic w.suicidio w.jacquin w.jacan w.felipeneto w.luccasneto***`)

}

// comando sakura
if(comando === "sakura") {
  const m = await message.channel.send("Impacto da Flor de Cerejeira https://cdn.discordapp.com/attachments/603568752206020608/713089477194678372/sakura.gif");
  
}

// comando yoshino
if(comando === "yoshino") {
  const m = await message.channel.send("Zeige Dich Goethe https://cdn.discordapp.com/attachments/603568752206020608/741642276526227486/yoshino.png");
  
}

// comando yoshi
if(comando === "yoshi") {
  const m = await message.channel.send("Zeige Dich Nieder https://cdn.discordapp.com/attachments/603568752206020608/741642311519174656/yoshi.gif");
  
}

// comando ugaki
if(comando === "ugaki") {
  const m = await message.channel.send("Zeige Dich Gesell https://cdn.discordapp.com/attachments/603568752206020608/741642265168052274/ugaki.png");
  
}

// comando koga
if(comando === "koga") {
  const m = await message.channel.send("Zeige Dich Dalk https://cdn.discordapp.com/attachments/603568752206020608/741642441580609676/koga.png");
  
}

// comando sawatari
if(comando === "sawatari") {
  const m = await message.channel.send("Zeige Dich Baura https://cdn.discordapp.com/attachments/603568752206020608/741642178274787358/sawatari.gif");
  
}
// comando mabashi
if(comando === "mabashi") {
  const m = await message.channel.send("Zeige Dich Ritz https://cdn.discordapp.com/attachments/603568752206020608/741642494529241108/mabashi.gif");
  
}

// comando utagawa
if(comando === "utagawa") {
  const m = await message.channel.send("Zeige Dich Fried https://cdn.discordapp.com/attachments/603568752206020608/741642317378879538/utagawa.gif");
  
}

// comando kariya
if(comando === "kariya") {
  const m = await message.channel.send("Zeige Dich Messer https://cdn.discordapp.com/attachments/603568752206020608/741642390648913980/kariya.gif");
  
}

// comando ichinose
if(comando === "ichinose") {
  const m = await message.channel.send("Nijigasumi https://cdn.discordapp.com/attachments/603568752206020608/741642343354204170/ichinose.gif");
  
}

// comando pain
if(comando === "pain") {
  const m = await message.channel.send("Shinra Tensei.... https://cdn.discordapp.com/attachments/603568752206020608/713089805721796618/pain.gif");
  
}

// comando roronoa
if(comando === "roronoa") {
  const m = await message.channel.send("Ittoryu Iai: Shishi Sonson!!! https://cdn.discordapp.com/attachments/603568752206020608/713090166914285658/roronoa_zoro.gif");
  
}

// comando zoro
if(comando === "zoro") {
  const m = await message.channel.send("Ittoryu Iai: Shishi Sonson!!! https://cdn.discordapp.com/attachments/603568752206020608/713090166914285658/roronoa_zoro.gif");
  
}

// comando roronoazoro
if(comando === "roronoazoro") {
  const m = await message.channel.send("Ittoryu Iai: Shishi Sonson!!! https://cdn.discordapp.com/attachments/603568752206020608/713090166914285658/roronoa_zoro.gif");
  
}

// comando luffy
if(comando === "luffy") {
  const m = await message.channel.send("Gomu Gomu no Pistol!!! https://cdn.discordapp.com/attachments/603568752206020608/713090941283467324/luffy.gif");
  
}

// comando monkeydluffy
if(comando === "monkeydluffy") {
  const m = await message.channel.send("Gomu Gomu no Pistol!!! https://cdn.discordapp.com/attachments/603568752206020608/713090941283467324/luffy.gif");
  
}

// comando ulquiorra
if(comando === "ulquiorra") {
  const m = await message.channel.send("Cerro Negro!!! https://cdn.discordapp.com/attachments/603568752206020608/713092399320268810/cero.gif");
  
}

// comando cifer
if(comando === "cifer") {
  const m = await message.channel.send("Cerro Negro!!! https://cdn.discordapp.com/attachments/603568752206020608/713092399320268810/cero.gif");
  
}

// comando aizen
if(comando === "aizen") {
  const m = await message.channel.send("Hadou 90!!! https://cdn.discordapp.com/attachments/603568752206020608/713094059409014824/aizen.gif");
  
}

// comando bankai
if(comando === "bankai") {
  const m = await message.channel.send("Tensa Zangetsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713094792334016572/bankai.gif");
  
}

// comando kimimaru
if(comando === "kimimaru") {
  const m = await message.channel.send("Dança das Camélias!!! https://cdn.discordapp.com/attachments/603568752206020608/713095448923078746/kimimaro.gif");
  
}

// comando kimimaro
if(comando === "kimimaro") {
  const m = await message.channel.send("Dança das Camélias!!! https://cdn.discordapp.com/attachments/603568752206020608/713095448923078746/kimimaro.gif");
  
}

// comando kabuto
if(comando === "kabuto") {
  const m = await message.channel.send("Edo Tensei https://cdn.discordapp.com/attachments/603568752206020608/713096254837620869/edo_tensei.gif");

}

// comando kisame
if(comando === "kisame") {
  const m = await message.channel.send("Fúria da Samehada!!! https://cdn.discordapp.com/attachments/603568752206020608/713096513148026900/samehada.gif");

}

// comando deidara
if(comando === "deidara") {
  const m = await message.channel.send("A Arte é uma Explossão https://cdn.discordapp.com/attachments/603568752206020608/713096889683148800/deidara.gif");

}

// comando kakuzu
if(comando === "kakuzu") {
  const m = await message.channel.send("Jiongu!!! https://cdn.discordapp.com/attachments/603568752206020608/713097394710904913/kakuzu.gif");

}

// comando konan
if(comando === "konan") {
  const m = await message.channel.send("Dança do Shikigami https://cdn.discordapp.com/attachments/603568752206020608/713098045893640212/konan.gif");

}

// comando sasori
if(comando === "sasori") {
  const m = await message.channel.send("Marionete Preparada: Oito Ondas de Agulhas!!! https://cdn.discordapp.com/attachments/603568752206020608/713098425016778842/sasori.gif");

}

// comando nagato
if(comando === "nagato") {
  const m = await message.channel.send("Banshō Ten'in https://cdn.discordapp.com/attachments/603568752206020608/713098977268072518/nagato.gif");

}

// comando zetsu
if(comando === "zetsu") {
  const m = await message.channel.send("Transferência de Chakra!!! https://cdn.discordapp.com/attachments/603568752206020608/713099576600428606/zetsu.gif");

}

// comando suicidio
if(comando === "suicidio") {
  const m = await message.channel.send("Parabéns, Está Pessoa Acabou de MORRER!!! https://cdn.discordapp.com/attachments/603568752206020608/713100932866637824/suicidio.gif");

}

// comando kenpachi
if(comando === "kenpachi") {
  const m = await message.channel.send("Armadura de Reiatsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713374237276241930/zaraki.gif");

}

// comando zaraki
if(comando === "zaraki") {
  const m = await message.channel.send("Armadura de Reiatsu!!! https://cdn.discordapp.com/attachments/603568752206020608/713374237276241930/zaraki.gif");

}

// comando yoruichi
if(comando === "yoruichi") {
  const m = await message.channel.send("Shunkō: Raijin Senkei https://cdn.discordapp.com/attachments/603568752206020608/713376192023232582/Yoruichi.gif");

}

// comando Shihoin
if(comando === "shihoin") {
  const m = await message.channel.send("Shunkō: Raijin Senkei https://cdn.discordapp.com/attachments/603568752206020608/713376192023232582/Yoruichi.gif");

}

// comando renji
if(comando === "renji") {
  const m = await message.channel.send("Bankai: Hihio Zabimaru https://cdn.discordapp.com/attachments/603568752206020608/713378281096740864/renji.gif");

}

// comando abarai
if(comando === "abarai") {
  const m = await message.channel.send("Bankai: Hihio Zabimaru https://cdn.discordapp.com/attachments/603568752206020608/713378281096740864/renji.gif");

}

// comando haku
if(comando === "haku") {
  const m = await message.channel.send("Espelhos Demoníacos de Cristais de Gelo https://cdn.discordapp.com/attachments/603568752206020608/714585248519815218/haku.gif");

}

// comando haku
if(comando === "haku") {
  const m = await message.channel.send("https://cdn.discordapp.com/attachments/603568752206020608/714585130974576660/haku2.gif");

}

// comando kaguya
if(comando === "kaguya") {
  const m = await message.channel.send("Amenominaka https://cdn.discordapp.com/attachments/603568752206020608/725084785759879248/Kaguya.gif");

}

// comando hagoromo
if(comando === "hagoromo") {
  const m = await message.channel.send("Seis Caminhos, Chibaku Tensei https://cdn.discordapp.com/attachments/603568752206020608/725085492726726809/hagoromo.gif");

}

// comando indra
if(comando === "indra") {
  const m = await message.channel.send("Ashuraaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/729428333762183238/indra.gif");

}

// comando ashura
if(comando === "ashura") {
  const m = await message.channel.send("Indraaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa!!! https://cdn.discordapp.com/attachments/603568752206020608/729428313117950102/ashura.gif");

}

// comando yumeko
if(comando === "yumeko") {
  const m = await message.channel.send("Se Você quer Ganhar Alguma coisa, Você Precisa tentar Alcançá-La!!! https://cdn.discordapp.com/attachments/603568752206020608/729431222601777233/jabami.gif");

}

// comando jabami
if(comando === "jabami") {
  const m = await message.channel.send("Se Você quer Ganhar Alguma coisa, Você Precisa tentar Alcançá-La!!! https://cdn.discordapp.com/attachments/603568752206020608/729431222601777233/jabami.gif");

}

// comando Ajuda Stats
if(comando === "stats") {
  const m = await message.channel.send("**Para Conseguir Alterar o Status do WarioBOT Escreva w.stats E um Numero de 1 à 13 (Tudo Junto)**");

}

// comando Status 1
if(comando === "stats1") {
  const m = await client.user.setActivity(`| CS:GO com Meu Pai Ultimate Strength#2307, Matando os Bot.....`);

}

// comando Status 2
if(comando === "stats2") {
  const m = await client.user.setActivity(`| Meu Joguinho de Waifu....`);

}

// comando Status 3
if(comando === "stats3") {
  const m = await client.user.setActivity(`| Meu Prefixo é "w."`);

}

// comando Status 4
if(comando === "stats4") {
  const m = await client.user.setActivity(`| Minha Loli na Cama`);

}

// comando Status 5
if(comando === "stats5") {
  const m = await client.user.setActivity(`| Entre no Site do Meu Criador https://migatte-no-ultizin.webnode.com/`);

}

// comando Status 6
if(comando === "stats6") {
  const m = await client.user.setActivity(`| Minecraft, Saga Tentando Matar o Ender Dragon`);

}

// comando Status 7
if(comando === "stats7") {
  const m = await client.user.setActivity(`| Brocolis na Cara dos Noob!!!`);

}

// comando Status 8
if(comando === "stats8") {
  const m = await client.user.setActivity(`| Gosto Muito de Cookie AAAAAA`);

}

// comando Status 9
if(comando === "stats9") {
  const m = await client.user.setActivity(`| Estou em ${client.guilds.cache.size} Servidores, ${client.users.cache.size} Usuarios, e ${client.channels.cache.size} Canais!!!`);

}

// comando Status 10
if(comando === "stats10") {
  const m = await client.user.setActivity(`| Meu Criador no Lixo e Sendo Independente!!!`);

}

// comando Status 11
if(comando === "stats11") {
  const m = await client.user.setActivity(`| Pesquise UltiServer of Strength no Seu Navegador e Entre em Top.gg`);

}

// comando Status 12
if(comando === "stats12") {
  const m = await client.user.setActivity(`| Macarronada na Cabeça da Sua Vó`);

}

// comando Status 13
if(comando === "stats13") {
  const m = await client.user.setActivity(`| #AdeEmeTbmÉGente`);

}

});

client.login(config.token);

---------------------------------------------------------------------------------------------

# config.json

{
    "prefix": "w.",
    "token": "BOT_TOKEN"
}

---------------------------------------------------------------------------------------------

# procfile

worker node bot.js
worker node config.json
