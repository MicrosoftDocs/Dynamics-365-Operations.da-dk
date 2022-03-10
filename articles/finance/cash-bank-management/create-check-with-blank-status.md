---
title: Opret checks, der har statussen Blank
description: Dette emne forklarer, hvordan du kan oprette blanke checks for en bankkonto på siden Checks.
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3c431ed975aecf116fbf626018038b112a0a8cca063e1462e31e206480643e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720544"
---
# <a name="create-checks-that-have-blank-status"></a>Opret checks, der har statussen Blank

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan oprette blanke checks. Du kan f.eks. oprette en blank check for at registrere en check, der er blevet beskadiget og ikke kan bruges til betaling.

På siden **Checks** kan du udføre vedligeholdelsesopgaver for checks. Du kan f.eks. oprette nye checknumre og slette checks. Du kan også oprette checks med statussen **Blank**. Når blanke checks er oprettet, kan de ikke slettes eller genbruges i systemet.

> [!NOTE]
> Denne funktion er kun tilgængelig på siden **Checks**, hvis du aktiverer funktionen **Opret checks med statussen Blank på siden Checks** på siden **Administration af funktioner**. Hvis funktionen ikke er aktiveret, kan der kun oprettes checks, der har statussen **Blank**, fra dialogboksen **Betaling med check** under processen til oprettelse af betaling i Kreditor.

Hvis du vil åbne siden **Checks**, skal du gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**, og derefter i handlingsruden vælge **Checks** på fanen **Administrer betalinger** i gruppen **Relaterede oplysninger**. Du kan også gå **Kontant- og bankstyring \> Forespørgsler og rapporter \> Checks**.

Hvis du derefter vil oprette checks med statussen **Blank**, skal du vælge **Create blank checks** (Opret blanke checks) i handlingsruden. Når systemet opretter blanke checks, er den tilknyttede bankkonto midlertidigt deaktiveret. Dette reducerer risikoen for, at der genereres betalinger, samtidig med at der oprettes checks. Når behandlingen er fuldført, aktiveres den tilknyttede bankkonto igen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]