---
title: Revidere fakturaer og nøgledata for kreditorer
description: Dette emne viser, hvordan du kan revidere fakturaer og nøgledata for kreditorer.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441443"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Revidere fakturaer og nøgledata for kreditorer

[!include [banner](../../includes/banner.md)]

Når du modtager en faktura fra en leverandør af varer eller tjenester på en indkøbsordre, kræver forretningsprocesserne måske, at varerne eller tjenesterne modtages, før fakturaen kan godkendes til betaling. Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt. 

På siden **Kreditorparametre** skal du sørge for, at indstillingen Aktivér validering af fakturasammenholdelse er valgt, at feltet **Bogfør faktura med uoverensstemmelser** er angivet til **Kræv godkendelse**, og at feltet **Sammenholdelsespolitik for linjer** er angivet til **Trevejs-sammenholdelse**.

Denne procedure bruger demofirmaet USMF. Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.


## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre
1. Gå til **Alle indkøbsordrer**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Kreditorkonto**.
4. Klik på **OK**.
5. Klik på **Tilføj linje**.
6. Indtast en værdi i feltet **Varenummer**.
7. Klik på **Køb** i handlingsruden.
8. Klik på **Bekræft**.

## <a name="post-a-product-receipt"></a>Bogfør en produktkvittering
1. Klik på **Modtag** i handlingsruden.
2. Klik på **Produktkvittering**.
3. Skriv en værdi i feltet **Produktkvittering**.
4. Klik på **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Registrere og sammenholde en kreditorfaktura med en produktkvittering
1. Klik på **Faktura > Faktura** i handlingsruden.
2. Skriv en værdi i feltet **Nummer**.
3. Klik på **Modtag fra: Bestilt antal** for at åbne dialogboksen Fjern.
4. Vælg en indstilling i feltet **Standardmængde for linjer**.
5. Klik på **OK**.
6. Klik på **Ja**.
7. Klik på **Sammenhold produktkvitteringer**.
8. Klik på **OK**.
9. Klik på **Gennemse** i handlingsruden.
10. Klik på **Detaljer om sammenholdelse**.

