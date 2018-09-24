---
title: Administrere validering af IBAN-kontonummer (International Bank Account Number)
description: I dette emne beskrives, hvordan du administrerer validering af IBAN-kontonumre.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: da-dk
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Administrere validering af IBAN-kontonummer (International Bank Account Number)

[!include [banner](../includes/banner.md)]

Validering af IBAN-kontonummeret øger omfanget af den validering, der sker, når du føjer et IBAN til en bankkonto.

IBAN-strukturen gemmes i Microsoft Dynamics 365 for Finance and Operations og indlæses automatisk, første gang du bruger IBAN-nummeret på bankkonti. Bankkontonummeret er en del af den struktur, der er defineret for et IBAN-nummer. Hvis placeringen og længden af kontonummeret i IBAN ikke stemmer med den placering, der er defineret i strukturen for hvert land eller område, får du vist advarselsmeddelelser baseret på denne struktur.

## <a name="set-up-iban-structures"></a>Oprette IBAN-strukturer

1. Gå til **Kontant- og bankstyring \> Opsætning \> IBAN-strukturer**.
2. Bemærk, at IBAN-strukturerne for hvert land eller område er oprettet automatisk.
3. Hvis du skal tilpasse strukturerne for et bestemt land eller område, kan du redigere dem.
4. Definitioner af strukturerne bliver en del af hver ny frigivelse. Du kan bruge menuen **Nulstil strukturer** til at indlæse de nyeste definitioner efter hvert opdatering.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Validere IBAN-strukturen på en bankkonto

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Opret en bankkonto.
3. I oversigtspanelet **Flere oplysninger** skal du angive IBAN.

    Hvis placeringen og længden af kontonummeret i IBAN ikke stemmer med den placering, der er defineret i strukturen for hvert land eller område, får du vist meddelelse. Du kan ikke fortsætte, hvis længden af IBAN ikke stemmer overens med længden i IBAN-strukturen.

    Valideringen kontrollerer også, at nummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankkontonummeret. Hvis bankkontonummeret ikke stemmer overens, modtager du en advarsel. Denne meddelelse er kun en advarsel. Du kan fortsætte, selvom bankkontoen ikke stemmer overens.

