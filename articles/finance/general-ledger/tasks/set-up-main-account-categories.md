---
title: Konfigurere hovedkontokategorier
description: I dette emne beskrives, hvordan du konfigurerer hovedkontokategorier i Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144783"
---
# <a name="set-up-main-account-categories"></a>Konfigurere hovedkontokategorier

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer hovedkontokategorier. Hovedkontokategorier bruges til standardrapporter i økonomisk rapportering og Power BI. Hovedkontokategorier, der oprettes som standard, kan omdøbes, men ikke slettes. Yderligere kontokategorier kan oprettes og bruges til rapportering og analyse. I dette emne demofirmaet USMF.

## <a name="create-a-main-account-category"></a>Opret en hovedkontokategori
1. Gå i navigationsruden **Moduler > Finans > Kontoplan > Konti > Hovedkontokategorier**.
2. Vælg **Ny**.
3. Angiv et entydigt navn i feltet **Hovedkontokategori**.
4. Angiv en beskrivelse af hovedkontokategorien i feltet **Beskrivelse**.
5. I feltet **Hovedkontotype** skal du vælge den hovedkontotype, der skal knyttes til kategorien.

## <a name="link-main-accounts-to-account-category"></a>Link hovedkonti til kontokategori
1. Klik på **Sammenkæd hovedkonti**.
2. På listen skal du vælge de hovedkonti, der skal knyttes til hovedkontokategorien, ved at markere felterne i kolonnen **Tilknyttet**. Hvis du tildeler hovedkonti til en hovedkontokategori, samles saldiene for kontiene, når denne kategori bruges til finansiel rapportering og analyse.  
3. Markér eller fjern markeringen af indstillingen **Tilknyttet** for at vælge hovedkontiene.
4. Vælg **OK**.
5. Vælg **Ja**.
