---
title: Diagnosticeringstyper for uoverensstemmelser
description: Denne artikel beskriver, hvordan du bruger og opretter diagnosticeringstyper, der kan bruges sammen med uoverensstemmelser.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b7a051f807c9faab3169d2672d47f663892225
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852441"
---
# <a name="diagnostic-types-for-nonconformances"></a>Diagnosticeringstyper for uoverensstemmelser

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du bruger og opretter diagnosticeringstyper, der kan bruges sammen med uoverensstemmelser.

Du kan bruge siden **Diagnosticeringstyper** til definere en klassifikation af diagnosticeringshandlinger. Når du derefter opretter en rettelse til en uoverensstemmelse, skal du vælge en diagnosticering. En rettelse angiver, hvilken type diagnosticeringshandling der skal udføres for en godkendt uoverensstemmelse, og hvem der skal udføre den pågældende handling. Den angiver også den ønskede slutdato og den planlagte slutdato.

## <a name="examples-of-diagnostic-types"></a>Eksempler på diagnosticeringstyper

Du arbejder for en produktionsvirksomhed, og flere varer har ikke bestået kvalitetstesten. Disse varer flyttes ind i et karantæneområde og markeres som uoverensstemmende produkter. Der oprettes en uoverensstemmelsespost i Microsoft Dynamics 365 Supply Chain Management for at spore detaljerne gennem problemløsningen.

I dette tilfælde opstår der kvalitetsproblemer, fordi lejerne i den maskine, der pakker varerne, er gået i stykker og bliver overophedede. Håndteringen af dette problem er at udskifte delene i maskinen.

Når du konfigurerer diagnosticeringstyperne, kan du oprette flere poster, som hver repræsenterer en problemtype, som maskinen kan blive ramt af. Du kan også oprette en generel diagnosticeringstype, som repræsenterer maskinreparation.

## <a name="create-a-diagnostic-type"></a>Oprette en diagnosticeringstype

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Diagnosticeringstyper**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Diagnosticering** – Angiv et entydigt id eller navn til diagnosticeringstypen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af diagnosticeringstypen.

1. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser](quality-responsible-workers.md)
- [Karantænezoner for uoverensstemmelser](quality-quarantine-zones.md)
- [Problemtyper for uoverensstemmelser](quality-problem-types.md)
- [Kvalitetsgebyrer for uoverensstemmelser](quality-charges.md)
- [Operationer for uoverensstemmelser](quality-operations.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
