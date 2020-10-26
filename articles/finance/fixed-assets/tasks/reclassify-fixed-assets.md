---
title: Genklassificer anlægsaktiver
description: Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd108f2e778b31749c66b2787d9f59467cae97dd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977209"
---
# <a name="reclassify-fixed-assets"></a>Genklassificer anlægsaktiver

[!include [banner](../../includes/banner.md)]

Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe. 

Når et anlægsaktiv genklassificeres:

* Alle bøger til det eksisterende anlægsaktiv oprettes for det nye anlægsaktiv. Oplysninger, der var oprettet for det oprindelige anlægsaktiv, kopieres til det nye anlægsaktiv. Status for det oprindelige anlægsaktivs bøger er Lukket. 

* Det nye anlægsaktivs nye bøger indeholder datoen for genklassificeringen i feltet **Anskaffelsesdato**. Datoen i feltet **Startdato for afskrivning** kopieres fra de oprindelige aktivoplysninger. Hvis afskrivningen allerede er startet, vises datoen for genklassificeringen i feltet **Dato, hvor afskrivning sidst blev udført**. 

* De eksisterende anlægsaktivposteringer for det oprindelige anlægsaktiv annulleres og oprettes for det nye anlægsaktiv igen.

Benyt følgende fremgangsmåde for at genklassificere et anlægsaktiv:

1. Gå til **Anlægsaktiver > Periodiske opgaver > Genklassificering**.
2. I feltet **Anlægsaktivgruppe** skal du vælge den gruppe, som skal genklassificeres.
3. Vælg det anlægsaktiv, der skal genklassificeres, i feltet **Nummer på anlægsaktiv**.
4. Vælg en gruppe, som det nye anlægsaktiv skal overføre til, i feltet **Ny anlægsaktivgruppe**.
    * Hvis den nye anlægsaktivgruppe er knyttet til en nummerserie, opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien for den nye anlægsaktivgruppe. Ellers opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien, der er konfigureret på siden **Parametre for anlægsaktiver**. Hvis der ikke er konfigureret en nummerserie på siden **Parametre for anlægsaktiver**, skal du angive et tal i feltet **Nyt nummer på anlægsaktivet**.  
5. Indtast en dato i feltet **Dato for genklassificering**.
6. Indtast eller vælg en værdi i feltet **Bilagsserie**.
7. Klik på **OK**.
