---
title: Karantænezoner for uoverensstemmelser
description: Dette emne beskriver, hvordan du opretter og bruger karantænezoner til uoverensstemmelser.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956598"
---
# <a name="quarantine-zones-for-nonconformances"></a>Karantænezoner for uoverensstemmelser

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter og bruger karantænezoner til uoverensstemmelser.

Du kan bruge siden **Karantænezoner** til at definere de zoner, der kan tildeles til uoverensstemmelser. Når du opretter en uoverensstemmelse, kan du angive felterne **Karantænezone** og **Karantænetype** under fanen **Generelt** på siden **Uoverensstemmelser**. Feltet **Karantænezone** angiver typisk det område eller den lokation, hvor varen er placeret. Feltet **Karantænetype** definerer varen som enten *Begrænset brug* eller *Ubrugelig*.

Når du udskriver en uoverensstemmelses- eller korrektionsrapport for en uoverensstemmelse, kan du få vist karantænezonen, hvor varen er placeret.

Du kan også udskrive et uoverensstemmelsesmærkat for en uoverensstemmelse. Denne rapport viser den tildelte karantænezone og oplysninger om brugen for at vejlede om, hvordan defekt materiale skal håndteres. Karatænezonerne kan svare til lagerlokationer eller operationsressourcer.

## <a name="examples-of-quarantine-zones"></a>Eksempler på karantænezoner

### <a name="example-1"></a>Eksempel 1

Du arbejder i en virksomhed, der producerer og distribuerer tv, højttalere og medieafspillere. I dette tilfælde kan du konfigurere en karantænezone, der repræsenterer hver produkttype.

### <a name="example-2"></a>Eksempel 2

Tre beholdere og to reoler bruges til opbevaring af varer, der ikke opfylder kravene. I dette tilfælde kan du konfigurere fem karantænezoner, én for hver beholder og hver reol.

## <a name="create-a-quarantine-zone"></a>Oprette en ny karantænezone

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Karantænezoner**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Karantænezone** – Angiv et entydigt id eller navn til karantænezonen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af karantænezonen.

1. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser](quality-responsible-workers.md)
- [Problemtyper for uoverensstemmelser](quality-quarantine-zones.md)
- [Diagnosticeringstyper for uoverensstemmelser](quality-diagnostic-types.md)
- [Kvalitetsgebyrer for uoverensstemmelser](quality-charges.md)
- [Operationer for uoverensstemmelser](quality-operations.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
