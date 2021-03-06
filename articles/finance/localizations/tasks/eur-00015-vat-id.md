---
title: EUR 00015 Konfigurere moms-id
description: Denne fremgangsmåde fører dig gennem forudsætninger for moms-id-registrering,f.eks. oprettelse af en registreringstype og tildeling af denne registreringstype til en registreringskategori.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5488bb020209d6bf6fb39ae0b4f897f5513bdf93
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821797"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR 00015 Konfigurere moms-id

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde fører dig gennem forudsætninger for moms-id-registrering,f.eks. oprettelse af en registreringstype og tildeling af denne registreringstype til en registreringskategori. Du kan finde flere oplysninger om registrering-id'er og behandling af registrering-id'er , herunder nødvendige forudsætninger, i Hjælp-emnet Registrerings-id'er. 

Oplysningerne her gælder for alle europæiske lande/områder. Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF med Tyskland som primær adresse for den juridiske enhed. Denne opgave er beregnet til systemadministratorer. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]