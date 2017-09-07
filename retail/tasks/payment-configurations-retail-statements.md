--- 
title: " Betalingskonfigurationer for detailopgørelser"
description: "Denne procedure viser konfigurationer for betalingsmetoder for detailbutikker, der påvirker, hvordan detailopgørelser oprettes og bogføres."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ccb17342ebbec67a9d6223354a4daa1e99b05262
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="payment-configurations-for-retail-statements"></a> Betalingskonfigurationer for detailopgørelser

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure viser konfigurationer for betalingsmetoder for detailbutikker, der påvirker, hvordan detailopgørelser oprettes og bogføres.

Denne registrering anvender demofirmaet USRT.

1. Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på Konfigurer i handlingsruden.
5. Klik på Betalingsmetoder.
6. Udvid eller skjul sektionen Bogføring.
7. Klik på Rediger.
    * Vælg, om de beløb, der er modtaget for denne betalingsmetode, skal bogføres på en finanskonto eller bankkonto.  
    * Vælg den konto, som beløb, der er modtaget til denne betalingsmetode, skal bogføres på.  
    * Vælg en konto for at bogføre eventuelle forskelle mellem det samlede posteringsbeløb, der er modtaget, og det beløb, der er optalt for denne betalingsmetode.  
    * I dette felt angiver du et beløb til at styre, når differencebeløbet skal bogføres til en anden differencekonto. Du kan bruge til at spore store forskelle.  
    * Vælg en konto til bogføring af eventuelle forskelle mellem det samlede posteringsbeløb, der er modtaget, og det optalte beløbs, når den overstiger den værdi, der er defineret i feltet "Maksimale differencebeløb".  
    * Vælg "Ja" for at bogføre beløb til indsættelse i bank på en separat konto.  
    * I dette felt kan du vælge, om beløb til indsættelse i bank skal bogføres på en finanskonto eller en bankkonto.  
    * Vælg den konto, som beløb til indsættelse i bank skal bogføres på.  
    * Vælg den bankposteringstype, der skal bruges ved bogføring af beløb til indsættelse i bank på bankkontoen.  
    * Vælg "Ja" for at bogføre deponering til pengeskab på en separat konto.  
    * Vælg om deponeringer til pengeskab skal bogføres på finanskontoen eller bankkontoen.  
    * Vælg den konto, som deponeringer til pengeskab skal bogføres på.  
8. Klik på Gem.

