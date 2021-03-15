---
title: Indgå salgsaftaler
description: Dette emne viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter.
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c63097340cf709976510451c157ab691e87d06e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010795"
---
# <a name="enter-sales-agreements"></a>Indgå salgsaftaler

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du opretter en salgsaftale, der forpligter en af dine kunder til at købe et produkt for et aftalt beløb over en tidsperiode mod at få særlige rabatter. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.


## <a name="set-up-sales-agreement-header"></a>Konfigurere salgsaftaleoverskrift
1. Gå i navigationsruden til **Moduler > Salg og marketing > Salgsaftaler > Salgsaftaler**.
2. Vælg **Ny**.
3. Vælg den ønskede post på rullemenuen i feltet **Debitorkonto**.
4. Vælg den ønskede post på rullemenuen i feltet **Salgsaftaleklassifikation**.
5. Udvid sektionen **Generelt**.
6. Vælg **Bundet produktværdi** i feltet **Standardtilsagn**. En tilsagnstype er et obligatorisk kriterium, som du skal tildele til aftalen for at definere, hvordan aftalekontrakten skal opfyldes. Med de fire foruddefinerede typer kan du angive kundens tilsagnsmål udtrykt som en mængde eller værdi. Mængdetilsagnstypen kan kun anvendes på et bestemt produkt, men de værdibaserede typerne gælder for salget af specifikke og ikke-specifikke produkter.  
7. Indstil datoen i feltet **Udløbsdato** til en fremtidig dato, hvor du vil have, at aftalen udløber.
8. Vælg **OK**.

## <a name="set-up-product-value-commitment-lines"></a>Konfigurere bundede produktværdilinjer
1. Vælg **Tilføj linje**.
2. Vælg den ønskede post på rullemenuen i feltet **Varenummer**. Tilsagnstypen, som du har valgt til denne aftale, påvirker, hvilken type oplysninger du kan angive for aftalelinjerne. For en værdibaseret aftale skal du for eksempel angive det samlede nettobeløb (i den aftalte valuta), som kunden giver tilsagn om at købe varer fra dig for. I dette eksempel er felterne **Antal** og **Enhed** på linjen ikke tilgængelige, fordi du opretter en aftale for kunden om at købe en bestemt værdi af et produkt.   
3. Angiv det pengebeløb, som kunden har forpligtet sig til at købe for, i feltet **Nettobeløb**.
4. Angiv en værdi i procent, som skal gælde for kundens salgsordrelinjer, der er knyttet til denne aftale, i feltet **Rabatprocent**.
5. Vis eller skjul sektionen **Linjedetaljer**.
6. Vælg **Ja** i feltet **Maks. gennemtvinges**.
    - Hvis du vælger **Maks. gennemtvinges** betyder det, at det samlede beløb for alle de salgsordrelinjer, der bruger tilsagnets specielle priser, rabatter og/eller betalingsbetingelser, ikke må overstige det beløb, der er angivet i tilsagnet.  
    - Minimum- og maksimumfrigivelsesbeløbet angiver et interval af værdier, der skal sælges på hver salgsordre, der bruger den valgte aftale.   
7. Udvid sektionen **Salgsaftaleoverskrift**. Medmindre aftalens status er indstillet til **Gældende**, kan salgsordrer ikke knyttes til aftalen og kan derfor ikke bidrage til opfyldelsen af denne aftale. Du kan ændre statussen manuelt på dette trin. Status vil dog normalt ændres, når du bekræfter aftalen for kunden.  
8. Klik på **Salgsaftale** i handlingsruden.
9. Vælg **Bekræftelse**. Kontrollér, at indstillingen **Markér aftale som gældende** er sat til **Ja**.  
10. Vælg **Ja** i feltet **Udskriv rapport**.
11. Vælg **OK**.
12. Luk siden. Aftalen er nu gældende. Du kan begynde at knytte kundens ordrer til aftalen for at modpostere mod tilsagnsmålet.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]