---
title: Power BI-indhold til styring af kredit og inkasso
description: "I dette emne beskrives, hvad der indgår i Power BI-indhold til styring af kredit og inkasso. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 694a8bfd4601b48a80872662fa7a16bf15d6e65c
ms.contentlocale: da-dk
ms.lasthandoff: 12/18/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Power BI-indhold til styring af kredit og inkasso

I dette emne beskrives, hvad der indgår i Microsoft Power BI-indhold til **Styring af kredit og inkasso**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **Styring af kredit og inkasso** er oprettet til kreditchefer og inkassomedarbejdere. Det giver kredit- og rykkertal, f.eks. dage med udestående salg, forfaldne saldi, kreditrisici og kunder, der har overskredet deres kreditmaksimum. Det bruger transaktionsdata og indeholder samlede oversigter over kredit og rykkere på tværs af alle firmaer. Det indeholder også en opdeling pr. firma, debitorgruppe og debitor.

Dette Power BI-indhold består af 10 rapportsider:

- To oversigtssider (én side for en kreditoversigt og én side for en oversigt over rykkere)
- Otte oplysningssider med oplysninger om kredit- og rykkernøgletal, der er underopdelt på tværs af forskellige dimensioner

Alle beløb vises i systemvalutaen. Du kan angive systemvalutaen på siden **Systemparametre**.

Som standard vises kredit og rykkerdata for det aktuelle firma. Hvis du vil se dataene i alle firmaer, kan du tildele afgiften **CustCollectionsBICrossCompany** for rollen.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
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

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Hvis du vil finde flere oplysninger om filtrering og fastgørelse i Power BI, skal du se [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruge funktionen til eksport af underliggende data til at eksportere underliggende data, der opsummeres i en visuel effekt.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Følgende data bruges til at udfylde rapporten i Power BI-indholdet til **Styring af kredit og inkasso**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](../../dev-itpro/analytics/power-bi-integration-entity-store.md).

| Enhed                                      | Samlede nøglemålinger           | Datakilde                                 | Felt                                                      | Betegnelse |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Antallet af lukkede aktiviteter og gennemsnitlig tid til at lukke disse aktiviteter. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Antallet af åbne aktiviteter. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Summen af aldersfordelte saldi. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | De beløb, der er forfaldne. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Antallet af lukkede sager og den gennemsnitlige tid til at lukke disse sager. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Antallet af åbne sager. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Antallet af åbne rykkere. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Saldoen for bogførte rykkere. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Saldoen for posteringer med rykkerstatus. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Summen af kreditrisici og beløb, kunder, som kunders kreditmaksimum er overskredet med. |
| CustCollectionsBICustOnHold                 | Blokeret                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Antallet af kunder, der er sat på hold. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Antal dages salg, der har været udestående i 30 dage. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Summen af forventede betalinger inden for det næste år. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Det antal rentenotaer, der er blevet oprettet. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Det samlede antal salgsordrer, der er sat på hold. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Summen af transaktioner, der er blevet afskrevet. |

