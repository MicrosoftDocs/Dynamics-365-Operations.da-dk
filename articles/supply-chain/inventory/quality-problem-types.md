---
title: Problemtyper for uoverensstemmelser
description: Denne artikel beskriver, hvordan du opretter og bruger problemtyper til uoverensstemmelser.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a73e692257c2a27085d60e75e028445811ee778a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857744"
---
# <a name="problem-types-for-nonconformances"></a>Problemtyper for uoverensstemmelser

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du opretter og bruger problemtyper til uoverensstemmelser.

Du kan bruge siden **Problemtyper** til at definere en klassifikation af de kvalitetsproblemer, der kan opstå for de forskellige uoverensstemmelsestyper. For hver problemtype, du opretter, skal du angive de typer uoverensstemmelser, som problemtypen kan bruges til. Du kan oprette følgende typer af uoverensstemmelser:

- **Interne** – Uoverensstemmelser af denne type er relateret til den disponible lagerbeholdning (f.eks. kvalitetsordrer eller karantæneordrer).
- **Debitor** – Uoverensstemmelser af denne type er relateret til salgsordrer.
- **Kreditor** – Uoverensstemmelser af denne type er relateret til indkøbsordrer.
- **Serviceanmodning** – Uoverensstemmelser af denne type er relateret til serviceordrer.
- **Produktion** – Uoverensstemmelser af denne type er relateret til batchordrer eller produktionsordrer.
- **Produktion af samprodukter** – Uoverensstemmelser af denne type er relateret til batchordrer for samprodukter.

Når du opretter en ny problemtype, skal du vælge **Uoverensstemmelsestyper** i handlingsruden for at oprette en liste over en eller flere uoverensstemmelsestyper, der er godkendt for problemtypen. En problemtype, der er relateret til en defektkode kunne f.eks. gælde for alle uoverensstemmelsestyper. Men en problemtype, der er relateret til kundeklager, gælder måske kun for uoverensstemmelsestyperne **Debitor** og **Serviceanmodning**.

## <a name="examples-of-problem-types"></a>Eksempler på problemtyper

Her er nogle eksempler på scenarier for problemtyper, der kan bruges til de forskellige uoverensstemmelsestyper:

- **Kunde:** En kunde har indsendt en klage, en kunde har returneret en vare, eller kvalitetsspecifikationer er ikke opfyldt.
- **Leverandør:** Produktet er beskadiget, kvalitetsspecifikationer er ikke opfyldt, eller det forkerte produkt er modtaget.
- **Serviceanmodning:** Kvalitetsspecifikationer er ikke opfyldt, en kunde har indsendt en klage, eller der kræves vedligeholdelse af maskiner.
- **Produktion:** Kvalitetsspecifikationer er ikke opfyldt, der kræves vedligeholdelse af maskiner, eller produktet er beskadiget.
- **Produktion af samprodukter:** Kvalitetsspecifikationer er ikke opfyldt, der kræves vedligeholdelse af maskiner, eller produktet er beskadiget.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Oprette en problemtype og tildele den til uoverensstemmelsestyper

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Problemtyper**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Problemtype** – Angiv et entydigt id eller navn til problemtypen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse af problemtypen.

1. Mens den nye række stadig er markeret, skal du vælge **Uoverensstemmelsestyper** i handlingsruden.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Derefter skal du for den nye række indstille feltet **Uoverensstemmelsestype** til den uoverensstemmelsestype, som du vil tillade for problemtypen.
1. Gentag det forrige trin for hver ekstra uoverensstemmelsestype, du vil autorisere for problemtypen.
1. Luk siderne.

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
