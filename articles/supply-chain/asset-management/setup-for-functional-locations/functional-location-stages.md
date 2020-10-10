---
title: Livscyklustilstande for arbejdssted
description: Dette emne beskriver, hvordan du konfigurerer arbejdsstedstilstande og livscyklusmodeller i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eedc21dde32671b4f5539ac4e798a8e1329c191
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890100"
---
# <a name="functional-location-lifecycle-states"></a>Livscyklustilstande for arbejdssted

[!include [banner](../../includes/banner.md)]

 

Dette emne beskriver, hvordan du konfigurerer livscyklustilstande for arbejdssteder og livscyklusmodeller i Styring af aktiver. Livscyklustilstande for arbejdssted definerer de tilstande, som et arbejdssted kan gennemgå, for eksempel oprettet, aktiv og afsluttet. Du kan få vist alle arbejdssteder, uanset deres livscyklustilstand, på listesiden **Alle arbejdssteder**. Du kan ændre tilstanden for et arbejdssted ved at vælge det på listesiden **Alle arbejdssteder** og vælge **Opdater arbejdsstedets tilstand**.

## <a name="set-up-functional-location-lifecycle-states"></a>Opsætning af livscyklustilstande for arbejdssted

1. Vælg **Styring af aktiver** > **Opsætning** > **Arbejdssteder** > **Livscyklustilstande**.
2. Vælg **Ny** for at oprette en ny tilstand for arbejdssted.
3. Indsæt tilstands-id'et i feltet **Livscyklustilstand** og et navn til arbejdsstedets tilstand i feltet **Navn**. I feltet **Livscyklusmodeller** kan du se antallet af livscyklusmodeller for arbejdssted, der bruger den tilstanden for arbejdssted.
4. I oversigtspanelet **Generelt** skal du vælge "Ja" på til/fra-knappen **Aktiv**, hvis arbejdsstedet skal være aktivt i denne tilstand.
5. Vælg "Ja" på til/fra-knappen **Opret aktiver**, hvis det skal være muligt automatisk at oprette et aktiv med samme navn som arbejdsstedet og installere det på arbejdsstedet i denne tilstand.  
>[!NOTE]
>Denne til/fra-knap relaterer til feltet **Aktivtype** i oversigtspanelet **Generelt** i formen **Arbejdsstedstyper** (**Styring af aktiver** > **Opsætning** > **Arbejdssteder** > **Arbejdsstedstyper**).
6. Vælg "Ja" på til/fra-knappen **Omdøb sted**, hvis det skal være muligt at ændre navnet på arbejdsstedet i denne tilstand.
7. Vælg "Ja" på til/fra-knappen **Nye underlokationer**, hvis det skal være muligt at føje nye underlokation til arbejdsstedet i denne tilstand.
8. Vælg "Ja" på til/fra-knappen **Installer aktiver**, hvis det skal være muligt at installere aktiver på arbejdsstedet i denne tilstand.
9. Vælg "Ja" på til/fra-knappen **Slet arbejdssted**, hvis det skal være muligt at slette arbejdsstedet i denne tilstand.
10. Vælg en aktivtilstand i feltet **Livscyklustilstand**, hvis du ønsker, at livscyklustilstanden for alle aktiver, der installeres på arbejdsstedet, automatisk skal opdateres i denne tilstand. Eksempel: Hvis du lukker et arbejdssted og indstiller livscyklustilstanden for arbejdsstedet til "Afsluttet", vil du måske automatisk ændre livscyklustilstanden for de aktiver, der er installeret på det pågældende arbejdssted, til "Ikke i brug".


>[!NOTE]
>Livscyklustilstande for arbejdssted, livscyklusmodeller og -typer er relaterede og bruges på samme måde som livscyklustilstande for arbejdsordre, livscyklusmodeller for arbejdsordre og arbejdsordretyper. 

## <a name="set-up-functional-location-lifecycle-models"></a>Opsætning af livscyklusmodeller for arbejdssted

Når du har oprettet de livscyklustilstande, der kræves til dine arbejdssteder, kan de opdeles i grupper. Dette gøres for at oprette livscyklusmodelstrømmen, der kan bruges til forskellige typer af arbejdssteder. Der skal som minimum oprettes én standardlivscyklusmodel for arbejdssteder.

1. Vælg **Styring af aktiver** > **Opsætning** > **Arbejdssteder** > **Livscyklusmodeller**.
2. Vælg **Ny** for at oprette en ny livscyklusmodel.
3. Indsæt livscyklusmodel-id'et i feltet **Livscyklusmodel** og et navn til livscyklusmodellen i feltet **Navn**. I felterne **Arbejdsstedstyper** og **Livscyklusstilstande** kan du se antallet af arbejdsstedstyper, der bruger livscyklusmodellen, og det antal tilstande, som er valgt i livscyklusmodellen.
4. I oversigtspanelet **Livscyklustilstande** skal du vælge de tilstande, der skal inkluderes i modellen. Dette gøres ved at klikke på en tilstand i sektionen **Resterende livscyklustilstande** og klikke på knappen ![fremadrettet pil](media/02-setup-for-functional-locations.png).
5. Hvis du vil vælge alle tilgængelige tilstande for en model, skal du klikke på knappen ![Vælg alle tilgængelige faser](media/03-setup-for-functional-locations.png). Alle tilstande overføres til sektionen **Valgte livscyklustilstande**.
6. Hvis du vil fjerne en valgt tilstand fra modellen, skal du vælge tilstanden i afsnittet **Valgte livscyklustilstande** og derefter vælge knappen ![tilbage-pil](media/04-setup-for-functional-locations.png).
7. Vælg **Opdateringer til livscyklustilstande** for at definere de livscyklustilstande, der kan følge en valgt tilstand.
