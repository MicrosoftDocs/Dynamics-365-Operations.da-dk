---
title: EUR 00015 Konfigurere moms-id
description: Denne fremgangsmåde fører dig gennem forudsætninger for moms-id-registrering,f.eks. oprettelse af en registreringstype og tildeling af denne registreringstype til en registreringskategori.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bf6fe6926a7cc1aecb1f0a2bb7f3c47cc8828e8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144316"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR 00015 Konfigurere moms-id

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde fører dig gennem forudsætninger for moms-id-registrering,f.eks. oprettelse af en registreringstype og tildeling af denne registreringstype til en registreringskategori. Du kan finde flere oplysninger om registrering-id'er og behandling af registrering-id'er , herunder nødvendige forudsætninger, i Hjælp-emnet Registrerings-id'er. 

Oplysningerne her gælder for alle europæiske lande. Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF med Tyskland som primær adresse for den juridiske enhed. Denne opgave er beregnet til systemadministratorer. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

1. Gå til Virksomhedsadministration > Globalt adressekartotek > Registreringstyper > Registreringstyper.
2. Klik på Ny for at åbne dialogboksen Fjern.
3. Skriv "Moms-id" i feltet Navn.
4. Skriv Momsnummer i feltet Beskrivelse.
5. Indtast eller vælg værdien DEU i feltet Land/område
6. Vælg Ja i feltet Entydig.
    * Marker dette afkrydsningsfelt for at kontrollere, om moms-id'et er entydigt.  
7. Vælg Ja i feltet Primært til land/område.
    * Marker dette afkrydsningsfelt, hvis moms-id'et skal gælde for alle de adresser, der hører til det angivne land/område.  
8. Klik på Opret.
9. Klik på Tilføj.
10. Indtast eller vælg værdien ITA i feltet Land/område
11. Skriv '###########' i feltet Format.
    * Når du angiver et registrerings-id af denne type for det valgte land/område, kontrolleres registrerings-id'et i forhold til dette format.  
12. Marker afkrydsningsfeltet Entydig.
    * Marker dette afkrydsningsfelt for at kontrollere, om moms-id'et er entydigt.  
13. Markér afkrydsningsfeltet Primært til land/område.
    * Marker dette afkrydsningsfelt, hvis moms-id'et skal gælde for alle de adresser, der hører til det angivne land/område.  
14. Klik på Gem.
15. Gå til Virksomhedsadministration > Globalt adressekartotek > Registreringstyper > Registreringskategorier.
16. Klik på Ny.
17. Indtast eller vælg Moms-id, DEU i feltet Land/område
18. Vælg 'Moms-id' i feltet Registreringskategori.
    * Tildel den registreringstype, som du oprettede tidligere, til en foruddefineret registreringskategori.  
19. Klik på Ny.
20. Indtast eller vælg Moms-id, ITA i feltet Land/område
21. Vælg 'Moms-id' i feltet Registreringskategori.
    * Tildel den registreringstype, som du har oprettet, til en foruddefineret registreringskategori.  
22. Klik på Gem.

