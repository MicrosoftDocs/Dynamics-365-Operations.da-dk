---
title: Forpligtelser i den offentlige sektor i Frankrig
description: "Tilsagn er kildedokumenter til budgetstyring, som bruges af den offentlige sektor i Frankrig. De bruges til at reservere budgetterede beløb, så du kan spore udtrykkeligt budgetreservationer for administration og rapportering i hele udgiftscyklussen, en organisation."
author: rschloma
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetControlConfiguration, PurchAgreement, PurchCommitment_PSN, PurchTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19531
ms.assetid: dbdb051c-9240-4f00-9a60-122c5f2e62ea
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 57bb3c122339b89c96f89faff1d741fa8aa2df2f
ms.lasthandoff: 03/31/2017


---

# <a name="commitments-in-the-public-sector-in-france"></a>Forpligtelser i den offentlige sektor i Frankrig

Tilsagn er kildedokumenter til budgetstyring, som bruges af den offentlige sektor i Frankrig. De bruges til at reservere budgetterede beløb, så du kan spore udtrykkeligt budgetreservationer for administration og rapportering i hele udgiftscyklussen, en organisation. 

Når forpligtelser, der bruges som en del af budgetprocessen, er hver købsaftale, en indkøbsordre og en kreditorfaktura knyttet til mindst én forpligtelse. Forpligtelsen, der eftergives, når indkøbsordren er bekræftet, og midlerne, der er frigivet fra købsaftalen. Når en faktura ikke refererer til en indkøbsordre eller købsaftale, eftergives den forpligtelse, der er tilknyttet fakturaen, når fakturaen bogføres. En forpligtelse kan desuden angive en leverandør. Når der er angivet en kreditor, har en købsordre, købsaftale eller kreditorfaktura, der henviser til forpligtelsen, der samme leverandør. Forpligtelser, der er gyldige fra den dato, de er oprettet til slutningen af regnskabsåret, eller indtil de er lukket. Tilsagn kan ikke overføres fra ét regnskabsår til næste. Yderligere oplysninger finder du [Luk forpligtelser](#close) i dette emne. 
>[!NOTE]
>Den **forpligtelsestype** på den **købsaftale** side er ikke relateret til engagement i dokumentet. Dette felt angiver kun, om købsaftalen er baseret på en værdi eller et antal.

## <a name="set-up-budget-control-and-related-prerequisites"></a>Konfigurere budgetstyring og relaterede forudsætninger
Før du kan bruge forpligtelser, engagement nummerserier skal defineres, skal konfigureres budgetstyring og disponible budgetbeløb skal være tilgængelige. Arbejdsgang for tilsagn er valgfri, men anbefales.

-   På den **budgetparametre** side, oprette nummerserier til forpligtelser.
-   Konfigurere arbejdsgang til at administrere gennemsynsprocessen for forpligtelser.
-   På den **konfiguration af budgetstyring** side, konfigurere budgetstyring. De indstillinger, der er anført nedenfor er påkrævet for forpligtelser. Indstillinger, der ikke er angivet her, kan vælges efter behov og praksis i organisationen.
    -   I den **disponible budgetmidler** skal du vælge følgende indstillinger:
        -   Oprindeligt budget
        -   Faktiske udgifter
        -   Budgetreservation for behæftelser
        -   Budgetreservationer for budgetreservationer
        -   Budgetreservationer for ikke-bekræftede budgetreservationer
    -   I den **bilag og kladder** afsnit:
        -   Kontroller, at både hoved og linje indstillinger er valgt for forpligtelser, indkøbsordrer og kreditorfakturaer.
        -   Kontroller, at den både hovedet og linje-indstillinger er markeret for indkøbsrekvisitioner.
    -   I den **aktivere budgetstyring** kan du aktivere budgetstyringskonfigurationen og aktiverer budgetstyring.
-   På den **Økonomiparametre** skal du kontrollere, at indstillingerne i den **rammeaftale** i den **Finans** afsnit er fjernet. Når du aktiverer forpligtelser, kan du ikke bogføre budgetmæssige transaktioner til Finans.

## <a name="consume-a-commitment"></a>Forbruge en forpligtelse
Der er tre måder at forbruge en forpligtelse.

-   **Tildele en købsaftale til en forpligtelse.** Forpligtelsen, der er forbrugt, når midler, der er frigivet fra købsaftalen. For at gøre dette skal du angive købsaftalen på linjen engagement, når du opretter en forpligtelse.
-   **Henvise til forpligtelsen direkte på en indkøbsordrelinje.** Forpligtelsen, der er forbrugt, når indkøbsordren er bekræftet. Ingen købsaftale er involveret. Dette gør du ved at oprette en købsordre ifølge din normale proces. Når du tilføjer en linje til indkøbsordren, kan du vælge forpligtelsen, der skal bruges til denne købsordre.
-   **Henvise til forpligtelsen direkte på en kreditorfaktura.** Der kan være en købsaftale, der er tildelt i hovedet i fakturaen, men ingen indkøbsordre er involveret. Forpligtelsen, der er forbrugt, når fakturaen bogføres. Dette gør du ved at oprette en kreditorfaktura ifølge din normale proces. Når du tilføjer en linje til fakturaen, markere forpligtelsen, der skal bruges til denne faktura.

En forpligtelse kan være begrænset til en bestemt leverandør, eller det kan være tilgængelige for tildeling til en kreditor. Hvis forpligtelsen er begrænset til en bestemt leverandør, den er tilgængelig for markering, når kreditorfakturaen eller køb order angiver den samme leverandør.

## <a name="increase-or-decrease-a-commitment"></a>Forøge eller formindske en forpligtelse
Nogle gange er det nødvendigt at ændre en bekræftet forpligtelse. For eksempel hvis hårdt vejr resulterer i højere end planlagt forbrug for fjernelse af sne og relaterede tjenester, du muligvis forøge en forpligtelse. Når en ordre eller en kreditor købsfaktura der allerede er refereret til en forpligtelse linje, kan muligheden for at slette eller ændre linjen forpligtelse begrænses.

## <a name="close-commitments"></a>Luk tilsagn
Forpligtelser skal lukkes manuelt.

-   Du kan lukke en enkelt engagement linje eller et engagement i hele ved hjælp af den **lukke** knap i handlingsruden, hvor forpligtelsen består.
-   Proces for indkøbsordrers årsafslutning automatisk annullerer ultimoposter og opretter eller opdaterer budget i forpligtelsesdokumenter i det nye regnskabsår. Dette foregår ved processen. Der kræves ingen manuel handling. Men når du har behandlet indkøbsordrer og forpligtelser, skal du gå til den **engagement i tæt** side for at lukke forpligtelserne i ultimoregnskabsåret.

**Vigtige**: Når du vælger de forpligtelser, som du vil lukke, er det vigtigt, at du ikke vælger de forpligtelser, som du allerede har oprettet for det nye regnskabsår. Lukke en forpligtelse linje kan ikke fortrydes. Hvis du lukker en forpligtelse linje ved en fejltagelse, skal du oprette en ny forpligtelse til at gendanne Budgetreservationen. Hvis du vil vide mere om årsafslutningsprocessen, se [årsafslutningen i den offentlige sektor](../public-sector/year-end-processing-public-sector.md).

<a name="see-also"></a>Se også
--------

[Offentlige regnskab i Frankrig](emea-fra-public-sector-accounting.md)


