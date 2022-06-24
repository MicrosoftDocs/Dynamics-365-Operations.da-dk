---
title: Konfigurere hovedkontokategorier
description: Denne artikel beskriver, hvordan du konfigurerer hovedkontokategorier i Dynamics 365 Finance.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c48011c9988bdca694851476540db574efef7909
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879557"
---
# <a name="set-up-main-account-categories"></a>Konfigurere hovedkontokategorier

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer hovedkontokategorier. Hovedkontokategorier bruges til standardrapporter i økonomisk rapportering og Power BI. Hovedkontokategorier, der oprettes som standard, kan omdøbes, men ikke slettes. Yderligere kontokategorier kan oprettes og bruges til rapportering og analyse. Denne artikel anvender demofirmaet USMF.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
