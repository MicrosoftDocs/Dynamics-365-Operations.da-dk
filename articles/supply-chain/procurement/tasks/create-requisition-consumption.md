---
title: Oprette en forbrugsrekvisition
description: I dette emne beskrives processen til oprettelse af en rekvisition.
author: mkirknel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2948282d8b40f7d34ffbae072a195cf954ab6e2
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738898"
---
# <a name="create-a-requisition-for-consumption"></a>Oprette en forbrugsrekvisition

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives processen til oprettelse af en rekvisition. Den viser forskellige måder at søge efter produkter i indkøbskataloget, og hvordan du tilføjer et produkt, der ikke findes i kataloget. Inden du begynder denne procedure, skal du have en indkøbspolitik, der er konfigureret med Forbrug som standardtypen for rekvisitionen. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data. Proceduren kan kun udføres af en brugerprofil, der er angivet som arbejder. Denne opgave vil normalt udføres af en medarbejder. **Medarbejder**-sikkerhedsrollen tillader, at du kan udføre opgaverne, eller hvis du bruger USMF, kan du logge på som **Alicia**.


## <a name="create-a-new-requisition"></a>Opret en ny rekvisition
1. Gå til **Navigationsrude > Moduler > Indkøb og forsyning > Indkøbsrekvisitioner > Indkøbsrekvisitioner, der er udarbejdet af mig**.
2. Vælg **Ny**.
3. Angiv et navn for rekvisitionen i feltet **Navn**.
4. Angiv en dato i feltet **Ønsket dato**. Som standard kopieres den ønskede dato og regnskabsdatoen til indkøbsrekvisitionslinjerne. De kan ændres på linjeniveau. Den ønskede dato er den leveringsdato, der er anmodet om.  
5. Angiv en dato i feltet **Regnskabsdato**. Regnskabsdatoen bruges til registrering af regnskabsposten i finans og til at kontrollere, om budgetmidlerne er tilgængelige.  
6. Vælg **OK**.
7. Vælg en indstilling på rullelisten i feltet **Årsag**. Den forretningsberettigelsesårsag, som du vælger, vises som standard for indkøbsrekvisitionslinjerne, men du kan ændre den på linjeniveau.  
8. Vælg årsagen.
9. Angiv en mere beskrivende begrundelse for rekvisitionen i feltet til **detaljer**.

## <a name="add-a-line-to-the-requisition"></a>Føj en ny linje til rekvisitionen.
1. Vælg **Tilføj linje**. Der er to måder at føje linjer til indkøbsrekvisitionen på. Hvis du allerede kender produktnummeret, eller du allerede ved, at du anmoder om et produkt, der ikke findes i produktkataloget, kan du tilføje linjen direkte med **Tilføj linje**. Den anden måde er at bruge **Tilføj produkter**, hvor du kan bruge søgning og filtrering til at finde varer i produktkataloget.    
2. Vælg den række, du lige har oprettet.
    - Anmoderen er den arbejder, der har anmodet om rekvisitionen.   
    - Den person, der forbereder rekvisitionen, er som standard den arbejder, der har anmodet om den. Der skal gives tilladelse til at forberede en rekvisitionslinje på vegne af en anden arbejder. Hvis du har sådanne tilladelser, vises de andre arbejdere i dette opslag.  
3. Indtast en værdi i feltet **Varenummer**. De varer, du kan vælge, er begrænset af kategoriadgangspolitik og indkøbskataloget for den juridiske indkøbsenhed.   
4. Angiv et tal i feltet **Antal**.

## <a name="add-more-products-to-the-requisition"></a>Føj flere produkter til rekvisitionen
1. Vælg **Tilføj produkter**. Dette er indstillingen, hvor du kan søge efter produkter i produktkataloget.    
2. Skriv den første del af navnet på den kategori, du søger efter, i feltet **Find indkøbskategorinode**, og vælg derefter **Angiv**. Angiv for eksempel `comput`.  
3. Brug genvejen **InvokeDefaultButton**.
4. I den valgte kategori skal du bruge **Filter** til filtrering af listen over produkter.
5. Vælg det produktkort, der skal føjes til rekvisitionen.
6. Vælg **Tilføj til linjer**.
7. Angiv et tal i feltet **Antal**.
8. Skriv den første del af navnet på den kategori, du søger efter, i feltet **Find indkøbskategorinode**, og vælg derefter **Angiv**. Skriv eksempelvis `High` (overstregningstuscher).  
9. Brug genvejen **InvokeDefaultButton**.
10. Vælg **Tilføj ikke-angivet produkt til linjer** for at tilføje et produkt, der ikke findes i indkøbskataloget.
11. Skriv en værdi i feltet **Produktnavn**.
12. I feltet **Enhed** skal du angive en værdi.
13. Vælg **OK**.
14. Tilføj en beskrivelse af produktet i feltet **Varebeskrivelse**.
15. Angiv et tal i feltet **Antal**.
16. Angiv et tal i feltet **Enhedspris**. Hvis du kender prisen for en bestemt leverandør (som du vælger i feltet kreditorkonto), kan denne pris indtastes.   
17. I feltet **Kreditorkonto** skal du åbne rullelisten for at vælge en indstilling. De kreditorer, der findes i dette felt, afhænger af de indkøbspolitikker og den status, som kreditoren har for den aktuelle indkøbskategori. Som et alternativ til valg af kreditor her kan du vælge **Foreslå kreditor**.    
18. Vælg den kreditor, du vil bruge, på listen.
19. Skriv en værdi i feltet **Eksternt varenummer**. Dette er et referencenummer til det produkt, der er kendt af kreditoren. Dette kan eksempelvis være varenummeret for produktet i kreditorens eget katalog.  
20. Vælg **OK**.

## <a name="distribute-amounts"></a>Fordel beløb
1. Vælg **Finans**.
2. Vælg **Fordel beløb**. Denne fremgangsmåde viser, hvordan du fordeler omkostningerne for den første linje mellem 2 konti. Dette kan også foretages senere, når rekvisitionen er til gennemsyn.  
3. Vælg **Opdel** for at oprette en ny fordelingslinje.
4. Vælg den første bærer, som skal være en del af omkostningen, i feltet **Finanskonto**.
5. Vælg den anden fordelingslinje.
6. Angiv den anden bærer i feltet Finanskonto.
7. Vælg **Fordel ligeligt**.
8. Luk siden.

## <a name="view-line-details"></a>Vis linjedetaljer
1. Slå udvidelsen af sektionen **Linjedetaljer** til/fra.

## <a name="submit-the-requisition"></a>Send rekvisitionen
1. Vælg **Arbejdsgang** for at åbne dialogboksen.
2. Vælg **Send**.
3. Luk siden.
4. Skriv en bemærkning til godkenderen af rekvisitionen i feltet **Kommentar**.
5. Vælg **Send**.
6. Luk siden.
7. Opdater siden.

