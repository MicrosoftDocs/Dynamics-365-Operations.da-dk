---
title: Tilsidesætte standardreservationsprincippet for materialer i produktion
description: I dette emne beskrives, hvordan du angiver et standardreservationsprincip for hver varemodelgruppe, så der automatisk kan anvendes forskellige reservationsprincipper for hver vare, der er en del af en stykliste (BOM) eller batchordreformel.
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b12740e58b2bf8667bee8a2c51917d69771779f2
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103357"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Tilsidesætte standardreservationsprincippet for materialer i produktion

[!include [banner](../includes/banner.md)]

Funktionen *Tilsidesæt standardreservation for produktion* gør det muligt angive et standardreservationsprincip for hver varemodelgruppe. Derfor kan der automatisk anvendes forskellige reservationsprincipper for hver vare, der indgår i en stykliste (BOM) eller batchordreformel. Du kan vælge, om hver varemodelgruppe skal tilsidesætte det standardreservationsprincip, der er angivet for en ordre, og hvilket reservationsprincip der skal bruges i stedet (*manuel*, *forkalkulation*, *planlægning*, *frigivelse* eller *start*).

Når du opretter en ny produktionsordre eller batchordre, bliver du bedt om at vælge det reservationsprincip, der skal anvendes på denne ordre og alle styklistelinjer eller formellinjer. Når funktionen *Tilsidesæt standardreservation for produktion* bruges, kan nogle eller alle stykliste- eller formellinjer tilsidesætte dette reservationsprincip og i stedet bruge det reservationsprincip, der er angivet for den relevante varemodelgruppe.

Hvis der f.eks. er råmaterialer eller ingredienser, der kræver plukarbejde, stykliste- eller formellinjer, der oprettes for disse produkter, som kræver en fysisk reservation, da fysisk reservation er en forudsætning for generering af lagerstedsarbejde. Hvis reservationen skal foregå automatisk, skal du typisk vælge et af følgende reservationsprincipper: *forkalkulation*, *planlægning*, *frigivelse* eller *start*. Hvis du derimod har materialer eller ingredienser, der ikke kræver plukarbejde, fordi de forbruges direkte fra en lokation, skal du typisk vælge reservationsprincippet *manuel*, som ikke foretager fysiske reservationer eller genererer plukarbejde.

## <a name="turn-the-override-default-production-reservation-feature-on-or-off"></a>Aktivere eller deaktivere funktionen Tilsidesæt standardreservation for produktion

Fra og med Supply Chain Management version 10.0.25 er denne funktion som standard aktiveret. Administratorer kan aktivere eller deaktivere denne funktion ved at søge efter funktionen *Tilsidesæt standardreservation for produktion* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Knytte en politik for produktionsreservation til en varemodelgruppe

1. Gå til **Omkostningsstyring \> Konfiguration af regnskabspolitik for lager \> Varemodelgrupper**.
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