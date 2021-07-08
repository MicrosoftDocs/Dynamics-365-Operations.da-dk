---
title: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
description: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301299"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer

Fejlkode: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Nogle af varerne, der skal bruges til lasten %1, er endnu ikke plukket og flyttet til den endelige afsendelseslokation.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Lasten eller forsendelsen kan ikke bekræftes i dens aktuelle tilstand, da en af følgende betingelser kan være til stede:

- Det relaterede arbejde er endnu ikke plukket og flyttet til det endelige afsendelsessted.
- Det plukkede arbejdsantal svarer ikke til det oprettede arbejdsantal på linjen for lasten.
- Lokationsvejledningen er konfigureret med pakkelokation som den endelig forsendelseslokation ved brug af containerisering for bølgeskabeloner.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor forsendelsesbekræftelsen mislykkes. Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.
- Annuller de arbejds-id'er, der er oprettet med pakkelokationen som den endelige forsendelseslokation, konfigurer lokationsvejledningen igen, og frigiv lasten igen.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens

Brug følgende procedure til at gennemse dine lastlinjer og kontrollere, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.
1. Notér værdien for feltet **Antal oprettet under arbejde**.
1. under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.
1. Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.
1. Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Annuller de arbejds-id'er, der er oprettet med pakkelokationen som den endelige forsendelseslokation, konfigurer lokationsvejledningen igen, og frigiv lasten igen

Du kan bruge følgende procedure til at annullere de arbejds-id'er, der har pakkelokationen som den endelige læg på lager-lokation med automatisk containerisering på plads.

1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.
1. Dialogboksen **Annuller arbejde** åbnes. Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**. For det valgte arbejds-id skal værdien for **Arbejdsstatus** være *Åben*, *I gang*, *Annulleret*, *Kombineret* eller *Lukket*.
1. Vælg **OK**.
1. Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.
1. Gentag denne procedure for de andre arbejds-id'er, hvis det er nødvendigt.

Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).

Benyt følgende fremgangsmåde for at genkonfigurere lokationsvejledningen, så den ikke bruger pakkelokationen som den endelige forsendelseslokation, når der er konfigureret automatisk containerisering for bølgeskabelonen.

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.
1. Vælg den lokationsvejledning, du bruger til automatiseret containerisering.
1. Vælg **Rediger forespørgsel** på værktøjslinjen i oversigtspanelet **Handlinger for lokationsvejledninger**.
1. Find den række, hvor **Felt** er angivet til *Lokationsprofil*, i dialogboksen med forespørgselseditoren under fanen **Interval**, og kontrollér, at feltet **Kriterie** for den pågældende række ikke er angivet til en lokationsprofil, hvor **Lokationstype** er *Emballage*. Juster feltet **Kriterie** for at rette den endelige placering.

Benyt følgende fremgangsmåde for at frigive lasten igen og oprette arbejds-id'er med den korrekte endelige forsendelseslokation.

1. Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.
1. Find den last, der skal frigives, i sektionen **Laster**.
1. Vælg **Frigiv \> Frigiv til lagersted** på værktøjslinjen for sektionen **Laster** for at frigive den valgte last til lagerstedet.
1. Gentag denne procedure for de andre laster, hvis det er nødvendigt.
