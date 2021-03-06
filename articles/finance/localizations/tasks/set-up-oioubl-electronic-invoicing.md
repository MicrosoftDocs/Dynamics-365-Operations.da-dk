---
title: Konfigurere elektronisk OIOUBL-fakturering
description: Denne procedure gennemgår, hvordan du konfigurerer elektronisk OIOUBL fakturering.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, OMLegalEntity, UnitOfMeasure, ExtCodeTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab2aa7d0e4e0937db365b3735ecb8f8a94ca2897
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832458"
---
# <a name="set-up-oioubl-electronic-invoicing"></a>Konfigurere elektronisk OIOUBL-fakturering

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]