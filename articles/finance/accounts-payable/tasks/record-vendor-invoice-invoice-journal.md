---
title: Registrere en kreditorfaktura i fakturakladden
description: Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140369"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Registrere en kreditorfaktura i fakturakladden

[!include [banner](../../includes/banner.md)]

Denne opgaveguide viser, hvordan du kan registrere kreditorfakturaer, der ikke er knyttet til indkøbsordrer. Eksempler på denne type faktura omfatter udgifter til vareleverancer og tjenesteydelser.  Denne registrering anvender demofirmaet USMF.

1. Gå til **Navigationsrude > Moduler > Kreditorer > Arbejdsområder > Kreditorfakturapostering**.
2. I **Handlingsruden** skal du klikke på **Ny fakturakladde**.
3. Klik på **Ny**.
4. Indtast kladdenavnet eller klik på rullelisten i feltet **Navn** for at åbne opslaget.
5. Indtast en værdi i feltet **Beskrivelse**.
6. Klik på **Linjer** i **Handlingsrude**. Indtast den bogføringsdato, der opdaterer Finans, i feltet **Dato**.  
7. Angiv **Kreditorkontoen** i feltet **Konto**.
8. Angiv fakturanummeret i feltet **Faktura**.
9. Indtast en værdi i feltet **Beskrivelse**.
10. Angiv et tal i feltet **Kredit**.
11. Indtast kontonummeret, eller klik på rullelisten i feltet **Modkonto** for at åbne opslaget.
    * **Momsgruppe** hentes som standard fra kreditorkontoen.  
    * **Varemomsgruppen** hentes som standard fra den hovedkonto, der er angivet i feltet **Modkonto**.  
    * **Forfaldsdatoen** beregnes på basis af betalingsbetingelserne.  
    * **Kasserabatten** hentes som standard fra kreditorkontoen.  
12. Klik på **Bogfør**.
13. Luk siden.

