--- 
title: Konfigurere elektronisk OIOUBL-fakturering (Danmark)
description: "Denne procedure gennemgår, hvordan du konfigurerer elektronisk OIOUBL fakturering."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a9ab627a4c1e5f9d7f335b408bb124f01e70e396
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-oioubl-electronic-invoicing-denmark"></a>Konfigurere elektronisk OIOUBL-fakturering (Danmark)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure gennemgår, hvordan du konfigurerer elektronisk OIOUBL fakturering. 



Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.



Det er den anden af seks procedurer, der viser processen til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer. Denne opgave bruger eksemplet med OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.

Før du kan udføre denne opgave, skal du importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering.


## <a name="set-up-electronic-invoice-formats"></a>Angive formater for elektroniske fakturaer
1. Gå til Debitor > Opsætning > Debitorparametre.
2. Klik på fanen Elektroniske dokumenter.
3. Udvid sektionen Elektronisk rapportering.
4. I feltet Salgs- og fritekstfaktura skal du angive eller vælge en værdi.
    * Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument. Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.  
5. I feltet Salgs- og fritekstkreditnota skal du angive eller vælge en værdi.
    * Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument. Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.  
6. Indtast eller vælg en værdi i feltet Projektfaktura.
    * Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument. Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.  
7. Indtast eller vælg en værdi i feltet Projektkreditnota.
    * Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument. Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.  
8. Klik på Gem.

## <a name="set-up-a-legal-entity"></a>Konfigurer en juridisk enhed
1. Gå til Virksomhedsadministration > Organisationer > Juridiske enheder.
2. Klik på Rediger.
3. Udvid sektionen Bankkontooplysninger.
4. Skriv en værdi i feltet Registreringsnummer.
    * Indtast for eksempel 12070918.  
5. Udvid sektionen Momsregistrering.
6. Skriv en værdi i feltet Momsregistreringsnummer.
    * Indtast for eksempel 55568510.  

## <a name="set-up-external-codes-for-units-of-measure"></a>Definere eksterne koder for måleenheder
1. Gå til Virksomhedsadministration > Konfiguration > Enheder > Enheder.
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Enhed med værdien 'pcs'.
3. Klik på Eksterne koder.
4. Markér den valgte række på listen.
5. Skriv en værdi i feltet Kode.
    * Skriv f.eks. PCSEA.  
6. Indtast en værdi i feltet Ekstern kodedefinition. For eksempel OIOUBL EA-kode.
7. Marker afkrydsningsfeltet Standardkode.
8. Klik på Tilføj.
9. Skriv en værdi i feltet Værdi.
    * Skriv f.eks. EA.  
10. Klik på Gem.


