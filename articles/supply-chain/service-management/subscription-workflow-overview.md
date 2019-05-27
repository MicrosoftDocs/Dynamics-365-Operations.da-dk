---
title: Oversigt over arbejdsgang til abonnement
description: Dette emne giver en oversigt over arbejdsgang for abonnement.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5cff6910dcb273fc081443546676426387f6625
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566404"
---
# <a name="subscription-workflow-overview"></a>Oversigt over arbejdsgang til abonnement 

[!include [banner](../includes/banner.md)]


Du er abonnementsadministrator for et lysfirma, og dit firma tilbyder abonnementer på vedligeholdelse af lysinstallationer. En kunde kontakter firmaet for at købe et årligt abonnement på vedligeholdelse af lysinstallationer.

## <a name="setting-up-subscriptions"></a>Definere abonnementer

Når du skal definere et abonnement, skal du først oprette en abonnementsgruppe til den nye serviceaftale eller kontrollere, at der findes en abonnementsgruppe. Hvis der findes en abonnementsgruppe, skal den være angivet til at fakturere kunden årligt og til at tillade periodisering af omsætning hver måned i året. Du kan finde flere oplysninger om oprettelse af abonnementer under [Konfigurere abonnementsgrupper](set-up-subscription-groups.md).

Når abonnementsgruppen er oprettet, kan du oprette abonnementet. Du kan finde flere oplysninger om oprettelse af serviceabonnementer under [Oprette serviceabonnementer fra en abonnementsgruppe](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Oprette og ændre abonnementstransaktioner

Når du har oprettet abonnementet, skal du oprette abonnementsgebyrtransaktionen for den første faktureringstermin, som er ét år. Posteringerne er af typen **Regulær**. Du kan derfor kun oprette abonnementstransaktioner, hvis fra-datoen og til-datoen svarer til perioder, der tidligere er oprettet i formularen **Periodetyper**. Du kan finde flere oplysninger om gebyrposteringer under [Oprette posteringer for abonnementsgebyr](create-subscription-fee-transactions.md).

Når du har defineret transaktionen for kunden, kommer du i tanke om, at de har forhandlet sig til en rabat på 10 % på alle listepriser på servicetilbud. Du skal derfor reducere prisen på det transaktionsgebyr, som du har oprettet.

Senere på dagen ringer din kundens kontaktperson til dig for at sige, at selvom de stadig vil have serviceaftalen til lysinstallationen, planlægger de at introducere en ny lysinstallation senere på året. De har derfor kun brug for vedligeholdelsesdækning frem til oktober 2013. For at reducere antallet af måneder i kundens abonnement opretter du en ny abonnementsgebyrtransaktion af typen **Reduktionsdage**. Du kan finde flere oplysninger om reducering af dage under [Reducere dagene på abonnementsgebyrer](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Fakturere og periodisere abonnementstransaktioner

Du er nu færdig med at definere abonnementer og er klar til at fakturere kunden for det. Du kan finde flere oplysninger om fakturering af abonnementer under [Fakturere abonnementstransaktioner](invoice-subscription-transactions.md).

To dag senere ringer kunden for at sige, at abonnementet skal faktureres i amerikanske dollars og ikke i euro. Du opretter derfor en kreditnota, og du opretter også en ny abonnementstransaktion i den rigtige valuta. Du kan finde flere oplysninger om kreditering af abonnementstransaktioner i [Kreditere abonnementstransaktioner](credit-subscription-transactions.md).

I slutningen af hver måned kan du periodisere en måneds omsætning fra kundens abonnementer til driftskontoen og IGVA-konti. Du kan finde flere oplysninger om periodisering af omsætning for abonnementer i [Periodisere abonnementsindtægt](accrue-subscription-revenue.md).

  


