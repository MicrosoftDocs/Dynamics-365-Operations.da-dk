---
title: Kreditoraftaler med betal ved betaling
description: "I denne artikel forklares betingelserne for \"betal ved betaling\" (PWP) for leverandøraftaler. PWP-betingelserne lader dig tilbageholde betaling til en kreditor helt eller delvist, indtil debitoren i projektet betaler dig. Denne artikel indeholder også et virkeligt eksempel for at vise, hvordan du kan bruge PWP-betingelserne til et projekt."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23131
ms.assetid: 20bf1d7f-8813-4c69-9cd7-576884a7e169
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7b21d4e93ec22715d530b75f75f3ba475e561f62
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="pay-when-paid-vendor-agreements"></a>Kreditoraftaler med betal ved betaling

[!include[banner](../includes/banner.md)]


I denne artikel forklares betingelserne for "betal ved betaling" (PWP) for leverandøraftaler. PWP-betingelserne lader dig tilbageholde betaling til en kreditor helt eller delvist, indtil debitoren i projektet betaler dig. Denne artikel indeholder også et virkeligt eksempel for at vise, hvordan du kan bruge PWP-betingelserne til et projekt.

Når du godkender en kreditor til at arbejde på et projekt som underleverandør, kan du vælge at tilbageholde betaling til kreditoren eller underleverandøren, indtil kunden betaler dig for projektet. Hvis du vil tilbageholde betaling til en kreditor, skal du oprette betingelserne for betal ved betaling, når du opretter indkøbsordren til kreditor. Når du opretter en indkøbsordre for kreditoren og tildeler indkøbsordren et projekt-id, knyttes betingelserne for betal ved betaling til indkøbsordren og kreditoren. På siden **Kreditorfakturaer med betal ved betaling** kan du få vist en liste over de ubetalte kreditorfakturaer for en indkøbsordre og de tilknyttede debitorfakturaer. Du kan bruge denne form til at afgøre, om kreditoren skal betales, og hvor meget der skal betales. Når en kunde betaler et beløb på en projektfaktura, kan du f.eks. frigive en del af eller alle de tilknyttede kreditorfakturaer til betaling. Du kan angive betingelser for betal ved betaling for at angive, at en kreditor betales, når du har modtaget en bestemt procentdel af den tilknyttede betaling fra en kunde. Når du modtager en delvis betaling fra en kunde, kan du manuelt frigive nogle af de tilknyttede kreditorfakturaer til betaling. I følgende eksempel vises det, hvordan du kan bruge betingelser for betal ved betaling for at tilbageholde betaling til en kreditor eller underleverandør, indtil kunden betaler dig. Din organisation indgår en aftale med en kunde om at levere 100 computere, hvorpå I installerer den software, som kunden ønsker. Den pris, som du og kunden har aftalt for hver computer, er 150,00. Du hyrer en tredjepartsleverandør til at levere computerne til dig. Kunden ønsker at godkende kvaliteten af computerne, før kunden betaler din organisation. Organisationens politik er at tilbageholde betalingen til en tredjepartsleverandør, indtil du har modtaget betaling af kunden på et projekt. Derfor opretter du projektet med en procentdel for betal ved betaling på 100 procent, så du kan tilbageholde alle betalinger til kreditoren, indtil du får fuld betaling for debitorfakturaen. Leverandøren fakturerer 100,00 for hver computer. Når kreditor sender computerne til dig, indeholder forsendelsen også en faktura på 10.000,00 for de 100 computere. Da du har konfigureret projektet med betingelser for betal ved betaling, betaler du ikke kreditoren. Når du modtager computerne fra leverandøren, installerer du den nødvendige software på computerne. Når du sender computerne til kunden, sender du også kunden en faktura på 15.000,00. Kunden undersøger computerne og godkender produktets kvalitet. Kunden betaler derefter din organisation det fulde beløb på projektfakturaen. Når du modtager den fulde betaling fra kunden, betaler du kreditoren det fulde beløb på kreditorfakturaen, 10.000,00.




