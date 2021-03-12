---
title: Nøglebegreber for opkrævningsstyring
description: Emnerne definerer nøglebegreber for opkrævningsstyring.
author: mikefalkner
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb2ec9969bdec985e1f8c731eade1c1a81a4766c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993008"
---
# <a name="collections-management-key-concepts"></a>Nøglebegreber for opkrævningsstyring

[!include [banner](../includes/banner.md)]

Før du begynder at oprette eller arbejde med rykkere, skal du kende følgende begreber:

- Aldersfordelte øjebliksbillede for debitorer indeholder saldooplysninger på et bestemt tidspunkt.
- Kundepuljer for rykkere hjælper dig med at organisere dit arbejde.
- Inkassatorer kan have deres egne kundepuljer.
- Listesider organiserer kunder, aktiviteter og sager for rykkere.
- Alle rykkeroplysningerne for en debitor findes på en side, og du kan udføre handlinger fra den pågældende side.
- Renter og gebyrer kan frafaldes, genindføres eller tilbageføres i ét trin.
- Afskrivningsposteringer kan oprettes i ét trin.
- Betalinger med ikke tilstrækkelige midler – NSF-betalinger (Non-sufficient Funds – USA) – kan behandles i ét trin.

I dette emne beskrives de enkelte begreber.

## <a name="customer-aging-snapshots"></a>Aldersfordelte øjebliksbilleder for debitor

Et aldersfordelt øjebliksbillede indeholder de beregnede aldersfordelte saldi for en debitor på et bestemt tidspunkt. Disse oplysninger vises på listesiden **Aldersfordelte saldi** og på siden **Rykkere**. Der skal oprettes et aldersfordelt øjebliksbillede, før du kan få vist oplysninger på listesiderne med rykkere(**Aldersfordelte saldi**, **Rykkeraktiviteter** og **Rykkersager**).

Et aldersfordelt øjebliksbillede har en overskrift og detaljerede poster for det aldersfordelte øjebliksbillede, der svarer til hver forældelsesperiode i definition af hver forældelsesperiode, for hver debitor.

Overskriften for det aldersfordelte øjebliksbillede indeholder det samlede skyldige beløb, kreditmaks., følgeseddelsbeløbet, salgsordrebeløbet, antallet af bestridte posteringer og det samlede beløb for bestridte posteringer for debitorkontoen. Alle posteringer for kunden er inkluderet i beregningen af disse beløb. Det samlede skyldige beløb, kreditmaks., følgeseddelsbeløbet og salgsordrebeløbet vises i faktaboksen **Kreditoplysninger** på siden **Rykkere**.

Der oprettes en detaljeret post for hver forældelsesperiode i definitionen af forældelsesperioden for det aldersfordelte øjebliksbillede. Den detaljerede post indeholder id'et for forældelsesperioden og det samlede beløb for posteringer, der har datoer inden for forældelsesperioden. Posteringer tildeles en forældelsesperiode, som f.eks 30 dage efter forfald. Datoen er relativ i forhold til datoværdien i **Aldersfordeling pr.**, som du angiver, når du opretter det aldersfordelte øjebliksbillede. Disse oplysninger vises på listesiden **Aldersfordelte saldi** og i faktaboksen **Aldersfordelte saldi** på siden **Rykkere**.

## <a name="collections-customer-pools"></a>Kundepuljer for rykkere

Kundepuljer er forespørgsler, der definerer en gruppe af kundeposter. Du kan bruge disse grupperede poster til at få vist oplysninger om de debitorkonti, der er medtaget, og til at administrere samlinger eller aldersfordelte processer for dem. Du kan bruge kundepuljer til at filtrere oplysningerne på listesiden for rykkere. Du kan også bruge dem til at filtrere de debitorkonti, der inkluderes ved oprettelsen af aldersfordelte øjebliksbilleder.

## <a name="collections-agents"></a>Inkassoagenter

Brugere kan som standard få vist alle kundeoplysninger på listesiderne med rykkerne. Med poster for inkassator kan du bestemme, hvilke kundepuljer der kan bruges til filtrering af oplysninger på listesiderne med rykkere og på siden **Rykkere**.

Inkassatorer samarbejder med kunderne om at sikre, at betalinger opkræves rettidigt. De er arbejdere, der er tildelt til brugere på siden **Brugerkonfiguration**.

## <a name="collections-list-pages"></a>Listesider for rykkere

På følgende listesider kan du få hjælp til at organisere dine rykkeroplysninger:

- **Aldersfordelte saldi** – Kolonnerne på denne listeside viser debitorsaldi og aldersfordelte beløb angivet efter forældelsesperiode. Disse oplysninger gemmes i et aldersfordelt øjebliksbillede. Forældelsesperioderne bestemmes af den anvendte definition af forældelsesperioder. Definitionen af forældelsesperiode hentes fra kundepuljen, hvis der er angivet en kundepulje for puljeforespørgslen. Hvis puljen ikke indeholder en definition af forældelsesperiode, bruges den standarddefinition af forældelsesperiode, som er angivet på siden **Debitorparametre**. Hvis der ikke er angivet en standarddefinition af forældelsesperiode, bruges den første definition af forældelsesperiode på siden **Definitioner af forældelsesperioder**.
- **Rykkeraktiviteter** – Kolonnerne på denne listeside viser de aktiviteter, der er identificeret som rykkeraktiviteter. Disse aktiviteter er oprettet på siden **Rykkere**. Du kan bruge aktiviteterne til at spore dit arbejde med at inddrive udeståender.
- **Rykkersager** – Kolonnerne på denne listeside viser oplysninger om sager, der hører til en sagskategori, der har sagstypen **Rykkere**.

### <a name="aging-snapshots"></a>Aldersfordelte øjebliksbilleder

Der skal oprettes et aldersfordelt øjebliksbillede, før du kan få vist oplysningerne på listesiden med rykkere. Der vises kun oplysninger for debitorer, der allerede er oprettet et aldersfordelt øjebliksbillede for. De poster, der vises på listesiden, kan filtreres yderligere som beskrevet her:

- Brugerne har som standard adgang til alle de debitorer, der findes et aldersfordelt øjebliksbillede for.
- Hvis der findes kundepuljer, skal brugeren oprettes som en inkassator for at kunne bruge puljerne til filtrering af oplysninger på listesiderne med rykkere. Oplysningerne er begrænset til kunder, der er inkluderet i den valgte kundepulje.
- Hvis en bruger oprettes som inkassator, er det kun de puljer, der er valgt for den pågældende inkassator, der er tilgængelige på listesiderne med rykkere. Hvis indstillingen **Tillad agent at få vist alle kundepuljer** er markeret på siden **Inkassoagent** for inkassoagenten, er alle puljer tilgængelige for den pågældende agent.

## <a name="collections-page"></a>Siden Rykkere

Du kan bruge siden **Rykkere** til at få vist, administrere og handle på rykkeroplysninger, -aktiviteter og -sager for en debitor.

Den øverste del af siden viser sager for den valgte debitor, den midterste sektion viser posteringerne for debitoren, og den nederste del viser aktiviteter, der er angivet for debitoren. Du kan oprette rykkersager til sporing af rykkeroplysninger for en eller flere posteringer eller aktiviteter. Oplysningerne i de øverste og nederste sektioner kan filtreres efter sag.

Faktaboksene viser aldersfordelte saldi og oplysninger om kreditmaksimum for den valgte debitor. Disse oplysninger gemmes i det aldersfordelte øjebliksbillede. Du kan om nødvendigt opdatere det aldersfordelte øjebliksbillede med aktuelle oplysninger.

Handlingsruden indeholder knapper, som du kan bruge til at få vist relaterede oplysninger for den valgte debitor, sag, postering eller aktivitet. Du kan også udføre almindelige handlinger, som f.eks. at ændre rykkerstatus for en postering, sende e-mail via integrationen med din e-mailudbyder, refundere kunder, behandle NSF-betalinger og afskrive saldi, der ikke kan inddrives.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Frafald, genindførelse eller tilbageførsel af renter og gebyrer

Du kan frafalde, genindføre eller tilbageføre hele rentenotaer eller de gebyrer og den posteringsrente, som indgår i rentenotaer. Under fanen **Indsaml** i handlingsruden på listen **Alle kunder** skal du vælge **Rentenota**, **Posteringsrente** eller **Gebyr**.

Disse reguleringer påvirker kun rentenotaer og de renter og gebyrer, som de omfatter. Du kan finde flere oplysninger om, hvordan du kan afskrive alle de gebyrer, som en kunde skylder, i afsnittet [Oprettelse af afskrivningstransaktioner](#creating-write-off-transactions) i dette emne.

Yderligere oplysninger finder du under Oprette en rentekode med et interval og Behandle renter.

## <a name="creating-write-off-transactions"></a>Oprettelse af afskrivningsposteringer

Du kan afskrive tab ved at vælge **Afskrivning** på siden **Rykkere** og listesiderne med rykkere.

Når du afskriver posteringer for en debitor, markeres alle posteringer for den pågældende debitor automatisk til udligning. Det beløb, er afskrives, afhænger af nettobeløbet for de markerede posteringer. Afskrivningsposteringen oprettes i en finanskladde og kan indeholde op til tre typer kladdelinjer:

- Den første kladdelinjetype indeholder debitorafskrivningsposten. Hvis de markerede posteringer indeholder flere kombinationer af valutakoder, dimensioner og posteringsprofiler, oprettes der en separat kladdelinje for hver enkelt kombination.
- Den anden kladdelinjetype indeholder posten for finansafskrivninger. Hvis de markerede posteringer indeholder flere kombinationer af valutakoder, dimensioner og posteringsprofiler, oprettes der en separat kladdelinje for hver enkelt kombination.
- Den tredje kladdelinjetype indeholder oplysninger om finansafskrivninger for moms. Denne kladdelinje oprettes kun, hvis indstillingen **Separat moms** er markeret på siden **Debitorparametre**. Hvis de markerede posteringer indeholder flere kombinationer af konti for udgående moms, dimensioner og momskoder, oprettes der en separat kladdelinje for hver enkelt kombination. Afskrivningsposteringen oprettes i posteringsvalutaen. Yderligere oplysninger finder du under Oprette en afskrivningskladde for en debitor.

## <a name="process-nsf-payments"></a>Behandle NSF-betalinger

Du kan behandle NSF-betalinger ved at vælge **NFS-betaling** på siden **Rykkere**. Når du vælger denne knap, annulleres betalingen. Hvis der gælder et NSF-gebyr for debitoren, oprettes der en gebyrpostering i en betalingskladde. Gebyrbeløbet baseres på indstillingerne for automatiske gebyrer. De automatiske gebyrer, der gælder for NSF-betalinger, specificeres med udgangspunkt i den gebyrgruppe, der er valgt på siden **Bankkonti** for den pågældende bankkonto.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfiguration af parametre for kundekreditstyring](./cm-credit-mgmt-setup.md)

[Konfigurationsoplysninger for kundekreditstyring](./cm-setup-information.md)

[Tilføje kreditstyringsoplysninger for en kunde](./cm-add-credit-mgmt-information-customer.md)

[Kundekreditgrupper](./cm-customer-credit-groups.md)

[Reguleringer af kundekreditmaksimum](./cm-credit-limit-adjustments.md)

[Kredithold for salgsordrer](./cm-sales-order-credit-holds.md)

[Periodiske opgaver for kundekreditstyring](./cm-periodic-tasks.md)
