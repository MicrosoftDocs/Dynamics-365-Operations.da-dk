--- 
title: Opgradere dit format ved at bruge en ny basisversion af formatet til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan bevare en formatkonfiguration af elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 02/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: e1558fd70453dfb9f521187259d9a1241bf36767
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="upgrade-your-format-by-adopting-of-new-base-version-of-that-format-for-electronic-reporting-er"></a>Opgradere dit format ved at bruge en ny basisversion af formatet til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan bevare en formatkonfiguration af elektronisk rapportering (ER). Denne fremgangsmåde forklarer, hvordan en brugerdefineret version af et format kan oprettes ud fra det format, der er modtaget fra konfigurationsudbyderen (CP). Det forklares også, hvordan en ny basisversion af det pågældende format skal implementeres.



For at fuldføre denne fremgangsmåde, skal du først udføre trinnene i procedurerne "Oprette en konfigurationsudbyder og markere den som aktiv" og "Bruge oprettet format for at generere elektroniske dokumenter til betalinger". Disse trin kan udføres i GBSI-virksomheden.


## <a name="select-format-configuration-for-customization"></a>Vælge formatkonfiguration, der skal tilpasses
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * I dette eksempel fungerer eksempelfirmaet Litware, Inc. (http://www.litware.com) som en konfigurationsudbyder, der understøtter formatkonfigurationer af elektroniske betalinger for et bestemt land/område.    Eksempelfirmaet Proseware, Inc. (http://www.proseware.com) vil fungere som en forbruger af den formatkonfiguration, som Litware, Inc. Proseware, Inc. bruger formater i bestemte dele af det pågældende land/område.  
2. Klik på Rapporteringskonfigurationer.
3. Klik på Vis filtre.
4. Anvend følgende filtre: Angiv filterværdien "BACS (UK-fiktiv)" i feltet "Navn" ved hjælp af filteroperatøren "begynder med".
    * BACS (UK-fiktiv)  
    * Den valgte BACS-formatkonfiguration (UK fiktivt brugerdefineret), som ejes af udbyderen Litware, Inc.  
5. Klik på Vis filtre.
6. Find og vælg den ønskede post på listen.
    * Versionen af formatet med statussen Fuldført vil blive brugt af Proseware, Inc. til tilpasning.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Oprette en ny konfiguration af det brugerdefinerede format for elektronisk dokument
    * Proseware, Inc. modtog version 1.1 af BACS-konfigurationen (UK fiktiv), der indeholder det oprindelige format til oprettelse af elektroniske betalingsdokumenter fra Litware, Inc. i overensstemmelse med deres serviceabonnement. Proseware, Inc. ønsker at begynde at bruge det som en standard for deres land/område, men nogle tilpasninger er påkrævet for at understøtte specifikke regionale krav. Proseware, Inc. ønsker også at bevare muligheden for at opgradere et brugerdefineret format, så snart der kommer en ny version af det (med ændringer for at understøtte nye lande-/områdespecifikke krav) fra Litware, Inc., og de ønsker at udføre denne opgradering med de laveste omkostninger.  For at kunne gøre dette skal Proseware, Inc. oprette en konfiguration og bruge BACS-konfigurationen af Litware, Inc. (UK fiktiv) som udgangspunkt.  
1. Luk siden.
2. Vælg Proseware, Inc., for at gøre den til en aktiv udbyder.
3. Klik på Angiv som aktiv.
4. Klik på Rapporteringskonfigurationer.
5. Udvid 'Betalinger (forenklet model)' i træet.
6. Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.
    * Vælg BACS-konfigurationen (UK fiktiv) fra Litware, Inc. Proseware, Inc. bruger version 1.1 som udgangspunkt for den brugerdefinerede version.  
7. Klik på Opret konfiguration for at åbne dialogboksen.
    * Dette gør det muligt at oprette en ny konfiguration for et brugerdefineret betalingsformat.  
8. Angiv 'Afled af navn: BACS (UK fiktivt), Litware, Inc.' i feltet Ny.
    * Vælg indstillingen Afled for at bekræfte brugen af BACS (UK fiktivt) som basis for at oprette den brugerdefinerede version.  
9. Skriv 'BACS (UK-fiktivt brugerdefineret) i feltet Navn.
    * BACS (UK fiktivt brugerdefineret)  
10. Skriv "BACS kreditorbetalingsformat (UK fiktivt brugerdefineret)" i feltet Beskrivelse.
    * BACS-kreditorbetaling (UK fiktivt brugerdefineret)  
    * Den aktive konfigurationsudbyder (Proseware, Inc.) indsættes automatisk her. Denne udbyder vil kunne vedligeholde denne konfiguration. Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.  
11. Klik på Opret konfiguration.

## <a name="customize-your-format-for-the-electronic-document"></a>Tilpasse format for det elektroniske dokument
1. Klik på Designer.
2. Klik på Udvid/skjul.
3. Klik på Udvid/skjul.
4. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank" i træet.
5. Klik på Tilføj for at åbne dialogboksen.
6. Vælg "XML\Element'' i træet.
7. Skriv "IBAN" i feltet Navn.
    * IBAN  
8. Klik på OK.
9. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\IBAN" i træet.
10. Klik på Tilføj for at åbne dialogboksen.
11. Vælg "Tekst\Streng" i træet.
12. Klik på OK.
13. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn\Streng" i træet.
14. Angiv '60' i feltet Maksimumlængde.
15. Klik på fanen Tilknytning.
16. Udvid 'model' i træet.
17. Udvid 'model\Betalinger' i træet.
18. Udvid "model\Betalinger\Kreditor" i træet.
19. Udvid 'model\Betalinger\Kreditor\Konto' i træet.
20. Vælg "model\Betalinger\Kreditor\Konto\IBAN" i træet.
21. Vælg "Xml\Meddelelse\Betalinger\Vare = model.Betalinger\Kreditor\Bank\IBAN\Streng" i træet.
22. Klik på Bind.
23. Klik på Gem.

## <a name="validate-the-customized-format"></a>Validere det tilpassede format
1. Klik på Valider.
    * Validér det tilpassede formatlayout og ændringer af datatilknytningen til at sikre, at alle bindinger er i orden.  
2. Luk siden.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Ændre statussen for den aktuelle version af den brugerdefinerede formatkonfiguration
    * Skift status for den designede formatkonfiguration fra Kladde til Fuldført for at gøre den tilgængelig for oprettelse af betalingsdokumenter.  
1. Klik på Skift status.
    * Bemærk, at den aktuelle version af den valgte konfiguration har statussen Kladde.  
2. Klik på Fuldført.
3. Skriv en værdi i feltet Beskrivelse.
4. Klik på OK.
5. Find og vælg den ønskede post på listen.
    * Bemærk, at den oprettede konfiguration gemmes som fuldført version 1.1.1. Det betyder, at det er version 1 af det brugerdefinerede BACS-format (UK fiktivt brugerdefineret), der er baseret på version 1 af BACS-formatet (UK fiktivt), der er baseret på version 1 af datamodellen Betalinger (forenklet model).  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Teste det tilpassede format for at generere betalingsfiler
    * Udfør trinnene i proceduren "Bruge oprettet format for at generere elektroniske dokumenter til betalinger" i en parallel Dynamics 365 for Finance and Operations, Enterprise edition-session. Vælg BACS-formatet (UK fiktivt brugerdefineret) i parametrene for den elektroniske betalingsmåde. Sørg for, at den oprettede betalingsfil indeholder den netop indførte XML-node, som præsenterer IBAN-kode i henhold til de regionale krav.  

## <a name="update-the-existing-country-specific-configuration"></a>Opdatere den eksisterende landespecifikke konfiguration
    * Litware, Inc. skal opdatere konfigurationen af BACS (UK fiktivt) og benytte nye lande/områdespecifikke krav til håndtering af formatet på det elektroniske dokument. Senere bliver det inkluderet i en ny version af denne konfiguration, som vil blive tilbudt til serviceabonnenter, herunder Proseware, Inc.  
    * I processer, der er relateret til reelle tjenesteydelser, kan hver ny version af BACS (UK fiktivt) importeres af Proseware, Inc. fra Litware, Inc.-konfigurationers LCS-lager. I denne procedure vil vi simulere dette ved at opdatere BACS (UK fiktivt) på vegne af en serviceudbyder.  
1. Luk siden.
2. Vælg Litware, Inc. .
3. Klik på Angiv som aktiv.
4. Klik på Rapporteringskonfigurationer.
5. Udvid 'Betalinger (forenklet model)' i træet.
6. Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.
    * Kladdeversionen, som ejes af BACS-udbyderen Litware, Inc. (UK fiktivt), er valgt til at sikre, at ændringer understøtter de nye lande/områdespecifikke krav.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Lokalisere basisformatet for det elektroniske dokument
    * Antag, at nogle nye lande/områdespecifikke krav skal understøttes af Litware, Inc.: - En værdi for kreditorbankens SWIFT-kode i hver betalingstransaktion.  - En grænse på 100 tegn for tekstlængden på kreditorens navn i en fil, der oprettes.  
    * Nye lande-/områdespecifikke krav  
    * Vælg kladdeversionen af den ønskede konfiguration for at indføre de nødvendige ændringer.  
1. Klik på Designer.
2. Klik på Udvid/skjul.
3. Klik på Udvid/skjul.
4. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank" i træet.
5. Klik på Tilføj for at åbne dialogboksen.
6. Vælg "XML\Element'' i træet.
7. Skriv "SWIFT" i feltet Navn.
    * SWIFT  
8. Klik på OK.
9. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\SWIFT" i træet.
10. Klik på Tilføj for at åbne dialogboksen.
11. Vælg "Tekst\Streng" i træet.
12. Klik på OK.
13. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn\Streng" i træet.
14. Angiv '100' i feltet Maksimumlængde.
15. Klik på fanen Tilknytning.
16. Udvid 'model' i træet.
17. Udvid 'model\Betalinger' i træet.
18. Udvid "model\Betalinger\Kreditor" i træet.
19. Udvid "model\Betalinger\Kreditor\Speditør" i træet.
20. Vælg "model\Betalinger\Kreditor\Speditør\SWIFT" i træet.
21. Vælg "Xml\Meddelelse\Betalinger\Vare = model.Betalinger\Kreditor\Bank\SWIFT\Streng" i træet.
22. Klik på Bind.
23. Klik på Gem.

## <a name="validate-the-localized-format"></a>Validere det lokaliserede format
1. Klik på Valider.
2. Luk siden.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Ændre statussen for den aktuelle version af basisformatkonfigurationen
    * Skift status for den opdaterede basisformatkonfiguration fra Kladde til Fuldført for at gøre den tilgængelig for oprettelse af betalingsdokumenter og opdateringer af de formatkonfigurationer, der er afledt af den.  
1. Klik på Skift status.
    * Bemærk, at den aktuelle version af den valgte konfiguration har statussen Kladde.  
2. Klik på Fuldført.
3. Skriv en værdi i feltet Beskrivelse.
4. Klik på OK.
5. Find og vælg den ønskede post på listen.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Ændre basisversionen af den brugerdefinerede formatkonfiguration
    * Proseware, Inc. får besked om, at en ny version 1.2 af BACS-konfigurationen (UK fiktivt) er tilgængelig for oprettelse af elektroniske betalingsdokumenter i henhold til de nyligt annoncerede lande/områdespecifikke krav. Proseware, Inc. ønsker at begynde at bruge den som en standard for landet/området.  For at kunne gøre dette skal Proseware, Inc. ændre basiskonfigurationsversionen af den brugerdefinerede BACS-konfigurationen (UK fiktivt brugerdefineret). Brug den nye version 1.2, i stedet for version 1.1 af BACS (UK fiktivt).  
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Vælg udbyderen Proseware, Inc., for at markere den som aktiv.
3. Klik på Angiv som aktiv.
4. Klik på Rapporteringskonfigurationer.
5. Udvid 'Betalinger (forenklet model)' i træet.
6. Udvid 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.
7. Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)\BACS (UK fiktivt brugerdefineret)' i træet.
    * Vælg BACS-konfigurationen (UK fiktivt brugerdefineret), som ejes af Proseware, Inc.  
    * Brug kladdeversionen af den valgte konfiguration for at indføre de nødvendige ændringer.  
8. Klik på Rebasér.
    * Vælg den nye version 1.2 af den basiskonfiguration, der skal anvendes som ny basis for opdatering af konfigurationen.  
9. Klik på OK.
    * Bemærk, at der er fundet nogle konflikter mellem fletning af den brugerdefinerede version og en ny basisversion, der repræsenterer nogle formatændringer, der ikke kan flettes automatisk.  

## <a name="resolve-rebase-conflicts"></a>Løse rebaseringskonflikter
1. Klik på Designer.
    * Bemærk, at ændringer af grænsen for tekstlængen på kreditorens navn ikke kunne løses automatisk. Dette vises derfor på en liste over konflikter. For hver konflikt af typen Opdatering er følgende indstillinger tilgængelige: - Anvend en tidligere basisværdi (knap oven på gitteret) for at overføre den tidligere basisversions værdi (0 i vores tilfælde).  - Anvend en basisværdi (knap oven på gitteret) for at overføre den nye basisversions værdi (100 i vores tilfælde).  - Bevar din egen (brugerdefineret) værdi (60 i dette tilfælde).  Klik på Anvend basisværdi for at anvende en lande/områdespecifik grænse på 100 tegn for tekstlængden på kreditorens navn.  
    * Bemærk, at Proseware, Inc. og Litware, Inc. har brugerdefinerede og lokale versioner af dette format, som benytter IBAN- og SWIFT-koder med relaterede komponenter, der flettes automatisk i håndteringen af formatet.  
2. Klik på Anvend basisværdi.
    * Klik på Anvend basisværdi for at anvende den landespecifikke grænse på 100 tegn for kreditornavne.  
3. Klik på Gem.
    * Hvis du gemmer formatet, fjernes løste konflikter fra listen over konflikter.  
4. Luk siden.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Ændre statussen for den nye version af den brugerdefinerede formatkonfiguration
1. Klik på Skift status.
    * Skift status for den opdaterede, brugerdefinerede formatkonfiguration fra Kladde til Fuldført. Dette vil gøre formatkonfigurationen tilgængelig for oprettelse af betalingsdokumenter. Bemærk, at den aktuelle version af den valgte konfiguration har statussen Kladde.  
2. Klik på Fuldført.
3. Skriv en værdi i feltet Beskrivelse.
4. Klik på OK.
    * Bemærk, at den oprettede konfiguration gemmes som fuldført version 1.2.2: version 2 af BACS-basisformatet (UK fiktivt brugerdefineret), der er baseret på version 2 af BACS-basisformatet (UK fiktivt), der er baseret på version 1 af datamodellen Betalinger (forenklet model).  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Teste det tilpassede format for generering af betalingsfiler
    * Udfør trinnene i proceduren "Bruge oprettet format for at generere elektroniske dokumenter til betalinger" i en parallel Dynamics 365 for Finance and Operations, Enterprise edition-session. Vælg det oprettede BACS-format (UK fiktivt brugerdefineret) i parametrene for den elektroniske betalingsmåde. Sørg for, at den oprettede betalingsfil indeholder Proseware, Inc.s netop indførte XML-node, som præsenterer IBAN-kontokode i henhold til de regionale krav. Filen skal også indeholde Litware, Inc.s netop indførte XML-node, som præsenterer SWIFT-bankkode i overensstemmelse med kravene i landet.  


