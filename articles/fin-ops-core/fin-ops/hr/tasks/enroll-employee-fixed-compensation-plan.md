---
title: Melde en medarbejder til en fast lønplan
description: Chefen for kompensation og frynsegoder kan tildele medarbejdere faste lønplaner for at administrere deres grundløn.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ba197ee47d2a2da2372b12291e5625ddc9ba1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190505"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Melde en medarbejder til en fast lønplan

[!include [task guide banner](../../includes/task-guide-banner.md)]

Chefen for kompensation og frynsegoder kan tildele medarbejdere faste lønplaner for at administrere deres grundløn. Denne procedure forudsætter, at en fast lønplan er blevet oprettet og er aktiv, og at der er angivet berettigelsesregler for planen. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Du begynder proceduren ved at gå til Personale > Arbejdere > Medarbejdere > Kompensation > Fast plan

1. Klik på Ny.
2. Vælg en Fast løn-handling af typen Ansæt/genansæt for at beskrive ændringen af medarbejderens kompensation i feltet Handling.
3. Klik op linket i den valgte række på listen.
4. Klik på rullelisten i feltet Stilling for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
    * Det niveau, der vises, er fra jobbets kompensationsniveau for stillingen. Niveauet skal være angivet på jobbet, før kompensation kan tildeles medarbejderen.  
6. Vælg Fast løn-struktur for medarbejderen i feltet Plan. Opslaget Plan er filtreret til kun at vise de planer, som medarbejderen er berettiget til, baseret på Berettigelsesregler.
7. Find og vælg den ønskede post på listen.
    * Ikrafttrædelses- og udløbsdatoer for kompensation er standard fra start- og slutdatoer for tildeling af arbejderens stilling. Du kan justere disse datoer efter behov.  
    * Hvis Fast lønplan er en trinplan, skal du vælge det trin, der indeholder den korrekte lønsats for medarbejderen. Hvis Fast lønplan er en omfangs- eller klasseplan, skal du angive lønsatsen for medarbejderen. Lønsatsen valideres mod toleranceindstillingerne for planen og minimale og maksimale referencepunkter for jobbets kompensationsniveau.  
8. Klik på OK.
