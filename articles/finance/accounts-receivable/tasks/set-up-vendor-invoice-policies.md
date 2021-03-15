---
title: Konfigurere politikker for kreditorfakturaer
description: I dette emne forklares, hvordan du konfigurerer politikker for kreditorfakturaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79cbabba74fdb76d8fcc0553d39e0f140aacf03e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995439"
---
# <a name="set-up-vendor-invoice-policies"></a>Konfigurere politikker for kreditorfakturaer

[!include [banner](../../includes/banner.md)]

I dette emne forklares, hvordan du konfigurerer politikker for kreditorfakturaer. Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura. Du kan også konfigurere arbejdsgangen for kreditorfakturaer til at køre politikker for kreditorfakturaer, hver gang du sender en faktura videre i arbejdsgangen. 

- Kreditorfakturapolitikker gælder ikke for fakturaer, der er oprettet i indgangsbogen eller i fakturajournalen.  
- Kreditorfakturapolitikker benyttes ikke til validering af fakturasammenholdelse, men er i stedet konfigureret på siden Kreditorparametre.  
- Denne registrering anvender demofirmaet USMF. Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin. Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Forberede oprettelse af politikker for kreditorfakturaer
1. Gå til **Navigationsrude > Moduler > Kreditor > Opsætning > Kreditorparametre**.
2. Vælg fanen **Fakturavalidering**.
3. Markér eller fjern markeringen fra afkrydsningsfeltet **Opdater status for fakturahoved automatisk**.
4. Vælg **OK**.
5. Vælg en indstilling i feltet **Bogfør faktura med uoverensstemmelser**.
6. Luk siden.
7. Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Kreditorfakturapolitikker**.
8. Vælg **Parametre**.
9. Vælg **Tilføj**.
10. Luk siden for at vende tilbage til startsiden.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Oprette politikregeltyper for kreditorfakturaer
1. Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Regeltyper for kreditorfakturapolitikker**.
2. Vælg **Ny**.
3. Angiv værdier i felterne **Regelnavn** og **Beskrivelse**.
4. I feltet **Forespørgselsnavn** skal du vælge rullelisten for at åbne opslaget, og derefter vælge den ønskede post.
5. Vælg **Gem**.
6. Luk siden for at vende tilbage til startsiden.

## <a name="define-a-vendor-invoice-policy"></a>Definere en politik for kreditorfaktura
1. Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Kreditorfakturapolitikker**.
2. Vælg **Ny**.
3. Angiv værdier i felterne **Navn** og **Beskrivelse**.
4. Udvid eller skjul sektionen **Politikorganisationer**.
5. Vælg **Contoso Entertainment System USA** i træet.
6. Vælg **Tilføj**.
7. Udvid eller skjul sektionen **Politikregler**.
8. Vælg **Opret politikregel**.
9. Skriv en værdi i feltet **Beskrivelse af politikregel**.
10. Vælg **Filter**.
11. Vælg **Tilføj**. Vælg den ønskede post.
12. Vælg eller angiv indstillingerne fra rullemenuerne i felterne **Afledt tabel** og **Felt** i **Afledt tabel**.
13. Luk siden.
14. Skriv en værdi i feltet **Kriterier**.
15. Vælg **OK**.
16. Vælg **OK**.
17. Luk siderne for at vende tilbage til startsiden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]