---
title: Arbejde med serienummerede varer
description: Dette emne forklarer, hvordan du kan registrere serienumre på følgesedler eller fakturaer under salgsprocessen. Denne funktionalitet er nyttig, hvis en virksomhed vil indsamle serienumre til service- og garantiformål men ikke behøver at gemme serienumre på lageret fra tilgang til afgang.
author: omulvad
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable, InventSerial
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50d591db4b71aad06c76242123cd1a4f9e866acb47df616c4ae3911ab52275bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713542"
---
# <a name="working-with-serialized-items"></a>Arbejde med serienummerede varer

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan registrere serienumre på følgesedler eller fakturaer under salgsprocessen. Denne funktionalitet er nyttig, hvis en virksomhed vil indsamle serienumre til service- og garantiformål men ikke behøver at gemme serienumre på lageret fra tilgang til afgang.

Mange virksomheder vil blot indsamle serienumre for service- og garantiformål og behøver ikke at gemme serienumre på lageret fra tilgang til afgang. I disse scenarier kan du registrere serienumre på følgesedler eller fakturaer, når produkterne sælges. Hvis produkterne på et senere tidspunkt returneres, kan du spore et produkt til en faktura for at finde ud af, om du har solgt produktet, og om servicen eller garantiforpligtelser er gældende.

Du skal aktivere serienumre for salgsprocessen ved at vælge indstillingen **Aktiv i salgsproces** på siden **Sporingsdimensionsgrupper**. Følgende hændelser forekommer derefter i Supply Chain Management:
-   I oversigtspanelet **Serienumre** er indstillingen **Serienummerkontrol** valgt. Hvis denne indstilling er markeret, skal du registrere et serienummer for hver vare på følgesedlen eller fakturaen.
-   Alle markeringer i sporingsdimensionsgruppen for serienumre fjernes, undtagen indstillingen **Blank afgang tilladt**. Du kan markere indstillingen **Blank afgang tilladt** for at tilsidesætte kontrollen af serienumre og tillade, at produkterne emballeres og faktureres uden registrering af serienumre.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Hvornår registrerer jeg serienumre under salgsprocessen?
Du kan registrere serienumre på enten følgesedlen for en salgsordre eller på fakturaen. Når du forbereder en faktura til en serienummereret vare, der er leveret sammen med en følgeseddel, kan du vælge, hvilken af serienumrene på følgesedlen der skal faktureres. Antallet af registrerede serienumre må ikke overstige det antal varer, der blev sendt. Hvis du opretter en delfaktura, kan du vælge færre serienummererede varer, end der blev registreret på følgesedlen. Når du udskriver en følgeseddel eller en faktura, medtages de serienumre, der blev registreret.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Kan jeg angive serienumre ved at scanne dem, eller er det nødvendigt at indtaste dem?
Du kan scanne eller indtaste serienumre. Når du bruger en scanner, bestemmer scanningstilstanden, om serienumrene tilføjes eller fjernes fra listen over serienumre på fakturaen eller følgesedlen. Hvis du vil scanne serienumre, for eksempel ved hjælp af en håndholdt stregkodescanner, kan du konfigurere scanneren til at sende en Enter- eller TAB-kommando efter serienummeret. Denne kommando angiver slutningen af datastrømmen. Ellers skal du trykke på Enter eller TAB på tastaturet efter scanning af hvert serienummer.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Hvis jeg aktiverer serienumre for salgsprocessen, er jeg så nødt til at registrere alle serienumre for alle varer?
Konfigurationen af den sporingsdimensionsgruppe, der tildelt til produktet, bestemmer om serienumre skal registreres for alle varer på følgesedlen eller fakturaen. Når du aktiverer serienumre for salgsprocessen, markeres indstillingen **Serienummerkontrol** automatisk. Du skal derefter registrere et serienummer eller registrere en tom registrering for et ulæselig tal for hver enkelt vare på følgesedlen eller fakturaen. Hvis du ikke vil kræve et serienummer for hver vare, kan du markere indstillingen **Blank afgang tilladt** på den sporingsdimensionsgruppe, der er knyttet til varen. Derefter kan du registrere færre serienumre end mængden af varer, der leveres. Hvis du registrerer flere serienumre end antallet varer, der afsendes, kan du ikke bogføre følgesedlen eller fakturaen.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Kan jeg registrere serienumre for delfakturaer og delleverancer?
Du kan oprette delfakturaer og følgesedler for salgsordrer og kun registrere serienumrene for de varer, som fakturaerne og følgesedlerne omfatter. Hvis du vil oprette en delfaktura, og du har mere end én følgeseddel for salgsordren, kan du medtage serienumre fra mere end én følgeseddel. Men der kan kun være én følgeseddel, hvor alle serienumre ikke medtages. Hvis du har tre følgesedler, og hver følgeseddel indeholder to serienummererede varer, kan du ikke oprette en delfaktura for en vare på hver enkelt følgeseddel.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Hvad skal jeg gøre, når et serienummer ikke kan læses?
Hvis et serienummer ikke kan læse eller scannes, kan du oprette en tom linje for varen ved at klikke på **Kan ikke læses** på siden **Serienumre**. Hvis serienummeret bliver tilgængeligt senere, kan du opdatere fakturaen eller følgesedlen. Yderligere oplysninger finder du i næste afsnit, "Kan jeg rette eller ændre de serienumre, jeg har registreret for en salgsordre?"

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Kan jeg rette eller ændre de serienumre, jeg har registreret for en salgsordre?
Ja, du kan rette serienumre, hvis følgende betingelser er opfyldt:
-   **Fakturaer** – Du kan ændre serienumrene for de varer, du ikke har faktureret endnu. Følgesedlen opdateres derefter også. Hvis en salgsordrelinje imidlertid blev rettet ved at registrere et negativt antal, kan du ikke ændre serienumre for salgsordrelinjen.
-   **Følgesedler** – Du kan ikke delvist rette en følgeseddellinje, der indeholder serienummererede varer. Du skal tilbageføre den fulde mængde for linjen. Hvis en følgeseddel er blevet annulleret eller rettet, behøver du ikke registrere de tilbageførte serienumrene igen, når du opretter en ny følgeseddel for de samme serienummererede varer. De tal, der blev registreret, vil blive brugt.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Kan jeg få vist de serienumre, der blev leveret sammen med en bestemt følgeseddel eller blev medtaget i en faktura?
Ja, du kan køre en forespørgsel på følgeseddelkladdelinjen eller fakturakladdelinjen for at få vist en liste over alle de serienumre, der blev medtaget i dokumentet.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Kan jeg få vist de serienummererede varer, som jeg har på lager?
Nej, du kan ikke se de serienummererede varer, du har på lager, fordi serienumre ikke registreres for varer, før varerne er solgt.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Kan jeg registrere serienumre for fangstvægtvarer?
Nej, du kan ikke registrere serienumre for fastvægtvarer under salgsprocessen. Hvis et produkt desuden er konfigureret som en fastvægtvare, kan du ikke tildele produktet til en sporingsdimensionsgruppe, der er konfigureret til kun at bruge serienumre under salgsprocessen.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Kan jeg registrere serienumre på retail POS?

Ja, retail POS beder brugeren om at indtaste et serienummer, når brugeren sælger en vare, der er tildelt en sporingsdimensionsgruppe, der er konfigureret til kun at bruge serienumre under salgsprocessen.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Hvilke sikkerhedsroller kræves der for at registrere serienumre under salgsprocessen?
Denne funktion er tilgængelig for alle de roller, der kan vedligeholde salgsfølgesedler og salgsfakturaer. Følgende pligter giver arbejderne mulighed for at rette serienumre og registrere tomme poster for serienumre, der ikke kan læses eller scannes:
-   Vedligehold korrektion af serienumre
-   Vedligehold registrering af ulæselige serienumre







[!INCLUDE[footer-include](../../includes/footer-banner.md)]