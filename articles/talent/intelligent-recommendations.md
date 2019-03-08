---
title: Intelligente anbefalinger
description: I dette emne beskrives, hvordan maskinel indlæring kan bruges til at give anbefalinger om job og jobkandidater.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303743"
---
# <a name="intelligent-recommendations"></a>Intelligente anbefalinger

[!include[banner](../includes/banner.md)]

Maskinel indlæring kan hjælpe rekrutteringsmedarbejdere og ansættelsesansvarlige med at identificere de bedste kandidater til en stilling. Det kan også hjælpe jobkandidater med finde den stilling, der passer bedst til deres profil og interesser. Når disse funktioner bruges, og der gives tilbagemeldinger, forbedres anbefalingerne.

> [!NOTE] 
> - Funktioner til intelligente anbefalinger er kun tilgængelige i tilføjelsesprogrammet til omfattende ansættelser.
> - For at aktivere kandidat- og stillingsanbefalingsfunktionerne skal en administrator aktivere eksempelindstillingerne for dem. I Administration under fanen **Administration af funktioner** kan du kontrollere, om indstillingen **Funktioner i prøveversion** er slået **Til**. Derefter skal du kontrollere, at de enkelte indstillinger **Kandidatanbefaling** og **Stillingsanbefaling** er slået **Til**.

## <a name="candidate-recommendations"></a>Kandidatanbefalinger

Da jobopslag kan tiltrække hundredvis af ansøgere, kan det være vanskeligt for rekrutteringsmedarbejdere og ansættelsesansvarlige at finde de kandidater, hvis færdigheder og baggrund bedst svarer til stillingen. Ved at analysere korrelation mellem stillingsbeskrivelsen og -kravene og data fra kandidaternes cv'er og profiler kan maskinel indlæring bruges til at producere kandidatanbefalinger. Kandidatanbefalinger kan hjælpe rekrutteringsmedarbejdere og ansættelsesansvarlige med at identificere de største talenter og hurtigere flytte dem til samtalestadiet. Hvis der til et job er mere end ti ansøgere eller jobkandidater, der har CV'er eller fuldstændige profiler, vises de ansøgere eller jobkandidater, der bedst opfylder kravene til jobbet, i sektionen **Ansøgere, der skal tages i betragtning** på **Job**-siden.

For enhver anbefalet kandidat kan du vælge **Vis kandidat** på kandidatkortet for at gennemgå kandidatens profil og handle på vedkommendes ansøgning. Du kan bruge ellipseknappen (**...**) til at åbne kandidatens profil under en ny fane. Du kan også bruge ellipseknappen til at give tilbagemeldinger om anbefalingen. På denne måde hjælper du med at finjustere anbefalingsprogrammet og forbedre fremtidige anbefalinger. Eventuelle anbefalinger, du ikke bryder dig om, fjernes fra sektionen **Ansøgere, der skal tages i betragtning**, når du opdaterer **Job**-siden. Du kan bruge tilbagemeldingskortet til at angive, hvorfor du ikke fandt anbefalingen nyttig.

## <a name="job-recommendations"></a>Stillingsanbefalinger 

Når en mulig medarbejder bruger karrierewebstedet til at ansøge om et job, anbefales andre ledige stillinger i organisationen. Disse anbefalinger er baseret på jobkandidatens tidligere ansøgninger og på hans eller hendes CV eller kandidatprofil. Derfor hjælper stillingsanbefalinger jobkandidater med hurtigt at identificere de job, der passer til dem. Stillingsanbefalinger vises for jobkandidater, hvis der er opslået mere end ti job på karrierewebstedet. Jobkandidater kan åbne detaljerne i et jobopslag fra anbefalingskortet. De kan også give tilbagemeldinger om en anbefaling for at forbedre fremtidige anbefalinger.
