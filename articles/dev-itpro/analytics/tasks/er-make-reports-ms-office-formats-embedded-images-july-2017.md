--- 
title: Udarbejde rapporter i Microsoft Office-formater med integrerede billeder til elektronisk rapportering (ER) (Del 1)
description: "Følgende trin beskriver, hvordan en bruger i rollen som enten \"Systemadministrator\" eller \"Udvikler af elektronisk rapportering\" kan designe konfigurationer til elektronisk rapportering (ER) med henblik på oprettelse af elektroniske dokumenter i MS Office-formater (Excel og Word), der indeholder integrerede billeder."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: f610fe4b7f265c4fc38db89938d5c208b4f7661a
ms.contentlocale: da-dk
ms.lasthandoff: 11/02/2017

---
# <a name="make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er--part-1"></a>Udarbejde rapporter i Microsoft Office-formater med integrerede billeder til elektronisk rapportering (ER) (Del 1) 

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som enten "Systemadministrator" eller "Udvikler af elektronisk rapportering" kan designe konfigurationer til elektronisk rapportering (ER) med henblik på oprettelse af elektroniske dokumenter i MS Office-formater (Excel og Word), der indeholder integrerede billeder.

I dette eksempel skal du bruge oprettede ER-konfigurationer for eksempelfirmaet Litware Inc.  For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "ER Oprette rapporter i Microsoft Office-formater med integrerede billeder (Del 2 - Gennemse konfigurationer)". Disse trin kan udføres i USMF-virksomhed.


## <a name="run-format-with-initial-model-mapping"></a>Køre format med startmodeltilknytning
1. Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.
2. Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "USMF OPER".
3. Klik på Konfigurer i handlingsruden.
4. Klik på Kontroller.
5. Klik på Udskriv prøve.
    * Kør formatet til testformål.  
6. Vælg Ja i feltet Omsætteligt checkformat.
7. Klik på OK.
    * Gennemse det oprettede output. Bemærk, at firmaets logo vises i rapporten sammen med den autoriserede persons signatur. Signaturbilledet hentes fra feltet af 'Container'-datatypen i den checklayoutpost, der er tilknyttet den valgte bankkonto.  
8. Udvid sektionen Kopier.
9. Klik på Rediger.
10. Angiv 'Udskriv vandmærke som Ugyldig' i feltet Vandmærke.
    * Rediger indstillingen for vandmærkelayout, så den viser vandmærketeksten i dokumentoprettelse i et Excel-figurelement.  
11. Klik på Udskriv prøve.
12. Klik på OK.
    * Gennemse det oprettede output. Bemærk, at vandmærket vises i den oprettede rapport i henhold til markeringsindstillingen.  
13. Luk siden.
14. Klik på Administrer betalinger i handlingsruden.
15. Klik på Checks.
16. Klik på Vis filtre.
17. Angiv følgende filtre: Angiv en filterværdi på "381", "385", "389" for feltet "Checknummer" ved hjælp af filteroperatoren "er én af".
18. Markér alle poster på listen.
19. Klik på Udskriv checkkopi.
    * Kør formatet for at udskrive de valgte checks igen.  
    * Gennemse det oprettede output. Bemærk, at de valgte checks er udskrevet igen. Firmaets logo og etiketter udskrives ikke, fordi de præsenteres i den fortrykte formular.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Ændre tilknytningen af den importerede datamodel
1. Luk siden.
2. Luk siden.
3. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
4. Vælg 'Model for checks' i træet.
5. Klik på Designer.
6. Klik på Tilknyt model til datakilde.
7. Klik på Designer.
    * Vi ændrer bindingen af datamodellens signaturelement for at få signaturbilledet fra den fil, der var vedhæftet i den checklayoutpost, der er tilknyttet den valgte bankkonto.  
8. Slå Vis detaljer fra.
9. Udvid 'layout' i træet.
10. Udvid 'layout\signatur' i træet.
11. Vælg 'layout\signatur\billede = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp' i træet.
12. Udvid 'chequesaccount' i træet.
13. Udvid 'chequesaccount\<Relationer' i træet.
14. Udvid 'chequesaccount\<Relationer\BankChequeLayout' i træet.
15. Udvid 'chequesaccount\<Relationer\BankChequeLayout\<Relationer' i træet.
16. Udvid 'chequesaccount\<Relationer\BankChequeLayout\<Relationer\<Dokumenter' i træet.
17. Vælg 'chequesaccount\<Relationer\BankChequeLayout\<Relationer\<Dokumenter\getFileContentAsContainer()' i træet.
18. Klik på Bind.
19. Klik på Gem.
20. Luk siden.
21. Luk siden.
22. Luk siden.
23. Luk siden.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Kør format ved hjælp af tilpasset modeltilknytning
1. Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Bankkonto med værdien "USMF OPER".
3. Klik på Konfigurer i handlingsruden.
4. Klik på Kontroller.
5. Klik på Udskriv prøve.
6. Klik på OK.
    * Gennemse det oprettede output. Bemærk, at billedet fra den vedhæftede fil i Dokumentstyring vises som en autoriseret persons signatur.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>Bruge MS Word-dokument som en skabelon i det importerede format
1. Luk siden.
2. Luk siden.
3. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
4. Udvid 'Model for checks' i træet.
5. Vælg 'Model for checks\Checkudskrivningsformat' i træet.
6. Klik på Designer.
7. Klik på Vedhæftede filer.
8. Klik på Slet.
9. Klik på Ja.
10. Klik på Ny.
11. Klik på Filer.
    * Klik på Gennemse, og vælg skabelonfilen 'Cheque template Word.docx', der er hentet på forhånd.  
12. Luk siden.
13. Indtast eller vælg en værdi i feltet Skabelon.
14. Klik på Gem.
15. Luk siden.
16. Klik på Rediger.
17. Vælg Ja i feltet Udkast til kørsel.
18. Luk siden.
19. Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.
20. Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "USMF OPER".
21. Klik på Kontroller.
22. Klik på Udskriv prøve.
23. Klik på OK.
    * Gennemse det oprettede output. Bemærk, at outputtet er oprettet som et Microsoft Word-dokument med integrerede billeder, der viser firmaets logo, en autoriseret persons signatur og den markerede tekst i vandmærket.  


