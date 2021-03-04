---
title: Designe ER-udtryk til kald af programklassemetoder
description: Denne vejledning indeholder oplysninger om, hvordan du genbruge den eksisterende programlogik i konfigurationer til elektronisk rapportering (ER) ved at kalde de krævede metoder for programklasser i ER-udtryk.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d79d1a4e86731a62de4896a489a13f624ce159f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682015"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Designe ER-udtryk til kald af programklassemetoder

[!include [banner](../../includes/banner.md)]

Denne vejledning indeholder oplysninger om, hvordan du genbruge den eksisterende programlogik i konfigurationer til elektronisk rapportering (ER) ved at kalde de krævede metoder for programklasser i ER-udtryk. Værdier for argumenter til kald af klasser kan defineres dynamisk på kørselstidspunktet, f.eks. baseret på oplysninger i parsingdokumentet for at sikre, at det er korrekt. I denne guide skal du oprette de krævede ER-konfigurationer til eksempelfirmaet Litware Inc. Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler. 

Disse trin kan udføres ved hjælp af ethvert datasæt. Du skal hente og gemme følgende fil lokalt: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Du skal først fuldføre trinnene i proceduren "ER Oprette en konfigurationsudbyder markere den som aktiv" for at fuldføre disse trin.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Kontrollér, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".   
    * Du designer en proces til fortolkning af indgående bankkontoudtog for en opdatering til programdata. Du får de indgående bankkontoudtog som TXT-filer, der indeholder IBAN-koder. Som en del af importprocessen for kontoudtog skal du validere rigtigheden af disse IBAN-koder ved brug af den logik, der allerede findes.   

## <a name="import-a-new-er-model-configuration"></a>Importere en ny ER-modelkonfiguration
1. Find og vælg den ønskede post på listen.
    * Vælg feltet Microsoft-udbyder.  
2. Klik på Lagre.
3. Klik på Vis filtre.
4. Tilføje et filterfelt 'Typenavn'. Angiv værdien "ressourcer" i feltet Navn, vælg filteroperatoren "indeholder", og klik derefter på Anvend.
5. Klik på Åbn.
6. Vælg 'Betalingsmodel' i træet.
    * Hvis knappen Importer i oversigtspanelet Versioner ikke er aktiveret, har du allerede importeret version 1 af ER-konfigurationen 'Betalingsmodel'. Du kan springe over resten af trinnene i denne underordnede opgave.   
7. Klik på Importer.
8. Klik på Ja.
9. Luk siden.
10. Luk siden.

## <a name="add-a-new-er-format-configuration"></a>Tilføje en ny ER-formatkonfiguration
1. Klik på Rapporteringskonfigurationer.
    * Tilføje et nyt ER-format til at fortolke indgående bankkontoudtog i TXT-formatet.  
2. Vælg 'Betalingsmodel' i træet.
3. Klik på Opret konfiguration for at åbne dialogmenuen.
4. Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.
5. Skriv 'Importformat for bankkontoudtog (eksempel)' i feltet Navn.
    * Importformat for bankkontoudtog (eksempel)  
6. Vælg Ja i feltet Understøtter dataimport.
7. Klik på Opret konfiguration.

## <a name="design-the-er-format-configuration---format"></a>Designe ER-formatkonfigurationen - format
1. Klik på Designer.
    * Det designede format repræsenterer den forventede struktur i den eksterne fil i TXT-format.  
2. Klik på Tilføj rod for at åbne dialogmenuen.
3. Vælg 'Text\Sequence' i træet.
4. Skriv 'Root' i feltet Navn.
    * Rod  
5. Vælg 'Ny linje – Windows (CR LF)' i feltet Specialtegn.
    * Indstillingen 'Ny linje – Windows (CR LF)' er blevet valgt i feltet 'Specialtegn'. Baseret på denne indstilling betragtes hver linje i parsingfilen som en separat post.  
6. Klik på OK.
7. Klik på Tilføj for at åbne dialogboksen.
8. Vælg 'Text\Sequence' i træet.
9. Indtast 'Rækker' i feltet Navn.
    * Rækker  
10. Vælg 'Én mange' i feltet Multiplicitet.
    * Indstillingen 'Én mange' er valgt i feltet 'Multiplicitet'. Baseret på denne indstilling forventes det, at der vises mindst én linje i parsingfilen.  
11. Klik på OK.
12. Vælg 'Rod\Rækker' i træet.
13. Klik på Tilføj rækkefølge.
14. Skriv 'Felter' i feltet Navn.
    * Felter  
15. Vælg 'Nøjagtig én' i feltet Multiplicitet.
16. Klik på OK.
17. I træet skal du vælge 'Rod\Rækker\Felter'.
18. Klik på Tilføj for at åbne dialogboksen.
19. Vælg "Tekst\Streng" i træet.
20. Skriv "IBAN" i feltet Navn.
    * IBAN  
21. Klik på OK.
    * Det er konfigureret, at hver linje i parsingfilen kun indeholder IBAN-kode.  
22. Klik på Gem.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>Designe ER-formatkonfigurationen – tilknytning til datamodel
1. Klik på Knyt format til model.
2. Klik på Ny.
3. Skriv "BankToCustomerDebitCreditNotificationInitiation" i feltet Definition.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges definitionen.
5. Skriv 'Tilknytning til datamodel' i feltet Navn.
    * Tilknytning til datamodel  
6. Klik på Gem.
7. Klik på Designer.
8. Vælg 'Dynamics 365 for Operations\Klasse' i træet.
9. Klik på Tilføj rod.
    * Tilføje en ny datakilde for at kalde den eksisterende programlogik til validering af IBAN-koder.  
10. Skriv 'checkkoder' i feltet Navn.
    * Kontrollér koder  
11. Skriv 'ISO7064' i feltet Klasse.
    * ISO7064  
12. Klik på OK.
13. Udvid 'format' i træet.
14. Udvid 'format\Rod: Sequence(Root)' i træet.
15. Vælg 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. * (rækker)'.
16. Klik på Bind.
17. Udvid ' format\Rod: Sequence(Root)\Rækker: sekvens 1.. * (rækker)' i træet.
18. Udvid 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. * (rækker)\Felter: sekvens 1..1 (felter)' i træet.
19. Vælg 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. * (rækker)\Felter: sekvens 1..1 (felter)\IBAN: String(IBAN)' i træet.
20. Udvid 'Betalinger = format.Root.Rows' i træet.
21. Udvid 'Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)' i træet.
22. Udvid 'Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identifikation' i træet.
23. Vælg 'Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identifikation\IBAN' i træet.
24. Klik på Bind.
25. Klik på fanen Valideringer.
26. Klik på Ny.
    * Tilføje en ny valideringsregel, der vises en fejlmeddelelse for hver linje i parsingfilen, der indeholder ugyldig IBAN-kode.  
27. Klik på Rediger betingelse.
28. Udvid "checkkoder" i træet.
29. Vælg 'check_codes\verifyMOD1271_36' i træet.
30. Klik på Tilføj datakilde.
31. Skriv "check_codes.verifyMOD1271_36(" i feltet Formel.
    * check_codes.verifyMOD1271_36(  
32. Udvid 'format' i træet.
33. Udvid 'format\Rod: Sequence(Root)' i træet.
34. Udvid ' format\Rod: Sequence(Root)\Rækker: sekvens 1.. * (rækker)' i træet.
35. Udvid 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. * (rækker)\Felter: sekvens 1..1 (felter)' i træet.
36. Vælg 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. * (rækker)\Felter: sekvens 1..1 (felter)\IBAN: String(IBAN)' i træet.
37. Klik på Tilføj datakilde.
38. Angiv 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)' i feltet Formel.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Klik på Gem.
40. Luk siden.
    * Valideringsbetingelsen er konfigureret til at returnere FALSE for eventuel ugyldige IBAN-kode ved at kalde den eksisterende metode 'verifyMOD1271_36' i programklassen 'ISO7064'. Bemærk, at værdien af IBAN-koden defineres dynamisk under kørsel som argument i kaldemetoden baseret på indholdet af TXT-filen til parsing.   
41. Klik på Rediger meddelelse.
42. Angiv 'CONCATENATE("Ugyldig IBAN-kode er fundet: ", format.Root.Rows.Fields.IBAN)' i feltet Formel.
    * CONCATENATE("Ugyldig IBAN-kode er fundet: ", format. Root.Rows.Fields.IBAN)  
43. Klik på Gem.
44. Luk siden.
45. Klik på Gem.
46. Luk siden.

## <a name="run-the-format-mapping"></a>Kør formattilknytningen
Til testformål skal du udføre formattilknytningen ved hjælp af filen SampleIncomingMessage.txt, som du tidligere har hentet. Det genererede output omfatter data, der importeres fra den valgte TXT-fil og udfylder den brugerdefinerede datamodel under den faktiske import.   
1. Klik på Kør.
    * Klik på Gennemse, og naviger til filen SampleIncomingMessage.txt, som du tidligere har downloadet.  
2. Klik på OK.
    * Gennemgå outputtet i XML-format, som viser de data, der er importeret fra den valgte fil og overført til datamodellen. Bemærk, at kun 3 linjer i den importerede TXT-fil blev behandlet. IBAN-koden på linje 4, der er ugyldig, blev sprunget over, og der findes en fejlmeddelelse i infologgen.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]