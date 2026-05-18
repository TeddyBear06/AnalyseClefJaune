# Analyse de la clef jaune

## Analyse des fichiers

Pour avoir une vue d'ensemble des fichier :

```
FsTx/
└── 95F62703B343F111A92A005056975458
    ├── FsTxLogs
    │   ├── FsTxKtmLog.blf
    │   ├── FsTxKtmLogContainer00000000000000000001
    │   ├── FsTxKtmLogContainer00000000000000000002
    │   ├── FsTxLog.blf
    │   ├── FsTxLogContainer00000000000000000001
    │   └── FsTxLogContainer00000000000000000002
    └── FsTxTemp
        └── 98F62703B343F111A92A005056975458
```

### FsTxKtmLog.blf

```
god@mode:FsTx/95F62703B343F111A92A005056975458/FsTxLogs$ file FsTxKtmLog.blf
FsTxKtmLog.blf: Targa image data - Map 33355 x 50764 x 1 ""
```

| TGA or TARGA format is a format for describing bitmap images, it is capable of representing bitmaps ranging from black and white, indexed colour, and RGB colour, the format also supports various compression methods. (http://www.paulbourke.net/dataformats/tga/)

Le fichier, comme son nom l'indique semble contenir des références à d'autres fichiers (lui-même et les 2 containers "FsTxKtmLogContainer00000000000000000001" et "FsTxKtmLogContainer00000000000000000002") :

![HxD FsTxKtmLog.blf](/images/FsTxKtmLog.blf_1.png)