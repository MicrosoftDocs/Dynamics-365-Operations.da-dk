---
title: Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser
description: Dette emne beskriver, hvordan du konfigurerer arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd1c7c86ac8627bd332bc578e98b4d7f091cdc8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575890"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser.

Uoverensstemmelser skal godkendes, før brugerne kan begynde at angive oplysninger, f.eks. rettelser eller operationer. Før brugere kan godkende eller afvise uoverensstemmelser, skal deres bruger-id (brugerpost) knyttes til en arbejderpost. Du kan vælge at konfigurere arbejdere, der er ansvarlige for kvalitet, og derefter tillade, at én arbejder godkender arbejde på vegne af en anden arbejder.

## <a name="enable-a-user-for-nonconformance-processing"></a>Aktivere en bruger til at håndtere af uoverensstemmelser

Før en bruger kan godkende eller afvise uoverensstemmelser, skal du knytte brugerens bruger-id (brugerpost) til en arbejderpost. Godkendelsesfelterne vil derefter blive udfyldt automatisk, og den aktuelle bruger bliver automatisk udfyldt for timesedlen. Før brugeren kan bruge dokumentnoter, skal du aktivere dokumenthåndtering i indstillingerne for brugeren.

1. Gå til **Systemadministration \> Brugere \> Brugere**.
1. Find og åbn den bruger, der skal kunne godkende eller afvise uoverensstemmelser.
1. Angiv feltet **Person** til navnet på den arbejder, der er knyttet til den aktuelle brugerpost.
1. Vælg **Brugerindstillinger** i handlingsruden.
1. På siden **Indstillinger** for den aktuelle brugerpost skal du angive indstillingen **Aktiver dokumenthåndtering** til **Ja** under fanen *Indstillinger*.
1. Luk siderne.

## <a name="define-workers-that-are-responsible-for-quality"></a>Definere arbejdere, der er ansvarlige for kvalitet

1. Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Arbejdere, der er ansvarlige for kvalitet**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Vælg den arbejder, der angiver kvalitetsdata i feltet **Arbejder**.
4. Vælg den arbejder, som den valgte arbejder angiver arbejde på vegne af, i feltet **Ansvarlig arbejder**. Når der oprettes og opdateres uoverensstemmelser, angives denne arbejder som standard i felter for **Arbejder**.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Kvalitetsgebyrer](quality-charges.md)
- [Karantænezoner for uoverensstemmelser](quality-quarantine-zones.md)
- [Diagnosticeringstyper for uoverensstemmelser](quality-diagnostic-types.md)
- [Kvalitetsgebyrer for uoverensstemmelser](quality-charges.md)
- [Operationer for uoverensstemmelser](quality-operations.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
