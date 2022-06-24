---
title: Gebyrer for uoverensstemmelsesoperationer
description: Denne artikel beskriver, hvordan du opretter kvalitetsgebyrer, der kan bruges sammen med operationer for en uoverensstemmelse.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29520afca07adee49846d1be987685a1ece8283c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850722"
---
# <a name="charges-for-nonconformance-operations"></a>Gebyrer for uoverensstemmelsesoperationer

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du opretter kvalitetsgebyrer, der kan bruges sammen med operationer for en uoverensstemmelse.

Du kan bruge siden **Kvalitetsgebyrer** til at definere de typer gebyrer, der kan tillægges operationer for en uoverensstemmelse. Gebyrer giver dig mulighed for at spore oplysninger om gebyrer eller gebyrer, som du skylder en kunde for uoverensstemmende produkter, eller som en kreditor skylder dig for uoverensstemmende produkter, du har modtaget. Du kan også bruge gebyrer til at spore omkostninger, der kræves af eksterne leverandører eller tjenester for at udføre en operation.

## <a name="examples-of-quality-charges"></a>Eksempler på kvalitetsgebyrer

Du arbejder i en produktionsvirksomhed. Din virksomhed har kontrakter med flere leverandører. Disse kontrakter skitserer standarderne for rettidig levering, skader og produktkvalitet for varer. På samme måde har flere kunder aftaler med virksomheden om returneringer, skader og produktkvalitet.

Der defineres en gebyrstruktur for hvert forhold, og den angives i kontrakten. Du kan konfigurere kvalitetsgebyrer for at skitsere forskellige gebyrtyper som f.eks. *Skader*, *Forsinket levering* og *Kvalitet*. Når du derefter opretter en uoverensstemmelse, tilføjer du en eller flere operationer. For hver operation skal du vælge **Gebyrer** for at definere detaljerne om gebyrerne.

## <a name="create-a-quality-charge"></a>Oprette et kvalitetsgebyr

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Kvalitetsgebyrer**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Gebyrkode** – Angiv et entydigt id eller navn for kvalitetsgebyret.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af kvalitetsgebyret.

1. Luk siden.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Føje et kvalitetsgebyr til en operation for en uoverensstemmelse

Yderligere oplysninger om, hvordan du føjer operationer til en uoverensstemmelse og lægger gebyrer på dem, finder du i [Operationer for uoverensstemmelser](quality-operations.md).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser](quality-responsible-workers.md)
- [Karantænezoner for uoverensstemmelser](quality-quarantine-zones.md)
- [Diagnosticeringstyper for uoverensstemmelser](quality-diagnostic-types.md)
- [Kvalitetsgebyrer for uoverensstemmelser](quality-charges.md)
- [Operationer for uoverensstemmelser](quality-operations.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
