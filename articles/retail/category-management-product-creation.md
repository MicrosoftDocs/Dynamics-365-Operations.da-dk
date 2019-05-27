---
title: Administrere produktkategorier og produkter i Retail
description: I dette emne beskrives, hvordan markedsføringschefer kan bruge detailproduktkategorier til at administrere relationer mellem detailprodukthierarkiet og oplysninger om frigivne produkter.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553618"
---
# <a name="manage-retail-product-categories-and-products"></a>Administrere produktkategorier og produkter i Retail

[!include [banner](./includes/banner.md)]

Dette emne beskriver en forbedret metode til styring af Retail-produktkategorier og produkter i Microsoft Dynamics 365 for Retail. Disse forbedringer giver markedsføringschefer mulighed for at se en fælles struktur for produktegenskaber, der deles mellem produkthierarkiet i Retail og frigivne produktdetaljer.

Yderligere oplysninger om administration af detailproduktkategorier i arbejdsområdet **Kategori og produktstyring**, skal du vælge feltet **Detailprodukthierarki**.

Bemærk, at den forbedrede struktur på siden **Detailprodukthierarki** vises. I tidligere versioner af Retail var produktegenskaberne inddelt i *Grundlæggende produktegenskaber* og *Egenskaber for detailprodukt*, baseret på omfanget af deres anvendelighed. Egenskaber for detailprodukt er *globale* i omfanget af deres anvendelighed. For en bestemt produktegenskab i Retail deles den samme værdi således på tværs af alle juridiske enheder. I modsat fald er de grundlæggende produktegenskaber *specifikke for den juridiske enhed*. For en given grundlæggende produktegenskab kan værdien med andre ord variere på tværs af juridiske enheder baseret på de enkelte forretningsbehov for hver juridisk enhed.

I den forbedrede struktur for produktkategorier i Retail er produktegenskaber logisk adskilte ud fra deres anvendelighed i en gruppe, så de afspejler detaljeformstrukturen formularstrukturen for de frigivne produktegenskaber.

![Felterne grupperes ud fra egenskabernes anvendelighed](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Du kan skifte mellem at administrere egenskaber, der er specifikke for juridiske enheder på tværs af alle juridiske enheder og administrere dem for en bestemt juridisk enhed.

For at administrere egenskaber på tværs af alle juridiske enheder skal du vælge **Vis for alle juridiske enheder** (eller **Rediger for alle juridiske enheder**).

![Få vist eller redigere for alle juridiske enheder](media/ToggleBackToEditForSpecificLegalEntity.PNG)

For at administrere egenskaberne for en bestemt juridisk enhed, skal du vælge **Vis for en bestemt juridisk enhed** (eller **Rediger for en bestemt juridisk enhed**).

![Få vist og redigere for en bestemt juridisk enhed](media/ToggleToEditForAllLegalEntities.PNG)

Derudover kan en markedsføringschef i den forbedrede struktur for detailproduktkategorier nu også definere standardværdier for et ekstra sæt produktegenskaber for det enkelte kategoriniveau. Når der derefter oprettes produkter, bliver de tildelt standardværdierne for deres produktegenskaber ud fra tilknytningen af disse egenskaber til en bestemt kategori i produkthierarkiet i Retail. Disse nedarvede produktegenskaber kan også ændres for hvert produkt for at opfylde individuelle virksomhedsbehov.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Valg af egenskaber til opdatering af produkter på siden Detailprodukthierarki

Du kan bruge den nye forbedrede struktur for produktegenskaber til at vælge, hvilke opdaterede produktegenskaber der skal anvendes til de tilknyttede produkter. På siden **Detailprodukthierarki** i handlingsruden skal du vælge **Kategori**. Vælg derefter **Opdater produkter** for at åbne dialogboksen **Opdater produkter**.

![Dialogboksen Opdater produkter](media/NewUpdateProductsEnhancedView.PNG)
