# Donation Campaign - NES RetroAchievements Adapter 
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/README.pt-br.md)

## Bringing Retro Achievements to the Original Console

Imagine being able to **unlock achievements** while playing on your **original NES**, just like you can on emulators. Thanks to a passionate retro gaming community and the infrastructure provided by RetroAchievements, our project aims to make this a reality: bringing community-mapped achievements to the physical NES, allowing players to earn them **using original cartridges**.

---

-> **You can build yours right now!** <- All code, circuit schematics, everything is shared [here](https://github.com/odelot/nes-ra-adapter)!

**Want to help?**

- **Donate to our campaign** (ends at the end of April) and help us **deliver it as we envisioned**, miniaturized, with a 3D case, and usable without opening the console.
- Help **spread the word about the project** and campaign!
- Build, use, test, and **be part of the project** ^.^

**Please Watch our Campaign Video below**
<p align="center">
  <a href="https://www.youtube.com/watch?v=FRES6z_qyDk">
    <img width="70%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/videoUS-animated.gif">
  </a>
</p>

## Our Donation Campaing

- **Goal**: U$ 3.333 dollars (R$ 20.000)
- **Duration:** 1 month - April
- **Progress**:
<p align="center">
  <img width="400px" height="75px" src="https://geps.dev/progress/10"/>
</p>

**Want to donate?** click on the buttons below

- [!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/nes.ra.adapter) - **For Foreigns** (Non Brazilians)
- [![Vakinha](https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/botaoVakinha.png)](https://www.vakinha.com.br/vaquinha/ajuda-para-continuar-com-o-projeto-do-adaptador-de-conquistas-para-o-nintendinho) - **For Brazillians**

## Our Journey and Challenges

So far, we have invested approximately **U$1.333** (R$8000) mainly with hardware (PCBs, microcontrollers, import taxes to Brazil, etc), not to mention countless hours of development and testing. Our prototype is already capable of:

- **Identifying the inserted cartridge**;
- **Logging into RetroAchievements** and fetching game data;
- **Inspecting the cartridge’s memory** to interface with the achievement system using the rcheevos library;
- **Providing a web-based configuration interface**, guiding users to input their Wi-Fi and RetroAchievements credentials.

- and ultimately, - **Detect Achievements and Upload them to RetroAchievements 🙌**;

The next step is to refine this prototype into a **final, accessible form** – with a miniaturized PCB, 3D-printed cases, and an optimized design – so that any retro gaming enthusiast can build or acquire their own adapter.

---

## Goals of This Campaign

We aim to raise **U$3.333** (R$20,000.00) to:

- **Cover past and future hardware expenses** necessary to complete the final prototype.
- **Develop a miniaturized PCB** and a 3D-printed case with a design inspired by the classic Game Genie.
<p align="center">
  <img width="70%"  src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/fitPCB-USEN.png"/>
</p>

---

## Transparency and Open Source Sharing

We are committed to transparency and collaboration. That’s why **on the first day of the campaign, on 03/29, we will share all project materials**. This includes:

- Complete source code;
- PCB schematics (including prototypes);
- 3D models for case printing;
- Documentation.

<p align="center">
  <img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/share.png"/>
</p>

This way, any enthusiast can build their own adapter using a breadboard or prototype PCBs, contribute improvements, and potentially develop new versions for other consoles.

## How the Funds Will Be Spent

The money raised will be divided between **odelot** and **gh**. All expenses so far have been covered by **odelot**, and **gh** will be responsible for the next phase, including refining the hardware and miniaturizing it to fit the size of a Game Genie cartridge. This will involve:

- Creating prototypes;
- Fabricating the PCB;
- Purchasing additional hardware;
- Creating test prototypes for community feedback;
- And covering any unforeseen costs during the development process.

---

## How it works

- it works similar to a Game Genie, but instead of altering the values from the cartridge, it watches every write on the memory to detect the achievements.
- It also adds Internet to NES, because it is necessary for interfacing with RetroAchievements in real-time.
- The user interface is made by the tiny LCD, the buzzer and also by the smartphone screen (to configure the adapter with your wifi and RetroAchievements credentials).
- It identifies the cartridge reading its content and intrepret the achievements using RA [rcheevos](https://github.com/RetroAchievements/rcheevos) library (awesome lib btw).
- It uses Raspberry Pico and ESP32 instead of a FPGA and it is affordable (~ U$20 in parts, excluding PCB, 3D case, shipping fees and import taxes)
<p align="center">
  <img width="80%"  src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/howItWorksUSEN.png"/>
</p>
(the adapter in this image, with this size and appearance, is our goal after the donation campaign)

---

## Limitations

We’ve already encountered a few challenges during development:

- **Testing with various games**: We've tested the adapter with around 50 games. While the vast majority of games we tested worked correctly, two had issues. Please see the [compatibility page](https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/Compatibility.md) to see which games we have tested and which ones we had issues with. We hope to improve the adapter to further increase compatibility.

- **Detecting a frame and reset**: We are unable to detect a frame just inspecting the signals of the cartridge. We use a heuristic that gave us very good results (until now, we couldn't notice a miss achievement), but it is not guaranteed this will work for all achievements ever created (example: two delta operators in the same achievement could be challenging). If this happens in the future, we can try to improve our heuristics. We also cannot detect a Console RESET yet, so for the adapter to work like an emulator with RetroAchievements, it will be necessary to turn off/on the console.
  
- **Server Response Size**: The amount of RAM available for the response from RetroAchievements, that contains the list of achievements and memory addresses to monitor, is currently **32KB**. We will make available an AWS lambda function source code to remove unused fields or some achievements to reduce the response size and fit within the 32KB limit.

---

## Support and Updates

We want to keep the community engaged and informed throughout the development process. Therefore:

- We’ll be hosting a **Discord channel** where you can ask questions, share feedback, and stay updated. [Join the Channel](https://discord.gg/9atpm3BR)

- A **FAQ section** will be available here as soon as the questions arrives.

- We will continue to **share details about the development process** throughout the campaign (starting in April), including progress updates, challenges faced, and solutions implemented.

### Schedule

- **03/29:** Official launch of the campaign and release of all project material (source code, schematics, 3D models, documentation).

- **April:** Improvement of documentation - necessary optimizations in software

- **April - June:** Iterations in the development, miniaturization and improvement of the hardware part, mainly in the PCB design and 3D modeling of the case

---

## Who We Are

### <img src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/profileOdelot.png" width="75px"> odelot

A Computer Science graduate, **odelot** dedicated several months of his sabbatical to studying NES architecture and developing the hardware and firmware for the adapter. He was responsible for creating the prototypes that proved the concept and also designed the 3D-printed case.

### <img src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/profileGH.png" width="75px"> GH

An Electrical Engineer and expert in analog audio circuits, **gh** contributes his expertise in circuit validation and innovative problem-solving. He will be responsible for designing the miniaturized adapter’s PCBs, which will take the form of a **cartridge similar to the Game Genie**.

---

## A Call to the Community

This project is driven by a passion for retro gaming and a commitment to preserving the legacy of classic consoles. Instead of simply producing and delivering the adapter to the community, **we believe that the true strength comes from everyone’s collaboration**. The **community** has so much to offer, and we want everyone to **contribute ideas**, **improve the project with new features**, **fix bugs**, and ultimately **evolve the project together**.

Moreover, we believe this adapter is just the beginning. What we’re creating is not just a product, but **a foundation for new adapters** that could be used on other retro consoles, such as the SNES, MegaDrive/Genesis, PS1, and more. With everyone’s support and open-source code, we can build something bigger and better than what could be accomplished if we were doing it alone.

**Join us on this journey!** Your contribution, whether financial support or active participation in development, brings us closer to turning this dream into reality, with the quality and transparency the community deserves.

---

## Acknowledgements

**RetroAchievements** and its entire community for creating achievements for almost any game and making the whole system available to everyone. [https://retroachievements.org/](https://retroachievements.org/)

**NESDEV** for documenting the NES in incredible detail and for its friendly forum, where the community helps each other create games, emulators, and anything NES-related. [https://nesdev.org/](https://nesdev.org/)

---

## Want to know more? 

### Video List

A list of all shared videos of the project, with a brief description and date. This helps to understand how the project has evolved over time.

| video link | description | release date |
|------------|-------------|--------------|
|<p align="center"><a href="https://www.youtube.com/shorts/PiTBeyToh9U"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video8.png"></a></p>|**Unlock Achievement with R.O.B.** - unlock this achievement with a real R.O.B. would be hard on emulatores |2025/03/29|  
|<p align="center"><a href="https://youtu.be/u1GWOFgOU88"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video7.png"></a></p>|**How NES RA Adapter Works** - short video summarizing how the adapter works|2025/03/29|  
|<p align="center"><a href="https://www.youtube.com/watch?v=FRES6z_qyDk"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video6.png"></a></p>|**NES Achievement Adapter Donation Campaign** - campaign video summarizing our goals|2025/03/20|  
|<p align="center"><a href="https://www.youtube.com/watch?v=uFExu-B9VnQ"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video5.png"></a></p>|**Marathon of achievements with the NES RA ADAPTER** - testing the adapter with four games in a row, showing the integration with RetroAchievements platform|2025/03/11|  
|<p align="center"><a href="https://www.youtube.com/shorts/HaBRKZ8vLvs"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video3.png"></a></p>|**Logs from NES RetroAchievements Adapter** - video showing changes being made on the "music test" screen of Ninja Gaiden 2 being detected in real time and output on logs|2025/03/09|  
|<p align="center"><a href="https://www.youtube.com/shorts/4dFQZovuEFs"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video2.png"></a></p>|**PoC Workflow to config NES Retroachievements Adapter** - video showing how you configure the adapter with the wifi and RA credentials using the smartphone|2024/12/27|  
|<p align="center"><a href="https://www.youtube.com/watch?v=FRES6z_qyDk"><img width="50%" src="https://github.com/odelot/nes-ra-adapter-donation-campaign/blob/main/images/video1.png"></a></p>|**PoC RetroAchievements NES Adapter** - proof of concept of the adapter, not fully integrated with RA yet, but already showing the detection of one hardcoded achievement, thus validating part of the idea |2024/12/27|  

---

## Other Projects and Contributions to the Retro Gaming Community

- **Web app for retro gaming tournaments:** [https://github.com/odelot/retro_videogame_championship](https://github.com/odelot/retro_videogame_championship)  
- **3D models for printing:** [https://www.thingiverse.com/odelot/designs](https://www.thingiverse.com/odelot/designs)  
- **Selecting video input for retro consoles using Alexa:** [https://hackaday.com/2021/08/27/consoles-consoles-on-the-wall-can-alexa-help-me-play-them-all](https://hackaday.com/2021/08/27/consoles-consoles-on-the-wall-can-alexa-help-me-play-them-all)

---

*All hail RetroAchievements!*
