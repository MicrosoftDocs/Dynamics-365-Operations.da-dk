---
title: Lokalisere fejl i salgsordrer
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgsordrer.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b5389b0d5a8ff68a3c16dedd2d8bb62f6e99af4f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824720"
---
# <a name="troubleshoot-sales-orders"></a>Lokalisere fejl i salgsordrer

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgsordrer.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Oplysningerne om moms opdateres ikke, hvis jeg ændrer placeringen på et salgsordrehoved.

### <a name="issue-description"></a>Problembeskrivelse

Hvis stedet, lagerstedet eller leveringsadressen ændres enten på et salgsordrehoved eller på linjeniveau, opdateres momsoplysningerne ikke automatisk for linjerne.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde er tilsigtet. Problemet opstår, fordi leveringsadressen, stedet og lagerstedet ikke ændres automatisk på linjeniveau. Du skal opdatere dem manuelt.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Hvis der er to samhandelsaftaler for samme periode eller overlappende perioder, er den samme aftalelinje altid valgt.

### <a name="issue-description"></a>Problembeskrivelse

Hvis der er defineret to samhandelsaftaler for samme periode eller overlappende perioder, ser den samme samhandelsaftale ud til at blive valgt, hver gang du opretter salgsordrelinjer, der indeholder de pågældende varer.

### <a name="issue-resolution"></a>Problemløsning

Hvis der er mere end én samhandelsaftale for en given dato, vil den samhandelsaftale, der har den laveste pris, altid blive valgt. Du kan finde flere oplysninger ved at hente følgende hvidbog: [Samhandelsaftaler i Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kan jeg knytte en indkøbsordre til en salgsordre for at opfylde efterspørgslen?

Du kan oprette en indkøbsordre ud fra en salgsordre. Du kan finde flere oplysninger i [Oprette en indkøbsordre fra en salgsordre](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Jeg kan ikke annullere eller slette en returordre eller salgsordre.

Du kan kun annullere salgsordrer og returordrer, der er i *Oprettet* tilstand. Du kan finde flere oplysninger under [Annullere en returordre](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Når jeg forsøger at annullere en salgsordre, modtager jeg fejlen "Reservationer kan ikke fjernes, fordi der er oprettet arbejde, der er afhængig af reservationerne".

Fejlkode: WAX4661

Hvis arbejdet er knyttet til en salgsordre, kan du ikke annullere salgsordren, før arbejdet er annulleret og tilbageført. Dette krav gælder, selvom det arbejde, der er tilknyttet salgsordren, er lukket.

Følg disse trin for at løse dette problem.

1. Annuller arbejdet, og læg lageret tilbage på den ønskede lokation. Gå til den relevante last af salgsordren, og vælg enten **Reducer plukket antal** på lastlinjen eller **Tilbagefør arbejde** i handlingsruden.

    Arbejdet har nu statussen *Annulleret*, og der oprettes og behandles automatisk nyt arbejde for lagerbevægelse for at bringe lagerbeholdningen tilbage til den lokation, der blev angivet, da den blev tilbageført.

2. Slet lasten. Forsendelsen slettes også.
3. Du skulle nu kunne gå til salgsordren og annullere den.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Jeg kan ikke annullere en intern indkøbsordre, der er knyttet til en salgsordre.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du forsøger at annullere en intern indkøbsordre, der er knyttet til en salgsordre, kan du få vist følgende fejlmeddelelse: "Antal kan ikke nedsættes, da restopdateringsantallet skifter fortegn".

### <a name="issue-resolution"></a>Problemløsning

Dette problem blev løst i Microsoft Dynamics 365 Supply Chain Management version 10.0.13. I denne version og senere versioner kan du nu annullere en intern indkøbsordre, der er knyttet til en salgsordre.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kan jeg gendanne en faktureret salgsordre, der er slettet?

### <a name="issue-description"></a>Problembeskrivelse

En faktureret salgsordre blev slettet ved en fejl, og du vil gendanne den eller se oplysningerne om den.

### <a name="issue-resolution"></a>Problemløsning

Hvis den slettede salgsordre allerede er faktureret, skal du gå til **Debitorkonto \> Transaktioner \> Oprindeligt dokument \> Vis detaljer**. Find den faktura, du leder efter, og vælg den for at få vist oplysninger om den. Disse oplysninger omfatter referencen til salgsordren. Du skulle også kunne få adgang til salgsordreoplysningerne fra den pågældende side.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Fristen for et salgsordrehoved blev ikke fundet i dataobjektet SalesOrderHeaderV2Entity.

Feltet Frist findes ikke i *SalesOrderHeaderV2Entity*-enheden.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Jeg skal slette poster for tabte salgsordrer.

Hvis du vil rydde op i tabte salgsordreposter, skal du køre det periodiske job *Sletning af salgsordre* ved at gå til et af følgende steder:

- Salg og markering \> Periodiske opgaver \> Oprydning \> Slet salgsordrer
- Detail og handel \> Retail og Commerce IT \> Oprydning \> Slet salgsordrer

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Er det muligt at beregne provision på fakturaer, der allerede er bogført?

Supply Chain Management understøtter i øjeblikket ikke beregningen af provisioner for bogførte fakturaer.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>En bundtvare understøttes ikke i en intern proces.

Bundtvaren er ikke tilgængelig for indkøbsordren, fordi antallet er *0* (nul) på salgsordrelinjerne for bundtvaren, og status er *Annulleret*. Denne funktionsmåde er tilsigtet. Salgsordren køber kun komponenterne i bundtvaren. Den køber ikke selve bundtvaren.

Hvis du skal købe et bundt, skal du overveje, om du vil markere det som en bundtvare, da denne funktionalitet er udviklet til scenarier for indtægtsføring. Yderligere oplysninger om bundtvarer finder du under [Bundter](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]