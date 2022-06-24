---
title: Genklassificer anlægsaktiver
description: Denne artikel indeholder en forklaring på processen til genklassificering af aktiver. Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c046b131afd1728b26465816eee98ee1898e49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861381"
---
# <a name="reclassify-fixed-assets"></a>Genklassificer anlægsaktiver

[!include [banner](../../includes/banner.md)]

Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe. 

Når et anlægsaktiv genklassificeres:

- Alle bøger til det eksisterende anlægsaktiv oprettes for det nye anlægsaktiv. Oplysninger, der var oprettet for det oprindelige anlægsaktiv, kopieres til det nye anlægsaktiv. Status for det oprindelige anlægsaktivs bøger er Lukket. 

- De nye anlægskartoteker indeholder datoen for genklassificeringen i feltet **Anskaffelsesdato**. Datoen i feltet **Startdato for afskrivning** kopieres fra de oprindelige aktivoplysninger. Hvis afskrivningen allerede er startet, vises datoen for genklassificeringen i feltet **Dato, hvor afskrivning sidst blev udført**. 

- De eksisterende anlægsaktivposteringer for det oprindelige anlægsaktiv annulleres og oprettes for det nye anlægsaktiv igen.

- Når et aktiv, der har en overførselstransaktion, er blevet omklassificeret, vil systemet vise en meddelelse i **Handlingscenteret** for at angive, at en overførselstransaktion ikke er fuldført under genklassificeringsprocessen. Det er nødvendigt at fuldføre en overførselstransaktion for at flytte de eksisterende genklassificeringstransaktioner til de relevante økonomiske dimensioner. 

   Under genklassificeringsprocessen kører systemet følgende handlinger for at genklassificere aktivsaldoen fra det oprindelige aktiv til det nye aktiv. 
   
   - I genklassificeringsprocessen kopieres dataene fra det oprindelige anlægskartotek til det nye anlægskartotek.

   - Genklassificeringstransaktionen bruger oplysninger fra den oprindelige bogførte anskaffelse, som omfatter oplysninger om økonomiske dimensioner, der er medtaget i anskaffelsestransaktionen.  
   
   - Samtidig tilbagefører genklassificeringsprocessen den oprindelige transaktion for aktivets anskaffelse og overførsel. 

Følgende diagram og procedure viser et eksempel på genklassificeringsprocessen. 

[![Diagram, der viser processen for genklassificering.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Benyt følgende fremgangsmåde for at genklassificere et anlægsaktiv:

1. Gå til **Anlægsaktiver > Periodiske opgaver > Genklassificering**.
2. I feltet **Anlægsaktivgruppe** skal du vælge den gruppe, som skal genklassificeres.
3. Vælg det anlægsaktiv, der skal genklassificeres, i feltet **Nummer på anlægsaktiv**.
4. Vælg en gruppe, som det nye anlægsaktiv skal overføre til, i feltet **Ny anlægsaktivgruppe**.
    * Hvis den nye anlægsaktivgruppe er knyttet til en nummerserie, opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien for den nye anlægsaktivgruppe. Ellers opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien, der er konfigureret på siden **Parametre for anlægsaktiver**. Hvis der ikke er konfigureret en nummerserie på siden **Parametre for anlægsaktiver**, skal du angive et tal i feltet **Nyt nummer på anlægsaktivet**.  
5. Indtast en dato i feltet **Dato for genklassificering**.
6. Indtast eller vælg en værdi i feltet **Bilagsserie**.
7. Vælg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
