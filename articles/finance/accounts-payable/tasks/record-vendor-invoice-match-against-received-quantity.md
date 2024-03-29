---
title: Registrere kreditorfaktura og sammenligne med modtaget antal
description: Når du modtager en faktura fra en leverandør af varer eller tjenester på en indkøbsordre, kræver forretningsprocesserne måske, at varerne eller tjenesterne modtages, før fakturaen kan godkendes til betaling.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: debf8ca47666252633e67e2592acd5a4e4122403
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778672"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Registrere kreditorfaktura og sammenligne med modtaget antal

[!include [banner](../../includes/banner.md)]

Når du modtager en faktura fra en leverandør af varer eller tjenester på en indkøbsordre, kræver forretningsprocesserne måske, at varerne eller tjenesterne modtages, før fakturaen kan godkendes til betaling. Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt. 

På siden **Kreditorparametre** skal du sørge for, at indstillingen **Aktivér validering af fakturasammenholdelse** er valgt, at feltet **Bogfør faktura med uoverensstemmelser** er angivet til **Kræv godkendelse**, og at feltet **Sammenholdelsespolitik for linjer** er angivet til **Trevejs-sammenholdelse**.

Denne procedure bruger demofirmaet USMF. Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.


## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre
1. Gå til **Alle indkøbsordrer**.
2. Klik på **Ny**.
3. I feltet **Kreditorkonto** skal du klikke på rullelisten for at åbne opslaget.
4. Skriv en værdi i feltet **Kreditorkonto**.
5. Klik på **OK**.
6. Klik på **Tilføj linje**.
7. Indtast en værdi i feltet **Varenummer**.
8. Klik på **Køb** i handlingsruden.
9. Klik på **Bekræft**.

## <a name="post-a-product-receipt"></a>Bogfør en produktkvittering
1. Klik på **Modtag** i handlingsruden.
2. Klik på **Produktkvittering**.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet **Produktkvittering**.
5. Klik på **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Registrere og sammenholde en kreditorfaktura med en produktkvittering
1. Klik på **Faktura** i handlingsruden.
2. Klik på **Faktura**.
3. Skriv en værdi i feltet **Nummer**.
4. Klik på **Modtag fra: Bestilt antal** for at åbne dialogboksen Fjern.
5. Vælg en indstilling i feltet **Standardmængde for linjer**.
6. Klik på **OK**.
7. Klik på **Ja**.
8. Klik på **Sammenhold produktkvitteringer**.
9. Klik på **OK**.
10. Klik på **Gennemse** i handlingsruden.
11. Klik på **Detaljer om sammenholdelse**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
