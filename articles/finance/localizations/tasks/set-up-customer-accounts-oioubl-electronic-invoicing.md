---
title: Konfigurere debitorkonti til elektronisk OIOUBL-fakturering
description: Denne opgave gennemgår, hvordan du konfigurerer en debitorkonto for elektronisk OIOUBL fakturering.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, RegNumTaxIdLookup, smmContactPerson, DirPartyLookup, ContactPersonLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31e588d97b299f674a33193fe9e25b5b731536ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819442"
---
# <a name="set-up-customer-accounts-for-oioubl-electronic-invoicing"></a>Konfigurere debitorkonti til elektronisk OIOUBL-fakturering

[!include [banner](../../includes/banner.md)]

Denne opgave gennemgår, hvordan du konfigurerer en debitorkonto for elektronisk OIOUBL fakturering. 



Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.



Det er den tredje af seks procedurer, der viser processen til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer. Denne opgave bruger eksemplet med OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.

1. Gå til Debitor > Kunder > Alle kunder.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Konto med værdien "US-023".
3. Klik på Rediger.
4. Klik op linket i den valgte række på listen.

## <a name="enable-a-customer-account-for-oioubl-electronic-invoicing"></a>Aktivere en debitorkonto til elektronisk OIOUBL-fakturering
1. Udvid sektionen Faktura og levering.
2. Indtast eller vælg en værdi i feltet SE-nummer.
3. Vælg Ja i feltet eFaktura.
4. Skriv en værdi i feltet EAN. For eksempel "5798000362147".

## <a name="set-up-contact-information-for-a-customer"></a>Konfigurer kontaktoplysninger for en kunde



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]