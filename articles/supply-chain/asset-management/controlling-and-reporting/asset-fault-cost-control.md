---
title: Omkostningsstyring for aktivfejl
description: I dette emne beskrives omkostningsstyring af aktivfejl i Styring af aktiver.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c36fc791fac6cce0433935adb88eb8cdc23003368204a87efc12cf5a419ec9d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752027"
---
# <a name="asset-fault-cost-control"></a>Omkostningsstyring for aktivfejl

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver kan du beregne omkostninger for registreringer af aktivfejl for at få vist en oversigt over faktiske omkostninger sammenlignet med budgetomkostninger. De faktiske omkostninger er baseret på bogførte transaktioner. Datoen er den fejldato, hvor symptomet blev registreret.

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Omkostningsstyring af aktivfejl**.

2. Vælg en økonomisk dimension, der skal inkluderes i beregningen, hvis det er nødvendigt, i dialogboksen **Omkostningsstyring for aktiver**.

4. Vælg "Ja" på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater med en omkostning på nul.

5. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede omkostningsstyringslinjerne skal være i forbindelse med arbejdssteder. 

    Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktivfejls omkostningsstyringslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
    
    Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle aktivfejls omkostningsstyringslinjer på alle de arbejdsstedsniveauer, de er relateret til.

6. Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver, fejldatoer og fejlårsager i oversigtspanelet **Poster, der skal indgå**.

7. Klik på **OK** for at starte beregningen.

8. Klik på **Sammenlæg pr.**-knapper for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte **Sammenlæg pr.**-knapper er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

## <a name="example"></a>Eksempel

I dette eksempel vises beregning af omkostningskontrol for aktivfejl.

- I feltet **Oprindeligt budget** vises budgetomkostninger fra arbejdsordrebudgettet. 
- I feltet **Faktiske omkostninger** vises bogførte omkostninger på arbejdsordrer. 
- I feltet **Bindende omkostning** vises de samlede omkostninger, som dit firma er bundet til i forbindelse med arbejdsordrer.

    ![Figur 1.](media/05-controlling-and-reporting.png)

Se emnet [Fejlstyring](../setup-for-work-orders/fault-management.md), hvis du vil have oplysninger om, hvordan du definerer fejl.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]