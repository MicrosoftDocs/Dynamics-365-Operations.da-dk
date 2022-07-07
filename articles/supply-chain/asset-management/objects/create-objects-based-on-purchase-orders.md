---
title: Oprette aktiver baseret på indkøbsordrer
description: Denne artikel forklarer, hvordan du kan oprette en liste over aktivelementer, der kan bruges som grundlag for oprettelse af aktiver til vedligeholdelsesjob i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccd14493aac6484dc54ccf51ae159a071c8697a5
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015603"
---
# <a name="create-assets-based-on-purchase-orders"></a>Oprette aktiver baseret på indkøbsordrer

[!include [banner](../../includes/banner.md)]

 

Denne artikel forklarer, hvordan du kan oprette en liste over aktivelementer, der kan bruges som grundlag for oprettelse af aktiver til vedligeholdelsesjob i Styring af aktiver. På basis af aktivelementerne kan du få vist en oversigt over de indkøbsordrelinjer, der er oprettet på disse elementer. Formålet med denne funktion er nemt at kunne oprette et aktiv i Styring af aktiver baseret på en indkøbsordre.

Først skal du oprette de varer, der skal bruges til at oprette aktiver ud fra en indkøbsordre, i **Aktivelementer**. Når du har oprettet en indkøbsordrelinje, skal du oprette aktiverne i **Ventende aktiver**. Det er muligt at beslutte, på hvilket stadie af indkøbsordren aktivet skal oprettes.


## <a name="select-asset-items"></a>Vælge aktivelementer

1. Klik på **Styring af aktiver** > **Opsætning** > **Aktiver** > **Elementer**.
2. Klik på **Nyt** for at oprette et nyt aktivelement.
3. Vælg elementet i feltet **Varenummer**. Når du forlader dette felt, indsættes varenavnet automatisk i feltet **Produktnavn**.
4. Vælg en aktivtype for varen i oversigtspanelet **Generelt**.
5. Vælg aktivproducent og -model for varen.
6. Gem varen.


## <a name="create-assets-from-pending-assets"></a>Oprette aktiver ud fra ventende aktiver

1. Klik på **Styring af aktiver** > **Aktiver** > **Ventende aktiver**.
2. Du kan se en opdateret liste over indkøbsordrer baseret på de varer, som er valgt i **Aktivelementer**.
3. Du kan filtrere statussen for indkøbsordrer for at vælge, i hvilken livscyklusstilstand aktivet skal oprettes. Du vil måske kun oprette aktiver, når der er bogført en produktkvittering på en indkøbsordre.
4. Vælg **Referencenummer**-linket på en indkøbsordrelinje for at få vist detaljerede oplysninger om varen.
5. Hvis du vil redigere, hvilke dimensioner der vises i oversigtspanelet **Lagerdimensioner**, skal du klikke på knappen **Vis dimensioner** og foretage dine valg.
6. Hvis du vil oprette et aktiv, der er baseret på en indkøbsordrelinje, skal du markere afkrydsningsfeltet i kolonnen **Markér** for den pågældende linje på listesiden og klikke på **Opret aktiver**. Der vises en meddelelse med oplysning om aktiv-id'et.
7. Vælg aktivet på listen **Alle aktiver**, og klik på knappen **Rediger** for at føje yderligere oplysninger til aktivet.
8. Hvis du vil slette en linje i **Ventende aktiver**, fordi du ikke vil oprette et aktiv, skal du markere afkrydsningsfeltet i kolonnen **Markér** for den pågældende linje og klikke på **Kassér ventende aktiver**. Der vises en meddelelse med oplysning om aktiv-id'et. Du sletter ikke indkøbsordren eller salgsordren, men kun den post, som du kunne have oprettet et aktiv for i **Styring af aktiver**.

>[!NOTE]
>Alle produktdimensioner (størrelse, farve, konfiguration osv.) overføres automatisk til aktivattributterne. Sporingsdimensioner (serienummer) gemmes direkte på aktivet, når aktivet oprettes.


## <a name="find-pending-assets"></a>Finde ventende aktiver

Du kan beregne **antal ventende aktiver** for at kontrollere, om der er ventende aktiver. For eksempel kan denne funktion bruges til at modtage en besked, hver gang et ventende aktiv er klar til at blive oprettet som et aktiv.

1. Klik på **Styring af aktiver** > **Periodisk** > **Aktiver** > **Antal ventende aktiver**.
2. Klik på **OK** for at køre jobbet og opdatere listen i **Ventende aktiver**.
3. Du kan konfigurere dette job til at køre som et batchjob, f.eks. en gang om dagen.

**Advarsel!** Hvis data ændres på en indkøbsordre, *efter* at du har oprettet et aktiv baseret på det pågældende element, afspejles disse ændringer ikke på aktivet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]