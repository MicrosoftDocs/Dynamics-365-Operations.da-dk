---
title: Arbejde med serienummererede varer i POS
description: Dette emne forklarer, hvordan du kan håndtere serienummererede varer i POS-programmet.
author: boycezhu
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1e0d6aa7cd5576578378e70c6ee808833314aff3
ms.sourcegitcommit: 919620b4aca425e6a1248ee12f50a622d2531e58
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290764"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbejde med serienummererede varer i POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Mange detailhandlere sælger produkter, der kræver en seriel kontrol. Disse varer kaldes *serienummererede varer*. Nogle detailhandlere kan få brug for at bevare serienumre til sporingsformål. Andre detailhandlere kan få brug for at registrere serienumre under salgsprocessen mht. service- og garantiformål. Dette emne forklarer, hvordan du kan håndtere serienummererede varer i Microsoft Dynamics 365 Commerce POS-programmet.

## <a name="serial-number-configurations"></a>Serienummerkonfigurationer

En vare betragtes som en serienummereret vare, hvis den er tildelt en sporingsdimensionsgruppe, der er konfigureret til at tillade serienumre. Vælg indstillingen **Aktiv** i Commerce Headquarters på siden **Sporingsdimensionsgrupper** for at aktivere serienumre for lagerprocessen. Hvis du vil aktivere serienumre for salgsprocessen, skal du vælge indstillingen **Aktiv i salgsproces**.

Hvis indstillingen **Blank tilgang tilladt** er slået til på oversigtspanelet **Sporingsdimensioner**, er serienummeret et valgfrit input under lagertilgangsprocessen. Hvis indstillingen er deaktiveret, er et serienummer påkrævet.

Hvis indstillingen **Serienummerkontrol** er aktiveret på oversigtspanelet **Serienumre**, skal serienummeret være entydigt pr. enhed. Det vil sige, at duplikerede serienumre ikke er tilladt.

## <a name="serialized-items-in-the-receiving-process"></a>Serienummererede varer i tilgangsprocessen

Operationen **Indgående lager** i POS-programmet giver brugere mulighed for at udføre følgende opgaver for serienummererede varer:

- Registrér serienumre i forhold til serienummererede varer, når disse varer modtages i butikken via en indkøbsordre.
- Valider serienumre, der er registreret på forhånd, i forhold til serienummererede varer, når disse varer modtages i butikken via en indkøbsordre eller flytteordre.

> [!NOTE]
> Hvis du vil bruge operationen **Indgående lager** til at registrere eller validere en serienummereret vare, skal varen tildeles en sporingsdimensionsgruppe, der er konfigureret til at tillade serienumre for indstillingen **Aktiv** og ikke for indstillingen **Aktiv i salgsproces**.

Du kan gå i gang med tilgangsprocessen ved at starte med at scanne varens stregkode eller ved at angive vare-id'et i visningen **Modtag nu** i operationen **Indgående lager**. Du kan også starte i visningen **Fuld ordreliste** ved manuelt at vælge varen.

Hvis den vare, der vælges eller modtages, er en serienummereret vare, indeholder ruden **Detaljer** for varen linket **Administrer serienummer**, der åbner siden **Administration af serienumre**. Du kan også åbne siden **Administration af serienumre** ved at vælge **Serienummer** på applinjen i visningen med ordredetaljer eller ved at vælge **Administrer serienummer** i den dialogboks, der vises under tilgangsprocessen. Siden **Administration af serienumre** viser alle åbne serienummerlinjer, der afventer registrering eller validering. Der kan være to faner på denne side: en for den aktuelle vare og en for alle de serienummererede varer i ordren.

Feltet **Status** på siden **Administration af serienumre** indeholder oplysninger om den aktuelle status for hvert serienummer:

- **Ikke registreret** – serienummeret er ikke leveret, eller det allerede registrerede serienummer er endnu ikke valideret.
- **Registreret** – serienummeret er registreret og gemt lokalt i butikkens kanaldatabase, eller det allerede registrerede serienummer er blevet valideret. Der sendes kun serienumre, der har status som **Registreret**, til Commerce Headquarters, når du er færdig med tilgangsprocessen.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrere serienumre i forhold til serienummererede varer

I forbindelse med en indkøbsordre indeholder en dialogboks, der vises under tilgangsprocessen for en serienummereret vare, indstillingen **Administrer serienummer**. Du kan vælge denne indstilling for at åbne siden **Administration af serienumre** og begynde at registrere serienumre. Du kan også springe dette trin over under tilgangsprocessen og angive dette input senere, før tilgangen bogføres.

Fanen for den aktuelle vare vises som standard. Alle serienummerlinjer har en tom serienummerværdi og statussen **Ikke registreret**. Du kan scanne serienummerstregkoder, eller du kan vælge **Serienummer** på applinjen for at angive serienumre i dialogboksen flere gange. De serienumre, du angiver, vises på listen, og statussen på serienummerlinjerne ændres til **Registreret**. Det maksimale antal serienumre, du kan registrere på listen, er lig med tilgangsantallet. Hvis du laver en fejl, kan du vælge **Rediger** eller **Ryd** i ruden **Detaljer** for at ændre de angivne serienumre.

Du kan også registrere serienumre på fanen **Alle serienummererede varer** på siden **Administration af serienumre**. På listen skal du vælge den vare, du vil registrere serienumre for.

Under serienummerregistreringen på denne side udføres der en duplikeringsvalidering. Hvis du forsøger at angive et duplikeret serienummer for en vare, som serienummerkontrolelementet er aktiveret for, vises der en fejlmeddelelse, og du skal angive et andet nummer.

### <a name="validate-serial-numbers-on-serialized-items"></a>Validere serienumre for serienummererede varer

I forbindelse med en flytteordre skal den udgående side forudregistrere serienumre for de serienummerede varer under forsendelsesprocessen. For en indkøbsordre kan leverandøren levere serienummeroplysninger via en Advance Shipping Notice (ASN), og du kan forudregistrere numrene på de varer, der skal sendes. I begge tilfælde kendes serienumrene før tilgangen. På den indgående side skal du derfor blot validere, at du har modtaget det, du skulle modtage.

Hvis du vil validere serienumre, kan du åbne siden **Administration af serienumre** under tilgangsprocessen eller når som helst, før tilgangen bogføres. For hver serienummereret vare, der forudregistrerede serienumre, angives alle serienumre automatisk til den indledende status **Ikke registreret** på denne side. Hvis du vil validere serienumre, kan du scanne eller angive dem. Når serienumre angives, validerer programmet, om de stemmer overens med de forudregistrerede serienumre. Hvis de stemmer overens, ændres deres status til **Registreret**. Ellers får du en fejlmeddelelse. Det maksimale antal serienumre, du kan validere på listen, er lig med tilgangsantallet.

Du kan også validere serienumre på fanen **Alle serienummererede varer** på siden **Administration af serienumre**. På listen skal du vælge den vare, du vil validere serienumre for.

## <a name="additional-resources"></a>Yderligere ressourcer

[Indgående lagerhandling i POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
