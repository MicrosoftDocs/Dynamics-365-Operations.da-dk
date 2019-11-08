---
title: Administrere validering af IBAN-kontonummer (International Bank Account Number)
description: I dette emne beskrives, hvordan du administrerer validering af IBAN-kontonumre.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2aaccd7c09d6daf8a237a433cc22ac1bfc3c1541
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551244"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Administrere validering af IBAN-kontonummer (International Bank Account Number)

[!include [banner](../includes/banner.md)]

Validering af IBAN-nummeret øger omfanget af den validering, der sker, når du føjer et IBAN-nummer til en bankkonto.

Oplysninger om strukturen af IBAN er gemt i Microsoft Dynamics 365 Finance. Disse oplysninger indlæses automatisk, første gang du bruger IBAN-nummeret på bankkonti. De indeholder længden af IBAN-nummeret, startplaceringen af bankkontonummeret og registreringsnummeret og længden af bankkontonummeret og registreringsnummeret.

## <a name="set-up-iban-structures"></a>Oprette IBAN-strukturer

1. Gå til **Kontant- og bankstyring \> Opsætning \> IBAN-strukturer**.
2. Bemærk, at IBAN-strukturerne for hvert land eller område er oprettet automatisk.
3. Hvis du vil tilpasse strukturerne for et bestemt land eller område, kan du redigere dem.
4. Definitioner af strukturerne bliver en del af hver ny frigivelse. Du kan bruge menuen **Nulstil strukturer** til at indlæse de nyeste definitioner efter hvert opdatering.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Validere IBAN-strukturen på en bankkonto

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Opret en bankkonto.
3. I oversigtspanelet **Flere oplysninger** skal du angive IBAN.

    Hvis længden af IBAN-nummeret ikke svarer til den længde, der er defineret for hvert land eller område, vises en advarsel. Du kan ikke fortsætte, hvis længden af IBAN ikke stemmer overens med den angivne længde i IBAN-strukturen.

    Valideringen kontrollerer også, at nummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankkontonummeret. Hvis bankkontonummeret ikke stemmer overens, vises en advarsel. Denne meddelelse er kun en advarsel. Du kan fortsætte, selvom bankkontoen ikke stemmer overens.

    Valideringen kontrollerer også, at registreringsnummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankens registreringsnummer. Registreringsnummeret omfatter et banknummer og ofte en ekstra bankafdeling. Hvis bankens registreringsnummer ikke stemmer overens, vises en advarsel. Denne meddelelse er kun en advarsel. Du kan fortsætte, selvom bankregistreringsnummeret ikke stemmer overens.