---
title: Rykkere i Debitor
description: Oplysninger om rykkere for debitorer administreres i en central visning, siden Rykkere i Microsoft Dynamics 365 Finance. De ansvarlige for kredit og rykkere kan bruge denne centrale visning til at administrere rykkere. Inkassatorerne kan begynde rykkerprocessen fra debitorlisten, der genereres ved hjælp af foruddefinerede rykkerkriterier eller fra siden Debitorer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4dd9887debf73b94fb976af873690dcc53b8f53c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224783"
---
# <a name="collections-in-accounts-receivable"></a>Rykkere i Debitor

[!include [banner](../includes/banner.md)]

Oplysninger om rykkere for debitorer administreres i en central visning, siden Rykkere i Microsoft Dynamics 365 Finance. De ansvarlige for kredit og rykkere kan bruge denne centrale visning til at administrere rykkere. Inkassatorerne kan begynde rykkerprocessen fra debitorlisten, der genereres ved hjælp af foruddefinerede rykkerkriterier, eller fra siden Kunder.

Før du begynder at oprette eller arbejde med rykkere, skal du kende følgende begreber:
-   Aldersfordelte øjebliksbillede for debitorer indeholder saldooplysninger på et bestemt tidspunkt
-   Kundepuljer for rykkere hjælper dig med at organisere dit arbejde
-   Inkassatorer kan have deres egne kundepuljer
-   Listesider organiserer kunder, aktiviteter og sager for rykkere
-   Alle rykkeroplysningerne for en debitor findes på en side, og du kan udføre handlinger fra den pågældende side
-   Frafalde, genindføre eller tilbageføre renter og gebyrer kan gøres i ét trin
-   Oprette afskrivningsposteringer kan gøres i ét trin
-   Behandle NSF-betalinger (Non-sufficient Funds – USA) kan gøres i ét trin

Følgende afsnit indeholder beskrivelser af hvert enkelt begreb.

## <a name="customer-aging-snapshots"></a>Aldersfordelte øjebliksbilleder for debitor 
Et aldersfordelt øjebliksbillede indeholder de beregnede aldersfordelte saldi for en debitor på et bestemt tidspunkt. Disse oplysninger vises på listesiden Aldersfordelte saldi og på siden Rykkere. Der skal oprettes et aldersfordelt øjebliksbillede, før du kan få vist oplysningerne på listesiderne Rykkere. 

Et aldersfordelt øjebliksbillede indeholder en overskrift og detaljerede poster for det aldersfordelte øjebliksbillede, der svarer til hver forældelsesperiode i definition af hver forældelsesperiode, for hver debitor. 

Overskriften for det aldersfordelte øjebliksbillede indeholder det samlede skyldig beløb, kreditmaks., følgeseddelsbeløbet, salgsordrebeløbet, antallet af bestridte posteringer og det samlede beløb for bestridte posteringer for debitorkontoen. Alle posteringer for kunden er inkluderet i beregningen af disse beløb. Det samlede skyldige beløb, kreditmaks., følgeseddelsbeløbet og salgsordrebeløbet vises i faktaboksen Kreditoplysninger på siden Rykkere. 

Der oprettes en detaljeret post for det aldersfordelte øjebliksbillede for hver forældelsesperiode i definitionen af forældelsesperioden. Den detaljerede post for det aldersfordelte øjebliksbillede indeholder forældelsesperiode-id'et og det samlede beløb for postering med datoer, der er inden for forældelsesperioden. Posteringer tildeles en forældelsesperiode, som f.eks 30 dage efter forfald. Datoen er relativ i forhold til datoen Aldersfordeling pr., der angives, når du opretter det aldersfordelte øjebliksbillede. Disse oplysninger vises på listesiden Aldersfordelte saldi og i faktaboksen Aldersfordelte saldi på siden Rykkere.

## <a name="collections-customer-pools"></a>Kundepuljer for rykkere
Kundepuljer er forespørgsler, der definerer en gruppe kundeposter, der kan vises og administreres for rykkere eller aldersfordelte processer. Brug kundepuljer til at filtrere oplysningerne på listesiderne Aldersfordelte saldi, Rykkeraktiviteter og Rykkersager. Du kan også bruge kundepuljer til at filtrere de debitorkonti, der inkluderes ved oprettelsen af aldersfordelte øjebliksbilleder.

## <a name="collections-agents"></a>Inkassoagenter
Brugere kan som standard få vist alle kundeoplysninger på listesiderne med rykkere. Du kan bruge poster for inkassator til at bestemme de kundepuljer, der er tilgængelige til filtrering af oplysninger på listesiderne med rykkere og på siden Rykkere. 

En inkassator er en person, der arbejder sammen med kunderne om at sikre, at betalinger opkræves rettidigt. Inkassatorer er arbejdere, der er tildelt til brugere på siden Brugerkonfiguration.

## <a name="collections-list-pages"></a> Listesider for rykkere 
Følgende listesider hjælper dig med at organisere dine rykkeroplysninger.
-   Aldersfordelte saldi – Kolonnerne på listesiden viser debitorsaldi og aldersfordelte beløb angivet efter forældelsesperiode. Disse oplysninger gemmes i et aldersfordelt øjebliksbillede. Forældelsesperioderne bestemmes af den anvendte definition af forældelsesperioder. Definitionen på forældelsesperioder hentes fra kundepuljen, hvis der er angivet en til puljeforespørgslen. Hvis puljen ikke indeholder en definition af forældelsesperiode, bruges den standarddefinition af forældelsesperiode, som er angivet på siden Debitorparametre. Hvis der ikke er angivet en standarddefinition af forældelsesperiode, bruges den første definition af forældelsesperiode på siden Definitioner af forældelsesperioder.
-   Rykkeraktiviteter – Kolonnerne på listesiden viser de aktiviteter, der er identificeret som rykkeraktiviteter. Disse aktiviteter er oprettet ved hjælp af siden Rykkere. Brug aktiviteter til at spore dine bestræbelser på at inddrive udeståender.
-   Rykkersager – Kolonnerne på listesiden viser oplysninger om sager, der har en sagskategori med sagstypen Rykkere.

> [!NOTE]
> Der skal oprettes et aldersfordelt øjebliksbillede, før du kan få vist oplysningerne på disse listesider. Der vises kun oplysninger for debitorer, for hvem der allerede er oprettet et aldersfordelt øjebliksbillede. De poster, der vises på listesiden, kan filtreres yderligere på følgende måde:
> <li>En Finance and Operations-bruger har som standard adgang til alle de kunder, som der findes et aldersfordelt øjebliksbillede for.</li>
> <li>Hvis der findes kundepuljer, skal brugeren oprettes som en inkassator for at kunne bruge puljerne til filtrering af oplysninger på listesiderne med rykkere. Oplysningerne er begrænset til kunder, der er inkluderet i den valgte kundepulje.</li>
> <li>Hvis en bruger oprettes som inkassator, er det kun de puljer, der er valgt for den pågældende inkassator, der er tilgængelige på listesiden. Hvis til/fra-tasten Tillad agent at få vist alle kundepuljer er markeret på siden Inkassoagent for inkassoagenten, er alle puljer tilgængelige for den pågældende agent.</li>


## <a name="collections-page"></a> Siden Rykkere
Brug siden Rykkere til at få vist, administrere og handle på rykkeroplysninger, -aktiviteter og -sager for en debitor. 

Den øverste rude viser sager for den valgte kunde. Den midterste rude viser posteringer for den valgte kunde. Den nederste rude viser aktiviteter for kunden. Du kan oprette rykkersager til sporing af rykkeroplysninger for en eller flere posteringer eller aktiviteter. Oplysningerne i de øverste og nederste ruder kan filtreres efter sag. 

Faktaboksene viser aldersfordelte saldi og oplysninger om kreditmaksimum for den valgte debitor. Disse oplysninger gemmes i det aldersfordelte øjebliksbillede. Du kan om nødvendigt opdatere det aldersfordelte øjebliksbillede med aktuelle oplysninger. 

Handlingsruden indeholder knapper, der viser relaterede oplysninger for den valgte debitor, sag, postering eller aktivitet. Du kan også udføre almindelige handlinger, som f.eks. at ændre rykkerstatus for en postering, sende e-mail via integrationen med din e-mailudbyder, refundere kunder, behandle NSF-betalinger og afskrive saldi, der ikke kan inddrives.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Frafalde, genindføre eller tilbageføre renter og gebyrer 
Du kan frafalde, genindføre eller tilbageføre hele rentenotaer eller gebyrer og posteringsrente, som indgår i rentenotaer. Du kan gøre dette på fanen Indsaml i handlingsruden på listen Alle debitorer ved at klikke på Rentenota, Posteringsrente eller gebyr. 

Disse reguleringer påvirker kun rentenotaer og de renter og gebyrer, som de omfatter. Brug trinnene i afsnittet "Oprette afskrivningsposteringer med ét trin" til at afskrive alle de tillæg, som en debitor skylder.

Yderligere oplysninger finder du under [Oprette en rentekode med et interval](tasks/create-interest-code-range.md) og [Behandle renter](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Oprette afskrivningsposteringer
Du kan afskrive tab på debitorer ved at klikke på Afskriv i formularen Rykkere og på listesiderne Aldersfordelte saldi, Debitorer og Åbne debitorfakturaer. 

Når du afskriver posteringer for en debitor, markeres alle posteringer for debitoren automatisk til udligning. Det beløb, er afskrives, afhænger af nettobeløbet for de markerede posteringer. Afskrivningsposteringen oprettes i en finanskladde og kan indeholde op til tre typer kladdelinjer.

-   Den første kladdelinjetype indeholder debitorafskrivningsposten. Hvis de markerede posteringer indeholder flere kombinationer af valutakode, dimension og posteringsprofil, oprettes der en separat kladdelinje for hver enkelt kombination.
-   Den anden kladdelinjetype indeholder posten for finansafskrivninger. Hvis de markerede posteringer indeholder flere kombinationer af valutakode, dimension og posteringsprofil, oprettes der en separat kladdelinje for hver enkelt kombination.
-   Den tredje kladdelinjetype indeholder oplysninger om finansafskrivninger for moms. Denne kladdelinje oprettes kun, til/fra-tasten Separat moms er markeret på siden Debitorparametre. Hvis de markerede posteringer indeholder flere kombinationer af konto for udgående moms, dimension og momskode, oprettes der en separat kladdelinje for hver enkelt kombination.

Afskrivningsposteringen oprettes i posteringsvalutaen.

Yderligere oplysninger finder du under [Oprette en afskrivningskladde for en debitor](tasks/create-write-off-journal-customer.md).

<a name="process-not-sufficient-funds-nsf-payments"></a>Behandle NSF-betalinger (Non-sufficient Funds – USA)  
--------------------------------------------

Du kan behandle NSF-betalinger ved at klikke på NFS-betaling på siden Rykkere. Når du klikker på denne knap, annulleres betalingen. Hvis der gælder et NSF-gebyr for debitoren, oprettes der en gebyrpostering i en betalingskladde. Gebyrbeløbet baseres på indstillingerne for automatiske gebyrer. De automatiske gebyrer, der gælder for NSF-betalinger, specificeres med udgangspunkt i den gebyrgruppe, der er valgt på siden Bankkonti for den pågældende bankkonto.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]