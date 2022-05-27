---
title: Melde en medarbejder til en fast lønplan
description: Chefen for kompensation og frynsegoder kan tildele medarbejdere faste lønplaner for at administrere deres grundløn.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d611f2631a59fbe1e131e82ca9937a5adaaf2ebd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688735"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Melde en medarbejder til en fast lønplan


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Chefen for kompensation og frynsegoder kan tildele medarbejdere faste lønplaner for at administrere deres grundløn. Denne procedure forudsætter, at en fast lønplan er blevet oprettet og er aktiv, og at der er angivet berettigelsesregler for planen. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Du begynder proceduren ved at gå til **Personale** > **Arbejdere** > **Medarbejdere** > **Kompensation** > **Fast plan**.

1. Klik på **Ny**.
2. Vælg en Fast løn-handling af typen  **Ansæt/genansæt**  for at beskrive ændringen af medarbejderens kompensation i feltet **Handling**.
3. Klik op linket i den valgte række på listen.
4. Klik på rullelisten i feltet **Stilling** for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
    * Det niveau, der vises, er fra oversigtspanelet **Kompensation** > **Niveau**-felt fra **Job**, der er tildelt til **Stilling**. Niveauet skal være angivet på jobbet, før kompensation kan tildeles medarbejderen.  
6. Vælg Fast løn-struktur for medarbejderen i feltet **Plan**. Opslaget **Plan** er filtreret til kun at vise de planer, som medarbejderen er berettiget til, baseret på **Berettigelsesregler**.
7. Find og vælg den ønskede post på listen.
    * **Ikrafttrædelses**- og **udløbsdatoer** for kompensation er standard fra start- og slutdatoer for tildeling af arbejderens stilling. Du kan justere disse datoer efter behov.  
    * Hvis Fast lønplan er en trinplan, skal du vælge det trin, der indeholder den korrekte lønsats for medarbejderen. Hvis Fast lønplan er en omfangs- eller klasseplan, skal du angive lønsatsen for medarbejderen. Lønsatsen valideres mod toleranceindstillingerne for planen og minimale og maksimale referencepunkter for jobbets kompensationsniveau.  
8. Klik på **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
