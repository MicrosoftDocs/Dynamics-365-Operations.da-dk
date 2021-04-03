---
title: Emballage og gebyrer
description: Dette emne indeholder oplysninger om emballagegebyrer, der betales til genbrugsfirmaer med bestemte intervaller.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b9ca8653bb3dc00285774d4ead9a8c14c606f24
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234723"
---
# <a name="packing-materials-and-fees"></a>Emballage og gebyrer

[!include [banner](../includes/banner.md)]

Emballagegebyrer betales med bestemte intervaller til et genbrugsfirma. Der betales et beløb pr. vægtenhed for hvert materiale, som en pakkeenhed består af. Selv om emballagegebyrer beregnes og rapporteres, men der bogføres ingen finanstransaktioner, da gebyrerne ikke betragtes som afgifter, der skal betales til en myndighed.

Der beregnes emballagevægt og -gebyrer for salgsordrelinjer og indkøbsordrelinjer.

Du kan definere en eller flere emballageenheder for en enkelt vare, en gruppe af varer (emballagegruppe) eller alle varer. En pakkeenhed består af de emballage, deres vægt og det antal varer, der indgår i pakkeenheden. Der tildeles en emballagekode til hver type emballage, der er defineret. På baggrund af emballagekoden kan du angive en pris for en bestemt periode. Emballagegebyret beregnes på baggrund af disse oplysninger.

> [!NOTE]
> Selvom firmaet ikke betaler emballagegebyrer, kan du bruge funktionen til at beregne statistik i forbindelse med emballagens vægt.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Konfigurer emballagetildeling

Før du kan beregne emballagevægt, emballagegebyrer eller begge dele, skal du aktivere beregningen og definere, hvilke materialer og gebyrer der skal gælde for hvilke varer.

1. Gå til **Lagerstyring \> Opsætning \> Parametre til lager- og lagerstedsstyring**.
1. Angiv indstillingen **Beregn emballagegebyrer** til **Ja** på fanen **Generelt** i afsnittet **Emballage**.
1. Gå til **Lagerstyring \> Opsætning \> Emballage \> Emballagegrupper**, og opret alle de emballagegrupper, du bruger. Alle varer i en emballagegruppe vil bruge samme emballagetildeling. Hvis du ikke bruger emballagegrupper, kan du springe dette trin over.

    > [!TIP]
    > Når du har oprettet emballagegrupperne, kan du tildele en gruppe til hvert af de produkter, du har brug for. Gå til **Styring af produktoplysninger \> Produkter \> Frigivne produkter**, vælg et produkt, og vælg derefter den relevante emballagegruppe på oversigtspanelet **Administrer lagerbeholdning** i feltet **Emballagegruppe**.

1. Gå til **Lagerstyring \> Opsætning \> Emballage \> Emballagekoder**, definer hver type emballage, du bruger, og angiv den enhed, som emballagen skal forbruges i, når du forbereder forsendelser.
1. Gå til **Lagerstyring \> Opsætning \> Emballage \> Emballagegebyrer**, og angiv et gebyr for hver type emballage, du lige har defineret. Gebyrer beregnes på basis af den pris pr. enhed, der forbruges.
1. Hvis du vil tildele emballage til varer, skal gå til **Lagerstyring \> Opsætning \> Emballage \> Emballagetildeling** og oprette tildelinger. Du kan oprette lige så mange tildelinger, du har brug for. Du kan tildele emballage til individuelle varer, grupper af varer (emballagegrupper) eller alle varer, afhængigt af hvor detaljeret tildelingerne skal være.

    I hver tildeling, du opretter, skal du følge disse trin:

    1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

        - **Varekode** – Vælg omfanget af tildelingen:

            - **Tabel** – Opret en tildeling for en enkelt bestemt vare.
            - **Gruppe** – Opret en tildeling for alle de varer, der hører til en pakkegruppe, som er defineret på siden **Emballagegrupper**.
            - **Alle** – Opret en tildeling for alle varer.

            > [!NOTE]
            > Du bør normalt foretage alle dine tildelinger på samme niveau **(Tabel**, **Gruppe** eller **Alle**). Hvis du bruger mere end ét niveau, vil den mest specifikke matchende tildeling blive brugt for hver vare. (Niveauet **Tabel** har højere prioritet end niveauet **Gruppe**, og begge niveauer tilsidesætter niveauet **Alle**.)

        - **Varerelation** – hvis du vil tildele en enkelt vare, skal du vælge varen. Hvis du vil tildele en gruppe varer, skal du vælge emballagegruppen. Hvis du vil tildele til alle varer, skal du lade feltet være tomt.
        - **Konfiguration**, **Størrelse**, **Farve** og **Typografi** – Angiv værdier for disse dimensioner, som du har brug for, for yderligere at definere den vare, du vil tildele til.
        - **Emballageenhed** – Vælg den enhed, som varen er emballeret i, når emballagen anvendes. Denne enhed kan være forskellig fra den enhed, som varen er købt og gemt i.
        - **Emballageenhedsfaktor** – Angiv den omregningsfaktor, der skal bruges til omregning fra lagerenheden til emballageenheden. (Omregningen bruger formlen *Emballageenheder* = *Vareenheder* x *Emballageenhedsfaktor*.)

    1. I oversigtspanelet **Emballage** skal du tilføje en linje for hvert stykke emballage, der kræves til den aktuelle tildeling. På hver linje skal du angive materialetypen (som defineret på siden **Emballagekoder**) og det antal, der forbruges for hver forsendelses enhed af den aktuelle vare.

## <a name="packing-units-on-sales-order-lines"></a>Pakkeenheder på salgsordrelinjer

Når du har [slået beregningen af emballagegebyrer til og konfigureret tildelingerne](#allocations), kontrollerer systemet, at der er angivet emballageenheder for hver vare, der føjes til en salgsordre. Derefter beregnes eventuelle påkrævede gebyrer. Når en vare føjes til en salgsordre, forekommer et af følgende trin:

- **Hvis en emballagetildeling gælder for varen:** Systemet opdaterer salgsordrelinjen med den angivne emballageenhed og antallet af emballageenheder. (Antallet af pakkeenheder beregnes vha. formlen *Emballageenhedsmængde* = *Bestilt mængde* ÷ *Antal varer i den valgte emballageenhed*.)
- **Hvis ingen emballagetildeling gælder for varen:** Du kan manuelt angive en pakkeenhed og et antal pakkeenheder på salgsordrelinjen.

Du kan også ændre pakkeenheden og antallet af pakkeenheder, når salgsordrelinjen bogføres. Denne mulighed er relevant, hvis salgsordrelinjen kun er delvist leveret eller delvist faktureret.

Når du fakturerer salgsordren, opretter systemet emballagetransaktioner. Emballageposteringer indeholder emballagevægten for salgslinjen. Du kan redigere transaktionerne, efter at du har faktureret dem. Du kan derefter oprette nye transaktioner.

## <a name="packing-units-on-purchase-order-lines"></a>Pakkeenheder på indkøbsordrelinjer

Systemet opretter ikke emballagetransaktioner for indkøbsordrelinjer. I stedet skal du oprette transaktioner for fakturerede indkøbsordrelinjer manuelt på siden **Emballagetransaktionerne**.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Konfigurere licensnumre til kunder, der skal betale emballagegebyrer

Hvis salgsordrerne for en bestemt kunde skal inkludere opkrævninger til emballagen, der bruges til de enkelte ordrer, skal du følge disse trin.

1. Gå til **Debitorer \> Kunder \> Alle kunder**.
1. Vælg den kunde, der skal opkræves for emballage.
1. I oversigtspanelet **Faktura og levering** skal du indstille følgende felter:

    - Angiv firmaets licensnummer i feltet **Licensnummer for emballageafgift** i afsnittet **Moms**.
    - Angiv firmaets licensnummer i feltet **Licensnummer** i afsnittet **Emballagegebyr**.

Når du nu opretter og fakturerer en salgsordre, som indeholder en eller flere varer, der bruger emballage, viser fakturaen emballagegebyrerne.

For kunder, der ikke skal betale emballagegebyrer, skal du følge disse trin, men rydde licens numrene fra felterne **Licensnummer for emballageafgift** og **Licensnummer**. Fakturaer for kunder, der ikke betaler emballagegebyrer, viser emballagevægten, men de viser ikke gebyrerne.

Hvis du vil generere en rapport, der viser alle de emballagegebyrer, som dit firma skylder i en bestemt periode, skal du gå til **Lagerstyring \> Forespørgsler og rapporter \> Emballagerapporter \> Beregning af emballagegebyr**, angive et datointerval og derefter vælge **OK**.

## <a name="print-packing-material-weights-on-invoices"></a>Udskrive emballagevægt på fakturaer

Du kan udskrive emballagevægten på en faktura og angive, hvem der skal betale de relaterede gebyrer. I rapporten opsummeres vægten efter emballagekoder.

1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
1. Angiv indstillingen **Udskriv emballagevægt** til **Ja** i oversigtspanelet **Faktura** på fanen **Opdateringer**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]