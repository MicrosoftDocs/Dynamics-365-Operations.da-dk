---
title: Oprette og bogføre en debitorfaktura for en debitor i den offentlige sektor
description: Denne procedure hjælper dig med at oprette og bogføre en salgsordrefaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, ContactPersonLookup, SalesEditLines,  CustInvoiceJournal, ERFormatMappingRunJobTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 101294c3cf1a1fe7e25f6e43a24c079e2e39d0e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990015"
---
# <a name="create-and-post-a-customer-invoice-for-a-public-sector-customer"></a>Oprette og bogføre en debitorfaktura for en debitor i den offentlige sektor

[!include [banner](../../includes/banner.md)]

Denne procedure hjælper dig med at oprette og bogføre en salgsordrefaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering. 



Den blev oprettet ved hjælp af demodatafirmaet USMF med primær adresse for en juridisk enhed i Danmark.



Det er den femte af seks procedurer, der viser den afsluttende proces til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer. Den er baseret på OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge. Du kan finde mindre forskelle for andre landespecifikke e-fakturaimplementeringer, som spansk eller italiensk, i tilgængelige WIKI-artikler.



Før du kan udføre denne procedure, skal du udføre følgende procedurer: 'Importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering', 'Konfigurere elektronisk OIOUBL-fakturering' og 'Konfigurere en debitorkonto til elektronisk OIOUBL-fakturering'.


## <a name="create-a-sales-order"></a>Oprette en salgsordre
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
    * Vælg en kunde, der er aktiveret til elektronisk fakturering.  
4. Klik på OK.
5. Vælg en visning for salgsordreoverskrift.
6. Indtast eller vælg en værdi i feltet Kontakt.
7. Skriv en værdi i feltet Debitorrekvisition.
8. Skriv en værdi i feltet Kundereference.
9. Udvid sektionen Konfiguration.
10. Vælg en visning for salgsordrelinje.
11. Indtast eller vælg en værdi i feltet Varenummer.
    * Du kan bruge varenummer 'D0001'.  
12. Klik på Gem.

## <a name="post-an-invoice-for-a-sales-order"></a>Bogføre en faktura for en salgsordre
1. Klik på Faktura i handlingsruden.
2. Klik på Faktura.
3. Udvid sektionen Parametre.
4. Vælg "Alle" i feltet Antal.
5. Klik på OK.
6. Klik på OK.

## <a name="generate-oioubl-electronic-invoice"></a>Oprette elektronisk OIOUBL faktura
1. Klik på Faktura.
2. Klik på Faktura i handlingsruden.
3. Klik på Send.
4. Klik på Oprindelig.

## <a name="view-an-oioubl-electronic-invoice"></a>Se en elektronisk OIOUBL faktura
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Elektroniske rapporteringsjob.
2. Klik på Vis filer.
3. Klik på Åbn.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]