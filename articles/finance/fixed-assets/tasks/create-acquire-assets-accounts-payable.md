---
title: Oprette og anskaffe aktiver fra Kreditor
description: Denne opgaveguide fører gennem oprettelse og anskaffelse af et anlægsaktiv med indkøbsprocessen.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cb9a37c65fb8eab4db6084b91a71c13a45ba42c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441591"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Oprette og anskaffe aktiver fra Kreditor

[!include [banner](../../includes/banner.md)]

Denne opgaveguide fører gennem oprettelse og anskaffelse af et anlægsaktiv med indkøbsprocessen.  Den bruger bogholder- og kreditorassistenter og demofirmaet USMF.


## <a name="set-fixed-assets-parameters"></a>Konfigurere parametre for anlægsaktiver
1. I **navigationsruden** skal du gå til **Moduler > Anlægsaktiver > Opsætning > Anlægsaktivparametre**.
2. Udvid oversigtspanelet **Indkøbsordrer**.
3. Markér afkrydsningsfeltet **Tillad aktivanskaffelse fra Indkøb**.
4. Markér afkrydsningsfeltet **Opret aktiv under bogføring af produktkvittering eller faktura**.

## <a name="create-a-new-vendor-invoice"></a>Opret en ny kreditorfaktura
1. Gå til **Navigationsrude** **Moduler > Kreditorer > Arbejdsområder > Kreditorfakturapostering**.
2. Klik på **Ny kreditorfaktura**.
3. Klik på rullelisten i feltet **Fakturakonto** for at åbne opslaget.
4. Klik op linket i den valgte række på listen.
5. Skriv en værdi i feltet **Nummer**.
6. Angiv en dato i feltet **Bogføringsdato**.
7. Klik på **Tilføj linje**.
8. Klik på rullelisten i feltet **Varenummer** for at åbne opslaget. Ikke-lagerførte varer eller indkøbskategorier kan bruges til anskaffelse af anlægsaktiver.  
9. Klik op linket i den valgte række på listen.
10. Angiv et tal i feltet **Antal**. En fakturalinje opretter kun ét anlægsaktiv uanset antal. Feltværdien Fakturaantal overføres til anlægsaktivantallet.  
11. Angiv et tal i feltet **Enhedspris**.
12. Vis eller skjul oversigtspanelet **Linjedetaljer**.
13. Klik på fanen **Anlægsaktiver**.
14. Markér afkrydsningsfeltet **Opret et nyt anlægsaktiv**.
15. Klik på rullelisten i feltet **Anlægsaktivgruppe** for at åbne opslaget.
16. Vælg på listen den anlægsaktivgruppe, der skal bruges ved oprettelse af det nye anlægsaktiv.
17. Klik op linket i den valgte række på listen.
18. Klik på **Bogfør**. Anlægsaktivet oprettes og anskaffes, når fakturaen bogføres.  

