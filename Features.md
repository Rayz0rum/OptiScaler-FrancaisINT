## Caractéristiques
* Prise en charge de plusieurs systèmes de mise à l'échelle (XeSS, FSR 2.1.2, FSR 2.2.1, FSR 3.1 et DLSS)
* Prise en charge expérimentale de la génération d'image (OptiFG par FSR) à partir de la version 0.7.0
* Prise en charge du DLSS 3.7 et versions ultérieures (consultez les [instructions d'installations](#intaller-en-tant-que-non-nvngx))
* Prise en charge du DLSS-D (Reconstruction de faisceau) sur les cartes graphiques Nvidia (Prise en charge du changement de préréglages et des améliorations apportées par OptiScaler)
* Permets la modification à la volée des préréglages du DLSS et du DLSS-D
* Prise en charge du XeSS v1.3.x's en Ultra Performance et en mode Résolution native (**En utilisant les anciens ratios du XeSS 1.3.x, pas les nouveaux**) 
* Un [menu en jeu](https://github.com/optiscaler/OptiScaler/blob/master/Config.md) est disponible pour modifier et sauvegarder les paramètres à la volée (Raccourci clavier étant **INSERT**)
* Intégration complète avec [DLSS Enabler](https://www.nexusmods.com/site/mods/757) pour une compatibilité avec la génération d'image DLSS
* Prise en charge du **RCAS** avec la (Netteté adaptative au mouvement) **MAS** pour tous les algorithmes de mise à l'échelle qui supporte le Dx12 ou Dx11 (temporels ou spatiaux)
* Une option **Mise à l'échelle de la sortie** est disponible (0.5x jusqu'à 3.0x) pour les moteurs de rendue baser sur le DX11 et le DX12
* Prise en charge de la falsification du DXGI (lorqu'utilisé en tant que `dxgi.dll`) en tant que cartes graphiques Nvidia (avec détection XeSS pour permettre l'utilisation du XMX sur les cartes graphiques Arc de Intel)
* Prise en charge de la falsification de Vulkan (lorsqu'activé depuis le `nvngi.ini`) en tant que cartes graphiques Nvidia (ne fonctionne pas sur Doom Eternal)
* Prise en charge du chargement d'un fichier `nvapi64.dll` distinct (lorsqu'utilisé en mode non nvngx)
* Prise en charge du chargement d'un fichier `nvngx_dlss.dll` distinct (lorsqu'utilisé en mode non nvngx)
* Prise en charge de redéfinition des ratios de mise à l'échelle
* Prise en charge la redéfinition de la plage DRS
* Correction automatique du problème de [lumières multicolores](https://github.com/optiscaler/OptiScaler/blob/master/Config.md#resource-barriers-dx12-only) qui affecte les cartes graphiques AMD lorsque couplé avec le moteur de jeu Unreal Engine.
* Correction automatique du problème d'informations manquantes au sujet des [données de textures d'exposition](https://github.com/optiscaler/OptiScaler/blob/master/Config.md#init-flags)
* Possibilité de modifier les valeurs par défaut du [biais de niveau de détail](https://github.com/optiscaler/OptiScaler/blob/master/Config.md#mipmap-lod-bias-override-dx12-only) du jeu
* Intégration du [Fakenvapi](https://github.com/FakeMichau/fakenvapi), ce qui permet l'accrochage de Reflex et l'injection d'Anti-Lag 2 ou de LatencyFlex (LFX)
* Prise en charge de l'intégration Nukem de l'algorithme de génération d'image FSR [dlssg-to-fsr3](https://github.com/Nukem9/dlssg-to-fsr3) (depuis la version 0.7.7)  
 
**Pour contourner les exigences de vérifications de signature du DLSS 3.7, OptiScaler utilise une méthode développée par **Artur** (créateur de [DLSS Enabler](https://www.nexusmods.com/site/mods/757?tab=description)).**
