---
title: Administrere validering af IBAN-kontonummer (International Bank Account Number)
description: Denne artikel beskriver, hvordan du administrerer validering af IBAN-kontonumre.
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 3d825e8699fbe10e080cd85f15d3d86f8c780f15
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880893"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Administrere validering af IBAN-kontonummer (International Bank Account Number)

[!include [banner](../includes/banner.md)]

Validering af IBAN-nummeret øger omfanget af den validering, der sker, når du føjer et IBAN-nummer til en bankkonto.

Oplysninger om IBAN-strukturen gemmes i Microsoft Microsoft Dynamics 365 Finance og indlæses automatisk, når du første gang bruger IBAN på bankkonti. De indeholder længden af IBAN-nummeret, startplaceringen af bankkontonummeret og registreringsnummeret og længden af bankkontonummeret og registreringsnummeret.

## <a name="set-up-iban-structures"></a>Oprette IBAN-strukturer

1. Gå til **Kontant- og bankstyring \> Opsætning \> IBAN-strukturer**.
2. Bemærk, at IBAN-strukturerne for hvert land eller område er oprettet automatisk.
3. Klik på knappen **Rediger**, hvis strukturen skal opdateres for et bestemt land eller område.
4. Definitioner af strukturerne bliver en del af hver ny frigivelse. Du kan bruge menuen **Nulstil strukturer** til at indlæse de nyeste definitioner efter hvert opdatering.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Validere IBAN-strukturen på en bankkonto

1. Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.
2. Opret en bankkonto.
3. I oversigtspanelet **Flere oplysninger** skal du angive IBAN.

    Hvis længden af IBAN-nummeret ikke svarer til den længde, der er defineret for hvert land eller område, vises en advarsel. Du kan ikke fortsætte, hvis længden af IBAN ikke stemmer overens med den angivne længde i IBAN-strukturen.

    Valideringen kontrollerer også, at nummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankkontonummeret. Hvis bankkontonummeret ikke stemmer overens, vises en advarsel. Denne meddelelse er kun en advarsel. Du kan fortsætte, selvom bankkontoen ikke stemmer overens.

    Valideringen kontrollerer også, at registreringsnummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankens registreringsnummer. Registreringsnummeret omfatter et banknummer og ofte en ekstra bankafdeling. Hvis bankens registreringsnummer ikke stemmer overens, vises en advarsel. Denne meddelelse er kun en advarsel. Du kan fortsætte, selvom bankregistreringsnummeret ikke stemmer overens.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
