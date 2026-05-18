# Analyse de la clef jaune

## 1. Analyse des fichiers

Pour avoir une vue d'ensemble des fichiers :

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

### a. FsTxKtmLog.blf

Un fichier de 64K.

```
god@mode:FsTx/95F62703B343F111A92A005056975458/FsTxLogs$ file FsTxKtmLog.blf
FsTxKtmLog.blf: Targa image data - Map 33355 x 50764 x 1 ""
```

| TGA or TARGA format is a format for describing bitmap images, it is capable of representing bitmaps ranging from black and white, indexed colour, and RGB colour, the format also supports various compression methods. (http://www.paulbourke.net/dataformats/tga/)

Le fichier, comme son nom l'indique semble contenir des références à d'autres fichiers (lui-même et les 2 containers "FsTxKtmLogContainer00000000000000000001" et "FsTxKtmLogContainer00000000000000000002") :

![HxD FsTxKtmLog.blf](/images/FsTxKtmLog.blf_1.png)

### b. FsTxKtmLogContainer00000000000000000001

Un fichier de 512K.

```
god@mode:FsTx/95F62703B343F111A92A005056975458/FsTxLogs$ file FsTxKtmLogContainer00000000000000000001
FsTxKtmLogContainer00000000000000000001: Targa image data - Map 65536 x 65536 x 1 ""
```

Un fichier complètement vide avec une signature dans son header qui fait penser à file qu'il s'agit également d'un Targa.

![HxD FsTxKtmLogContainer00000000000000000001](/images/FsTxKtmLogContainer00000000000000000001_1.png)