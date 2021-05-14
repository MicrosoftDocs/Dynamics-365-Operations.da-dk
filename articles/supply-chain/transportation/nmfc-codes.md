---
title: NMFC-koder (National Motor Freight Classification)
description: Dette emne beskriver, hvordan du kan arbejde med NMFC-koder (National Motor Freight Classification) i Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941876"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>NMFC-koder (National Motor Freight Classification)

[!include [banner](../includes/banner.md)]

Du kan bruge MNFC-koder (National Motor Freight Classification) til at klassificere varer, der kan fragtes. NMFC-koden er en betegnelse, der bruges til at gruppere varer. Transportfirmaerne kan evaluere varer til forsendelse ved at klassificere varerne ud fra overvejelser som f.eks. egnethed til lastbil, lastningsproblemer, håndtering af problemer og læsbarhed. Varer grupperes i en af 18 fragtklasser ved hjælp af en række numre fra 50 til 500. Den klasse, som en vare er grupperet i, er baseret på en evaluering af fire transportegenskaber: massefylde, muligheder for optimal lastning, håndtering og erstatningsansvar. Tilsammen bestemmer disse egenskaber varens egnethed til transport.

En NMFC-kode er tilknyttet hver forsendelsesvare mindre end truckload (LTL). En bærbar computer kan f.eks. tildeles en NMFC-kode med klasse 2,5, mens strømledninger kan tildeles en NMFC-kode med klasse 65.

Denne funktion kan hjælpe arbejdere med at bruge NMFC-koder til at klassificere LTL-forsendelsesvarer. Her er nogle eksempler:

- Hvis din virksomhed medtager en fragtbeskrivelse på fragtsedlen, har fragtmanden en ide om, hvad fragten går ud på. Fragt er en vigtig klassifikation, da mange transportfirmaer baserer hele deres forretningsmodel på de typer fragt, de håndterer.
- Denne klassifikation kan være vigtig for virksomheden, fordi den bruges til at bestemme omkostningerne for en given last.
- Din virksomhed kan identificere rentabiliteten af et LTL-logistik- og transportfirma.

Dette emne beskriver, hvordan du kan arbejde med NMFC-koder i Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Forudsætninger

Før du kan oprette NMFC-koder, skal du konfigurere alle LTL-fragtklasser, der skal knyttes til dem. LTL-fragtklasser repræsenterer varekategorier, hvorimod NMFC-koder er relateret til specifikke varer i hver af de 18 fragtklasser. Du kan finde flere oplysninger om, hvordan du arbejder med LTL-klasser, i [Mindre end truckload-klasser (LTL)](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Oprette en NMFC-kode

Benyt følgende fremgangsmåde for at oprette en NMFC-kode.

1. Udfør ét af følgende trin:

    - Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> NMFC-koder**.
    - Gå til **Transportstyring \> Opsætning \> Transportstandarder \> NMFC-koder**.

1. Vælg **Ny** for at oprette en NMFC-kode. Angiv derefter følgende felter:

    - **NMFC-kode** – Indtast NMFC-koden for varetypen.
    - **Navn** – Angiv et navn til NMFC-koden.
    - **LTL-klasse** – Vælg den LTL-klasse, der er tilknyttet NMFC-koden.
    - **Håndteringsenhed for stykliste** – Definer standardhåndteringstypen for forsendelsen.

## <a name="example-set-up-nmfc-codes"></a>Eksempel: Konfigurere NMFC-koder

I følgende eksempel vises det, hvordan du kan konfigurere to forskellige NMFC-koder, som kan bruges til forskellige produkter.

1. Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> NMFC-koder**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier på den nye linje:

    - **NMFC-kode:** *92,5*
    - **Navn:** *Computere*
    - **LTL-klasse:** *92,5*
    - **Håndteringsenhed for stykliste:** *Enhed*

1. Vælg **Gem** i handlingsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier på den nye linje:

    - **NMFC-kode:** *125*
    - **Navn:** *Telefoner*
    - **LTL-klasse:** *125*
    - **Håndteringsenhed for stykliste:** *Enhed*

1. Vælg **Gem** i handlingsruden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Mindre end truckload-klasser (LTL)](ltl-class.md)
- [Oprette en fragtseddel](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
