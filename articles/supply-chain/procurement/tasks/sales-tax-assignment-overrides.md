---
title: Tildeling og tilsidesættelser af moms
description: Denne procedure viser, hvordan du kan tildele momsgrupper til handelskanaler.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207582"
---
# <a name="sales-tax-assignment-and-overrides"></a>Tildeling og tilsidesættelser af moms

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan tildele momsgrupper til handelskanaler. Den gennemgår også processen til oprettelse af en ny momsændring og tildeling af ændringen til en eksisterende momsændringsgruppe. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.
2. På listen skal du klikke på linket Kanal-id for "Houston".
3. Klik på Rediger.
    * Feltet "Momsgruppe" indeholder listen over momsgrupper for det aktuelle firma. Den aktuelt tildelte gruppe er en generisk momsgruppe i "Texas". Der findes også momsgrupper for "Washington" og "Washington, King County." Momsgrupper kan omfatte afgifter til flere kommuner.  
    * Feltet "Momsændring" er det sted, hvor momsændringsgrupper kan knyttes til kanalen. Momsændringsgrupper kan bruges til at gruppe momsændringer, der fungerer for flere butikker. I stedet for at tildele momsændringer én ad gangen manuelt kan gruppen oprettes og tildeles direkte til kanalerne for at spare tid.  
4. Klik på Gem.
5. Luk siden.
6. Gå til Retail og Commerce > Konfiguration af kanal > Moms > Momsændringer.
7. Klik på Ny.
8. Angiv et navn til din nye ændring i feltet Momsændring.
9. Angiv en beskrivelse af ændringen i feltet Beskrivelse.
10. Angiv status til "Aktivér".
11. Vis eller skjul sektionen Tilsidesæt.
12. Vælg en indstilling i feltet Type.
    * Varemomsgrupper kan bruges til at tilsidesætte moms for bestemte varer, der tilhører gruppen. For eksempel beskattes fødevarer normalt på en anden måde end varige forbrugsgoder og vil sandsynligvis have sin egen momsgruppe. Momsgrupper er grupper af skatter og afgifter, der gælder for en bestemt kanal. Hvis en kanal f.eks. sælger både detail og til andre virksomheder, kan der bruges forskellige varemomsgrupper. Alle gældende afgifter ville være tilknyttet momsgruppen.  
    * Nu kan du vælge afgifterne "Fra" og "Til" eller "Fra momsgruppe" og "Til momsgruppe" for at oprette din momsændring. Feltet "Fra" angiver den moms eller momsgruppe, der skal ændres. Ændring af varemomsgruppen giver andre indstillinger end ændring af en momsgruppe. Momsændringer kan konfigureres til at ændre moms på hele posteringer eller på bestemte linjer i transaktionen.  
13. Klik på Gem.
14. Luk siden.
15. Gå til Retail og Commerce > Konfiguration af kanal > Moms > Momsændringsgrupper.
    * I dette trin tildeler du den nyoprettede momsændring til den momsændringsgruppe, der er tildelt Houston-kanalen.  
16. Klik på Rediger.
17. Udvid eller skjul sektionen Konfiguration.
18. Klik på Tilføj.
19. Klik på rullelisten i feltet Momsændring for at åbne opslaget.
20. Vælg den tidligere oprettede momsændring på listen.
21. Klik op linket i den valgte række på listen.
22. Klik på Gem.

