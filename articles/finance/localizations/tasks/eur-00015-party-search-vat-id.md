---
title: EUR-00015 Parts søgning ved hjælp af moms-id
description: Denne fremgangsmåde viser, hvordan du fuldfører søgning efter en part ved hjælp af et registrerings-id.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
ms.openlocfilehash: 0688de30327abe0925efe3daf44bcbab8a096c97
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288470"
---
# <a name="eur-00015-party-search-using-vat-id"></a>EUR-00015 Parts søgning ved hjælp af moms-id

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du fuldfører søgning efter en part ved hjælp af et registrerings-id. Før du kan udføre denne procedure, skal du konfigurere moms-id'er og angive moms-id'er for kreditorer, debitorer eller juridiske enheder.

Denne procedure gælder for alle europæiske lande/områder. Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland. Denne fremgangsmåde er beregnet til en kreditorchef eller debitorchef. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

1. Gå til Virksomhedsadministration > Globalt adressekartotek > Globalt adressekartotek.
2. Klik på Søgning efter registrerings-id.
3. Klik på Tilføj.
4. Indtast eller vælg en værdi i feltet Registreringstype.
    * Hvis du f.eks. vil finde parter med et registrerings-id af typen moms-id, skal du vælge moms-id.  
5. Indtast eller vælg en værdi i feltet Land/område.
    * Angiv for eksempel DEU.  
6. Skriv en værdi i feltet Registreringsnummer.
7. Klik på Søg.
    * Alle parter med dette registrerings-id vises.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
