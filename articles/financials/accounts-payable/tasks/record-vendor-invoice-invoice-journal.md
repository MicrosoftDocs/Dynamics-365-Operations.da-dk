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
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837006"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Registrere en kreditorfaktura i fakturakladden

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

