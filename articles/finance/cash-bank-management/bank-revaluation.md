---
title: Værdiregulering af udenlandsk valuta i bank
description: Dette emne giver et overblik over processen med værdiregulering af udenlandsk valuta i banker. Det omfatter oplysninger om opsætning og kørsel af samt beregningerne til processen og tilbageføring af værdireguleringstransaktioner.
author: mikefalkner
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 706b47afe6cf51f8cf8cd612b579bb8d20083d02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830538"
---
# <a name="bank-foreign-currency-revaluation"></a>Værdiregulering af udenlandsk valuta i bank

[!include [banner](../includes/banner.md)]


Dette emne giver et overblik over processen med værdiregulering af udenlandsk valuta i banker. Emnet beskriver, hvordan du opsætter og kører processen samt tilvejebringer oplysninger om beregningerne til processen. Det beskriver endvidere, hvordan man tilbagefører værdireguleringstransaktioner, såfremt der er behov herfor.

Regnskabsmæssige konventioner stiller krav om, at saldi for bankkonti i fremmedvalutaer værdireguleres ved hjælp af forskellige valutakurstyper (aktuelle, historiske, gennemsnitlige osv.) som led i en periodeafslutning. Værdiregulering af udenlandsk valuta i banker-funktionen kan anvendes til at værdiregulere en eller flere bankkonti. Dette er endvidere en global funktion. Du kan med andre ord værdiregulere banker på tværs af alle de juridiske enheder, du har adgang til, fra den samme side.

> [!NOTE]
> Når du kører processen til værdiregulering, bliver saldoen for hver bankkonto, der er bogført i udenlandsk valuta, værdireguleret. De transaktioner for ikke-realiseret gevinst eller tab, der oprettes under værdireguleringsprocessen, er genereret af systemet. Der kan oprettes to transaktioner – én for regnskabsvalutaen og én for rapporteringsvalutaen, såfremt rapporteringsvalutaen er relevant. Hver regnskabspost bogføres på kontoen for ikke-realiseret gevinst eller tab og den hovedkonto, der værdireguleres.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Klargøre kørsel af værdiregulering af udenlandsk valuta

Før du kan køre processen til værdiregulering, kræves følgende konfiguration.

- På siden **Finans** skal du angive valutakurstypen. Hvis en valutakurstype ikke er defineret på hovedkontoen, anvendes denne valutakurstype i forbindelse med værdireguleringen af udenlandsk valuta.
- På siden **Finans** skal du angive den realiserede gevinst, det realiserede tab og kontiene for urealiseret tab for værdiregulering af valuta. Konti for realiserede gevinster og realiserede tab anvendes, når transaktionerne for debitor og kreditor skal afregnes. Konti for ikke-realiserede gevinster og ikke-realiserede tab anvendes til at værdiregulere åbne transaktioner og hovedfinanskonti.
- På siden **Konti for valutaværdiregulering** kan du vælge forskellige valutaværdireguleringskonti for hver valuta og hver virksomhed. Hvis der ikke er defineret nogen konti, bruges kontiene på siden **Finans**.

## <a name="enable-foreign-currency-revaluation"></a>Aktiver værdiregulering af udenlandsk valuta

Du skal aktivere funktionen til værdireguleringer af udenlandsk valuta i banker, før du kan behandle værdireguleringer af udenlandsk valuta.

1. Gå til **Kontant- og bankstyring \> Opsætning \> Kontant- og bankstyringsparametre**.
2. På fanen **Generelt** under **Værdiregulering af udenlandsk valuta** skal du ved **Aktiver værdiregulering i bank** indstille den til **Ja** for at slå funktionen til for den aktuelle juridiske enhed. 
3. Tilføj en nummerserie for værdiregulering af udenlandsk valuta under fanen **Nummerserier**.
4. Genindlæs browseren for at få vist **Værdiregulering af udenlandsk valuta** under afsnittet med **Periodiske opgaver** på områdesiden.

Du skal aktivere funktionen for alle de juridiske enhed, der skal anvende værdiregulering af udenlandsk valuta. Hvis du er tildelt rollen som systemadministrator eller funktionsleder, kan du eliminere dette trin ved at aktivere funktionen **Aktiver værdiregulering i bank uden en parameter** i arbejdsområdet **Administration af funktioner**.

> [!NOTE]
> Såfremt jeres juridiske enhed anvender en russisk, polsk eller ungarsk lande-/områdekode, kan du allerede foretage værdiregulering af udenlandsk valuta i banker. Du kan ikke anvende den værdiregulering af udenlandsk valuta, der anvendes af andre lande eller områder.

## <a name="process-foreign-currency-revaluation"></a>Behandle værdiregulering af udenlandsk valuta

Når opsætningen er fuldført, skal du benytte siden **Værdiregulering af udenlandsk valuta** under "Kontant- og bankstyring" til at værdiregulere saldiene for en eller flere af de juridiske enheders bankkonti. Du kan køre processen i realtid eller planlægge, at den skal køre ved hjælp af en batch.

Siden **Værdiregulering af udenlandsk valuta** viser historikken for hver værdireguleringsproces. Den viser, hvornår processen blev kørt, og hvilke kriterier, der blev angivet, samt leverer et link til det bilag, der blev dannet i forbindelse med værdireguleringen. Det fremgår endvidere, hvorvidt der er sket en tilbageføring af en tidligere værdiregulering. For at køre værdireguleringsprocessen skal du vælge **Værdiregulering af udenlandsk valuta** i handlingsruden for at åbne dialogboksen med **Bank - værdiregulering af udenlandsk valuta**.

Feltet **Dato for værdiregulering** fastsætter skæringsdatoen for beregningen af saldoen for den udenlandske valuta, der skal værdireguleres. Det samlede beløb for alle banktransaktioner, der har fundet sted frem til denne dato, værdireguleres.

Feltet **Dato for valutakurs** fastsætter datoen for den valutakurs, der anvendes til at værdiregulere valutasaldiene. Du kan eksempelvis værdiregulere saldiene pr. 31. januar, men anvende den valutakurs, der er gældende for den 1. februar.

Værdireguleringsprocessen kan køres for en eller flere juridiske enheder. Opslagene viser alene de juridiske enheder, du har adgang til. For at vælge de bankkonti, der er egnede til værdiregulering af udenlandsk valuta, skal du markere de juridiske enheder, som disse konti tilhører. Alle de pågældende juridiske enheders bankkonti vil derefter fremgå af gitteret.

Angiv indstillingen **Forhåndsvisning før bogføring** til **Ja**, hvis du ønsker at se en forhåndsvisning af resultaterne af værdireguleringen, før du bogfører dem. Værdireguleringen af udenlandsk valuta har en forhåndsvisning, som kan bogføres. Det er ikke nødvendigt at køre værdireguleringsprocessen igen. Du kan eksportere resultaterne i forhåndsvisningen til Microsoft Excel for at bibeholde en oversigt over, hvordan beløbene er beregnet. Du kan ikke anvende batchbehandling, hvis du ønsker at se en forhåndsvisning af resultaterne af værdireguleringen.

Vælg **OK** for at behandle værdireguleringen af udenlandsk valuta. Der oprettes en oversigt for at spore historikken for hver kørsel. Der oprettes en separat oversigt for hver juridisk enhed og posteringslag.

## <a name="calculate-unrealized-gainloss"></a>Beregne ikke-realiseret gevinst/tab

Under "Kontant- og bankstyring" anses bankens valuta for at være basisvalutaen og værdireguleres ikke. Saldoen på bankkontoen i regnskabsvalutaen værdireguleres ved hjælp af valutakurser for henholdsvis bankens valuta og regnskabsvalutaen på **Datoen for valutakursen"**. Saldoen på bankkontoen i rapporteringsvalutaen værdireguleres ligeledes ved hjælp af valutakurser for henholdsvis bankens valuta og rapporteringsvalutaen på **Datoen for valutakursen"**.

Der oprettes en transaktion for differencen mellem bankkontoens saldo og den nye saldo, der beregnes for regnskabsvalutaen. Der oprettes yderligere en transaktion for differencen mellem bankkontoens saldo og den nye saldo, der beregnes for rapporteringsvalutaen. Posteringerne for disse transaktioner markeres som afstemt. 

Der foretages ingen posteringer for regnskabsvalutaen, såfremt bankvalutaen er den samme som regnskabsvalutaen. Tilsvarende foretages der ingen posteringer for rapporteringsvalutaen, såfremt bankvalutaen er den samme som rapporteringsvalutaen.

Transaktionen for værdiregulering af udenlandsk valuta deles ligeledes ud på de dimensioner, som forefindes i banktransaktionerne. Opdelingen baseres på hver dimensions saldo. Som eksempel kan nævnes, at den samlede banksaldo er 10.000, men virksomhedsenhed 001's saldo er 4.000 og virksomhedsenhed 002's saldo er 6.000. I dette tilfælde bogføres 40 procent af værdireguleringsbeløbet på virksomhedsenhed 001's værdireguleringskonto og 60 procent på virksomhedsenhed 002's værdireguleringskonto. Såfremt kontostrukturen ikke indeholder en virksomhedsenhed, bogføres det fulde beløb på værdireguleringskontoen.

## <a name="reverse-foreign-currency-revaluation"></a>Tilbagefør værdiregulering af udenlandsk valuta

Hvis du er nødsaget til at tilbageføre værdireguleringstransaktionen, skal du vælge **Tilbagefør transaktion** i handlingsruden på siden **Værdiregulering af udenlandsk valuta**. Der oprettes en ny historikpost for værdiregulering af udenlandsk valuta med henblik på at bibeholde det historiske revisionsspor for, hvornår reguleringen blev udført eller tilbageført.

For at tilbageføre flere værdireguleringer skal du tilbageføre den nyeste værdiregulering først. Dernæst skal du fortsætte med at tilbageføre de ældre værdireguleringer i henhold til dato. Du kan derefter behandle nye værdireguleringer for de perioder, du har tilbageført.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]