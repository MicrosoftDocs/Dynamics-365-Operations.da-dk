---
title: Lukke regnskabsåret
description: Denne procedure gennemgår processen for årsafslutning, som overfører saldi til et nyt regnskabsår.
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779794"
---
# <a name="close-the-fiscal-year"></a>Lukke regnskabsåret

[!include [banner](../../includes/banner.md)]

Denne procedure gennemgår processen for årsafslutning, som overfører saldi til et nyt regnskabsår.


## <a name="validate-year-end-close-parameters"></a>Valider årsafslutningens parametre
1. Gå til **Navigationsrude > Moduler > Finans > Opsætning Finans > Finansparametre**.
2. Udvid sektionen **Årsafslutning**.
3. Vælg **Ja** eller **Nej** for indstillingen **Slet årsafslutningsposter ved overførsel**.
    
Denne indstilling er vigtig, hvis regnskabsåret er blevet lukket, og årsafslutningen køres igen. Hvis indstillingen er angivet til **Ja**, slettes bilaget for forrige årsafslutning, og der oprettes et nyt bilag for alle kontienes primosaldi. Hvis indstillingen er angivet til **Nej**, forbliver det tidligere bilag, og der oprettes kun et nyt bilag til regulering af poster, der blev bogført efter den sidste årsafslutning.

4. Vælg **Ja** eller **Nej** for indstillingen **Opret ultimoposter ved overførsel**.

Hvis værdien angives til **Ja**, oprettes der to posteringer. Der oprettes et bilag i det regnskabsår, der afsluttes, for at bringe saldiene for alle finanskontiene til nul, og der oprettes et andet bilag i det næste regnskabsår for startsaldiene. Hvis værdien angives til **Nej**, oprettes der et enkelt bilag i det næste regnskabsår for startsaldiene.  

5. Vælg **Ja** eller **Nej** for indstillingen **Indstil status til permanent afsluttet for regnskabsåret**.

Hvis værdien er angivet til **Ja**, angives regnskabsårets status til **Permanent lukket**. Da et permanent lukket år ikke kan åbnes igen, er den bedste fremgangsmåde at angive denne indstilling til **Nej**.  

6. Vælg **Ja** eller **Nej** for indstillingen **Bilagsnummeret skal udfyldes under årsafslutning**.

Hvis værdien er angivet til **Ja**, skal der manuelt angives et bilagsnummer under processen for årsafslutning. Der bruges ikke en nummerserie til at oprette dette bilagsnummer. Det er bedste fremgangsmåde at angive den til **Ja**.  

7. Luk siden.
8. Gå til **Finans > Luk periode > Årsafslutning**.
9. Klik på **Ny** for at oprette en årsafslutningsskabelon.

Der kan oprettes en skabelon for en gruppe af juridiske enheder, der skal køres årsafslutning for. Denne skabelon kan bruges igen år efter år.  

10. I feltet **Gruppenavn** skal du angive et navn til årsafslutningsskabelonen.
11. Vælg det regnskabsår, som skabelonen skal oprettes for, i feltet **Regnskabskalender**.

Det er kun juridiske enheder, der bruger samme regnskabsår, der kan grupperes sammen i skabelonen for årsafslutning. Det skyldes, at årsafslutningen sker ved at vælge et regnskabsår, ikke en dato.  

12. Klik på **Gem** i **handlingsruden**.
13. I sektionen **Juridiske enheder** skal du klikke på **Tilføj** for at vælge de juridiske enheder for denne skabelon.
    
Juridiske enheder kan tilføjes ved enten at vælge de juridiske enheder eller ved at vælge et organisationshierarki. Der kan kun tilføjes juridiske enheder, hvor det organisatoriske hierarki med den samme regnskabskalender er valgt.  

14. Vælg enten de juridiske enheder eller organisationshierarkiet.
15. Klik på **OK**.
16. Vælg **Ja** eller **Nej** i **Overfør balancedimensioner**.

Det er den bedste praksis at angive denne indstilling til **Ja** for statuskonti. Derved bevares de økonomiske dimensioner for bogførte posteringer, når der oprettes primosaldi for statuskonti. Til driftskonti kan du vælge at bevare de økonomiske dimensioner (**Luk alle**), når saldiene er flyttet til Overført resultat, eller du kan vælge at få de økonomiske dimensioner erstattet med en anden dimensionsværdi (**Luk et enkelt**). Hvis du vælger **Luk et enkelt**, kan du definere en bestemt dimensionsværdi for hver dimension eller vælge at lade det være tomt.  

17. Klik på **Gem**.
18. Start årsafslutningen ved at vælge **Kør regnskabsafslutning** i **handlingsruden**. Årsafslutningen køres for den valgte skabelon.  
19. Vælg alle eller nogle af de juridiske enheder fra den skabelon, som årsafslutningen skal køres for.

Når årsafslutningen køres første gang, vælger de fleste organisationer at køre årsafslutningen for alle juridiske enheder i skabelonen for at få primosaldi. Hvis der foretages reguleringsposteringer herefter, kan du vælge at køre årsafslutningen kun for de juridiske enheder, der har justeringer.  

20. Klik på **OK**.
21. Vælg regnskabskalender, som årsafslutningen skal køres for.
22. Skriv en værdi i feltet **Bilag**. Det er god praksis at medtage regnskabsåret i bilagsnummeret for at gøre det nemmere at finde på det årsafslutningsbilag, der oprettes.  
23. Årsafslutningen køres som standarder i batch. Det er den bedste praksis for langvarige processer, der skal køres i batchtilstand. Det er typisk en af disse processer, hvilket er grunden til, at standarden er at bruge batchtilstand.  
24. Klik på **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
