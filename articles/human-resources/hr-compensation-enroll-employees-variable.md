---
title: Melde en medarbejder til en variabel lønstruktur
description: Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a173403e79212be5e4aac36d99f349da159e08
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111938"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Melde en medarbejder til en variabel lønstruktur

Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere. Denne procedure forudsætter, at en variabel kompensationsstruktur er blevet oprettet med feltet Aktiver tilmelding angivet til Ja, og at berettigelsesregler er oprettet for den variable kompensationsstruktur. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Du begynder denne procedure ved at gå til Human Resources > Arbejdere > Medarbejdere > Kompensation > Tilmelding til variabel plan

1. Klik på Ny.
2. Klik på rullelisten i feltet Plan for at åbne opslaget.
    * Opslaget Plan filtreres til kun at vise de planer for variabel kompensation, som medarbejderen er berettiget til, baseret på Berettigelsesregler.  
3. Klik op linket i den valgte række på listen.
4. Slå udvidelsen af sektionen Generelt til/fra.
5. Angiv en dato i feltet Ikrafttrædelsesdato.
6. Klik på Gem.
7. Slå udvidelsen af sektionen Tilsidesættelser til/fra.
    * Eventuelt kan en dato for ansættelsesregel indstilles til at tilsidesætte medarbejderens ansættelsesdato, hvis ansættelsesreglen, der er angivet for den valgte variable struktur, er i Procent.  
    * Hvis den variable struktur er en procentdel af den grundlæggende struktur, kan bonusprocenten tilsidesættes for medarbejderen. Hvis den variable kompensationsstruktur er et antal enheder på plan, kan antallet af enheder tilsidesættes for medarbejderen.  
    * Hvis medarbejderen skal modtage et fladt beløb som bonus, kan du angive beløbet her.  
8. Slå udvidelse af sektionen Organisationsmæssige overstyringer til eller fra.
    * Hvis medarbejderens præstation skal tages i betragtning, præstationen i forskellige afdelinger eller en anden afdeling end den, der er tildelt på medarbejderens stilling, kan afdelingen tilsidesættes. Kolonnen Procent bør i alt være 100.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]