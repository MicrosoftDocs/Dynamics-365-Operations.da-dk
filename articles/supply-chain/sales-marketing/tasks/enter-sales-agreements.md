--- 
title: "Indgå salgsaftaler"
description: "Denne procedure viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a1c4b7623f3409d4474adcd04fb1331b944b9fbb
ms.openlocfilehash: a0d49068d2c6a62bf7912c2fd7cccd53308bd196
ms.contentlocale: da-dk
ms.lasthandoff: 02/13/2018

---
# <a name="enter-sales-agreements"></a>Indgå salgsaftaler

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.


## <a name="set-up-sales-agreement-header"></a>Konfigurere salgsaftaleoverskrift
1. Gå til salg og marketing > Salgsaftaler > Salgsaftaler.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på rullelisten i feltet Salgsaftaleklassifikation for at åbne opslaget.
7. Klik op linket i den valgte række på listen.
8. Udvid afsnittet Generelt.
9. Vælg "Bundet produktværdi" i feltet Standardtilsagn.
    * En tilsagnstype er et obligatorisk kriterium, som du skal tildele til aftalen for at definere, hvordan aftalekontrakten skal opfyldes. Med de fire foruddefinerede typer kan du angive kundens tilsagnsmål udtrykt som en mængde eller værdi. Mængdetilsagnstypen kan kun anvendes på et bestemt produkt, men de værdibaserede typerne gælder for salget af specifikke og ikke-specifikke produkter.  
10. Indstil datoen i feltet Udløbsdato til en fremtidig dato, hvor du vil have, at aftalen udløber.
11. Klik på OK.

## <a name="set-up-product-value-commitment-lines"></a>Konfigurere bundede produktværdilinjer
1. Klik på Tilføj linje.
2. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
    * Tilsagnstypen, som du har valgt til denne aftale, påvirker, hvilken type oplysninger du kan angive for aftalelinjerne. For en værdibaseret aftale skal du for eksempel angive det samlede nettobeløb (i den aftalte valuta), som kunden giver tilsagn om at købe varer fra dig for. I dette eksempel er felterne Antal og Enhed på linjen ikke tilgængelige, fordi du opretter en aftale for kunden om at købe en bestemt værdi af et produkt.   
5. Angiv det pengebeløb, som kunden har forpligtet sig til at købe for, i feltet Nettobeløb.
6. Angiv en værdi i procent, som skal gælde for kundens salgsordrelinjer, der er knyttet til denne aftale, i feltet Rabatprocent.
7. Vis eller skjul sektionen Linjedetaljer.
8. Vælg Ja i feltet Maks. gennemtvinges.
    * Hvis du vælger Maks. gennemtvinges betyder det, at det samlede beløb for alle de salgsordrelinjer, der bruger tilsagnets specielle priser, rabatter og/eller betalingsbetingelser, ikke må overstige det beløb, der er angivet i tilsagnet.  
    * Minimum- og maksimumfrigivelsesbeløbet angiver et interval af værdier, der skal sælges på hver salgsordre, der bruger den valgte aftale.   
9. Udvid sektionen Salgsaftaleoverskrift.
    * Medmindre aftalens status er indstillet til Gældende, kan salgsordrer ikke knyttes til aftalen og kan derfor ikke bidrage til opfyldelsen af denne aftale. Du kan ændre statussen manuelt på dette trin. Status vil dog normalt ændres, når du bekræfter aftalen for kunden.  
10. Klik på Salgsaftale i handlingsruden.
11. Klik på Bekræftelse.
    * Kontrollér, at indstillingen Markér aftale som gældende er sat til Ja.  
12. Vælg Ja i feltet Udskriv rapport.
13. Klik på OK.
14. Luk siden.
    * Aftalen er nu gældende, og du kan begynde at tilknytte kundens ordrer til aftalen for at modpostere mod tilsagnsmålet.  


