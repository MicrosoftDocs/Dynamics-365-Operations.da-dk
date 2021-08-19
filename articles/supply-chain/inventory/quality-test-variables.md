---
title: Testvariabler for kvalitetsstyring
description: Dette emne beskriver, hvordan du opretter testvariabler, som kan bruges til kvalitative test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8233864d6b668c8462a59a425e66b1aec38576633922062573d8605c9c73d2a8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734205"
---
# <a name="quality-management-test-variables"></a>Testvariabler for kvalitetsstyring

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter testvariabler, som kan bruges til kvalitative test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

For hver kvalitativ test, der er defineret på siden **Test**, skal du definere en testvariabel og dens mulige udfald (resultater). (For kvalitative test er feltet **Type** på siden **Test** angivet til *Indstilling*.)

Du kan bruge siden **Testvariabler** til at konfigurere, redigere og få vist de mulige udfald for en testvariabel, der er knyttet til en kvalitativ test. For hvert udfald tildeler du udfaldsstatussen *Bestået* eller *Mislykket* for at angive, om testen er bestået eller mislykket, når udfaldet er valgt som et testresultat. Du kan bruge siden **Testgrupper** til at tildele en testvariabel og et standardudfald for den til en individuel kvalitativ test.

For hver testvariabel anbefales det, at du definerer mindst to udfald: En med udfaldsstatussen *Bestået*, og en, der har udfaldsstatussen *Mislykket*. Der er ingen grænse for det samlede antal variabler eller udfald, der kan defineres. Desuden kan flere test bruge samme testvariabler til at registrere resultater.

## <a name="examples-of-test-variables"></a>Eksempler på testvariabler

### <a name="example-1"></a>Eksempel 1

En produktionsvirksomhed udfører to test af producerede materialer. I én test knyttes pH-niveauet til en farvestribe. Acceptable pH-niveauer har lysere farver, og uacceptable pH-niveauer har mørkere farver. I en anden test udføres flere visuelle inspektioner, og kvalitetsmedarbejdere bruger deres vurderingsevne til at afgøre, om varen er bestået eller mislykket i den visuelle inspektion.

### <a name="example-2"></a>Eksempel 2

En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt. Denne inspektionstest har adskillige variabler. En af variablerne er smag, og de mulige udfald er "god" og "dårlig". Farve er en anden variabel, og de mulige udfald er "for mørk", "for lys" og "korrekt".

## <a name="create-a-test-variable"></a>Oprette en testvariabel

Benyt denne fremgangsmåde for at oprette en testvariabel.

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Testvariabler**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Variabel** – Angiv et entydigt id eller navn til variablen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af variablen.

1. Mens den nye række stadig er markeret, skal du vælge **Udfald** i handlingsruden.
1. På siden **Udfald for testvariabler** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Udfald** – Angiv et entydigt id eller navn til udfaldet.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af udfaldet.
    - **Udfaldsstatus** – Vælg *Bestået* eller *Mislykket* for at angive, om testen er bestået eller mislykket, når udfaldet er valgt som et testresultat.

1. Gentag det foregående trin for hvert ekstra udfald. Sørg for, at mindst ét udfald har udfaldsstatussen *Bestået*, og at mindst ét har udfaldsstatussen *Mislykket*.
1. Luk siderne.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md)
- [Test for kvalitetsstyring](quality-tests.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
