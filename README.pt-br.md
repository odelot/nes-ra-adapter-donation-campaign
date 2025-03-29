# Campanha de Doação - Adaptador NES RetroAchievements
[![en-us](https://img.shields.io/badge/lang-en--us-red.svg)](https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/README.md)

## Levando Conquistas Retro para o Console Original

Imagine poder **desbloquear conquistas** enquanto joga no seu **NES original**, assim como acontece nos emuladores. Graças a uma comunidade apaixonada por retrogames e à infraestrutura do RetroAchievements, nosso projeto torna isso realidade: traz as conquistas mapeadas pela comunidade para o NES físico, permitindo que os jogadores as registrem **usando cartuchos originais**.

---

-> **Voce pode fazer o seu agora mesmo!** <- Todo o código, esquemas de circuito, tudo está compartilhado [aqui](https://github.com/odelot/nes-ra-adapter-temp/blob/main/README.pt-br.md)! 

**Quer ajudar?**

- **Doe para nossa campanha** (termina no fim de abril) e nos ajuda a **entrega-lo da forma como idealizamos**, miniaturizado, com case 3d e sendo usado sem ser necessário abrir o console.
- Ajude a **divulgar o projeto** e a campanha!
- Construa, use, teste e **faça parte do projeto** ^.^

**Assista ao vídeo da nossa campanha abaixo**  
<p align="center">
  <a href="https://youtu.be/GlHCe4abKAs">
    <img width="70%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/videoUS-animated.gif">
  </a>
</p>

## Nossa Campanha de Doação

- **Meta:** R$ 20.000
- **Duração** 1 mês - Abril
- **Progresso:**
<p align="center">
  <img width="400px" height="75px" src="https://geps.dev/progress/7"/>
</p>

**Quer doar?** Clique nos botões abaixo

- [![Vakinha](https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/botaoVakinha.png)](https://www.vakinha.com.br/vaquinha/ajuda-para-continuar-com-o-projeto-do-adaptador-de-conquistas-para-o-nintendinho) - **Para brasileiros**
- [!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/nes.ra.adapter) - **Para estrangeiros** (não brasileiros)

## Nossa Jornada e Desafios

Até agora, investimos aproximadamente R$8.000 principalmente em hardware (PCBs, microcontroladores, taxas de importação, etc.), sem contar as inúmeras horas de desenvolvimento e testes. Nosso protótipo já é totalmente funcional e permite que você, se quiser, recrie o seu na protoboard ou utilizando as PCBs de protótipo que desenvolvemos.

Além disso, grande parte da tecnologia desenvolvida – como a interface LCD, o fluxo de configuração e a implementação dos operadores do RA – poderá ser reutilizada em futuros projetos para adaptadores de outros consoles, como SNES, MegaDrive/Genesis, PS1 e outros.

Nosso próximo objetivo é refinar esse protótipo em uma **versão final e acessível** – com uma PCB miniaturizada, capaz de caber no formato do cartucho (sem a necessidade de abrir o console, como ocorre atualmente com o protótipo). Isso envolve iterações de melhoria na PCB, construir prototipos para distribuir para membros da comunidade testar, ou seja, um investimento consideravel. 

## Objetivos da Campanha

Pretendemos arrecadar R$20.000,00 para:

- **Cobrir os custos passados e futuros:** Com os investimentos já realizados em hardware e taxas, e também com os custos para a próxima fase.
- **Finalizar o projeto conforme idealizado:** Refino e miniaturização da PCB para que o adaptador caiba no formato de um cartucho, sem que o console precise ser aberto.

<p align="center">
  <img width="70%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/fitPCB-PTBR.png"/>
</p>

## Transparência e Compartilhamento Open Source

Estamos comprometidos com a transparência e a colaboração. Por isso, **no primeiro dia da campanha, em 29/03, compartilharemos todo o material do projeto**. Isso inclui:

- Código-fonte completo;
- Esquemas das PCBs (incluindo os protótipos);
- Modelos 3D para impressão do case;
- Documentação.

<p align="center">
  <img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/share.png"/>
</p>


Dessa forma, qualquer entusiasta poderá montar seu próprio adaptador utilizando a protoboard ou as PCBs de protótipo, além de contribuir com melhorias e, quem sabe, desenvolver novas versões para outros consoles.

## Como o Dinheiro Será Usado

O dinheiro arrecadado será dividido entre **odelot** e **gh**. Todos os gastos até agora foram cobertos por **odelot** e, na próxima fase, **gh** será responsável por:

- Refinar e miniaturizar o hardware para que o adaptador se encaixe no formato de um cartucho.
- Criar novos protótipos e testar com a comunidade.
- Comprar hardware adicional e cobrir eventuais custos imprevistos no desenvolvimento.

## Como Funciona

- Funciona de forma semelhante ao Game Genie, mas em vez de alterar valores do cartucho, ele monitora cada escrita na memória para detectar as conquistas.
- Adiciona conectividade à Internet no NES, permitindo a comunicação em tempo real com o RetroAchievements.
- A interface do usuário ocorre por meio de um LCD, um buzzer e também via smartphone (para configurar o adaptador com as credenciais de Wi-Fi e RA).
- Identifica o cartucho lendo seu conteúdo e interpreta as conquistas utilizando a biblioteca [rcheevos](https://github.com/RetroAchievements/rcheevos).
- Utiliza Raspberry Pi Pico e ESP32, tornando o projeto acessível (aproximadamente R$120,00 em componentes, sem contar PCB, case 3D, taxas de importação e frete).
- Mais detalhes técnicos podem ser encontrados no reposítorio do projeto.

<p align="center">
  <img width="80%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/howItWorksUSEN.png"/>
</p>
*(A imagem acima representa nossa meta para o adaptador após a campanha de doação.)*

## Limitações

Já encontramos alguns desafios durante o desenvolvimento:

- **Testes com diferentes jogos:** Nos testamos o adaptador com cerca de 50 games. Enquanto a maioria funcionou corretamente, dois tiveram problemas. Confira a [pagina de compatibilidade](https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/Compatibility.md) para ver quais games foram testados e quais tiveram problemas. Nós esperamos melhorar o adaptador para aumentar a compatibilidade.

- **Detecção de frame e reset:** Não conseguimos detectar um frame apenas inspecionando os sinais do cartucho. Utilizamos uma heurística que, até agora, tem mostrado bons resultados, mas não há garantia de que funcione para todas as conquistas. Além disso, a detecção de RESET do console ainda não está implementada, exigindo que o console seja desligado e ligado para reinicialização.

- **Tamanho da Resposta do Servidor:** A RAM disponível para armazenar a resposta do RetroAchievements, que contém a lista de conquistas e endereços de memória a serem monitorados, é limitada a **32KB**. Publicaremos um código-fonte de uma função AWS Lambda para remover campos desnecessários ou reduzir a lista de conquistas, garantindo que a resposta caiba dentro desse limite.

## Apoio e Atualizações

Queremos manter a comunidade envolvida e informada durante todo o processo de desenvolvimento. Por isso:

- Teremos um **canal no Discord** para dúvidas, feedbacks e atualizações. [Junte-se ao canal](https://discord.gg/9atpm3BR)

- Uma **seção de FAQ** será disponibilizada à medida que as dúvidas surgirem.

- Compartilharemos detalhes do desenvolvimento e atualizações ao longo da campanha.

### Cronograma

- **29/03:** Lançamento oficial da campanha e liberação de todo o material do projeto (código-fonte, esquemas, modelos 3D, documentação).

- **Abril:** Melhoria da documentação - otimizações necessárias em software

- **Abril - Junho:** Iterações no desenvolvimento, miniaturização e melhoria da parte de hardware, principalmente no desenho da PCB e modelagem do case em 3d

## Quem Somos

### <img src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/profileOdelot.png" width="75px"> odelot

Formado em Ciência da Computação, **odelot** dedicou meses de seu período sabático ao estudo da arquitetura do NES e ao desenvolvimento do hardware e firmware do adaptador. Ele criou os protótipos que comprovaram o conceito e também modelou o case para impressão 3D.

### <img src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/profileGH.png" width="75px"> GH

Engenheiro Eletricista e especialista em circuitos analógicos de áudio, **gh** contribui com sua experiência na validação de circuitos e no desenvolvimento de soluções inovadoras. Ele será responsável pelo design final e miniaturização das PCBs do adaptador, que terão o formato de um **cartucho semelhante ao Game Genie**.

---

## Um Chamado à Comunidade

Este projeto é movido pela paixão por retrogames e pelo compromisso com a preservação dos consoles clássicos. Em vez de simplesmente produzir e entregar um produto final, **acreditamos que a verdadeira força está na colaboração da comunidade.** Convidamos todos a contribuir com ideias, melhorias, correções e a construir suas próprias versões a partir dos nossos protótipos.

Além disso, acreditamos que este adaptador é apenas o começo. O que estamos criando não é apenas um produto, mas **uma base para novos adaptadores** que poderão ser utilizados em outros consoles retrô, como SNES, Mega Drive/Genesis, PS1 e muitos outros. Com o apoio de todos e o código aberto, podemos construir algo maior e melhor do que seria possível se estivéssemos fazendo isso sozinhos.

**Junte-se a nós nesta jornada!** Sua contribuição, seja com apoio financeiro ou participação ativa no desenvolvimento, nos aproxima de transformar esse sonho em realidade, com a qualidade e transparência que a comunidade merece.

---

## Quer saber mais?

### Lista de videos

Uma lista de todos os vídeos compartilhados sobre o projeto, com uma breve descrição e data de publicação. Ajuda a entender a evolução do projeto ao longo do tempo. 

| Link do vídeo | Descrição | Data de lançamento |  
|--------------|-----------|--------------------|  
|<p align="center"><a href="https://www.youtube.com/shorts/PiTBeyToh9U"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video8.png"></a></p>|**Desbloqueando Conquista com o R.O.B.** - desbloquear essa conquista com um R.O.B. de verdade e um emulador seria dificil |2025/03/29|  
|<p align="center"><a href="https://youtu.be/SEKSnkoNz1k"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video7.png"></a></p>|**Como o NES RA Adapter funciona** - video curto resumindo como o adaptador funciona|2025/03/29|  
|<p align="center"><a href="https://youtu.be/GlHCe4abKAs"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video6.png"></a></p>|**Campanha de Doação do Adaptador de Conquistas para NES** – vídeo da campanha resumindo nossos objetivos|2025/03/20|  
|<p align="center"><a href="https://www.youtube.com/watch?v=uFExu-B9VnQ"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video5.png"></a></p>|**Maratona de conquistas com o NES RA ADAPTER** – testando o adaptador em quatro jogos seguidos, demonstrando a integração com a plataforma RetroAchievements|2025/03/11|  
|<p align="center"><a href="https://www.youtube.com/shorts/HaBRKZ8vLvs"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video3.png"></a></p>|**Logs do Adaptador NES RetroAchievements** – vídeo mostrando mudanças na tela de "teste de música" do Ninja Gaiden 2 sendo detectadas em tempo real e exibidas nos logs|2025/03/09|  
|<p align="center"><a href="https://www.youtube.com/shorts/4dFQZovuEFs"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video2.png"></a></p>|**Fluxo de Configuração do Adaptador NES RetroAchievements** – vídeo mostrando como configurar o adaptador com as credenciais de Wi-Fi e RA usando um smartphone|2024/12/27|  
|<p align="center"><a href="https://www.youtube.com/watch?v=FRES6z_qyDk"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video1.png"></a></p>|**Prova de Conceito do Adaptador RetroAchievements para NES** – demonstração inicial do adaptador, ainda sem integração total com o RA, mas já detectando uma conquista pré-programada, validando parte da ideia|2024/12/27|  

---

## Outros Projetos e Contribuições para a Comunidade Retrogame  

- **Web app para campeonatos de videogames retrô:** [https://github.com/odelot/retro_videogame_championship](https://github.com/odelot/retro_videogame_championship)  
- **Modelos 3D para impressão:** [https://www.thingiverse.com/odelot/designs](https://www.thingiverse.com/odelot/designs)  
- **Selecionando a entrada de vídeo dos consoles retrô usando Alexa:** [https://hackaday.com/2021/08/27/consoles-consoles-on-the-wall-can-alexa-help-me-play-them-all](https://hackaday.com/2021/08/27/consoles-consoles-on-the-wall-can-alexa-help-me-play-them-all)

---

*All hail RetroAchievements!*  


