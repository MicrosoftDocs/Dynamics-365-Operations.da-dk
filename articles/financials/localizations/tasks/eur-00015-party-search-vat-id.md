---
title: EUR-00015 Parts søgning ved hjælp af moms-id
description: Denne fremgangsmåde viser, hvordan du fuldfører søgning efter en part ved hjælp af et registrerings-id.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3cb847d4950b02aa7392cd3b307934b008d5e1c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537708"
---
# <a name="eur-00015-party-search-using-vat-id"></a>EUR-00015 Parts søgning ved hjælp af moms-id

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du fuldfører søgning efter en part ved hjælp af et registrerings-id. Før du kan udføre denne procedure, skal du konfigurere moms-id'er og angive moms-id'er for kreditorer, debitorer eller juridiske enheder.

Denne procedure gælder for alle europæiske lande. Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland. Denne fremgangsmåde er beregnet til en kreditorchef eller debitorchef. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

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

