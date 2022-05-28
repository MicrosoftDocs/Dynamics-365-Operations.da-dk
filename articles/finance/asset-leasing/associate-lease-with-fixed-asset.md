---
title: Tilknytte anlægsaktiv med en leasingaftale
description: I emnet forklares, hvordan et eksisterende anlægsaktiv knyttes til en ny leasingaftale.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0ae7a850ceb13cb41ee5adc406e71105cdad4fe
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712140"
---
# <a name="associate-fixed-assets-with-leases"></a>Tilknytte anlægsaktiv med en leasingaftale

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I emnet forklares, hvordan et eksisterende anlægsaktiv knyttes til en ny leasingaftale. Når du knytter et anlægsaktiv til en rettighed, vil aktivets aktivværdi (ROU) ved første anerkendelse blive anskaffelsesomkostningen for anlægsaktivet.

Før du kan knytte et anlægsaktiv til en leasingaftale, skal du oprette en post for anlægsaktivet i anlægsaktiver. Derefter skal du på siden **Leasingoversigt** oprette en leasingaftale og knytte aktivet til den pågældende leasingaftale.

1. Tilføj en leasignaftale ved at følge trinnene i [Tilføj eller Kopiér leasingaftaler](add-lease.md). På siden **Tilføj leasingaftale** i feltet **Anlægsaktivnummer** skal du vælge det aktiv, der endnu ikke er anskaffet.
2. Vælg **Kartoteker**, og bekræft betalingsplanen.
3. Vælg **Første indregning**.
4. Vælg **Aktivleasingkladde**.

    Postering af den oprindelige genkendelseskladde for leasingaftalen afskaffer anlægsaktivet for det beløb, der normalt debiteres på ROU aktivkontoen.

    Du kan nu se posteringstypen og bogføre anlægsaktivet.

5. Vælg **Kladdedetaljer**.
6. Vælg **linjer** for at se de enkelte linjer til kladdeposteringen.
7. Vælg den kladdelinje, der indeholder aktivet, og vælg derefter fanen **Anlægsaktiver**.

    Fanen **Anlægsaktiver** vises posteringstypen og bogføringen. Feltet **Transaktiontype** er som standard angivet til **Anskaffelse**, og feltet **Kartotek** angives til den aktuelle bogføringsmodel for anlægsaktivet.

Når du har bogført den første genkendelseskladdepost, vises transaktionen som en anskaffelsespostering for anlægsaktivet. Hvis du vil se transaktionstabellen, skal du gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver** og vælge **Vurderinger**. Du bør se, at den første genkendelseskladdepost har oprettet en anskaffelsespostering for det angivne anlægsaktiv.

Anlægsaktivet kan nu afskrives med standardafskrivningsfunktionen i anlægsaktiver. Du kan finde flere oplysninger om afskrivning under [Afskrivningsmetoder og -principper](../fixed-assets/depreciation-methods-conventions.md).

Når en leasing er tilknyttet et anlægsaktiv, opdateres feltet **Levetid** i anlægskartoteket, så det tilpasses den mindste værdi ud fra følgende kriterier: 

 - Aktivets brugstid
 - Leasingperioden fra den tilknyttede leasingbog

Hvis feltet **Overførsel af ejerskab** er angivet til **Ja** for leasingbogen, vil værdien i feltet **Levetid** altid være aktivets brugstid. 
 
Levetiden opdateres, hver gang leasingaftalen justeres for at sikre, at brugsretaktivet afskrives i løbet af leasingperioden, som om det blev afskrevet som et leaset anlægsaktiv.

> [!NOTE]
> Hvis du knytter et anlægsaktiv til en leasingaftale, deaktiveres knapperne til **Afskrivning af aktiv** og **Værdiforringelse af leasingaftale**. Du kan se anlægsaktivafskrivninger og leasingaftalens værdiforringelsestransaktioner fra anlægsaktiver. Knappen **Aaktivtransaktioner**, der åbner en forespørgselsform, deaktiveres også. Du kan også åbne formularen **Aktivtransaktioner** i anlægsaktiver.  

På siderne **Anlægsaktiver** og **Anlægskartoteket** vises det leasing-id, der er knyttet til et anlægsaktiv. Hvis et anlægsaktiv er tilknyttet en leasingaftale, vises leasing-id'et og beskrivelsen af leasingen i oversigtspanelet **Leasingoplysninger** på siden **Anlægsaktiver**. I forbindelse med anlægskartoteker, der er knyttet til leasingbøger, vil felterne **Leasing-id**, **Leasingbeskrivelse** og **Bogtype** vise oplysninger om den valgte anlægskartotek i oversigtspanelet **Leasingoplysninger** for at angive, at det er knyttet til en leasingbog.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
