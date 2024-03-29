---
title: Konfigurationsproces for avanceret bankafstemning
description: Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme med banktransaktioner i Microsoft Dynamics 365 Finance. I denne artikel forklares opsætningsprocesserne ved afstemning.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a1757f7901a12a5b0fc3de730953c5b79cbefb
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715409"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Konfigurationsproces for avanceret bankafstemning

[!include [banner](../includes/banner.md)]

Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme med banktransaktioner i Microsoft Dynamics 365 Finance. I denne artikel forklares opsætningsprocesserne ved afstemning.  

Der er et antal enheder, der skal konfigureres, før du kan bruge den avancerede bankkontoafstemningsfunktion. Du kan finde flere oplysninger om opsætning af import af bankkontoudtog under [Konfigurer den avancerede importprocessen for bankkontoudtog](set-up-advanced-bank-reconciliation-import-process.md).  Krav til konfiguration af afstemningsprocessen er beskrevet nedenfor.

## <a name="transaction-codes"></a>Transaktionskategorier
Posteringskoder kan bruges som en del af sammenholdningsreglerne for bankafstemningen. Posteringskoder gør det nemmere kun at sammenholde de samme typer transaktioner mellem Finance og bankkontoudtoget. For at udføre denne type sammenholdelse skal du først definere posteringstyper, der bruges til banktransaktioner fra Finance, og derefter knytte disse typer til kontoudtogstransaktionskoder, der bruges af din bank. Posteringstyper for bankposteringer defineres på siden **Bankposttyper**. Det er også her, at du kan definere den hovedkonto, der skal bruges til posteringer, der er knyttet til denne posteringstype. 

Når dine banktransaktionskoder er defineret, skal du knytte dem til de transaktionskoder, der bruges i dine elektroniske bankkontoudtog. Denne tilknytningsproces udføres fra siden **Tilknytning af transaktionskode**. Tilknytning af transaktionskode fuldføres separat for hver bankkonto.

## <a name="matching-rules-and-matching-rule-sets"></a>Sammenholdningsregler og sammenholdningsregelsæt
Sammenholdningsregler giver dig mulighed at definere kriterier for automatisk afstemning mellem Finance-banktransaktioner og transaktioner på bankkontoudtog. Konfiguration af sammenholdningsregler udføres på siden **Sammenholdningsregler for afstemning**. Du kan finde flere oplysninger under [Oprette sammenholdningsregler for bankafstemning](set-up-bank-reconciliation-matching-rules.md). 

Sammenholdningsregelsæt bruges til at definere en gruppe af sammenholdningsregler, der køres i rækkefølge under bankafstemningsprocessen.  Sammenholdningsregelsæt konfigureres på siden **Sammenholdningsregelsæt for afstemning**.

## <a name="cash-and-bank-management-parameters"></a>Kontant- og bankstyringsparametre
Der er en række parametre, som er specifikke for den avancerede bankafstemningsproces på siden **Kontant- og bankstyringsparametre**.  **Vis beløb i kontoudtogslinje i debet/kredit** ændrer visningen af beløb på siden **Bankkontoudtog**. Hvis denne indstilling er valgt, vises bankkontoudtogets posteringsbeløb i separate debet- og kreditkolonner. Hvis den ikke er valgt, vises bankkontoudtogets posteringsbeløb i et enkelt beløbskolonne med passende fortegn. 

De valideringsindstillinger, der er angivet på siden med parametre, tilsidesætter de valg, der er angivet for sammenholdningsregler. For eksempel kan du ikke manuelt eller automatisk sammenholde dokumenter ud over den datoforskel, der er angivet på parametersiden. Og hvis indstillingen **Valider tilknytning af transaktionstype** er valgt, skal posteringstyperne tilknyttes mellem Finance-bankposteringen og transaktionen på bankkontoudtoget, for at transaktionerne kan sammenholdes manuelt eller automatisk. 

Du skal også konfigurere de nødvendige nummerserier på siden **Kontant- og bankstyringsparametre**.  Under fanen **Nummerserier** skal du indstille nummerseriekoder for hentning af **ID, kontoudtogs-id, afstemnings-id og bankafstemning**-hentningsreferencerne.

## <a name="bank-account-reconciliation-options"></a>Indstillinger for bankkontoafstemning
Du skal først aktivere avanceret bankafstemning for bankkontoen. En række yderligere indstillinger er tilgængelige på siden **Bankkonto**, når den avancerede bankkontoafstemningsfunktion er aktiveret. 

Funktionen **Brug bankkontoudtog som bekræftelse på elektroniske betalinger** integrerer funktionaliteten til bankkontoafstemning med elektronisk betalingsstatus. Når dette er aktiveret, oprettes der automatisk et bankdokument, når den elektroniske betalingsstatus er indstillet til **Sendt**. Desuden opdateres status for en elektronisk betaling fra **Sendt** til **Modtaget**, når betalingen er sammenholdt, afstemt og bogført. 

Feltet **Bankkontonavn i kontoudtog** er det navn, der anvendes til bankkontoen på dine elektroniske bankkontoudtog. Dette navn bruges, når det skal bestemmes, hvilke posteringer der skal importeres til en bankkonto fra et kontoudtog, der kan indeholde oplysninger om flere bankkonti. 

Indstillingen **Afstem efter import** validerer automatisk bankkontoudtoget, opretter en ny bankafstemning og regneark og kører Standard for sammenholdningsregelsæt. Denne funktion automatiserer processen indtil det punkt, hvor der er posteringer, som skal afstemmes manuelt. Standardindstillingen på bankkontoen anvendes ved import.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
