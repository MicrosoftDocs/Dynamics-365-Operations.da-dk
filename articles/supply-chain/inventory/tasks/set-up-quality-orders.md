---
title: Konfigurere kvalitetsordrer
description: "Denne fremgangsmåde viser, hvordan du aktiverer en proces til kvalitetsstyring, hvor indgående lager skal undersøges umiddelbart efter modtagelsesregistrering."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-quality-orders"></a>Konfigurere kvalitetsordrer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du aktiverer en proces til kvalitetsstyring, hvor indgående lager skal undersøges umiddelbart efter modtagelsesregistrering. Proceduren udføres normalt af en kvalitetschef. Processen omfatter oprettelse af en kvalitetsgruppe til at definere de varer, der skal udtages, og en testgruppe til at gruppere de test, der skal udføres på varer i kvalitetsgruppen. Du kan køre denne guide i USMF-demodatafirmaet.


## <a name="enable-quality-management"></a>Aktivere kvalitetsstyring
1. Gå til lagerstyring > Opsætning > Parametre til lager- og lagerstedsstyring.
2. Klik på fanen Kvalitetsstyring.
3. Angiv indstillingen Brug kvalitetsstyring til Ja.
4. Klik på Rapportopsætning.
    * Rapportopsætning til kvalitetsstyring er allerede defineret i USMF. Hvis dette ikke var gjort, skulle du tilføje nye linjer her for de forskellige rapporttyper og vælge typen af dokument, der skal bruges til hver rapport.  
5. Luk siden.
6. Luk siden.

## <a name="create-a-test"></a>Oprette en test
1. Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Test.
2. Klik på Ny.
3. Skriv en værdi i feltet Test.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg "Indstilling" i feltet Type.
    * I dette eksempel vil vi vælge "Indstilling", som gør det muligt at tildele testresultaterne, der er baseret på foruddefinerede værdier.  
6. Klik på Gem.
7. Luk siden.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Opret testvariabler for at definere, hvordan testresultaterne registreres
1. Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Testvariabler.
2. Klik på Ny.
3. Skriv en værdi i feltet Variabel.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Gem.
6. Klik på Udfald.
7. Klik på Ny.
8. Skriv en værdi i feltet Udfald.
9. Skriv en værdi i feltet Beskrivelse.
10. Vælg "Bestået" i feltet Status for udfald.
11. Klik på Gem.
12. Klik på Ny.
13. Skriv en værdi i feltet Udfald.
14. Skriv en værdi i feltet Beskrivelse.
15. Klik på Gem.
16. Luk siden.
17. Luk siden.

## <a name="set-up-item-sampling"></a>Konfigurer vareprøve
1. Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Vareprøve.
2. Klik på Ny.
3. Indtast en værdi i feltet Vareprøve.
4. Skriv en værdi i feltet Beskrivelse.
5. Angiv et tal i feltet Værdi.
    * Denne værdi, der er relateret til den angivelse af antal, der er valgt i det tilstødende felt.  
6. Udvid eller skjul sektionen Proces.
7. Marker eller fjern markeringen i afkrydsningsfeltet Fuld spærring.
    * Hvis du vælger denne indstilling, blokeres hele partiet eller ordrelinjeantallet, hvis en test mislykkes. Hvis du ikke vælger den, blokeres kun varerne i kvalitetsordren.  
8. Klik på Gem.
9. Luk siden.

## <a name="create-a-quality-group"></a>Oprette en kvalitetsgruppe
1. Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Kvalitetsgrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Kvalitetsgruppe.
    * Brug et beskrivende navn for at identificere, hvilken form for varer gruppen indeholder (prøvekriterier).  
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Gem.
6. Klik på Tilføj varer.
7. Vælg varenummerrækken
    * I dette eksempel vil filtrering blive kørt baseret på varenummeret.  
8. Skriv en værdi i feltet Kriterier.
    * Skriv f.eks. T* for at filtrere på de varenumre, der begynder med T.  
9. Klik på OK.
10. Klik på OK.
11. Klik på Varekvalitetsgrupper.
12. Luk siden.
13. Luk siden.

## <a name="create-a-test-group"></a>Oprette en testgruppe
1. Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Testgrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Testgruppe.
    * Giv testgruppen et navn, der hjælper dig med at huske, hvilken slags test udføres, og hvilken kvalitetsgruppe den skal knyttes til. For eksempel hvis skal den bruges med en kvalitetsgruppe, der vælger elementer, der starter med "T", kan du kalde den "T-elementtest".  
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg den vareprøvelinje, du oprettede før, i feltet Vareprøve.
6. Find og vælg den ønskede post på listen.
7. Klik på Tilføj.
8. Indtast et tal i feltet Sekvensnummer.
9. Vælg den test, som du oprettede tidligere, i feltet Test.
10. Find og vælg den ønskede post på listen.
11. Klik på fanen Test.
12. Vælg den testvariabel, som du oprettede før, i feltet Variabel
13. Find og vælg den ønskede post på listen.
14. Klik på rullelisten i feltet Standardudfald for at åbne opslaget.
15. Klik op linket i den valgte række på listen.
16. Klik på Gem.
17. Luk siden.

## <a name="define-when-quality-orders-will-be-created"></a>Definere, hvornår der oprettes kvalitetsordrer
1. Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Kvalitetstilknytninger.
2. Klik på Ny.
3. Vælg en indstilling i feltet Referencetype.
4. Vælg "Gruppe" i feltet Varekode:
    * I dette eksempel vælger vi "Gruppe" og bruger den kvalitetsgruppe, vi oprettede før. Du kan også angive denne indstilling til "Tabel" for at angive varerne manuelt eller vælge "Alle" for at føje alle varer til kvalitetsordren.  
5. Vælg den kvalitetsgruppe, du oprettede før, i feltet Vare.
    * De tilgængelige indstillinger i feltet Vare afhænger af, hvad du har angivet i feltet Varekode.  
6. Find og vælg den ønskede post på listen.
7. Udvid eller skjul sektionen Proces.
8. Vælg en indstilling i feltet Hændelsestype.
    * Dette er den hændelse, der udløser testen. De tilgængelige indstillinger her afhænger af, hvilken proces du har valgt i feltet Referencetype.  
9. Vælg en indstilling i feltet Udførelse.
10. Udvid eller skjul sektionen Proces for kvalitetsordre.
11. Klik på rullelisten i feltet Hændelsesspærring for at åbne opslaget.
    * Dette felt viser en liste over processer, som det er muligt at blokere, hvis kvalitetsordren stadig er åben. Indstillingerne afhænger af, hvad du har valgt i feltet Hændelsestype.  
12. Klik op linket i den valgte række på listen.
    * Dette vil være afhængigt af de tidligere valgte værdier. Markér, hvis følgende processer skal blokeres, mens du har åbne kvalitetsordrer, der er knyttet til en kildedokumentlinje.  
13. Udvid eller skjul sektionen Specifikationer.
14. Vælg den testgruppe, som du oprettede før, i feltet Testgruppe.
15. Find og vælg den ønskede post på listen.
16. Klik på Gem.
17. Luk siden.

