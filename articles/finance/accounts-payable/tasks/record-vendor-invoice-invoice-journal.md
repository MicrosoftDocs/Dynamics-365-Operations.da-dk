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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18d8b74bd8783c23e548a3185414d1461bc1d869
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971822"
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
12. Hvis du har aktiveret arbejdsgang for kreditorfakturakladde, skal du klikke på **Aarbejdsgang > Send**.
    * Når din afsendelse er godkendt, vil datoen blive forskudt til den første dag i den næste åbne periode, hvis posteringsdatoen for bogføring ligger inden for en periode, der er sat i venteposition eller er lukket for finanskontering.
12. Klik på **Bogfør**.
13. Luk siden.

