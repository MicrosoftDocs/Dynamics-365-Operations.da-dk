---
title: Aktivmålinger
description: Dette emne beskriver, hvordan du opretter typer af aktivmålinger i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 41bedaaace09f632ca7506f504c3086a1dabf193
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217143"
---
# <a name="counters"></a>Tællere

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du opretter tællertyper i Styring af aktiver. Tællertyper bruges til at foretage tællerregistreringer på aktiver, for eksempel antal produktionstimer eller antal, der produceres på aktivet. Aktivtyper er relateret til tællertyperne. Det betyder, at en tæller kun kan bruges på et aktiv, hvis tælleren er konfigureret på den aktivtype, der bruges på aktivet.

Før du kan foretage tællerregistreringer på aktiver, skal du først oprette de tællertyper, du vil bruge, i **Tællere**. Derefter kan du oprette tællerregistreringer for aktiver i **Tællere**. 

Tællere kan anvendes på vedligeholdelsesplaner. En vedligeholdelsesplanlinje kan være af typen "Tæller", for eksempel vedrørende antallet af produktionstimer eller producerede mængder. 

En tællerregistrering kan opdateres manuelt eller automatisk baseret på produktionstimer eller producerede antal. En tæller kan konfigureres til at bruge en af tre opdateringsmetoder (valgt i feltet **Opdater** i **Tællere**):
  
- Manuel – du skal registrere tællerværdier manuelt.  
- Produktionstimer – tælleren opdateres automatisk baseret på antallet af produktionstimer.  
- Produktionsantal – tælleren opdateres automatisk baseret på det producerede antal.  

>[!NOTE]
>Hvis der bruges producerede mængder, medtages *alle* registrerede varer i tællerregistreringen, både antal gode og antal fejl. Det er altid muligt at foretage manuelle tællerregistreringer, hvis det er nødvendigt.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Oprette tællertyper for registreringer af aktivtæller

1. Vælg **Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere**.
2. Vælg **Ny** for at oprette en ny tællertype.
3. Indsæt et id i feltet **Tæller** og et tællernavn i feltet **Navn**.
4. I oversigtspanelet **Generelt** skal du vælge en tællerenhed i feltet **Enhed**.
5. Vælg den opdateringsmetode, der skal bruges til tælleren, i feltet **Opdater**.
6. Vælg "Ja" på knappen **Arv tællerværdier**, hvis underordnede aktiver i en aktivstruktur automatisk skal arve de tællerregistreringer, der er foretaget på det overordnede aktiv.
7. I feltet **Samlet aggregat** skal du vælge den opsummeringsmetode, der skal bruges til en tæller ved hjælp af denne tællertype. "Sum" er standardvalget, der bruges til løbende at lægge registrerede værdier til den samlede værdi. "Gennemsnit" kan bruges, hvis en tæller er sat op til at overvåge en tærskel, for eksempel med hensyn til temperatur, vibrationer eller slitage på et aktiv. 
8. I feltet **Afvigelse over** skal du indsætte det øverste niveau i procent for validering, hvis manuelle tællerregistreringer er inden for et forventet interval. Valideringen er baseret på en lineær stigning i eksisterende tællerregistreringer.
9. I feltet **Afvigelse under** skal du indsætte det nederste niveau i procent for validering, hvis manuelle tællerregistreringer er inden for et forventet interval. Valideringen er baseret på et lineært fald i eksisterende tællerregistreringer.
10. I feltet **Type** skal du vælge den typemeddelelse (oplysninger, advarsel, fejl), der skal vises, hvis afvigelser uden for det definerede interval indtræffer, når du foretager manuelle tællerregistreringer.
11. Brug oversigtspanelet **Aktivtyper** til at tilføje de aktivtyper, der skal bruge tælleren.
12. I oversigtspanelet **Relaterede aktivtællere** skal du tilføje den tæller, der skal opdateres automatisk, når denne tæller opdateres.


>[!NOTE]
>En relateret tæller opdateres kun automatisk, hvis den relaterede tæller har den aktivtype, som den er relateret til, i tælleropsætningen. For eksempel: Du konfigurerer en tæller for "Produktionstimer" og tilføjer aktivtypen "Lastbilmotor". Når denne tæller opdateres, opdateres en relateret tæller "Olie" også med de samme tællerværdier. Opsætningen i **Tællere** omfatter opsætningen på "Timer". På tælleren "Olie" bør aktivtypen "Lastbilmotor" også føjes til oversigtspanelet **Aktivtyper** for at sikre tællerrelationen. Se skærmbilleder nedenfor med et eksempel på opsætningen af Timer og Olie som tællere.

Når aktivtyper føjes til en tællertype i **Tællere**, føjes denne tæller automatisk til aktivtyperne i oversigtspanelet **Tællere** i [Aktivtyper](../setup-for-objects/object-types.md).

![Figur 1](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]