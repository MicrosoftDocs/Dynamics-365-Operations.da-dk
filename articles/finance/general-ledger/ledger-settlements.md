---
title: Finansudligninger
description: Denne artikel beskriver, hvordan du kan bruge siden Finansudligninger til at udligne finansposteringer og tilbageføre udligninger.
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800625"
---
# <a name="ledger-settlements"></a>Finansudligninger

[!include [banner](../includes/banner.md)]

Med Finansudligning kan du sammenholde debet- og kreditposteringer i finansmodulet. Udligningen af debet- og kreditbeløbene bruges til at afstemme finanskontoens saldo med de detaljerede posteringer, som udgør saldoen.

Udlignede posteringer kan udelades fra forespørgsler og rapporter. På denne måde er det lettere at analysere de åbne finansposteringer, der udgør saldoen på finanskontoen.

> [!IMPORTANT] 
> Udligning af fakturaer og betalinger findes også i modulerne Debitor og Kreditor. Når der foretages udligning i debitor- og kreditorreskontroen, udlignes de tilsvarende finansposter ikke automatisk.

## <a name="ledger-settlement-features"></a>Funktioner til finansudligning
I Microsoft Dynamics 365 Finance version 10.0.21 blev indstillingen **Aktivér avanceret finansudligning** fjernet fra siden **Finansparametre**. Avanceret finansudligning er nu altid aktiveret.
I Finans version 10.0.25 blev funktionen **Opmærksomhed mellem finansudligning og årsafslutning** indført. Denne funktion ændrer den grundlæggende funktion i både finansudligning og årsafslutning af finans. Før du aktiverer denne funktion i arbejdsområdet **Funktionsstyring**, skal du se [Opmærksomhed mellem finansudligning og årsafslutning](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Konfigurere finansudligning
Du skal vælge de hovedkonti, du vil udføre finansudligning for. Du kan vælge disse hovedkonti på to måder.

1. Gå til **Finans** > **Opsætning Finans** > **Finansparametre**.
2. Vælg de kontoplaner, du vil vælge hovedkonti fra, under fanen **Finansudligninger**.
3. Vælg de hovedkonti, der skal udlignes finans for. Da kontoplanerne er globale, vil alle firmaer, som de valgte kontoplaner er tildelt, få valgt de samme hovedkonti til finansudligning.

  -eller-

1. Gå til **Finans** > **Periodiske opgaver** > **Finansudligninger**.
2. Vælg **Finansudligningskonti**.
3. Vælg de kontoplaner og hovedkonti, du vil udføre finansudligning for, i dialogboksen. Denne dialogboks er en genvej. De hovedkonti, du tilføjer her, afspejles også på siden **Finansparametre**.

Du kan når som helst bruge de samme grundlæggende procedurer til at fjerne hovedkonti fra finansudligning. Fjernelse af en hovedkonto har ingen indflydelse på tidligere finansudligninger. Hovedkontoen og posteringerne vises dog ikke længere på siden **Finansudligning**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Udlign transaktioner
Du kan udligne finanstransaktionerne ved at følge disse trin.

1. Gå til **Finans** > **Periodiske opgaver** > **Finansudligninger**.
2. Angiv filtrene øverst på siden:

    - Vælg et datointerval. Eller vælg en datointervalkode for automatisk at udfylde datointervallet. Du frarådes at udføre finansudligning for posteringer, der går på tværs af regnskabsår.
    - Rediger posteringslaget efter behov. Du kan ikke udligne posteringer, der findes i forskellige posteringslag.
    - For at få vist hovedkontoen og dimensionerne hver for sig, skal du vælge et økonomisk dimensionssæt.

3. Vælg **Vis posteringer** for at få vist alle de posteringer, der svarer til de filtre, du har angivet, og listen over konti, du angav, da du konfigurerede kontoplanen i det forrige afsnit.

    - Hvis du ændrer nogen af filtrene eller dimensionssættene, skal du vælge **Vis posteringer** igen.
    - Hvis du vil filtrere posteringerne til en enkelt hovedkonto, skal du bruge filteret i feltet **Finanskonto**. Vi fraråder at udføre finansudligning for posteringer, der er bogført på forskellige hovedkonti.

4. Vælg linjer til udligning. Værdien i feltet **Valgt beløb** øverst på siden forøges eller formindskes for at afspejle det samlede beløb på de linjer, du har valgt.
5. Når du er færdig med at vælge posteringer, skal du vælge **Markér valgte**. Der vises en markering i kolonnen **Markeret** for hver postering, du har valgt. Værdien i feltet **Markeret beløb** over gitteret forøges eller formindskes for at afspejle det samlede beløb på de linjer, du har markeret.
6. Når værdien i feltet **Markeret beløb** er **0** (nul), skal du vælge **Udlign markerede posteringer**. Status for de markerede posteringer opdateres til **Udlignet**.

    > [!IMPORTANT]
    > Alle de posteringer, du har markeret til udligning for den aktive juridiske enhed, udlignes, også selvom de ikke vises på finansudligningssiden for øjeblikket, fordi du har anvendt et filter.

## <a name="make-transactions-easier-to-find"></a>Gøre posteringer nemmere at finde
Siden **Finansudligninger** indeholder funktioner, der gør det nemmere at få vist de posteringer, du skal bruge til udligning.

- Brug filteret **Markeret** til at filtrere posteringer afhængigt af, om afkrydsningsfeltet **Markeret** er valgt for dem.
- Brug filteret **Status** til at filtrere posteringer på baggrund af deres status.
- Vælg **Sortér efter absolut beløb** for at sortere beløbene efter absolut værdi. På denne måde kan du gruppere debet- og kreditbeløb med samme beløb.

## <a name="reverse-a-settlement"></a>Tilbageføre en udligning
Du kan tilbageføre en udligning, der er foretaget ved en fejl.

1. Følg trin 1 til og med 3 i sektionen [Udligne posteringer](#settle-transactions) for at få vist de posteringer, du er interesseret i.
2. Vælg **Udlignet** i filteret **Status**.
3. Vælg linjer til tilbageførsel.
4. Vælg **Tilbagefør markerede posteringer**. Statussen for alle posteringer, der har samme udlignings-id, opdateres til **Ikke udlignet**.

    > [!IMPORTANT]
    > Alle posteringer, der har samme udlignings-id, tilbageføres, selvom de ikke er markeret. Der er f.eks. markeret og udlignet fire linjer. Alle fire linjer har samme udlignings-id. Hvis du markerer en af de fire linjer og derefter vælger **Tilbagefør markerede posteringer**, tilbageføres alle fire linjer.

## <a name="unmark-for-selected-users"></a>Fjern markeringen for valgte brugere
Vælg **Fjern markeringen for valgte brugere** for at fjerne markeringen af finansududlignede posteringer for alle juridiske enheder efter bruger-id. Det kan f.eks. give en regnskabschef mulighed for at fjerne markeringen af posteringer for en bruger, der var på ferie, før udligningen blev afsluttet, eller for en bruger, der har forladt organisationen. Handlingen vil tillade, at disse transaktioner kan markeres til udligning af en anden bruger.


## <a name="unmark-all-transactions"></a>Fjern markering af alle transaktioner
Vælg **Fjern markering af alle transaktioner** for at fjerne markeringen af alle finansududlignede posteringer for alle juridiske enheder og alle brugere. Denne opgave administrator er tilgængelig for rollen Administrator.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
