---
title: Tilknytte anlægsaktiv med en leasingaftale
description: I emnet forklares, hvordan et eksisterende anlægsaktiv knyttes til en ny leasingaftale.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d627633e43c2e6f5cad90dfe4100ff95a71541f7
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441765"
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