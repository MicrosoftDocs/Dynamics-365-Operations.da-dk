---
title: Oprette leasingbøger
description: I dette emne beskrives de oplysninger, der vedligeholdes i leasingkartoteker. Leasingkartoteker indeholder de regnskabspolitikker, der bestemmer, hvordan en leasingaftale redegøres for i systemet.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ba442b3085593221e2182b848e6879a96bbca127
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727083"
---
# <a name="set-up-lease-books"></a>Oprette leasingbøger

[!include [banner](../includes/banner.md)]

Leasingkartoteker indeholder de regnskabspolitikker, der bestemmer, hvordan en leasingaftale redegøres for i systemet. Ud over bogføring af kontant grundlag understøtter aktivleasing følgende standarder:

- Almindeligt anerkendte regnskabsprincipper i USA (US GAAP)
- Accounting Standards Codification Topic 842 (ASC 842)
- ASC 840
- International Financial Reporting Standard 16 (IFRS 16)
- International bogholderi standard 17 (IAS 17)

Du kan oprette et nyt leasingkartotek ved at følge disse trin.

1. Gå til **Aktivleasing \> Konfiguration \> Leasingkartotek**.
2. Vælg **Ny** for at tilføje et kartotek.
3. Angiv følgende felter.

    | Navn                                     | Betegnelse |
    |------------------------------------------|-------------|
    | Posteringslag                            | Vælg det posteringslag, der skal bruges. Hvert enkelt kartotek, der er tilknyttet en leasingaftale, konfigureres for et bestemt posteringslag. Hvert posteringslag har forskellige bogføringsformål. |
    | Leasingtype                               | Vælg, om leasingaftalen skal klassificeres automatisk, eller om den skal foruddefineres som finansierings- eller driftsleasingaftale. |
    | Regnskabsstruktur                     | Vælg den struktur, der er tilknyttet kartoteket. |
    | Konfiguration af leasingperiode/brugstid          | Systemet klassificerer leasingaftalen som finansiel, hvis leasingtypen er angivet til **Automatisk**, og hvis leasingperioden for aktivets brugstid er større end eller lig med den procent, der er defineret i dette felt.  |
    | Konfiguration af nutidsværdi/handelsværdi af aktiv   | Angiv et heltal for at definere den tærskel, der bestemmer, hvilken leasingtype der skal bestemmes. Hvis den nuværende værdi af fremtidige minimums leasingbetalinger er større end den brugerdefinerede værdi fra opsætningen af kartoteket, og hvis kartotekets leasingklassifikation er indstillet til automatisk, klassificerer systemet leasingaftalen som en finansieringsleasing. |
    | Kortsigtet grænse                     | Angiv det antal måneder, der skal bruges som tærskel for kortfristede leasingaftaler. Hvis leasingperioden er mindre end eller lig med det antal måneder, du angiver her, klassificerer systemet leasingaftalen som en kortfristet leasingaftale, og den udskudte lejebehandling anvendes. |
    | Grænseværdi for lav værdi                      | Angiv et beløb, der skal bruges som en tærskel for leasingaftaler med lav værdi. Hvis aktivets rimelige værdi er mindre end eller lig med den værdi, du angiver her, klassificerer systemet leasingaftalen som en lavværdileasingaftale, og den udskudte lejebehandling anvendes. |
    | Betal til kreditor                            | Angiv denne indstilling til **Ja** for at tillade, at leasingbetalinger bogføres som en faktura til den kreditorkonto, der er angivet for hver leasingaftale. Når en leasingbetaling bogføres, vil kreditorkontoen blive krediteret. Hvis denne indstilling er angivet til **Nej**, krediteres den konto, der er angivet for **Leasingbetaling**-bogføringstypen for siden **Leasingbogføringsparametre** i stedet. |
    | Leasingkonvention                       | Vælg convention for udfyldningsdatoen for leasingaftalen:<ul><li><b>Ingen</b> – Brug leasingaftalens startdato som startdato.</li><li><b>Fuld måned</b> - Brug den første dag i måneden, hvor startdatoen for leasingaftalen ligger, som startdato.</li></ul><p>Hvis du vælger <b>Ingen</b>, er der en risiko for, at passiv-amortisering og afskrivningsplaner for aktiver periodiseres og bogføres udgifter midt i måneden i stedet for ved udgangen af måneden. Hvis du vælger <b>Fuld måned</b>, sikrer du, at systemet begynder at gøre regnskab for lejen den første dag i måneden, og at hele månedens udgift periodiseres og bogføres den sidste dag i måneden.</p><p><strong>Bemærk:</strong> Funktionen til leasingkonventioner kan aktiveres via Funktionsstyring. I arbejdsområdet i <b>Funktionsstyring</b> skal du finde og vælge den funktion, der hedder <b>Leasingkonvention for leasingfunktionen</b>, og derefter vælge <b>Aktivér nu</b>.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
