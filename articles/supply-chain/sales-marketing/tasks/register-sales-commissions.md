--- 
title: Registrere salgskommissioner
description: Denne procedure viser, hvordan salgsprovisioner beregnes og registreres.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5535f1627526b97ddc9ca2c210db4e332782d656
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="register-sales-commissions"></a>Registrere salgskommissioner

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan salgsprovisioner beregnes og registreres. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. Før du starter denne vejledning, skal du køre vejledningen "Konfigurer regler for salgsprovision" for at sikre, at du har den nødvendige provisionsberegningsopsætning.

Notér de kunde- og varenumre, du har valgt til provisionsprocessen, og brug dem, når du bliver bedt om at oprette en salgsordre i denne vejledning.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Fakturere en salgsordre, der kvalificerer en sælger til en provision
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på OK.
7. Klik på Indstillinger i handlingsruden.
8. Klik på Skift visning.
9. Klik på Overskriftsvisning.
10. Udvid sektionen Konfiguration.
    * Værdien i feltet Salg repræsenterer en gruppe med en eller flere sælgere, der knyttet til den. Personerne i gruppen er dem, der modtager provision, når ordren faktureres i henhold til foruddefinerede satser og fordeling.   Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.  Gruppen Salg kopieres også til salgsordrelinjen. Du kan ændre den, så den er anderledes end den i hovedet og/eller mellem linjerne.  
    * Værdien i feltet Provisionsgruppe repræsenterer en gruppe, du har oprettet for en eller flere kunder med det formål at spore provisioner.   Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.   
11. Klik på Indstillinger i handlingsruden.
12. Klik på Skift visning.
13. Klik på Linjevisning.
14. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
15. Vælg den vare, du har angivet for provisioner, på listen. 
16. Angiv et tal i feltet Antal.
    * Bemærk linjens nettobeløb. Det repræsenterer salgsindtægter, som i dette eksempel danner grundlag for provisionsberegningen.  
17. Klik på Gem.
18. Klik på Faktura i handlingsruden.
19. Klik på Faktura.
20. Udvid sektionen Parametre.
21. Vælg "Alle" i feltet Antal.
22. Vælg Ja i feltet Bogføring.
23. Klik på OK.
24. Klik på OK.
    * Det kan tage omkring et minut at bogføre transaktionen. Vent på, at behandlingen fuldføres, og luk ikke siden.  

## <a name="review-the-registered-sales-commissions"></a>Gennemse de registrerede salgsprovisioner
1. Klik på Faktura i handlingsruden.
2. Klik på Faktura.
3. Klik på Faktura i handlingsruden.
4. Klik på Provisionsposter.
    * Fanen Oversigt viser linjer, der repræsenterer provisionsbeløb, der skal betales til sælgere, der er knyttet til fakturerede salgsordrer. Lad os se nærmere på det.     
    * Hvis du har brugt guiden "Konfigurer regler for salgsprovision" til at konfigurere provisionssalgsgruppen, er der to sælgere, som skal modtage en salgsprovision, og provisionen deles ligeligt mellem dem.  
    * I dette eksempel beregnes det samlede provisionsbeløb som en procentdel af salgsindtægterne (nettobeløbet på ordrelinjen).   
5. Luk siden.
6. Klik på Bilag.
    * Du kan gennemgå bilagsposteringer for provisionsbeløb, der er bogført til de foruddefinerede provisionsudgifts- og -kreditorkonti.  


