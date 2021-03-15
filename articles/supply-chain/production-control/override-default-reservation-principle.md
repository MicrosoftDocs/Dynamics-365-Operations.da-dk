---
title: Tilsidesætte standardreservationsprincippet for materialer i produktion
description: I dette emne beskrives, hvordan du angiver et standardreservationsprincip for hver varemodelgruppe, så der automatisk kan anvendes forskellige reservationsprincipper for hver vare, der er en del af en stykliste (BOM) eller batchordreformel.
author: johanhoffmann
manager: tfehr
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8756dc22ffd64f836740124ce08dadca84207147
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078243"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Tilsidesætte standardreservationsprincippet for materialer i produktion

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Funktionen *Tilsidesæt standardreservation for produktion* gør det muligt angive et standardreservationsprincip for hver varemodelgruppe. Derfor kan der automatisk anvendes forskellige reservationsprincipper for hver vare, der indgår i en stykliste (BOM) eller batchordreformel. Du kan vælge, om hver varemodelgruppe skal tilsidesætte det standardreservationsprincip, der er angivet for en ordre, og hvilket reservationsprincip der skal bruges i stedet (*manuel*, *forkalkulation*, *planlægning*, *frigivelse* eller *start*).

Når du opretter en ny produktionsordre eller batchordre, bliver du bedt om at vælge det reservationsprincip, der skal anvendes på denne ordre og alle styklistelinjer eller formellinjer. Når funktionen *Tilsidesæt standardreservation for produktion* bruges, kan nogle eller alle stykliste- eller formellinjer tilsidesætte dette reservationsprincip og i stedet bruge det reservationsprincip, der er angivet for den relevante varemodelgruppe.

Hvis der f.eks. er råmaterialer eller ingredienser, der kræver plukarbejde, stykliste- eller formellinjer, der oprettes for disse produkter, som kræver en fysisk reservation, da fysisk reservation er en forudsætning for generering af lagerstedsarbejde. Hvis reservationen skal foregå automatisk, skal du typisk vælge et af følgende reservationsprincipper: *forkalkulation*, *planlægning*, *frigivelse* eller *start*. Hvis du derimod har materialer eller ingredienser, der ikke kræver plukarbejde, fordi de forbruges direkte fra en lokation, skal du typisk vælge reservationsprincippet *manuel*, som ikke foretager fysiske reservationer eller genererer plukarbejde.

## <a name="turn-on-the-feature"></a>Slå funktionen til

Før du kan bruge funktionen, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Produktionsstyring*
- **Funktionsnavn:** *Tilsidesæt standardreservation for produktion*

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Knytte en politik for produktionsreservation til en varemodelgruppe

1. Gå til **Omkostningsstyring &gt; Konfiguration af regnskabspolitik for lager &gt; Varemodelgrupper**.
1. Opret eller vælg en varemodelgruppe.
1. I oversigtspanelet **Lagerpolitikker** skal du markere afkrydsningsfeltet **Tilsidesæt vareproduktionsreservation**.
1. I feltet **Reservation** skal du vælge reservationsprincippet for varer, der tilhører den valgte modelgruppe. (Disse varer inkluderer varer, der findes på en stykliste- eller formellinje).

    - **Manuel** – Varer i modelgruppen reserveres ikke fysisk til produktion automatisk. De kan dog stadig reserveres manuelt efter behov.
    - **Forkalkulation** – Varer i modelgruppen reserveres fysisk under forkalkulation af produktionsordren.
    - **Planlægning** – Varer i modelgruppen reserveres fysisk under planlægning af produktionsordren.
    - **Frigivelse** – Varer i modelgruppen reserveres fysisk, når produktionsordren frigives.
    - **Start** – Varer i modelgruppen reserveres fysisk ved starten af produktionsordren.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Eksempel: Bruge reservationsprincipper i et bulk-/pakkescenarie

Oliemateriale massefremstilles i en 1.000-liters blander. Når materialerne til masseproduktion er klar, pumpes de ud til flere påfyldningsstationer, hvor flasker i forskellige størrelser påfyldes. Når påfyldningen er fuldført, pakkes flaskerne i kasser. Kasserne pakkes derefter på paller.

I dette scenario oprettes en batchordre til at lave 1.000 liter materiale til masseproduktion. (Denne ordre er bulkordren). Når denne batchordre er fuldført, rapporteres den som fuldført til påfyldningslokationernes indlagringslokation for materiale. Derefter oprettes en batchordre til at påfylde og pakke hver flaskestørrelse. (Disse ordrer er pakkeordrerne). Pakkeordrerne har en formel, der består af bulkmaterialet, en tom flaske, en etiket og andre emballagematerialer. Da bulkmaterialet flyder direkte fra blanderen til påfyldningsstationerne, kræves der ikke noget lagerstedsarbejde for at plukke dette stof, og bulkmaterialet forbruges direkte fra indlagringslokationen. Reservationsprincippet er derfor angivet til *manuel*. De øvrige materialer klargøres til påfyldningsstationen ved plukarbejde. Reservationsprincippet for disse linjer er f.eks. derfor angivet til *frigivelse*, så reservationen automatisk finder sted, når pakkeordren frigives.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]