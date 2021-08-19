---
title: Oprette en produktmaster
description: Opret en produktmaster for de foruddefinerede varianter.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4140232da68dacde49e236e587110be4f3bbea11fd6c2deec29aaa7ee9e107f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722337"
---
# <a name="create-a-product-master"></a>Oprette en produktmaster

[!include [banner](../../includes/banner.md)]

Opret en produktmaster for de foruddefinerede varianter. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til produktdesigneren.


## <a name="create-a-new-product-master"></a>Opret en ny produktmaster
1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Produktmastere**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Produktnummer**. Tallet skal være entydigt. En nummerserie kan konfigureres for feltet **Produktnummer**. I dette tilfælde skal brugeren ikke at angive en værdi.
4. Skriv en værdi i feltet **Produktnavn**. Indtast et beskrivende produktnavn. Værdien angives som standard til søgenavnet, men dette kan ændres af brugeren.
5. Klik på rullelisten i feltet **Produktdimensionsgruppe** for at åbne opslaget. Produktdimensionsgruppen styrer, hvilke af de 4 produktdimensioner der kan bruges til at oprette produktvarianter. I dette eksempel bruges en gruppe med farve og størrelse.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen. Standarden **Konfigurationsteknologi** er 'Foruddefineret variant'. Den vil blive brugt i dette eksempel.
8. Klik på **OK**.

## <a name="select-product-dimension-groups"></a>Vælg produktdimensionsgrupper
1. Klik på rullelisten i feltet **Farvegruppe** for at åbne opslaget.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på rullelisten i feltet **Størrelsesgruppe** for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
6. Klik op linket i den valgte række på listen.

## <a name="add-dimension-groups"></a>Tilføj dimensionsgrupper
1. Klik på **Produkt** i **handlingsruden**.
2. Klik på **Dimensionsgrupper** for at åbne dialogboksen.
3. Klik på rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget. Lagringsdimensionerne gør det lettere at styre, hvordan varer opbevares og plukkes på lageret. For eksempel kan en lagringsdimension omfatte lokation og lagersted.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget. Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du kan føje til et produkt. For eksempel bruges batchnummeret og serienummeret til at spore lagervarer.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Klik på **OK**.
10. Klik på **Gem**.
11. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]