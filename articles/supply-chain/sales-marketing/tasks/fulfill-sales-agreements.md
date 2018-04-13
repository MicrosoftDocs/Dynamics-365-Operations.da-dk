--- 
title: Opfylde salgsaftaler
description: Denne procedure viser, hvordan du opfylder en salgsaftale ved at knytte salgsordrer til den.
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
ms.openlocfilehash: f0894bf962c139c2e9e4c9f8d1589fd933afcedb
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="fulfill-sales-agreements"></a>Opfylde salgsaftaler

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opfylder en salgsaftale ved at knytte salgsordrer til den. Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data. Kontroller, at du har en gyldig salgsaftale af typen "Produkt værdi forpligtelse", før du starter denne vejledning. Du kan også køre opgaveguiden "Oprette salgsaftaler".  




## <a name="release-a-sales-order-from-the-agreement"></a>Frigive en salgsordre fra aftalen
1. Gå til salg og marketing > Salgsaftaler > Salgsaftaler.
2. Åbn den aftale, du vil frigive ordren mode, på listen.
3. Klik på Salgsaftale i handlingsruden.
4. Klik på Aftræksordre.
    * Som teksten over på siden Opret aftræksordre påpeger, vil de oplysninger, der kræves til salgsordrelinjerne, variere afhængigt af, om aftalen er baseret på mængde eller værdi.  
    * Aftalen i denne vejledning er af typen "Bundet produktværdi". Det er derfor området Linjer på denne side er tomt. Hvis tilsagnet var baseret på mængde, ville linjeoplysningerne blive kopieret fra aftalen.  
5. Klik på Opret.
    * Meddelelsen fortæller dig, at en salgsordre er blevet oprettet. Da ordren ikke indeholder nogen linjer, skal du tilføje ordrelinjeoplysningerne for at fuldføre frigivelsesprocessen.   
6. Luk siden.
7. Luk siden.
8. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
9. Find, og åbn den ordre, der blev oprettet som et resultat af ordrefrigivelsen i den forrige opgave, på listen.
10. Klik på Tilføj linje.
11. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
12. I feltet Varenummer skal du skrive eller vælge den vare, der er angivet på den tilknyttede salgsaftale.
13. Angiv et tal i feltet Antal.
    * Sørg for at angive en mængde, der bringer nettobeløbet under værdien af den tilknyttede salgsaftale.  
    * Bemærk, at fordi salgsordren er knyttet til aftalen, anvendes den aftalte rabatprocent på ordrelinjen.  
14. Klik på Opdater linje.
15. Klik på Vedhæftet.
    * Siden Tilknyttet aftale viser id'et og vilkårene i aftalen, som linjen er frigivet fra.  
16. Luk siden.
17. Klik på Generelt i handlingsruden.
18. Klik på Tilknyttet salgsaftale.
19. Vis eller skjul sektionen Linjedetaljer.
20. Klik på fanen Opfyldelse.
    * Fanen Opfyldelse viser en oversigt over alle de salgsordrelinjer, der er knyttet til dette tilsagn, og deres opfyldelsestilstand, samt beløbet eller mængden, der endnu ikke er frigivet.   
21. Luk siden.
22. Luk siden.
23. Luk siden.

## <a name="apply-sales-agreement-in-the-order-process"></a>Anvende salgsaftale i bestillingsprocessen
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Søg på listen, og vælg den kunde, der er angivet i salgsaftalen.
5. Klik op linket i den valgte række på listen.
6. Udvid afsnittet Generelt.
7. Klik på rullelisten i feltet Salgsaftale-id for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
9. Klik på Ja.
10. Klik på OK.
11. Markér den valgte række på listen.
12. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
13. I feltet Varenummer skal du skrive eller vælge den vare, der er angivet på den tilknyttede salgsaftale.
14. Klik op linket i den valgte række på listen.
15. Klik på Gem.
16. Klik på fanen Pluk og pak i handlingsruden.
17. Klik på Bogfør følgeseddel.
18. Udvid sektionen Parametre.
19. Vælg Ja i feltet Bogføring.
20. Klik på OK.
21. Klik på OK.
22. Klik på Generelt i handlingsruden.
23. Klik på Tilknyttet salgsaftale.
24. Klik på fanen Opfyldelse.


