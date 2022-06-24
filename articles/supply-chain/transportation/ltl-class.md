---
title: Mindre end truckload-klasser (LTL)
description: Denne artikel forklarer, hvad mindre end truckload-klasser (LTL) er, og beskriver, hvordan de konfigureres i Microsoft Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9ab05e1bc5d0ae2c8b5d98dda32660d2436676e9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857193"
---
# <a name="less-than-truckload-ltl-classes"></a>Mindre end truckload-klasser (LTL)

[!include [banner](../includes/banner.md)]

En klasse, der er mindre end truckload (LTL), er en forsendelsesklasse, der bruges til at klassificere varer, der kan afsendes. Generelt har alle typer produkter eller varer en NMFC-kode (National Motor Freight Classification), der svarer til nummeret på en bestemt fragtklasse for LTL-forsendelser. LTL-fragtklasser repræsenterer varekategorier, hvorimod NMFC-koder er relateret til specifikke varer i hver af de 18 fragtklasser.

Med denne funktion kan du bruge systemet til at udføre følgende opgaver:

- Definer de LTL-fragtklasser, der bruges i din virksomhed.
- Tildel hver LTL-klasse til en NMFC-kode på siden **NMFC-koder**. Du kan finde flere oplysninger i [NMFC-koder (National Motor Freight Classification)](nmfc-codes.md).
- Tildel en NMFC-kode (og dermed den tilknyttede LTL-kode) til hvert produkt på siden **Produkter**.
- Vurder nøje, den LTL-klasse for det enkelte produkt, som en NMFC-kode er tildelt.
- Fastlæg emballagekravene for hver LTL-klasse ved at kontrollere de internationale LTL-standarder. På denne måde sikrer du, at dine produkter bliver beskyttet korrekt og fragtet på sikker vis.
- Etabler nøjagtige forsendelsesestimater baseret på LTL-fragtklassen for hvert produkt.

Denne artikel beskriver, hvordan du opretter LTL-klasser i Microsoft Dynamics 365 Supply Chain Management.

## <a name="create-an-ltl-class"></a>Oprette en LTL-klasse

Benyt følgende fremgangsmåde for at oprette en LTL-klasse.

1. Udfør ét af følgende trin:

    - Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> LTL-klasser**.
    - Gå til **Transportstyring \> Opsætning \> Transportstandarder \> LTL-klasser**.

2. Vælg **Ny** i handlingsruden for at oprette en LTL-klasse. Angiv derefter følgende felter:

    - **LTL-klasse** – Angiv virksomhedens interne LTL-klasseidentifikation (id) for varetypen. De fleste virksomheder følger de internationale standarder. I dette tilfælde vil værdien i dette felt svare til værdien i feltet **Klasse**. Hvis virksomheden anvender sin egen standard, skal du dog angive en kode, der overholder standarden.
    - **Navn** – Angiv et beskrivende navn, der kan hjælpe dig og andre brugere med at vælge den rette LTL-klasse for hver NMFC-kode.
    - **Klasse** – Angiv den internationale LTL-standardklasses id for varetypen. Den kode, du angiver her, skal overholde den officielle standard.

## <a name="example-set-up-ltl-classes"></a>Eksempel: Konfigurere LTL-klasser

I følgende eksempel vises det, hvordan du kan konfigurere to forskellige LTL-klasser, som du kan bruge til forskellige typer produkter.

1. Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> LTL-klasser**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier på den nye linje:

    - **LTL-klasse:** *92,5*
    - **Navn:** *Computere, skærme, køleskabe*
    - **Klasse:** *92,5*

1. Vælg **Gem** i handlingsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier på den nye linje:

    - **LTL-klasse:** *125*
    - **Navn:** *Små husholdningsapparater*
    - **Klasse:** *125*

1. Vælg **Gem** i handlingsruden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [NMFC-koder (National Motor Freight Classification)](nmfc-codes.md)
- [Oprette en fragtseddel](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
