---
title: Tilbageføre bogførte leasingtransaktioner
description: Dette emne forklarer, hvordan du tilbagefører en bogført leasingtransaktion. Alle transaktioner, der oprettes via aktivleasing, kan tilbageføres.
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
ms.openlocfilehash: 259fd8f41eade1e873225f0d95c499c8cb8c1a6a
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441760"
---
# <a name="reverse-posted-lease-transactions"></a>Tilbageføre bogførte leasingtransaktioner

[!include [banner](../includes/banner.md)]

Alle transaktioner, der oprettes via aktivleasing, kan tilbageføres. Posteringer, der tilbageføres via aktivleasing, opdaterer dine leasingdata. De opdaterer derfor også leveringsværdierne i leasingforpligtelsen og brugsretsaktivet (ROU).

Udfør følgende trin for at oprette en tilbageførselstransaktion for en leasingaftale.

1. På siden **Aktivtransaktioner** eller siden **Ansvarsposteringer** skal du vælge transaktion og derefter vælge **Tilbagefør transaktion**.
2. I den dialogboks, der vises, kan du redigere den dato, hvor tilbageførslen vil blive bogført. Som standard er feltet **Dato** angivet til bogføringsdatoen for transaktionen for den valgte postering. Tilbageførselsposten kan ikke bogføres tidligere end den oprindelige bogføringsdato for den valgte transaktion.
3. Vælg **OK**. Der bogføres en kladdepost, der tilbagefører den valgte post. Tilbageførslen vises på siden **Aktiv posteringer** eller siden **Ansvarsposteringer**, og nettototalen for den aktuelle saldo, der vises på siden, opdateres.

Når du vælger **Tilbagefør sporing**, vises en dialogboks, der viser både de oprindelige posteringer og de tilbageførte posteringer sammen med et nummer, der kaldes et *sporingsnummer*. Hvis tilbageførslen skal være nemmere at forstå og for at forbedre synligheden, kan du også spore tilbageførsler ved hjælp af planlægningen af rettigheder.

Feltet **Seneste kladdenummer** på siden **Tidsplan** viser kladdenumrene på posteringerne. Når en postering tilbageføres, opdateres dette felt med kladdenummeret på en tilbageført postering. Desuden markeres afkrydsningsfeltet **Tilbageført** for at angive, at transaktionen skal tilbageføres, og at feltet **Bogført** er markeret.

## <a name="revoke-a-reversed-transaction"></a>Fortryde en tilbageført postering

Udfør følgende trin for at annullere en tilbageført postering.

1. På siden **Tidsplan** eller siden **Transaktioner** skal du vælge den oprindelige postering.
2. Udfør ét af følgende trin:

    - Hvis du har valgt transaktionen på siden **Planlæg** skal du udføre trinnene til oprettelse af en kladde i [Oprette månedskladdeposteringer i en batch](create-monthly-journals-batch.md). Du skal bogføre kladden manuelt.
    - Hvis du valgte posteringen på siden **Transaktioner** skal du vælge **Tilbagefør transaktion**. Du får vist en meddelelse, der angiver, at denne tilbagekaldelse er en tilbageføring af en tidligere tilbageførsel, og at du kan redigere bogføringsdatoen for denne tilbagekaldelse. De generelle forretningsvalideringer har dog indflydelse på de datoer, der kan angives i feltet **Dato**. 

3. Vælg **OK**. Der bogføres en kladdepost, der tilbagefører den valgte post. Tilbageførslen vises på siden **Transaktioner**, og den samlede nettosaldo er gendannet til hvad, den var før den første tilbageførsel. Derfor er den påvirkning, tilbageførslen havde på saldiene negativ.

Når du vælger **Tilbagefør sporing**, vises en dialogboks, der viser både de oprindelige posteringer og de tilbageførte posteringer sammen med et nummer, der kaldes et sporingsnummer.

Du kan også spore annulleringer ved hjælp af den relevante **Tidsplan**-side. Feltet **Tilbagefør** fjernes, mens feltet **Kladde** er markeret. Derudover opdateres feltet **Seneste journalnummer** med kladdenummeret for den tilbagekaldte postering, og feltet **Kladdenummer** opdateres med kladdenummeret for tilbageførslen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]