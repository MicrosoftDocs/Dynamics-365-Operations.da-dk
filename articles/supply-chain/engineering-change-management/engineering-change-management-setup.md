---
title: Fastlægge fælles værdier til styring af tekniske ændringer
description: Dette emne beskriver, hvordan du kan oprette fælles værdier, der bruges til parametre i forskellige dele af styring af tekniske ændringer.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 65f86fc488fe25cd4b093461088134fd7ad0c45ca569cd8f751314f1f5d88b6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753294"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Fastlægge fælles værdier til styring af tekniske ændringer

[!include [banner](../includes/banner.md)]

Når du konfigurerer styring af tekniske ændringer, skal du oprette flere samlinger af værdier, der skal bruges til at udfylde rullelisterne i andre dele af brugergrænsefladen (UI). Du skal angive disse værdier i henhold til de produkttyper, du producerer, og dine specifikke forretningsbehov.

## <a name="engineering-change-categories"></a>Tekniske ændringskategorier

Du kan bruge tekniske ændringskategorier til at organisere dine tekniske ændringsordrer, så de er nemmere at administrere og gennemgå. Det kan f.eks. være nyttigt at oprette en arbejdsproces, hvor, afhængigt af kategorien, en bestemt afdeling skal gennemgå de foreslåede ændringer. Den tekniske ændringsordre omfatter derfor et **Kategori**-felt.

Hvis du vil oprette en samling af tekniske ændringskategorier, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringskategorier**. Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.

## <a name="engineering-change-priorities"></a>Tekniske ændringsprioriteter

Du kan bruge tekniske ændringsprioriteter til at angive vigtigheden eller prioriteten af en teknisk ændringsordre. De kan hjælpe dig med at holde styr på vigtigheden af en teknisk ændringsordre, så du nemt kan identificere, hvilke ordrer der skal behandles først, og hvor hurtigt.

Hvis du vil oprette en samling af tekniske ændringsprioriteter, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringsprioriteter**. Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.

## <a name="engineering-change-reasons"></a>Årsager til den tekniske ændring

Tekniske ændringsårsager angiver årsagen til eller arten af ændringen i ændringsordren.

Hvis du vil oprette en samling af tekniske ændringsårsager, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringsårsager**. Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.

## <a name="material-disposal-codes"></a>Koder for afskaffelse af materiale

Du kan bruge materialekassationskoder til at kategorisere materialer, der bruges i færdigvarerne, eller komponenter, der skal kasseres på en bestemt måde eller kræver en vis håndtering, før de flyttes til den almindelige papirkurv. Når du føjer et relevant produkt til en teknisk ændringsordre, kan du tildele en kassationskode som en del af ændringsoplysningerne.

Hvis du vil oprette en samling af materialekassationskoder, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Materialekassationskoder**. Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.

## <a name="received-customer-approval"></a>Modtagne kundegodkendelser

Når du designer produkter til en bestemt kunde, skal designet og specifikationerne ofte valideres, før produktet kan angives som klar. Feltet **Modtaget kundegodkendelse** giver dig mulighed for at angive, hvor langt i kundegodkendelsesprocessen produktet er, og/eller om godkendelsen er modtaget.

Hvis du vil oprette en samling af værdier for modtaget kundegodkendelse, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Modtaget kundegodkendelse**. Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Teknisk ændring – Miljømæssige tilstands- og sikkerhedskoder

Hvis der skal tages hensyn til standardmiljøets tilstands- og sikkerhedsforskrifter eller firmaspecifikke forordninger eller procedurer i fremstillingen af et produkt, kan du bruge miljøets tilstands- og sikkerhedskoder til at definere dem. I den tekniske ændringsordre kan du angive, hvilke koder der gælder for fremstillingen af et produkt, mens du redigerer oplysningerne om det berørte produkt.

Hvis du vil oprette en samling af sundheds- og sikkerhedsværdier, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Teknisk ændring - Miljømæssige tilstands- og sikkerhedskoder**. Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.

## <a name="engineering-change-severities"></a>Tekniske ændrings alvorsgrad

Du kan bruge tekniske ændringers alvorsgrader til at angive det niveau af virkninger, der gælder for produkterne i en teknisk ændringsordre.

Hvis du vil oprette en samling af tekniske ændringers alvorsgrader, der bruges i dit firma, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringers alvorsgrader**. Du kan derefter bruge knapperne i handlingsruden til at tilføje, fjerne og redigere værdier og til at arrangere dem i den rækkefølge, de skal vises i på rullelisterne, hvor de vises.

Du kan oprette regler, der gælder for hvert af de niveauer af alvorsgrad, du opretter. Du kan finde flere oplysninger om, hvordan du tildeler disse regler, i næste afsnit.

## <a name="engineering-change-severity-rule-sets"></a>Regelsæt for alvorsgraden af den tekniske ændring

Du kan bruge de tekniske ændringers regelsæt for alvorsgrad til at oprette en gruppe regler, som du bruger til automatisk at beregne alvorsgraden af ændringsordren, baseret på typen af ændringer i de berørte produkter. Hvis du vil bruge regler for alvorsgraden, skal du åbne siden **Parametre for styring af tekniske ændringer** og angive feltet **Regel for alvorsgrad** til *Beregn* eller *Beregn automatisk*.

Når systemet evaluerer alvorsgraden, behandler det reglerne i den rækkefølge, som de vises på siden, oppefra og ned. For at en regel kan vælges og få dens prioritet fastlagt skal alle reglerne i et regelsæt opfyldes.

Hvis du vil oprette de regler, der gælder for hver enkelt ændrings niveau af alvorsgrad, du har defineret, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Teknisk ændringsstyring \> Tekniske ændringers regelsæt for alvorsgrad**. Udfør derefter ét af følgende trin.

- Hvis du vil oprette et nyt regelsæt, skal du vælge **Nyt** i handlingsruden og derefter angive felterne som beskrevet senere i dette afsnit.
- Hvis du vil redigere et eksisterende regelsæt, skal du vælge det i listeruden, vælge **Rediger** i handlingsruden og derefter angive felterne som beskrevet senere i dette afsnit.
- Hvis du vil slette et eksisterende regelsæt, skal du vælge det i listeruden og derefter vælge **Slet** i handlingsruden.
- Hvis du vil omarrangere listen med regelsæt, skal du vælge et regelsæt i listeruden og derefter bruge knapperne **Op** og **Ned** i handlingsruden til at flytte det.

For hvert regelsæt skal du angive følgende felt:

- **Alvorsgrad** – Vælg det niveau af alvorsgrad, der skal oprettes regler for. Du kan bruge siden **Tekniske ændringers alvorsgrader** til at oprette og navngive niveauerne. (Se det forrige afsnit for at få flere oplysninger).

Brug knapperne i oversigtspanelet **Regler** til at tilføje eller fjerne en regel for den aktuelle indstilling af alvorsgrad. Hver regel har et **Regel**-felt og et **Navn**-felt. Reglerne oprettes af systemet og angiver de typer af ændringer, et produkt kan have. Navnet angiver ændringstypen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]