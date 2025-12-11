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
**2.** [**Comment ça fonctionne ?**](#comment-ça-fonctionne-)  
**3.** [**APIs et upscalers pris en charge**](#quelles-api-et-moteurs-de-mise-à-léchelle-sont-pris-en-charge-)  
**4.** [**Installation**](#installation)  
**5.** [**Problèmes connus**](#problèmes-connus)  
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

## Comment ça fonctionne ?
* OptiScaler agit comme un intergiciel : Il intercepte les appels aux algorithmes de mise à l’échelle effectués par le jeu (**Entrées**) et les redirige vers le moteur de la mise à l’échelle sélectionné (**Sortie**), permettant ainsi de remplacer une technologie par une autre. **Entrées -> OptiScaler -> Sorties**  
* Pour l’expliquer plus simplement, **l’Entrée** correspond à l’algorithme de mise à l’échelle choisi dans les paramètres du jeu, et **la Sortie** est celui sélectionné dans la superposition Opti.

> [!NOTE]
> * Appuyer sur **`Insérer`** ouvre la **surcouche Opti Overlay** en jeu avec toutes les options (la valeur de `ShortcutKey=` peut être modifiée dans le fichier de configuration).
> * Appuyer sur **`Page précédente`** affiche la surcouche des statistiques de performance en haut à gauche, et vous pouvez basculer entre différents modes avec **`Page suivante`** (raccourcis configurables dans la superposition).
> * Si la superposition Opti se ferme instantanément après plusieurs tentatives avec **`Insérer`**, essayez **`Alt + Insérer`** ([solution signalée](https://github.com/optiscaler/OptiScaler/issues/484) pour les dispositions de clavier alternatives).

![inputs_and_outputs](https://raw.githubusercontent.com/Rayz0rum/OptiScaler-FrancaisINT/refs/heads/v0.9/images/entr%C3%A9es-sorties.png)

## Quelles API et moteurs de mise à l’échelle sont pris en charge ?
Actuellement, **OptiScaler** peut être utilisé avec DirectX 11, DirectX 12 et Vulkan, mais chaque API prend en charge un ensemble différent de moteurs de mise à l’échelle.  
[**OptiFG**](#optifg-powered-by-fsr3-fg--hudfix-experimental-hud-ghosting-fix) ne prend actuellement en charge que **DX12** et est expliqué dans un paragraphe séparé.

#### Pour DirectX 12
- XeSS (Par défaut)  
- FSR 2.1.2, 2.2.1  
- FSR 3.X (et FSR 2.3.X)  
- FSR 4.0.X (via la mise à jour FSR 3.X, _RDNA4 seulement_)  
- DLSS  

#### Pour DirectX 11
- FSR 2.2.1 (Par défaut, DX11 natif)  
- FSR 3.1.2 (port non officiel vers DX11 natif)  
- DLSS (DX11 natif)  
- XeSS 2.X (DX11 natif, _Intel ARC seulement_)  
- XeSS, FSR 2.1.2, 2.2.1, FSR 3.X avec DX12 (_via D3D11on12_)$`^1`$  
- FSR 4.0.X (via FSR 3.X avec DX12 update, _RDNA4 seulement_)

> [!NOTE]
> <details>
>  <summary><b>Déplier pour [1]</b></summary>
>
> _**[1]** Ces implémentations utilisent un dispositif DirectX12 en arrière-plan afin de pouvoir utiliser des upscalers réservés à DX12. Cette méthode entraîne une pénalité de performances pouvant atteindre environ 10 %, mais elle permet d’accéder à beaucoup plus d’options de mise à l'échelle. De plus, l’implémentation native DX11 de FSR 2.2.1 est un rétroportage du moteur Unity et comporte ses propres problèmes, dont certains ont été corrigés par OptiScaler._
> </details>

#### OptiFG (alimenté par la génération d'images FSR3) + corr. ATH (correction expérimentale du ghosting de l'affichage tête haute)  
**OptiFG** a été ajouté avec la **v0.7** et est **seulement pris en charge sur DX12**.  
C’est une méthode **expérimentale** pour ajouter FSR3 FG à des jeux sans génération de frames native, ou peut aussi être utilisée en dernier recours si la génération d'images native ne fonctionne pas correctement.

Pour plus d’informations sur OptiFG et son utilisation, consultez la page du guide - [OptiFG](https://github.com/optiscaler/OptiScaler/wiki/OptiFG).


## Installation
> [!CAUTION]
> _**Attention** : **Ne pas utiliser ce mod avec des jeux en ligne.** Il peut déclencher les logiciels anti-triche et entraîner des bannissements !_

> [!IMPORTANT]
> **Pour les étapes d’installation, veuillez consulter le [**Guide**](https://github.com/optiscaler/OptiScaler/wiki)**

## Configuration
Veuillez consulter [ce document](Config.md) pour les paramètres de configuration et leurs explications. Si votre carte graphique n’est pas une Nvidia, consultez les [options de contournement GPU](Spoofing.md) *(sera mis à jour)*.

## Problèmes connus
Si vous ne pouvez pas ouvrir la superposition du menu en jeu :  
1. Vérifiez que vous avez activé DLSS2+, XeSS ou FSR2+ depuis les options du jeu et que vous êtes bien en jeu, et non dans les paramètres du jeu.  
2. Si vous utilisez l’installation classique, essayez d’ouvrir le menu pendant que vous êtes en jeu (pendant le rendu 3D).  
3. Si vous utilisez **RTSS** (MSI Afterburner, CapFrameX), activez ce réglage dans RTSS et/ou essayez de mettre à jour RTSS. **Lors de l’utilisation d’OptiFG, désactivez RTSS pour une compatibilité optimale**.
 
 ![image](https://github.com/optiscaler/OptiScaler/assets/35529761/8afb24ac-662a-40ae-a97c-837369e03fc7)

Veuillez consulter [ce document](Issues.md) pour la liste complète des problèmes connus et leurs solutions possibles.  
Consultez également le [guide communautaire](https://github.com/optiscaler/OptiScaler/wiki) pour les éventuels problèmes liés aux jeux et les incompatibilités avec HUDfix.

## Compilation

### Prérequis
* Visual Studio 2022

### Instructions
* Clonez ce dépôt **avec tous ses sous-modules**.  
* Ouvrez le fichier OptiScaler.sln avec Visual Studio 2022.  
* Compilez le projet.

## Remerciements
* @PotatoOfDoom pour CyberFSR2  
* @Artur pour DLSS Enabler et pour m’avoir aidé à implémenter correctement l’API NVNGX  
* @LukeFZ & @Nukem pour leurs excellents mods et le partage de leur savoir  
* @FakeMichau pour son soutien continu, les tests et l’ajout de nouvelles fonctionnalités  
* @QM pour ses efforts continus de test et pour m’avoir aidé à atteindre les jeux  
* @TheRazerMD pour ses tests et son soutien continus  
* @Cryio, @krispy, @krisshietala, @Lordubuntu, @scz, @Veeqo pour leur travail acharné sur l’[ancien tableau de compatibilité](https://docs.google.com/spreadsheets/d/1qsvM0uRW-RgAYsOVprDWK2sjCqHnd_1teYAx00_TwUY)  
* Et toute la communauté DLSS2FSR pour leur soutien  
* @Rayz0rum et @Dagherbou pour la traduction française internationale inofficielle d’OptiScaler

## Crédits
Ce projet utilise [FreeType](https://gitlab.freedesktop.org/freetype/freetype) sous licence [FTL](https://gitlab.freedesktop.org/freetype/freetype/-/blob/master/docs/FTL.TXT)

## Sponsors
<table>
 <tbody>
  <tr>
   <td align="center"><img alt="[SignPath]" src="https://avatars.githubusercontent.com/u/34448643" height="30"/></td>
   <td>Signature de code gratuite sur Windows fournie par <a href="https://signpath.io/">SignPath.io</a>, certificat délivré par la <a href="https://signpath.org/">fondation SignPath</a></td>
  </tr>
 </tbody>
</table>

