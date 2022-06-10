---
title: Lagerbogføringsprofiler
description: Dette emne indeholder en oversigt over lagerbogføringsprofiler.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28e3a3051978f921e01a929496e96909e6c32429
ms.sourcegitcommit: 00b39900d3cbdbc9ca1ab3145265007f5dc98a3f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/25/2022
ms.locfileid: "8806368"
---
# <a name="inventory-posting-profiles"></a>Lagerbogføringsprofiler

[!include [banner](../includes/banner.md)]

Lagerbogføringsprofiler styrer bogføringen af lagerreskontrotransaktioner til finans. Der kan oprettes lagerreskontrotransaktioner fra mange moduler, herunder **Salg og marketing**, **Indkøb og forsyning**, **Produktionsstyring** med mere. Lagerreskontrotransaktioner kan bogføres, hver gang en vare bruges i en salgsordre eller indkøbsordre. 

Der kan bogføres yderligere lagerreskontrotransaktioner:
- Hver gang et dokument opdateres.
- Når følgesedlen eller fakturaen for en salgsordre bogføres.
- Når der genereres en produktkvittering eller faktura for en indkøbsordre.

Der er flere oplysninger i Lagerreskontrotransaktioner.

## <a name="inventory-transaction-overview"></a>Oversigt over lagertransaktioner

Hver enkelt lagerreskontrotransaktion indeholder:
 - Antal 
 - Pris 
 - Sted 
 - Lagersted 
 - Sted 

Under lagerreskontrotransaktioner oprettes to poster i finansmodulet via fysisk bogføring og økonomisk bogføring. Du kan få flere oplysninger under [Fysiske og økonomiske opdateringer](/supply-chain/cost-management/physical-financial-updates.md).
Følgende eksempel er en indkøbsordre med tre linjer. I dette eksempel kan du antage, at hele ordren gælder en enkelt lokation og et enkelt lagersted. Hver indkøbsordrelinje har en enkelt relateret InventTrans-post – også kaldet en lagertransaktion – og hver linje gælder for et antal på 10. Følgende diagram viser forholdet mellem et indkøbsordrehoved og tre indkøbsordrelinjer, hver med en InventTrans-post.

![Relationsdiagram for en indkøbsordre med tre linjer hver med én InventTrans-post.](./media/InventTransRelationship.PNG)

Et antal af 5 modtages på den første indkøbsordrelinje. Det fulde antal for den anden linje og intet antal modtaget på den tredje linje i indkøbsordren. Nu er endnu en lagertransaktion relateret til den første indkøbsordrelinje. Transaktionen for den anden indkøbsordrelinje opdateres til **Modtaget**, og den tredje transaktion vil være den samme. Følgende diagram viser relationen med den ekstra InventTrans-post for indkøbsordrelinje 1.

![Relationsdiagram for en indkøbsordre med tre linjer. Den ene linje er delvist modtaget og viser to InventTrans-poster.](./media/InventTransRelationshipPartialReceipt.PNG)

I dette eksempel bogføres et bilag i finansmodulet. Det er det fysiske bilag. Varemodelgruppen er konfigureret til at bogføre fysisk lager, og alle varer bruger samme varemodelgruppe. Lagerposteringsprofilen bruger et enkelt sæt hovedkonti. Der oprettes et enkelt bilag, og InventTrans-posten sammenkæder både InventTrans 1 og InventTrans 2 med samme bilag.

Derefter modtages en faktura for det antal, der er modtaget på linje 1 og 2. Der oprettes et andet bilag i finansmodulet. Det er det økonomiske bilag. Varemodelgruppen er konfigureret til at bogføre økonomisk lager. Det nye andet bilag er relateret til InventTrans 1 og InventTrans 2.

Afhængigt af efterkalkulationsmodellen kan der være en tredje finanspostering for dine lagerreskontrotransaktioner, der vedrører lukning og udligning af lageret. Du finder flere oplysninger under [Lagerlukning](/supply-chain/cost-management/inventory-close.md). Du kan få vist detaljerne om alle lagertransaktioner ved at gå til **Lagerstyring** > **Forespørgsler og rapporter** > **Transaktioner**.

>[!Important]
> Lagertransaktionerne opdeles for hver entydig kombination af lagerdimensioner og for hver delvise opdatering. Dette blev vist i det foregående eksempel i forbindelse med delvise opdateringer.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Opdelt lager baseret på lagerdimensionseksempel

Indkøbsordrelinje 3 i eksemplet er en serialiseret vare. Der registreres ti serienumre for indkøbsordren under modtagelsesprocessen. Lagertransaktionen opdeles i 10 lagertransaktioner. Følgende diagram viser relationen og yderligere lagertransaktioner, der hver især har deres eget serienummer, som er relateret til indkøbsordrelinje 3.

![Relationsdiagram for en indkøbsordre med tre linjer. Den ene linje er serialiseret og viser ekstra InventTrans-poster](./media/InventTransRelationshipSerialNumber.PNG)

Hvis hvert serienummer modtages på en enkelt produktkvittering i eksemplet ovenfor, oprettes der ét ekstra bilag. Det fysiske bilagsfelt knyttes til hvert serienummer. Det samme gælder den økonomiske opdatering, når du fakturerer indkøbsordren.

## <a name="inventory-transactions"></a>Lagerbevægelser

Du kan få vist lagertransaktioner på siden **Lagertransaktioner** under **Lager- og lokationsstyring** eller **Omkostningsstyring**. Du kan også få vist lagertransaktioner, der er relateret til en bestemt kildedokumentlinje, f.eks. en indkøbsordrelinje eller salgsordrelinje, ved at vælge **Lager** og derefter vælge **Transaktioner**. 

Siden **Lagertransaktioner** indeholder følgende felter.

| Felt            | Beskrivende tekst                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Varenummer      | Det varenummer, der er relateret til transaktionen.                                                                  |
| Fysisk dato    | Den dato, hvor lageret ankommer til lagerstedet, forlader lagerstedet, forbruges i produktionen eller produceres. F.eks. bogføringsdatoen på
bogføring af følgesedlen for en salgsordre eller for bogføringen af produktkvittering for en indkøbsordre.                             |
| Økonomisk dato   | Den dato, hvor lagertransaktionen lukkes, og omkostningen registreres i finansmodulet. F.eks. bogføringsdatoen på fakturaen 
genereres for en indkøbs- eller salgsordre. Opdateringer af referencedokumentet er ikke tilladt, når den økonomiske dato er udfyldt. |
| Reference        | Angiver kilden til transaktionen og den dokumenttype, der vises i feltet **Nummer**. Det kan f.eks. være en kvittering for salgsordre, indkøbsordre eller flytteordre.                                                 |
| Nummer           | Angiver reference-id'et for en transaktion. Hvis f.eks. feltet **Reference** angiver salgsordre, angiver feltet **Nummer** salgsordrenummeret.                                                       |
| Tilgang (status) | For lagertransaktioner, der er tilgange, angiver dette felt tilgangsstatus. En indkøbsordre er f.eks. en tilgang, og status kan være **Bestilt** eller **Købt**.                                                            |
| Afgang (status)   | For lagertransaktioner, der er afgange, angiver dette felt afgangsstatus. En salgsordre er f.eks. en afgang, og status kan være **I bestilling** eller **Solgt**.                         |
| Antal         | Antallet af lagertransaktionen. Positive tal bruges ved lagertilgange, mens negative tal bruges ved lagerafgange.                                                                                                                          |
| Enhed             | Den måleenhed, som antallet er udtrykt i.                                                                                   |
| Fastvægtantal      | Fastvægtantallet for transaktionen. Du kan finde flere oplysninger under [Om fastvægtvarer](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Fastvægtenhed          | Fangstvægtenheden, som fangstvægtantallet er udtrykt i.                                                         |
| Kostbeløb      | Lagertransaktionens endelige omkostning. Dette felt udfyldes, når en transaktion opdateres økonomisk. Processen til lagerlukning og -regulering kan opdatere dette felt, afhængigt af efterkalkulationsmetoden.                            |

## <a name="inventory-status"></a>Lagerstatus

Hver enkelt lagertransaktion har en status, der vises i feltet **Tilgang** eller **Afgang**. Det felt, der bruges, afhænger af lagertransaktionstypen. Tilgange er transaktioner, der øger lageret. Det kan f.eks. være en indkøbsordre med et positivt antal eller en salgsordre, der returneres med et negativt antal. Afgange er lagertransaktioner, der reducerer lageret. Det kan f.eks. være en salgsordre med et positivt antal eller en indkøbsordre, der returneres med et negativt antal.

### <a name="receipt-status"></a>Tilgangsstatus

Følgende tabel beskriver statustypen **Tilgang**.

| **Tilgangsstatus** | **Beskrivelse**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Bestilt            | Den første status for alle lagertransaktioner, der repræsenterer en tilgang. Dette omfatter indkøbsordrer med et positivt antal, produktionsordrer eller salgsordrer, der returneres med et negativt antal.                                                   |
| Registreret         | Denne status bruges, når der en modtagelsesproces i to trin er på plads, eller når varemodtagelse bruges til at angive, at produktet er ankommet. Det bruges, når batch- eller serienumre er "tildelt" eller registreret på ordren. Du kan få flere oplysninger om varemodtagelse ved at gå til [Modtagelsesoversigt](/supply-chain/inventory/arrival-overview.md). |
| Modtaget           | Denne status bruges, når transaktionen opdateres fysisk. Det er når produktkvitteringen bogføres for en indkøbsordre. For en returnering af salgsordre er det, når følgesedlen bogføres.                                                                            |
| Købt          | Denne status bruges, når transaktionen opdateres økonomisk. For en indkøbsordre eller salgsordrereturnering er det, når fakturaen genereres.                                                                                             |

### <a name="issue-status"></a>Afgangsstatus

Følgende tabel beskriver statustypen **Afgang**.

| **Afgangsstatus**  | **Beskrivelse**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| I bestilling          | Den første status for alle lagertransaktioner, der repræsenterer en afgang. Dette omfatter salgsordrer med et positivt antal, produktionsordrers styklister eller formellinjer eller indkøbsordrer, der returneres med et negativt antal.                                             |
| Reserveret bestilt  | Denne lagerstatus angiver, at lager er reserveret i forhold til en ordre, der er oprettet, men endnu ikke fysisk modtaget på lageret. Når lageret modtages, opdateres status automatisk til **Reserveret fysisk**. Du kan få flere oplysninger om reservationer ved at gå til [Reservere lagerantal](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Reserveret fysisk | Denne status angiver, at lageret er blevet fordelt eller reserveret i forhold til en bestemt ordre. Når lager er reserveret, er det ikke fysisk disponibelt for andre ordrer.                                 |
| Plukket         | Det angiver, at lageret er plukket fra lagerstedet. Lageret er stadig fysisk på lagerstedet, er ikke blevet fjernet, men er ikke tilgængeligt for andre ordrer.  |
| Trukket          | Denne status bruges, når transaktionen opdateres fysisk. Når det drejer sig om en salgsordre, sker det, når følgesedlen bogføres. For en indkøbsordreretur er det, når produktkvitteringen bogføres.                                                                      |
| Solgt              | Denne status bruges, når transaktionen opdateres økonomisk. For en indkøbsordre eller salgsordre er det, når fakturaen genereres.|

Du kan få flere oplysninger om lagertransaktioner ved at gå til [Detaljer om lagertransaktioner](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Konfigurere en lagerposteringsprofil

Benyt følgende fremgangsmåde for at konfigurere en lagerposteringsprofil:

1.  Åbn **Lagerstyring** > **Konfiguration** > **Bogføring** > **Bogføring**.
2.  Vælg fanen for transaktionstypen. Vælg f.eks. **Indkøbsordre**.
3.  Vælg alternativknappen for bogføringstypen. Vælg f.eks. **Udgifter til indkøb for udgift**.
4.  Vælg **Ny**.
5.  Vælg en indstilling for **Tabel**, **Gruppe**, **Alle** eller **Kategori** i feltet **Varekode**. Hvis du f.eks. vil konfigurere en posteringsprofil for en bestemt varegruppe, skal du vælge **Gruppe**.
     - Hvis du valgte **Tabel** i trin 5, skal du vælge det specifikke Varenummer for posteringsprofilen i feltet **Varerelation**.
     - Hvis du valgte **Gruppe** i trin 5, skal du vælge **Varegruppe** for posteringsprofilen i feltet **Varerelation**.
     - Hvis du valgte **Alle** i trin 5, vil feltet **Varerelation** være tomt.
     - Hvis du valgte **Kategori** i trin 5, vil feltet **Varerelation** være tomt. Vælg kategorien til posteringsprofilen i feltet **Kategorirelation**.

6.  Vælg en indstilling for **Tabel**, **Gruppe** eller **Alle** i feltet **Kontokode**. Hvis du f.eks. vil anvende posteringsprofilen på alle kreditorer, skal du vælge **Alle**.
     - Hvis du valgte **Tabel** i trin 5, skal du vælge det specifikke kreditornummer for posteringsprofilen i feltet **Kontorelation**.
     - Hvis du valgte **Gruppe** i trin 5, skal du vælge kreditorgruppe for posteringsprofilen i feltet **Kontorelation**.
     - Hvis du valgte **Alle** i trin 5, vil feltet **Kontorelation** være tomt.

7.  Hvis du vil tilknytte en bestemt momsgruppe, der har den valgte bogføringstype, skal du vælge **Momsgruppe**. Hvis dette felt er tomt, gælder bogføringstypen for alle eksisterende momsgrupper. Bogføring, der angives for momsgrupper, gælder kun for salgs- og købstransaktioner.
8.  Angiv det kontonummer, som kontotypen skal bogføres til, i feltet **Hovedkonto**. Hvis der ikke er oprettet et kontonummer, der skal bruges til konteringstypen, kan du oprette en ny konto. Du kan oprette en ny konto på siden **Oplysninger om hovedkonto** i Finans.

## <a name="additional-resources"></a>Yderligere ressourcer

Hver fane på siden **Lagerposteringsprofil** er relateret til en reskontro i Dynamics 365 Supply Chain Management. Du kan finde flere oplysninger i:
-   [Bogføring af salgsordre](sales-order-posting.md)
-   [Bogføring af indkøbsordre](purchase-order-posting.md)
-   [Lagerpostering](inventory-posting.md)
-   [Bogføring af produktionsstyring](production-posting.md)
-   [Bogføring af standardomkostningsafvigelse](standard-cost-variance-posting.md)
