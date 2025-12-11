<div align="center">

![Logo](https://github.com/user-attachments/assets/c7dad5da-0b29-4710-8a57-b58e4e407abd)

### Traduction française internationale non officielle de [OptiScaler](https://github.com/optiscaler/OptiScaler)
</div>

<div align="center">
  <a href="https://discord.gg/wEyd9w4hG5"><img src="https://img.shields.io/badge/OptiScaler-blue?style=for-the-badge&logo=discord&logoColor=white&logoSize=auto&color=5865F2" alt="Invitation Discord"></a>
  <a href="https://github.com/optiscaler/OptiScaler/releases/latest"><img src="https://img.shields.io/badge/Télécharger-Stable-green?style=for-the-badge&logo=github&logoSize=auto" alt="Version stable"></a>
  <a href="https://github.com/optiscaler/OptiScaler/releases/tag/nightly"><img src="https://img.shields.io/badge/Télécharger-Développement-purple?style=for-the-badge&logo=github&logoSize=auto" alt="Version de développement"></a>
  <a href="https://github.com/optiscaler/OptiScaler/wiki"><img src="https://img.shields.io/badge/Documentation-blue?style=for-the-badge&logo=gitbook&logoColor=white&logoSize=auto" alt="Wiki"></a>
</div>

<div align="center">
  <a href="https://github.com/optiscaler/OptiScaler/releases"><img src="https://img.shields.io/github/downloads/optiscaler/optiscaler/total?style=for-the-badge&logo=gitextensions&logoSize=auto&label=Total" alt="Total DL"></a>
  <a href="https://github.com/optiscaler/OptiScaler/releases/latest"><img src="https://img.shields.io/github/downloads/optiscaler/optiscaler/latest/total?style=for-the-badge&logo=gitextensions&logoSize=auto&label=Stable&color=green&logoColor=white" alt="Télécharger stable"></a>
  <a href="https://github.com/optiscaler/OptiScaler/releases/tag/nightly"><img src="https://img.shields.io/github/downloads/optiscaler/OptiScaler/nightly/total?style=for-the-badge&logo=gitextensions&logoColor=white&logoSize=auto&label=Nightly&color=purple" alt="Télécharger développement"></a>
  <a href="https://github.com/optiscaler/OptiScaler/stargazers"><img src="https://img.shields.io/github/stars/optiscaler/optiscaler?style=for-the-badge&logo=githubsponsors&logoColor=white&label=S.T.A.R.S." alt="Stars"></a>
</div>

## Table des matières

**1.** [**À propos**](#à-propos)  
**2.** [**Comment ça fonctionne ?**](#how-it-works)  
**3.** [**APIs et upscalers pris en charge**](#which-apis-and-upscalers-are-supported)  
**4.** [**Installation**](#installation)  
**5.** [**Problèmes connus**](#known-issues)  
**6.** [**Compilation et crédits**](#compilation)  
**7.** [**Guide**](https://github.com/optiscaler/OptiScaler/wiki)

## À propos

**OptiScaler** est un outil qui permet de remplacer les upscalers dans les jeux qui ***prennent déjà en charge DLSS2+, XeSS, ou FSR2+*** ($`^1`$), et qui supporte désormais également ***l’activation de la génération d’images*** dans ces mêmes jeux (via ***dlssg-to-fsr3 de Nukem*** ou ***OptiFG***). Il offre aussi de larges options de personnalisation pour tous les utilisateurs, y compris ceux disposant de cartes graphiques Nvidia utilisant DLSS.

> [!CAUTION]
> * Nous avons été informés de certains **sites FAUX** se présentant comme l’équipe d’OptiScaler, donc nous tenons à **RAPPELER QUE OPTISCALER N'A PAS de site officiel !**  
> * Les seuls **endroits LÉGITIMES** sont [le GitHub originel](https://github.com/optiscaler/OptiScaler), ce Github, leur serveur Discord et la page NexusMods de Nitec.  
> * OptiScaler est **GRATUIT**, toute demande d’argent est une arnaque car Optiscaler n’a même pas de lien de don pour le moment !

> [!TIP]
> _Par exemple, si un jeu ne propose que DLSS, OptiScaler peut être utilisé pour remplacer DLSS par XeSS ou FSR 3.1 (fonctionne également pour les jeux uniquement FSR2, comme The Outer Worlds : Spacer's Choice)._

**Principaux aspects d'OptiScaler :**
- Permet l'utilisation de XeSS, FSR2, FSR3, **FSR4**$`^2`$ (_RDNA4 uniquement_) et DLSS dans les jeux avec la mise à l'échelle activée
- Offre aux utilisateurs la possibilité d’affiner leur expérience de mise à l’échelle avec un large éventail d’options et d’améliorations (RCAS & MAS, mise à l’échelle de sortie, préréglages DLSS, ratio et surcharges DRS, etc.)
- Depuis la v0.7.0+, ajout du support expérimental de la génération d’images ***DX12*** avec solution possible de correction de l’affichage tête haute ([**OptiFG**](#optifg-powered-by-fsr3-fg--hudfix-experimental-hud-ghosting-fix) par la génération d'images FSR3)
- Supporte l’intégration de [**Fakenvapi**](#installation) - permet l'accrochage de Reflex et l’injection de _Anti-Lag 2_ (RDNA1+ uniquement), _LatencyFlex_ (LFX) ou _XeLL_ (Intel uniquement) - **_non inclus_**$`^3`$
- Depuis la v0.7.7, ajout du support du mod de génération d'images FSR3 de **Nukem** [**dlssg-to-fsr3**](#installation), uniquement pour les jeux avec ***la génération d'images DLSS natif*** - **_non inclus_**$`^3`$
- Depuis la v0.7.8, ajout du support du **chargement de plugins ASI** (_désactivé par défaut, charge depuis un dossier personnalisable, par défaut `plugins`_)
- Nouveau projet - [**OptiPatcher**](https://github.com/optiscaler/OptiPatcher) - un plugin ASI pour OptiScaler permettant d’activer DLSS sans spoofing dans les jeux pris en charge
- Depuis la v0.7.8, OptiScaler applique automatiquement certains patchs de jeux pour une meilleure expérience dès l’installation
- Pour une liste détaillée de toutes les fonctionnalités, consultez [Fonctionnalités](Features.md)


> [!IMPORTANT]
> _**Vérifiez toujours la [liste de compatibilité du Guide](https://github.com/optiscaler/OptiScaler/wiki) pour connaître les problèmes connus des jeux et leurs solutions.**_
> > Veuillez également consulter la [***liste des problèmes connus d’OptiScaler***](#known-issues) à la fin concernant la compatibilité avec **RTSS**.  
> Une [***liste de compatibilité FSR4***](https://github.com/optiscaler/OptiScaler/wiki/FSR4-Compatibility-List) distincte est disponible pour les jeux testés par la communauté.  
> ***[3]** Pour les éléments **non inclus**, veuillez consulter [Installation](#installation).*

> [!NOTE]
> ### Notes sur les mises à l'échelle
> <details>
>  <summary><b>Cliquez pour [1], [2]</b></summary>  
>  
> **[1]** Pour les jeux **Unreal Engine**, seules les remplacements UE XeSS -> Opti XeSS/Opti FSR4 fonctionnent.  
>  
> *Concernant les entrées **XeSS**, comme le **plugin Unreal Engine** ne fournit pas de profondeur, remplacer XeSS dans le jeu casse les autres mises à l'échelle (ex. Redout 2, jeu uniquement XeSS), mais vous pouvez toujours appliquer l’accentuation RCAS à XeSS pour réduire le flou visuel.*  
>
> *Concernant les entrées **FSR**, FSR 3.1 est la première version avec une API entièrement standardisée et moderne et devrait être entièrement supportée. Comme FSR2 et FSR3 supportent des interfaces personnalisées, la compatibilité des jeux dépendra de l’implémentation des développeurs. Pour les jeux Unreal Engine, il peut être nécessaire d’appliquer des [tweaks ini](https://github.com/optiscaler/OptiScaler/wiki/Unreal-Engine-Tweaks) pour les entrées FSR.*  
>
> **[2]** *Concernant **FSR4**, le support a été ajouté avec les récentes versions de développement. Veuillez consulter la [liste de compatibilité FSR4](https://github.com/optiscaler/OptiScaler/wiki/FSR4-Compatibility-List) pour les jeux supportés connus et les informations générales.*
> 
> </details>


## Serveur Discord officiel : [OptiScaler](https://discord.gg/wEyd9w4hG5)

*Ce projet est basé sur l’excellent [CyberFSR2](https://github.com/PotatoOfDoom/CyberFSR2) de [PotatoOfDoom](https://github.com/PotatoOfDoom).*

## How it works?
* OptiScaler acts as a middleware, it intercepts upscaler calls from the game (_**Inputs**_) and redirects them to the chosen upscaling backend (_**Output**_), allowing user to replace one technology with another one. **Inputs -> OptiScaler -> Outputs**  
* _Or put more bluntly, **Input** is the upscaler used in game settings, and **Output** the one selected in Opti Overlay._

> [!NOTE]
> * Pressing **`Insert`** should open the Optiscaler **Overlay** in-game with all of the options (_`ShortcutKey=` can be changed in the config file_). 
> * Pressing **`Page Up`** shows the performance stats overlay in the top left, and can be cycled between different modes with **`Page Down`** (_keybinds customisable in the overlay_).  
> * If Opti overlay is instantly disappearing after trying Insert a few times, maybe try **`Alt + Insert`** ([reported workaround](https://github.com/optiscaler/OptiScaler/issues/484) for alternate keyboard layouts).

![inputs_and_outputs](https://raw.githubusercontent.com/Rayz0rum/OptiScaler-FrancaisINT/refs/heads/v0.9/images/entr%C3%A9es-sorties.png)

## Which APIs and Upscalers are Supported?
Currently **OptiScaler** can be used with DirectX 11, DirectX 12 and Vulkan, but each API has different sets of supported upscalers.  
[**OptiFG**](#optifg-powered-by-fsr3-fg--hudfix-experimental-hud-ghosting-fix) currently **only supports DX12** and is explained in a separate paragraph.

#### For DirectX 12
- XeSS (Default)
- FSR 2.1.2, 2.2.1
- FSR 3.X (and FSR 2.3.X)
- FSR 4.0.X (via FSR3.X update, _RDNA4 only_)
- DLSS

#### For DirectX 11
- FSR 2.2.1 (Default, native DX11)
- FSR 3.1.2 (unofficial port to native DX11)
- DLSS (native DX11)
- XeSS 2.X (native DX11, _Intel ARC only_)
- XeSS, FSR 2.1.2, 2.2.1, FSR 3.X w/Dx12 (_via D3D11on12_)$`^1`$
- FSR 4.0.X (via FSR 3.X w/Dx12 update, _RDNA4 only_)

> [!NOTE]
> <details>
>  <summary><b>Expand for [1]</b></summary>
>
> _**[1]** These implementations use a background DirectX12 device to be able to use DX12-only upscalers. There's a performance penalty up to 10-ish % for this method, but allows many more upscaler options. Also native DX11 implementation of FSR 2.2.1 is a backport from Unity renderer and has its own problems of which some were fixed by OptiScaler._
> </details>

#### For Vulkan
- FSR2 2.1.2 (Default), 2.2.1
- FSR3 3.1 (and FSR2 2.3.2)
- DLSS
- XeSS 2.x

#### OptiFG (powered by FSR3 FG) + HUDfix (experimental HUD ghosting fix) 
**OptiFG** was added with **v0.7** and is **only supported in DX12**. 
It's an **experimental** way of adding FSR3 FG to games without native Frame Generation, or can also be used as a last case scenario if the native FG is not working properly.

For more information on OptiFG and how to use it, please check the Wiki page - [OptiFG](https://github.com/optiscaler/OptiScaler/wiki/OptiFG).


## Installation
> [!CAUTION]
> _**Warning**: **Do not use this mod with online games.** It may trigger anti-cheat software and cause bans!_

> [!IMPORTANT]
> **For installation steps, please check the [**Wiki**](https://github.com/optiscaler/OptiScaler/wiki)**  

## Configuration
Please check [this](Config.md) document for configuration parameters and explanations. If your GPU is not an Nvidia one, check [GPU spoofing options](Spoofing.md) *(Will be updated)*

## Known Issues
If you can't open the in-game menu overlay:
1. Please check that you have enabled DLSS, XeSS or FSR from game options and are in-game, not inside game settings
2. If using legacy installation, please try opening menu while you are in-game (while 3D rendering is happening)
3. If you are using **RTSS** (MSI Afterburner, CapFrameX), please enable this setting in RTSS and/or try updating RTSS. **When using OptiFG, please disable RTSS for best compatibility**.
 
 ![image](https://github.com/optiscaler/OptiScaler/assets/35529761/8afb24ac-662a-40ae-a97c-837369e03fc7)

Please check [this](Issues.md) document for the rest of the known issues and possible solutions for them.  
Also check the community [Wiki](https://github.com/optiscaler/OptiScaler/wiki) for possible game issues and HUDfix incompatible games.

## Compilation

### Requirements
* Visual Studio 2022

### Instructions
* Clone this repo with **all of its submodules**.
* Open the OptiScaler.sln with Visual Studio 2022.
* Build the project

## Thanks
* @PotatoOfDoom for CyberFSR2
* @Artur for DLSS Enabler and helping me implement NVNGX api correctly
* @LukeFZ & @Nukem for their great mods and sharing their knowledge 
* @FakeMichau for continous support, testing and feature creep
* @QM for continous testing efforts and helping me to reach games
* @TheRazerMD for continous testing and support
* @Cryio, @krispy, @krisshietala, @Lordubuntu, @scz, @Veeqo for their hard work on (now outdated) [compatibility matrix](https://docs.google.com/spreadsheets/d/1qsvM0uRW-RgAYsOVprDWK2sjCqHnd_1teYAx00_TwUY)
* And the whole DLSS2FSR community for all their support

## Credit
This project uses [FreeType](https://gitlab.freedesktop.org/freetype/freetype) licensed under the [FTL](https://gitlab.freedesktop.org/freetype/freetype/-/blob/master/docs/FTL.TXT)

## Sponsors
<table>
 <tbody>
  <tr>
   <td align="center"><img alt="[SignPath]" src="https://avatars.githubusercontent.com/u/34448643" height="30"/></td>
   <td>Free code signing on Windows provided by <a href="https://signpath.io/">SignPath.io</a>, certificate by <a href="https://signpath.org/">SignPath Foundation</a></td>
  </tr>
 </tbody>
</table>

