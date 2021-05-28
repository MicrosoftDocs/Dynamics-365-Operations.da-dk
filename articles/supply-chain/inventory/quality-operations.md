---
title: Operationer for uoverensstemmelser
description: Dette emne beskriver, hvordan du opretter og bruger operationer til uoverensstemmelser.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022198"
---
# <a name="operations-for-nonconformances"></a>Operationer for uoverensstemmelser

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter og bruger operationer til uoverensstemmelser.

Du kan bruge siden **Operationer** til at definere klassifikationer af det arbejde, der kan udføres for en godkendt uoverensstemmelse. Når du knytter en relateret operation til en uoverensstemmelse, kan du angive detaljer som f.eks. det tilknyttede materiale, de arbejdstimer og gebyrer, der kræves for at udføre operationen. Systemet bruger disse oplysninger bruges til at beregne en forkalkuleret omkostning for operationen. De detaljerede oplysninger og forkalkulerede omkostninger er til reference. De relaterede operationer for kvalitet er ikke de samme som de operationer, der kan angives for en produktionsrute.

> [!NOTE]
> Selvom du kan spore omkostninger, tid og de varer, der bruges i en operation, der er relateret til en uoverensstemmelse, er de data, du angiver, kun vejledende. De integreres ikke automatisk med finansregnskabet, lagerregnskabet eller modulet **Tid og fremmøde**.

## <a name="examples-of-operations"></a>Eksempler på operationer

Du arbejder i en produktionsvirksomhed. Der blev oprettet og godkendt en uoverensstemmelse for varer, der ikke bestod en kvalitetstest. Der er oprettet en rettelse, som angiver, at problemet var relateret til et beskadiget leje i en maskine. Der kræves adskillige trin for at udskifte lejet, og ansvaret for hver operation spores. Følgende trin kan f.eks. være påkrævede:

1. Produktionslinjen standses, og oprydningsrutinen udføres.
1. Reparatører udskifter lejet.
1. Kvalitetssikringsmedarbejdere inspicerer maskinen, før den er tændes igen.

I dette eksempel kan du oprette følgende operationer, der repræsenterer det arbejde, der skal udføres:

- Stands produktionslinjen.
- Ryd produktionslinjen.
- Udfør reparationer på maskinen.
- Inspicer maskinen.

## <a name="create-an-operation"></a>Oprette en operation

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Operationer**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Operation** – Angiv et entydigt id eller navn til operationen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af operationen.
    - **Type** – Hvis operationen kun kan bruges til uoverensstemmelser, der er relateret til en bestemt ordretype, skal du vælge ordretypen (*Indkøbsordre* eller *Salgsordre*).

1. Luk siden.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Oprette og behandle uoverensstemmelser](tasks/create-process-non-conformance.md)
- [Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser](quality-responsible-workers.md)
- [Karantænezoner for uoverensstemmelser](quality-quarantine-zones.md)
- [Diagnosticeringstyper for uoverensstemmelser](quality-diagnostic-types.md)
- [Kvalitetsgebyrer for uoverensstemmelser](quality-charges.md)
- [Problemtyper for uoverensstemmelser](quality-operations.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
