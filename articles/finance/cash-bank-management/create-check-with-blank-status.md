---
title: Opret checks, der har statussen Blank
description: I denne artikel beskrives, hvordan du kan oprette blankochecks for en bankkonto.
author: angelad116
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8d3f3857fe5261c1c95d02f3b7c7aaf9db7c096f
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151574"
---
# <a name="create-checks-that-have-blank-status"></a>Opret checks, der har statussen Blank

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan oprette blankochecks. Du kan f.eks. oprette en blankocheck for at registrere en check, der er blevet beskadiget og ikke kan bruges til betaling.

På siden **Checks** kan du udføre vedligeholdelsesopgaver for checks. Du kan f.eks. oprette nye checknumre og slette checks. Du kan også oprette checks med statussen **Blank**. Når blanke checks er oprettet, kan de ikke slettes eller genbruges i systemet.

> [!NOTE]
> Denne funktion er kun tilgængelig på siden **Checks**, hvis du aktiverer funktionen **Opret checks med statussen Blank på siden Checks** på siden **Administration af funktioner**. Hvis funktionen ikke er aktiveret, kan der kun oprettes checks, der har statussen **Blank**, fra dialogboksen **Betaling med check** under processen til oprettelse af betaling i Kreditor.

Hvis du vil åbne siden **Checks**, skal du gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**, og derefter i handlingsruden vælge **Checks** på fanen **Administrer betalinger** i gruppen **Relaterede oplysninger**. Du kan også gå **Kontant- og bankstyring \> Forespørgsler og rapporter \> Checks**.

Hvis du derefter vil oprette checks med statussen **Blank**, skal du vælge **Create blank checks** (Opret blanke checks) i handlingsruden. Når systemet opretter blanke checks, er den tilknyttede bankkonto midlertidigt deaktiveret. Dette reducerer risikoen for, at der genereres betalinger, samtidig med at der oprettes checks. Når behandlingen er fuldført, aktiveres den tilknyttede bankkonto igen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
