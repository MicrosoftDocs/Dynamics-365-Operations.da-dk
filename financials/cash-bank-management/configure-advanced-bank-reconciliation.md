---
title: Oversigt over avanceret bankafstemning
description: "Avanceret bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme med bankposteringer i Microsoft Dynamics 365 for operationer.  I denne artikel forklares opsætningsprocesserne ved afstemning."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Oversigt over avanceret bankafstemning

Avanceret bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme med bankposteringer i Microsoft Dynamics 365 for operationer.  I denne artikel forklares opsætningsprocesserne ved afstemning.  

Der er et antal enheder, der skal konfigureres, før du bruger den avancerede funktionen Bankkontoafstemning. Finde flere oplysninger om opsætning af bank-sætning import, [opsætning af bank-sætning importprocessen](set-up-advanced-bank-reconciliation-import-process.md).  Krav til konfiguration af afstemningen er beskrevet nedenfor.

## <a name="transaction-codes"></a>Transaktionskategorier
Posteringskoder kan bruges som en del af afstemningen, der svarer til regler.  Posteringskoder hjælper med at svarer til de samme typer transaktioner mellem Dynamics 365 for operationer og bankens kontoudtog.  For at gøre denne type sammenholdelse, skal du først definere posteringstyper, der bruges til banktransaktioner fra Dynamics 365 for operationer derefter knytte disse typer til kontoudtogstransaktionskoder, der bruges af din bank.  Posteringstyper for Dynamics 365 for operationer bankposteringer, der er defineret på den **bankposteringstypen** side.  Det er også, hvor du kan definere den hovedkonto, der skal bruges til posteringer, der er knyttet til denne type transaktion. 

Når din Dynamics 365 for operationer bank Posteringskoder er defineret, knyttes du derefter disse til de transaktionsartskoder, der bruges i din elektroniske bankkontoudtog.  Denne tilknytningsprocessen er færdig ved hjælp af den **transaktionskode** side.  Tilknytning af transaktionen er fuldført separat for hver bankkonto.

## <a name="matching-rules-and-matching-rule-sets"></a>Sammenholdningsregler og sammenholdningsregelsæt
Tilsvarende regler giver dig mulighed at definere kriterier for automatisk afstemning mellem Dynamics 365 for transaktioner på bankens operationer og transaktioner på bankens kontoudtog.  Konfiguration af tilsvarende regler er udført på **sammenholdningsregler** side.  Yderligere oplysninger finder du [opsætning af bank sammenholdningsregler](set-up-bank-reconciliation-matching-rules.md). 

Tilsvarende regelsæt, der bruges til at definere en gruppe af tilsvarende regler, der køres i rækkefølge under afstemningen bank.  Tilsvarende regelsæt er konfigureret på den **sammenholdningsregelsæt** side.

## <a name="cash-and-bank-management-parameters"></a>Kontant- og bankstyringsparametre
Der er en række parametre, som er specifikke for avancerede bankafstemningsprocessen på den **parametre for Likviditets- og bankstyring administration** side.  Den **Vis beløbet i debet/kredit** ændrer visningen af beløb på den **Bank sætning** side.  Hvis denne indstilling er markeret, vises bankens kontoudtog posteringsbeløbene i separate debet og kredit kolonner.  Hvis der ikke er markeret, vises bankens kontoudtog posteringsbeløbene i et enkelt beløb kolonne med passende fortegn. 

Valideringsindstillinger på siden parametre, tilsidesætter de valg, der er angivet på tilsvarende regler.  For eksempel, du kan ikke manuelt eller svarer til automatisk dokumenter ud over den dato forskel, der er angivet på siden parametre.  Også, hvis indstillingen for at **validere tilknytning af transaktionstype** er valgt, skal posteringstyperne knyttes mellem Dynamics-365 for operationer bankpostering og transaktion på bankens kontoudtog, for at transaktionerne, der kan være manuelt eller automatisk sammen. 

Du skal også konfigurere de nødvendige nummerserier i den **parametre for Likviditets- og bankstyring administration** side.  På den **nummerserier** under fanen sæt nummerseriekoder til hentning af **-ID, opgørelses-ID, afstemme ID og Bank afstemning** referencer.

## <a name="bank-account-reconciliation-options"></a>Indstillinger for bankkontoafstemning
Du skal først aktivere avanceret bankafstemning for bankkontoen.  En række yderligere indstillinger er tilgængelige på den **bankkonto** side, når den avancerede funktionen Bankkontoafstemning er aktiveret. 

**Brug bankkontoudtog som bekræftelse af elektronisk betaling** integrerer funktionaliteten i funktionen Bankkontoafstemning med elektronisk betaling status.  Når dette er aktiveret, et bankdokument oprettes automatisk for elektronisk betalingsstatus er angivet til **sendt**.  Desuden opdateres status for en elektronisk betaling fra **sendt** til **modtaget** når betalingen er afstemt, afstemmes og bogføres. 

Den **bankkonto navn i sætninger** felt er det navn, der anvendes til bankkontoen på dine elektroniske bankkontoudtog.  Dette navn bruges, når det bestemmes, hvilke posteringer der skal importeres til en bankkonto i en sætning, der kan indeholde oplysninger om flere bankkonti. 

Mulighed for at **afstemning efter import** vil automatisk validere bankkontoudtoget, oprette en ny bankafstemningen og regneark og køre standard tilsvarende regelsæt.  Denne funktion automatiserer op til sted, hvor de transaktioner, der skal afstemmes manuelt.  Når du importerer standard indstillingen på bank.


