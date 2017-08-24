--- 
title: "Udstede et EU-indførselscertifikat"
description: "Denne procedure fører dig gennem aktivering af et EU-posteringscertifikat og konfiguration af en debitorkonto for at bruge indførselscertifikater og udstede et certifikat."
author: mrolecki
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1eca89c0588b3611cdd3ac5a62b5ac95c83c8e62
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="issue-an-eu-entry-certificate"></a>Udstede et EU-indførselscertifikat

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fører dig gennem aktivering af et EU-posteringscertifikat og konfiguration af en debitorkonto for at bruge indførselscertifikater og udstede et certifikat. Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.


## <a name="enable-entry-certificate-management"></a>Aktivér administration af indførselscertifikater
1. Gå til Debitor > Opsætning > Debitorparametre.
2. Klik på fanen Forsendelser.
3. Udvid sektionen Postcertifikat.
4. Vælg Ja i feltet Aktivér administration af indførselscertifikater.
5. Vælg Ja i feltet Aktivér udstedelse af indførselscertifikater.
6. Klik på fanen Nummerserier.
7. Find og vælg rækken Postcertifikat på listen.
8. Skriv eller vælg en værdi i feltet Nummerseriekode.

## <a name="set-up-a-customer"></a>Oprette en kunde
1. Gå til Debitor > Kunder > Alle kunder.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Konto med værdien "DE-015".
3. Åbn kundens kontooplysninger.
4. Klik på Rediger.
5. Udvid sektionen Faktura og levering.
6. Vælg Ja i feltet Postcertifikat er påkrævet.
7. Vælg Ja i feltet Udsted indførselscertifikat.
8. Klik på Gem.

## <a name="create-an-eu-entry-certificate-automatically"></a>Oprette et EU-posteringscertifikat automatisk
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
4. Klik på OK.
5. Indtast eller vælg en værdi i feltet Varenummer.
6. Klik på Gem.
7. Klik på fanen Pluk og pak i handlingsruden.
8. Klik på Bogfør følgeseddel.
9. Udvid sektionen Parametre.
10. Vælg "Alle" i feltet Antal.
11. Fjern markeringen i feltet Udsted indførselscertifikat.
    * Et postcertifikat kan udstedes, når følgesedlen bogføres eller under fakturering. Lad afkrydsningsfeltet Udsted indførselscertifikat være umarkeret for at udstede det senere.  
12. Klik på OK.
13. Klik på OK.
14. Klik på Faktura i handlingsruden.
15. Klik på Faktura.
    * Kontroller, at afkrydsningsfelterne Postcertifikat er påkrævet og Udsted indførselscertifikat i afsnittet Oversigt.  Du kan også markere afkrydsningsfeltet Udskriv indførselscertifikat for at tillade udskrivning af certifikatet.  
16. Klik på OK.
17. Klik på OK.
18. Klik på Faktura i handlingsruden.
19. Klik på Faktura.
20. Klik på Faktura i handlingsruden.
21. Klik på Vis udstedte indførselscertifikater.
22. Klik på Udskriv.
23. Luk siden.
24. Klik på Skift status.
25. Vælg en indstilling i feltet Ny status.
26. Klik på OK.
27. Luk siden.

## <a name="create-an-eu-entry-certificate-manually"></a>Oprette et EU-posteringscertifikat manuelt
1. Klik på Faktura i handlingsruden.
2. Klik på Opret indførselscertifikat.
3. Klik på OK.
4. Klik på Faktura i handlingsruden.
5. Klik på Vis udstedte indførselscertifikater.


