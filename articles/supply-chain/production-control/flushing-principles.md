---
title: Rydningsprincipper
description: Denne artikel beskriver de fire rydningsprincipper, der bruges ved forbrug af råmaterialer.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 89fd38ea6d2c1635e9d8974ab99c2e4cdae4d6be
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266422"
---
# <a name="flushing-principles"></a>Rydningsprincipper

[!include [banner](../includes/banner.md)]

Rydningsprincipperne afspejler forskellige forbrugsstrategier for råvarer, der bruges i produktionsprocesser. Forbruget er den proces, der trækker materiale fra den disponible lagerbeholdning og indstiller værdien af de anvendte materialer til **Igangværende arbejde** (IGVA) for produktionsordrer og batchordrer. Råvarerne forbruges normalt fra en lokalitet, der er konfigureret for den proces, der forbruger materialet. Denne lokalitet kaldes produktionens indlagringslokation.

Inden materialeforbruget flyttes materialerne til indlagringslokationen. Følgende illustration viser processen.

[![scenario4a.](./media/scenario4a.png)](./media/scenario4a.png)

1. Materialelagersted
2. Råvarepluk
3. Produktionsindlagringslokation
4. Forbrug af råmateriale
5. Produktionsproces

Materialeforbruges styres ved hjælp af følgende fire rydningsprincipper:

- Manuelt
- Start
- Afslut
- Disponibel på lokation

Rydningsprincipperne konfigureres i et hierarki af standardværdier. Hierarkiet starter ved det frigivne produkt, hvor rydningsprincippet har værdien **Start**. På styklisten eller formellinjen kan rydningsprincippet fra produktet tilsidesættes. Standardrydningsprincippet på produktionsstyklistelinjer eller formellinjer i batchordrer hentes fra produktet eller den værdi, der er tilsidesat på styklisten eller i formler.

## <a name="description-of-the-flushing-principles"></a>Beskrivelse af rydningsprincipperne

### <a name="manual"></a>Manuelt
Det manuelle rydningsprincippet angiver, at registreringen af materialeforbrug er en manuel handling. Dette princip er relevant, hvis du f.eks. vil kunne registrere tid, og antallet af anvendte batchnumre eller serienumre skal tages i betragtning med henblik på sporing. Manuelt forbrug registreres i en produktionspluklistekladde. For varer, der er aktiveret til lokationsstyringsprocesser (WMS), kan der anvendes en håndholdt proces.

### <a name="start"></a>Start
Startrydningsprincippet angiver, at materialer forbruges automatisk, når produktionsordren startes. Mængden af materiale, der forbruges, er proportional med det antal, der startes. Når startrydningsprincippet bruges sammen med produktionsudførelsessystemet, kan det også bruges til at rydde materialer, når en handling eller et procesjob startes. Dette princip er relevant, hvis f.eks. afvigelsen i forbruget er lav, materialerne er af lav værdi, der ikke er nogen krav til sporing, eller der er en kort kørselstid på handlinger. 

### <a name="finish"></a>Afslut
Rydningsprincippet Afslut angiver, at materialer automatisk forbruges, når produktionsordren er færdigmeldt, eller når en operation, der er konfigureret til at forbruge materialerne, registreres som fuldført. Mængden af materiale, der forbruges, er proportional med det antal, der færdigmeldes. Når rydningsprincippet Afslut bruges sammen med produktionsudførelsessystemet, kan det også bruges til at rydde materialer, når en handling eller et procesjob er fuldført. Dette princip er relevant i de samme tilfælde som Start-princippet. Afslut-princippet gælder imidlertid for handlinger, der har en længere operationstid, hvor materialer ikke må indstilles til IGVA, før operationen er fuldført.

> [!NOTE]
> Du kan ikke bruge rydningsprincippet Udfør sammen med planlægningsvarer. Det anbefales, at du i stedet bruger startrydningsprincippet. Planlægningsvarer har produktionstypen *Planlægningsvare*, og kun samprodukter og biprodukter kan færdigmeldes på batchordrer, der er oprettet til planlægningsvarer.

### <a name="available-at-location"></a>Disponibel på lokation
Rydningsprincippet Disponibel på lokation angiver, at materialet forbruges automatisk, når det er registreret som plukket til produktion. Materialet registreres som plukket fra lokation, når arbejdet for råvareplukningen er fuldført, eller når materialet er tilgængeligt på produktionens indlagringslokation, og materialelinjen er frigivet til lageret. Pluklisten, der oprettes under processen, bogføres i et batchjob. Dette princip er relevant, hvis du f.eks. har mange plukaktiviteter for én produktionsordre. Hvis det er tilfældet, behøver du ikke at foretage en manuel opdatering af pluklisten, og du kan få en aktuel visning af IGVA-saldoen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
