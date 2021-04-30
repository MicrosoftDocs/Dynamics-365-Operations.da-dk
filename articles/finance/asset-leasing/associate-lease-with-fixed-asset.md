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
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881342"
---
# <a name="associate-fixed-assets-with-leases"></a>Tilknytte anlægsaktiv med en leasingaftale

[!include [banner](../includes/banner.md)]

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

> [!NOTE]
> Hvis du knytter et anlægsaktiv til en leasingaftale, deaktiveres knapperne til **Afskrivning af aktiv** og **Værdiforringelse af leasingaftale**. Du kan se anlægsaktivafskrivninger og leasingaftalens værdiforringelsestransaktioner fra anlægsaktiver. Knappen **Aaktivtransaktioner**, der åbner en forespørgselsform, deaktiveres også. Du kan også åbne formularen **Aktivtransaktioner** i anlægsaktiver.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
