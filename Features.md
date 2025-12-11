## Caractéristiques
* Prise en charge de plusieurs systèmes de mise à l'échelle (XeSS, FSR 2.1.2, FSR 2.2.1, FSR 3.1 et DLSS)
* Prise en charge expérimentale de la génération d'image (OptiFG par FSR) à partir de la version 0.7.0
* Prise en charge du DLSS 3.7 et versions ultérieures (consultez les [instructions d'installations](#intaller-en-tant-que-non-nvngx))
* Prise en charge du DLSS-D (Reconstruction de faisceau) sur les cartes graphique Nvidia (Prise en charge du changement de préréglages et des améliorations apportés par OptiScaler)
* Permet la modifications à la volée des préréglages du DLSS et du DLSS-D
* Prise en charge du XeSS v1.3.x's en Ultra Performance et en mode Résolution native (**En utilisant les anciens ratios du XeSS 1.3.x scaling ratios, pas les nouveaux**) 
* Un [menu en jeu](https://github.com/optiscaler/OptiScaler/blob/master/Config.md) est disponible pour modifier et sauvegarder les paramètres à la volée (Raccourci clavier étant **INSERT**)
* Intégration complète avec [DLSS Enabler](https://www.nexusmods.com/site/mods/757) pour une compatibilité avec la génération d'image DLSS
* Prise en charge du **RCAS** avec la (Netteté adaptative au mouvement) **MAS** pour tous les algorithmes de mise à l'échelle qui supporte le Dx12 ou Dx11 (temporels ou spatiaux)
* Une option **Mise à l'échelle de la sortie** est disponible (0.5x jusqu'à 3.0x) pour les moteurs de rendu basé sur le DX11 et le DX12
* Prise en charge de la falsification du DXGI (lorqu'utilisé en tant que `dxgi.dll`) en tant que cartes graphique Nvidia (avec détéction XeSS pour permettre l'utilisation du XMX sur les cartes graphique Arc de Intel)
* Prise en charge de la falsification de Vulkan (lorsqu'activé depuis le `nvngi.ini`) en tant que cartes graphique Nvidia (ne fonctionne pas sur Doom Eternal)
* Prise en charge du chargement du fichier `nvapi64.dll` spécifique (lorsqu'untilisé en mode non-nvngx)
* Prise en charge du chargement du fichier `nvngx_dlss.dll` spécifique (lorsqu'untilisé en mode non-nvngx)
* Prise en charge de redéfinition des ratios de mise à l'échelle
* Prise en charge la redéfinition de la plage DRS
* Autofixes for [colored lights](https://github.com/optiscaler/OptiScaler/blob/master/Config.md#resource-barriers-dx12-only) on Unreal Engine & AMD graphics cards 
* Autofixes for [missing exposure texture](https://github.com/optiscaler/OptiScaler/blob/master/Config.md#init-flags) information
* Ability to modify [Mipmap Lod Bias](https://github.com/optiscaler/OptiScaler/blob/master/Config.md#mipmap-lod-bias-override-dx12-only) game value
* Supports [Fakenvapi](https://github.com/FakeMichau/fakenvapi) integration which enables Reflex hooking and injecting Anti-Lag 2 or LatencyFlex (LFX)
* Supports Nukem's FSR FG mod [dlssg-to-fsr3](https://github.com/Nukem9/dlssg-to-fsr3) (since version 0.7.7)  
 
**To overcome DLSS 3.7's signature check requirements, OptiScaler uses a method developed by **Artur** (creator of [DLSS Enabler](https://www.nexusmods.com/site/mods/757?tab=description)).**
