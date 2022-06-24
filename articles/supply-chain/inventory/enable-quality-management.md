---
title: Aktivere styring af kvalitet og uoverensstemmelse
description: Denne artikel indeholder en oversigt over processen for opsætning og konfiguration af funktioner til kvalitets- og uoverensstemmelsesstyring i Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66229e3692e87f774c553eae955794330602598c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874037"
---
# <a name="enable-quality-and-nonconformance-management"></a>Aktivere styring af kvalitet og uoverensstemmelse

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over processen for opsætning og konfiguration af funktioner til kvalitets- og uoverensstemmelsesstyring i Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Aktivere styring af kvalitet og uoverensstemmelse

Benyt denne fremgangsmåde for at aktivere kvalitetsstyring på systemet.

1. Gå til **Lagerstyring \> Opsætning \> Parametre til lager- og lagerstedsstyring**.
1. Angiv indstillingen **Brug kvalitetsstyring** til *Ja* under fanen **Kvalitetsstyring**.
1. Brug feltet **Timepris** til at angive en timepris for arbejde i den lokale valuta. Timeprisen bruges til at beregne omkostningerne for operationer, der vedrører en uoverensstemmelse. Timeprisen og de beregnede omkostninger er referenceoplysninger for en uoverensstemmelse. De agerer ikke sammen med andre funktioner.
1. Vælg **Rapportopsætning**.
1. Tilføj nye linjer for de forskellige rapporttyper, og vælg den dokumenttype, der skal bruges til hver rapport.
1. Luk siden.
1. Luk siden.

## <a name="quality-management-configuration-process"></a>Konfigurationsproces for kvalitetsstyring

Før du kan begynde at bruge funktioner til kvalitetsstyring og generere kvalitetsordrer, skal du konfigurere systemet og forudsætningerne. Her er en liste over de trin, der kræves for at konfigurere kvalitetsstyring.

1. [Aktivere styring af kvalitet og uoverensstemmelse](#enable-qm).
1. Valgfrit: [Konfigurer testinstrumenter](quality-test-instruments.md).
1. [Konfigurere test](quality-tests.md).
1. [Konfigurer testvariabler og -udfald](quality-test-variables.md).
1. [Konfigurere testgrupper](quality-test-groups.md).
1. Valgfrit: [Konfigurer kvalitetsgrupper, og link til produkter](quality-groups.md).
1. Valgfrit: [Konfigurer kvalitetstilknytninger](quality-associations.md).

Når konfigurationen er fuldført, kan du begynde at oprette og behandle kvalitetsordrer. Du kan finde flere oplysninger om, hvordan du opretter og arbejder med kvalitetsordrer i [Kvalitetsordrer](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Konfigurationsproces for styring af uoverensstemmelser

Før du kan begynde at bruge funktioner til styring af uoverenstemmelser og generere uoverensstemmelser, skal du konfigurere systemet og forudsætningerne. Her er en liste over de trin, der kræves for at konfigurere styring af uoverenstemmelser.

1. [Aktivere styring af kvalitet og uoverensstemmelse](#enable-qm).
1. [Konfigurer arbejdere, der er ansvarlige for at godkende uoverensstemmelser](quality-responsible-workers.md).
1. [Konfigurer problemtyper](quality-problem-types.md).
1. [Konfigurer karantænezoner](quality-quarantine-zones.md).
1. [Konfigurer diagnosticeringstyper](quality-diagnostic-types.md).
1. [Konfigurer operationer](quality-operations.md).
1. Valgfrit: [Konfigurer kvalitetsgebyrer](quality-charges.md).

Når konfigurationen er fuldført, kan du begynde at oprette og behandle uoverensstemmelser. Du kan finde flere oplysninger om, hvordan du opretter og arbejder med uoverensstemmelser i [Oprette og behandle uoverensstemmelser](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
