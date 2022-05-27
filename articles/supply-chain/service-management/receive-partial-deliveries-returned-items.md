---
title: Modtage delleveringer af returvarer
description: Delleverancer defineres ved hjælp af returordrelinjer, ikke returordreforsendelser.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c0e27e3a5cb6be36a1d69190ce1b01ecada48a6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677108"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Modtage delleveringer af returvarer    

[!include [banner](../includes/banner.md)]


Delleverancer defineres ved hjælp af returordrelinjer, ikke returordreforsendelser.

Hvis du modtager hele det antal, der er angivet på en returordrelinje, men intet fra de andre linjer i returordren, er leverancen ikke en delleverance. Hvis en returordrelinje derimod angiver, at ti enheder af en bestemt vare skal returneres, men du kun modtager fire, er det en delleverance.

Hvis en returforsendelse indeholder mindre end det samlede antal for en returordrelinje, kan du sætte forsendelsen til side og vente, indtil resten af det returnerede antal modtages, eller du kan registrere og bogføre den pågældende del af antallet.

## <a name="register-and-post-a-partial-quantity"></a>Registrere og bogføre en del af et antal

1.  Når du har valgt en returordre til modtagelse i formularen **Oversigt over modtagelse - Lagersted: %1, område: %2, Kladdenavn: %3** skal du klikke på **Start modtagelse** for at oprette modtagelseskladden og derefter klikke på **Kladder** \> **Vis modtagelser fra tilgange** at åbne formularen **Lokationskladde**.

2.  Vælg den kladdelinje, du vil arbejde med, og klik derefter på **Linjer** for at åbne formularen **Kladdelinjer, lokationer**.

3.  Vælg linjen for det varenummer, som du kun har modtaget en del af antallet af, og klik derefter på **Funktioner** \> **Splitning** for at åbne formularen **Splitning**.

4.  Angiv mængden af det samlede antal varer, der er modtaget, i feltet **Splitantal**, og klik derefter på **OK**.

5.  Vælg linjen for det antal varer, der er modtaget, i formularen **Kladdelinjer, lokationer**, og klik derefter på **Bogfør**. Du kan bogføre linjen for det yderligere antal, når varerne er modtaget.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]