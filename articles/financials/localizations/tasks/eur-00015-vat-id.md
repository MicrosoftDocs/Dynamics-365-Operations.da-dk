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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66ee7215dc21921f9d8e405c3f77d9b5e0b89a9e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556601"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR 00015 Konfigurere moms-id

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

