---
title: Forpligtelser i den offentlige sektor i Frankrig
description: "Tilsagn er kildedokumenter til budgetstyring, som bruges af den offentlige sektor i Frankrig. De bruges til at reservere budgetterede beløb, så en organisation udtrykkeligt kan spore budgetreservationer til administration og rapportering i hele udgiftscyklussen."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, PurchAgreement, PurchCommitment_PSN, PurchTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 19531
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2d36867016f6bfeb149e417c1d86b585e01d59b2
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="commitments-in-the-public-sector-in-france"></a>Forpligtelser i den offentlige sektor i Frankrig

[!include [banner](../includes/banner.md)]

Tilsagn er kildedokumenter til budgetstyring, som bruges af den offentlige sektor i Frankrig. De bruges til at reservere budgetterede beløb, så en organisation udtrykkeligt kan spore budgetreservationer til administration og rapportering i hele udgiftscyklussen. 

Når forpligtelser bruges som en del af budgetteringsprocessen, er hver købsaftale, indkøbsordre og en kreditorfaktura knyttet til mindst én forpligtelse. Forpligtelsen eftergives, når midlerne er frigivet fra købsaftalen, og indkøbsordren er bekræftet. Når en faktura ikke henviser til en indkøbsordre eller købsaftale, eftergives den forpligtelse, der er tilknyttet fakturaen, når fakturaen bogføres. En forpligtelse kan desuden angive en leverandør. Når der er angivet en leverandør, skal en indkøbsordre, købsaftale eller kreditorfaktura, der henviser til forpligtelsen, have samme leverandør. Forpligtelser er gyldige fra den dato, de blev oprettet, til slutningen af regnskabsåret, eller indtil de lukkes. Forpligtelser kan ikke overføres fra ét regnskabsår til næste.  
>[!NOTE]
>Feltet **Tilsagnstype** på siden **Købsaftale** er ikke relateret til forpligtelsesdokumentet. Dette felt angiver kun, om købsaftalen er baseret på en værdi eller et antal.

## <a name="set-up-budget-control-and-related-prerequisites"></a>Konfigurere budgetstyring og relaterede forudsætninger
Før du kan bruge forpligtelser, skal forpligtelsesnummerserier defineres, budgetstyring skal konfigureres, og disponible budgetbeløb skal være tilgængelige. Arbejdsgangen for forpligtelser er valgfri, men anbefales.

-   På siden **Budgetparametre** skal du oprette nummerserier til forpligtelser.
-   Konfigurer arbejdsgang for at administrere evalueringsprocessen for forpligtelser.
-   På siden **Konfiguration af budgetstyring** skal du konfigurere budgetstyring. De indstillinger, der er anført nedenfor, er påkrævet for forpligtelser. Indstillinger, der ikke er angivet her, kan vælges efter behov og praksis i organisationen.
    -   I afsnittet **Disponible budgetmidler** skal du vælge følgende indstillinger:
        -   Oprindeligt budget
        -   Faktiske udgifter
        -   Budgetreservation for behæftelser
        -   Budgetreservationer for budgetreservationer
        -   Budgetreservationer for ikke-bekræftede budgetreservationer
    -   I afsnittet **Dokumenter og journaler**:
        -   Kontroller, at både hoved- og linjeindstillinger er valgt for forpligtelser, indkøbsordrer og kreditorfakturaer.
        -   Kontroller, at hverken hoved- eller linjeindstillinger er markeret for indkøbsrekvisitioner.
    -   I afsnittet **Aktivér budgetstyring** skal du aktivere konfigurationen af budgetstyring og aktivere budgetstyring.
-   På siden **Økonomiparametre** skal du kontrollere, at indstillingerne i gruppen **Rammeaftale** i afsnittet **Finans** ikke er markeret. Når du aktiverer forpligtelser, kan du ikke bogføre budgettransaktioner til Finans.

## <a name="consume-a-commitment"></a>Bruge en forpligtelse
Der er tre måder at forbruge en forpligtelse på.

-   **Tildele en købsaftale til en tilsagnslinje.** Forpligtelsen forbruges, når midler frigives fra købsaftalen. Det gør du ved at angive indkøbsrekvisitionen i tilsagnslinjen, når du opretter forpligtelsen.
-   **Refererer direkte til forpligtelsen på en indkøbsordrelinje.** Forpligtelsen bruges, når indkøbsordren er bekræftet. Ingen købsaftale er involveret. Dette gør du ved at oprette en købsordre ifølge din normale proces. Når du tilføjer en linje til indkøbsordren, skal du vælge den forpligtelse, der skal bruges til denne indkøbsordre.
-   **Referer til forpligtelsen direkte på en kreditorfaktura.** Der kan være tildelt en købsaftale i hovedet på fakturaen, men der er ikke involveret nogen indkøbsordre. Forpligtelsen bruges, når fakturaen er bogført. Dette gør du ved at oprette en kreditorfaktura ifølge din normale proces. Når du tilføjer en linje til fakturaen, skal du vælge den forpligtelse, der skal bruges til denne faktura.

En forpligtelse kan begrænses til en bestemt leverandør, eller den kan være tilgængelig for tildeling til enhver kreditor. Hvis forpligtelsen er begrænset til en bestemt leverandør, er den kun tilgængelig for markering, når den samme leverandør er angivet på kreditorfakturaen eller indkøbsordren.

## <a name="increase-or-decrease-a-commitment"></a>Forøge eller formindske en forpligtelse
Nogle gange er det nødvendigt at ændre en bekræftet forpligtelse. For eksempel hvis hårdt vejr resulterer i et forbrug til fjernelse af sne og relaterede tjenester, der er højere end planlagt, skal du muligvis forøge en forpligtelse. Når en indkøbsordre eller kreditorfaktura allerede refererer til en forpligtelseslinje, kan din mulighed for at slette eller ændre forpligtelseslinjen være begrænset.

## <a name="close-commitments"></a>Luk tilsagn
Forpligtelser skal lukkes manuelt.

-   Du kan lukke en enkelt forpligtelseslinje eller en forpligtelse i sin helhed ved hjælp af knappen **Luk** i handlingsruden for forpligtelsen.
-   Proces for indkøbsordrers årsafslutning tilbagefører automatisk ultimoposter og opretter eller opdaterer budget i forpligtelsesdokumenter i det nye regnskabsår. Dette håndteres af processen. Der kræves ingen manuel handling. Men når du har behandlet indkøbsordrer og forpligtelser, skal du gå til siden **Tilsagn lukket** for at lukke forpligtelserne i ultimoregnskabsåret.

**Vigtigt**! Når du vælger de forpligtelser, som du vil lukke, er det vigtigt, at du ikke vælger de forpligtelser, som du allerede har oprettet for det nye regnskabsår. Lukning af en forpligtelseslinje kan ikke fortrydes. Hvis du lukker en forpligtelseslinje ved en fejltagelse, skal du oprette en ny forpligtelse for at gendanne budgetreservationen. Hvis du vil vide mere om årsafslutningsprocessen, skal du se under [Årsafslutningen i den offentlige sektor](../public-sector/year-end-processing-public-sector.md).

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Regnskab i den offentlige sektor i Frankrig](emea-fra-public-sector-accounting.md)




