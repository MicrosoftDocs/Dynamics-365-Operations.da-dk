---
title: Power BI-indhold til styring af kredit og inkasso
description: I dette emne beskrives, hvad der indgår i Power BI-indhold til styring af kredit og inkasso. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der bruges til at oprette indholdspakken.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 03face220fd63962f645b4fe91f20aec2f19b1ef
ms.sourcegitcommit: 14b554b43b9d86152ef27fdde6141589bcaf1161
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2020
ms.locfileid: "3598052"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Power BI-indhold til styring af kredit og inkasso

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvad der indgår i **Microsoft Power BI-indhold til styring af kredit og inkasso**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **Styring af kredit og inkasso** er oprettet til kreditchefer og inkassomedarbejdere. Det giver kredit- og rykkertal, f.eks. dage med udestående salg, forfaldne saldi, kreditrisici og kunder, der har overskredet deres kreditmaksimum. Det bruger transaktionsdata og indeholder samlede oversigter over kredit og rykkere på tværs af alle firmaer. Det indeholder også en opdeling pr. firma, debitorgruppe og debitor.

Dette Power BI-indhold består af 10 rapportsider:

- To oversigtssider (én side for en kreditoversigt og én side for en oversigt over rykkere)
- Otte oplysningssider med oplysninger om kredit- og rykkernøgletal, der er underopdelt på tværs af forskellige dimensioner

Alle beløb vises i systemvalutaen. Du kan angive systemvalutaen på siden **Systemparametre**.

Som standard vises kredit og rykkerdata for det aktuelle firma. Hvis du vil se dataene i alle firmaer, kan du tildele afgiften **CustCollectionsBICrossCompany** for rollen.

## <a name="setup-needed-to-view-power-bi-content"></a>Opsætning, der kræves for at se Power BI-indhold

Følgende konfiguration skal være fuldført for de data, der skal vises i **Kundekredit og inkasso** i Power BI.

1. Gå til **Systemadministration > Konfiguration > systemparametre** for at angive **Systemvaluta** og **Systemvalutakurs**.
2. Gå til **Finans > Kalendere > Regnskabskalendere** for at validere regnskabskalenderdatoer, der er tildelt den aktive tidsperiode.
3. Gå til **Finans > Opsætning > Finans** for at angive **Regnskabsvaluta** og **Valutakurstype**.
4. Definer valutakurser mellem transaktionsvalutaer og regnskabsvaluta, regnskabsvaluta og systemvaluta. Det gør du ved at gå til **Finans > Valutaer > Valutakurser**.
5. Gå til **Systemadministration > Konfiguration > Enhedslager** for at opdatere den samlede måling af **CustCollectionsBIMeasurementsV2**.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet

Power BI-indholdet **Styring af kredit og inkasso** vises i arbejdsområdet **Kundekredit og inkasso**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet

Power BI-indholdet **CustCollectionsBICrossCompany** omfatter en rapport, der består af et sæt nøgletal. Disse metrikker visualiseres som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i Power BI-indholdet til **CustCollectionsBICrossCompany**.

| Rapportside                 | Visualisering |
|-----------------------------|---------------|
| Oversigt over rykkere        | <ul><li>Forfaldne debitorer</li><li>Kunders over kreditmaksimum</li><li>Debitorbeløb pr. dag 30 dage</li><li>Åbne sager</li><li>Gennemsnit i dage til lukning af sag</li><li>Åbne aktiviteter</li><li>Gennemsnit i dage til lukning af aktiviteter</li><li>Åbne rentenotaer</li><li>Åbne rykkere</li><li>Kundehold</li><li>Salgshold</li><li>Aldersfordelte saldi</li><li>Rykkerstatusbeløb</li><li>Rykkerkodebeløb</li><li>Afskrivning efter årsag</li><li>Forfalden saldo efter område</li><li>Forventede betalinger</li></ul> |
| Kreditoversigt             | <ul><li>Forfaldne debitorer</li><li>Kreditmaks. vs. forfalden saldo</li><li>Gitter for kunder over kreditmaksimum</li><li>Kunder over kreditmaksimum pr. firma</li><li>Anvendt kredit vs. samlet kreditmaksimum</li><li>Kreditgrænse vs. kredit brugt efter område</li><li>Kunder pr. kreditværdighed</li></ul> |
| Kreditmaks.                | <ul><li>Kreditmaks.</li><li>Detaljer om kreditmaks.</li><li>Kreditmaks. pr. kunde</li><li>Kreditmaksimum pr. kundegruppe</li><li>Kreditmaksimum pr. kreditvurdering pr. firma</li><li>Kreditgrænse vs. kredit brugt efter område</li></ul> |
| Kunders over kreditmaksimum | <ul><li>Kunders over kreditmaksimum</li><li>Detaljer om kunder over kreditmaksimum</li><li>Kunder over kreditmaksimum pr. firma</li><li>Kunde over kreditmaksimum pr. debitorgruppe</li><li>Kunder over kreditmaksimum efter område</li></ul> |
| Forfaldne debitorer          | <ul><li>Forfaldne debitorer</li><li>Detaljer om forfalden debitor</li><li>Forfalden debitor pr. firma</li><li>Forfalden kunde pr. kundegruppe</li><li>Forfalden kunde efter område</li></ul> |
| Aldersfordelte saldi               | <ul><li>Aldersfordelte saldi</li><li>Detaljer om aldersfordelte saldi</li><li>Aldersfordelte saldi pr. firma</li><li>Aldersfordelte saldi pr. kundegruppe</li></ul> |
| Forventede betalinger           | <ul><li>Forventede betalinger</li><li>Oplysninger om forventede betalinger</li><li>Forventede betalinger pr. firma</li><li>Forventede betalinger pr. kundegruppe</li><li>Forventede betalinger pr. område</li></ul> |
| Afskrivninger                  | <ul><li>Afskrivninger pr. område</li><li>Oplysninger om afskrivninger</li><li>Afskrivninger pr. hovedkonto</li><li>Afskrivninger pr. firma</li><li>Afskrivninger pr. debitorgruppe</li><li>Afskrivninger pr. område</li></ul> |
| Rykkerstatus          | <ul><li>Bestridt</li><li>Brudt betalingsløfte</li><li>Lover at betale</li><li>Oplysninger om rykkerstatus</li><li>Rykkerstatusbeløb</li><li>Åbne sager</li><li>Åbne aktiviteter</li></ul> |
| Rykkere         | <ul><li>Rykkerkodebeløb</li><li>Oplysninger om rykkerkodebeløb</li><li>Rykkerbeløb pr. firma</li><li>Rykkerbeløb pr. kundegruppe</li><li>Rykkerbeløb pr. område</li></ul> |

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruge funktionen til eksport af underliggende data til at eksportere underliggende data, der opsummeres i en visuel effekt.
