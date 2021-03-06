---
title: Udsende spørgeskemaer ved hjælp af planlægning
description: Planlægning af spørgeskemaet kan du planlægge og fordele spørgeskemaer til flere svarpersoner.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 952048ce0a2ac94be70d7bde0dc52610f19151ed
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056294"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Udsende spørgeskemaer ved hjælp af planlægning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Planlægning af spørgeskemaet kan du planlægge og fordele spørgeskemaer til flere svarpersoner. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

## <a name="create-a-questionnaire-schedule"></a>Opret en tidsplan for et spørgeskema

1. Gå til spørgeskemaet > fordel > tidsplaner for spørgeskemaer.

2. Klik på Ny.

3. Skriv en værdi i feltet Planlægning.

4. Skriv en værdi i feltet Beskrivelse.
    * Angiv tidsplanen til anonym, hvis svarene skal registreres uden navne, der er knyttet til svaret.  
    * Tilladelse af anonyme resultater skal først oprettes i HR-parametrene.  

5. Vælg planlægningstypen i feltet Type.  I dette eksempel bruger vi typen Tilfredshed.

6. Find og vælg den ønskede post på listen.

7. Klik op linket i den valgte række på listen.

8. Indtast en dato i feltet Dato.

9. Udvid sektionen E-mail for medarbejderselvbetjening.

10. Skriv en værdi i feltet Emne.

    * Eksempel: Tilgængeligt spørgeskema  

11. I feltet Tekst skal du skrive mailens brødtekst. Bemærk, at variablen kan bruges til at erstatte værdier i systemet.

    * Eksempel: Kære %P% Log på medarbejderselvbetjening for at udfylde spørgeskemaet om medarbejdernes sundhed.  Contoso  

12. Klik på Gem.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Brug opsætningsoplysningerne til at vælge eller spørgeskemaer, som skal besvares, samt eventuelle forespørgsler, der skal bruges til valg af svarpersoner.

1. Klik på Oplysninger om opsætning.

2. På listen skal du vælge en forespørgsel, som du bruge til at søge i systemet efter svarpersoner til spørgeskemaet.

    * Eksempel: Arbejdere  

3. Klik på Vis eller Rediger forespørgsel for at vælge bestemte personer eller justere forespørgslen for at søge efter personer, der opfylder bestemte søgekriterier.

    * Bemærk, at alle svarpersoner skal også brugere i systemet.  

4. Markér den valgte række for Person.

5. Indtast eller vælg en værdi i feltet Kriterier.

    * Vælg Julia Funderburk  

6. Vælg Julia Funderburk på listen

7. Klik på OK.

8. Klik på fanen Spørgeskemaer.

9. I træet skal du vælge indstillingen for at få vist noden for spørgeskemaet af typen Tilfredshedsundersøgelse i træet.

10. Markér 'Arbejdsstyrken helbredskontrol' i træet.

11. Klik på OK.

12. Klik på Planlagt besvarelse.

    * Bemærk, at det planlagte besvarelser, der er oprettet for hver bruger, der er markeret/forespørges.  

13. Luk siden.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Start spørgeskema tidsplanen for at stille til rådighed for svarpersonerne at udfylde spørgeskemaet.

1. Klik på Funktioner.

2. Klik på Start.

3. Klik på OK.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Send e-mail til at underrette svarpersoner for det spørgeskema, der er tilgængelige.

1. Klik på Funktioner.

2. Klik på Send e-mail.

3. Klik på Annuller.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Brug planlagte besvarelser til skærm, der skal udfylde spørgeskemaet.

1. Klik på Planlagt besvarelse.

    * Slette eventuelle resterende planlagte besvarelser når du er klar til at afslutte den planlagte session.  

2. Klik på Slet.

3. Klik på Ja.

4. Luk siden.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Afslut tidsplanen, når alle svarpersoner har udfyldt spørgeskemaet og/eller alle resterende Planlagte besvarelser-sessioner er slettet.

1. Klik på Funktioner.
2. Klik på Afslut.
3. Klik på OK.



[!INCLUDE[footer-include](../includes/footer-banner.md)]