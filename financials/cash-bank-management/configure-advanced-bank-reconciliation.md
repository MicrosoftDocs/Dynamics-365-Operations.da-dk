---
title: Oversigt over avanceret bankafstemning
description: "Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme med banktransaktioner i Microsoft Dynamics 365 for Operations.  I denne artikel forklares opsætningsprocesserne ved afstemning."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6c6b171fbba90b02b80c70783ecfd9ab57beb96d
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Oversigt over avanceret bankafstemning

[!include[banner](../includes/banner.md)]


Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme med banktransaktioner i Microsoft Dynamics 365 for Operations.  I denne artikel forklares opsætningsprocesserne ved afstemning.  

Der er et antal enheder, der skal konfigureres, før du kan bruge den avancerede bankkontoafstemningsfunktion. Du kan finde flere oplysninger om opsætning af import af bankkontoudtog under [Konfigurere importprocessen for bankkontoudtog](set-up-advanced-bank-reconciliation-import-process.md).  Krav til konfiguration af afstemningsprocessen er beskrevet nedenfor.

## <a name="transaction-codes"></a>Transaktionskategorier
Posteringskoder kan bruges som en del af sammenholdningsreglerne for bankafstemningen.  Posteringskoder gør det nemmere kun at sammenholde de samme typer transaktioner mellem Dynamics 365 for Operations og bankkontoudtoget.  For at udføre denne type sammenholdelse skal du først definere posteringstyper, der bruges til banktransaktioner fra Dynamics 365 for Operations og derefter knytte disse typer til kontoudtogstransaktionskoder, der bruges af din bank.  Posteringstyper for bankposteringer i Dynamics 365 for Operations defineres på siden **Bankposttyper**.  Det er også her, at du kan definere den hovedkonto, der skal bruges til posteringer, der er knyttet til denne posteringstype. 

Når dine Dynamics 365 for Operations-banktransaktionskoder er defineret, skal du knytte dem til de transaktionsartskoder, der bruges i dine elektroniske bankkontoudtog.  Denne tilknytningsproces udføres fra siden **Tilknytning af transaktionskode**.  Tilknytning af transaktionskode fuldføres separat for hver bankkonto.

## <a name="matching-rules-and-matching-rule-sets"></a>Sammenholdningsregler og sammenholdningsregelsæt
Sammenholdningsregler giver dig mulighed at definere kriterier for automatisk afstemning mellem Dynamics 365 for Operations-banktransaktioner og transaktioner på bankkontoudtog.  Konfiguration af sammenholdningsregler udføres på siden **Sammenholdningsregler for afstemning**.  Du kan finde flere oplysninger under [Oprette sammenholdningsregler for bankafstemning](set-up-bank-reconciliation-matching-rules.md). 

Sammenholdningsregelsæt bruges til at definere en gruppe af sammenholdningsregler, der køres i rækkefølge under bankafstemningsprocessen.  Sammenholdningsregelsæt konfigureres på siden **Sammenholdningsregelsæt for afstemning**.

## <a name="cash-and-bank-management-parameters"></a>Kontant- og bankstyringsparametre
Der er en række parametre, som er specifikke for den avancerede bankafstemningsproces på siden **Kontant- og bankstyringsparametre**.  **Vis beløb i kontoudtogslinje i debet/kredit** ændrer visningen af beløb på siden **Bankkontoudtog**.  Hvis denne indstilling er valgt, vises bankkontoudtogets posteringsbeløb i separate debet- og kreditkolonner.  Hvis den ikke er valgt, vises bankkontoudtogets posteringsbeløb i et enkelt beløbskolonne med passende fortegn. 

De valideringsindstillinger, der er angivet på siden med parametre, tilsidesætter de valg, der er angivet for sammenholdningsregler.  For eksempel kan du ikke manuelt eller automatisk sammenholde dokumenter ud over den datoforskel, der er angivet på parametersiden.  Også, hvis indstillingen **Valider tilknytning af transaktionstype** er valgt, skal posteringstyperne tilknyttes mellem Dynamics 365 for Operations-bankposteringen og transaktionen på bankkontoudtoget, for at transaktionerne kan sammenholdes manuelt eller automatisk. 

Du skal også konfigurere de nødvendige nummerserier på siden **Kontant- og bankstyringsparametre**.  Under fanen **Nummerserier** skal du indstille nummerseriekoder for hentning af **ID, kontoudtogs-id, afstemnings-id og bankafstemning**-hentningsreferencerne.

## <a name="bank-account-reconciliation-options"></a>Indstillinger for bankkontoafstemning
Du skal først aktivere avanceret bankafstemning for bankkontoen.  En række yderligere indstillinger er tilgængelige på siden **Bankkonto**, når den avancerede bankkontoafstemningsfunktion er aktiveret. 

Funktionen **Brug bankkontoudtog som bekræftelse på elektroniske betalinger** integrerer funktionaliteten til bankkontoafstemning med elektronisk betalingsstatus.  Når dette er aktiveret, oprettes der automatisk et bankdokument, når den elektroniske betalingsstatus er indstillet til **Sendt**.  Desuden opdateres status for en elektronisk betaling fra **Sendt** til **Modtaget**, når betalingen er sammenholdt, afstemt og bogført. 

Feltet **Bankkontonavn i kontoudtog** er det navn, der anvendes til bankkontoen på dine elektroniske bankkontoudtog.  Dette navn bruges, når det skal bestemmes, hvilke posteringer der skal importeres til en bankkonto fra et kontoudtog, der kan indeholde oplysninger om flere bankkonti. 

Indstillingen **Afstem efter import** validerer automatisk bankkontoudtoget, opretter en ny bankafstemning og regneark og kører Standard for sammenholdningsregelsæt.  Denne funktion automatiserer processen indtil det punkt, hvor der er posteringer, som skal afstemmes manuelt.  Standardindstillingen på bankkontoen anvendes ved import.




