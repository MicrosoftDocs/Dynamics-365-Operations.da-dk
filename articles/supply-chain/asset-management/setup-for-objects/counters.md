---
title: Aktivmålinger
description: Dette emne beskriver, hvordan du opretter typer af aktivmålinger i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783161"
---
# <a name="asset-measures"></a>Aktivmålinger

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emne beskriver, hvordan du opretter typer af aktivmålinger i Styring af aktiver. Aktivmålingstyper bruges til at foretage målingsregistreringer på aktiver, for eksempel med hensyn til antal produktionstimer eller antal, der produceres på aktivet. Aktivtyper er relateret til aktivmålingstyperne. Det betyder, at en aktivmåling kun kan bruges på et aktiv, hvis aktivaktivmålingen er konfigureret på den aktivtype, der bruges på aktivet.

Før du kan foretage målingsregistreringer på aktiver, skal du først oprette de aktivmålingstyper, du vil bruge i **Tællere**. Derefter kan du oprette målingsregistreringer for aktiver i **Aktivmålinger**. 

Aktivmålinger kan anvendes på vedligeholdelsesplaner. En vedligeholdelsesplanlinje kan være af typen "Tæller", for eksempel vedrørende antallet af produktionstimer eller producerede mængder. 

En registrering af aktivmåling kan opdateres manuelt eller automatisk baseret på produktionstimer eller producerede antal. En aktivmåling kan konfigureres til at bruge en af tre opdateringsmetoder (valgt i feltet **Opdater** i **Tællere**):
  
- Manuel – du skal registrere værdier for aktivmåling manuelt.  
- Produktionstimer – tælleren opdateres automatisk baseret på antallet af produktionstimer.  
- Produktionsantal – tælleren opdateres automatisk baseret på det producerede antal.  

>[!NOTE]
>Hvis der bruges producerede mængder, medtages *alle* registrerede varer i målingsregistreringen, både god mængde fejlmængde. Det er altid muligt at foretage manuelle registreringer af aktivmåling, hvis det er nødvendigt.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Oprette tællertyper for registreringer af aktivtæller

1. Vælg **Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere**.
2. Vælg **Ny** for at oprette en ny type af aktivmåling.
3. Indsæt et id i feltet **Tæller** og et tællernavn i feltet **Navn**.
4. I oversigtspanelet **Generelt** skal du vælge en måleenhed i feltet **Enhed**.
5. Vælg den opdateringsmetode, der skal bruges til aktivmålingen, i feltet **Opdater**.
6. Vælg "Ja" på knappen **Arv tællerværdier**, hvis underordnede aktiver i en aktivstruktur automatisk skal arve de registreringer af aktivmåling, der er foretaget på det overordnede aktiv.
7. I feltet **Samlet aggregat** skal du vælge den opsummeringsmetode, der skal bruges til en aktivmåling ved hjælp af denne aktivmålingstype. "Sum" er standardvalget, der bruges til løbende at lægge registrerede værdier til den samlede værdi. "Gennemsnit" kan bruges, hvis en aktivmåling er sat op til at overvåge en tærskel, for eksempel med hensyn til temperatur, vibrationer eller slitage på et aktiv. 
8. I feltet **Afvigelse over** skal du indsætte det øverste niveau i procent for validering, hvis manuelle registreringer af aktivmåling er inden for et forventet interval. Valideringen er baseret på en lineær stigning i eksisterende registreringer af aktivmåling.
9. I feltet **Afvigelse under** skal du indsætte det nederste niveau i procent for validering, hvis manuelle registreringer af aktivmåling er inden for et forventet interval. Valideringen er baseret på et lineært fald i eksisterende registreringer af aktivmåling.
10. I feltet **Type** skal du vælge den typemeddelelse (oplysninger, advarsel, fejl), der skal vises, hvis afvigelser uden for det definerede interval indtræffer, når du foretager manuelle registreringer af aktivmåling.
11. Brug oversigtspanelet **Aktivtyper** til at tilføje de aktivtyper, der skal bruge aktivmålingen.
12. I oversigtspanelet **Relaterede aktivmålinger** skal du tilføje de aktivmålinger, der skal opdateres automatisk, når denne aktivmåling opdateres.


>[!NOTE]
>En relateret aktivmåling opdateres kun automatisk, hvis den relaterede aktivmåling har den aktivtype, som den er relateret til, i opsætningen af aktivmåling. For eksempel: Du konfigurerer en aktivmåling for "Produktionstimer" og tilføjer aktivtypen "Lastbilmotor". Når denne aktivmåling opdateres, opdateres en relateret tæller "Olie" også med de samme værdier for aktivmåling. Opsætningen i **Tællere** omfatter opsætningen på "Timer". På aktivmålingen "Olie" bør aktivtypen "Lastbilmotor" også føjes til oversigtspanelet **Aktivtyper** for at sikre aktivmålingens relation. Se skærmbilleder nedenfor med et eksempel på opsætningen af Timer og Olie som aktivmålinger.

Når aktivtyper føjes til en aktivmålingstype i **Tællere**, føjes denne aktivmåling automatisk til aktivtyperne i oversigtspanelet **Tællere** i [Aktivtyper](../setup-for-objects/object-types.md).

![Figur 1](media/071-setup-for-objects.png)


