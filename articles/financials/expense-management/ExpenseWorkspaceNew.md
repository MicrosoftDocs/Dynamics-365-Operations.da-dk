---
title: Udgiftsrapporter i nyfortolkning
description: Dette emne indeholder oplysninger om den nyudviklede og nyfortolkede oplevelse for indtastning i udgiftsrapporter i Microsoft Dynamics 365 for Finance and Operations. Den nye oplevelse forenkler processen med at fuldføre udgiftsrapporter og reducerer den tid, der kræves.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 320984fc6be231c941df17abb7246e92f6aa4b9a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841051"
---
# <a name="expense-reports-reimagined"></a>Udgiftsrapporter i nyfortolkning

[!include[banner](../includes/banner.md)]

Indtastning i udgiftsrapporter er blevet ændret for at forenkle processen med at fuldføre udgiftsrapporter og reducere den tid, der kræves. Her er de vigtigste komponenter i den nye udgiftsangivelsesoplevelse:

- Et nyt arbejdsområde til udgiftsstyring, hvor du kan få adgang til den delegeredes udgifter.
- En ny kvitteringssammenholdelsesoplevelse med en forbedret visning af kvitteringer på hovedniveau og en forenklet proces med tilknytning af kvitteringer til udgiftslinjer.
- Et nyt skrivebeskyttet gitter, hvor du kan få vist mange flere udgiftslinjer og yderligere datakolonner. Du kan nu se alle specificerede og opdelte linjer sammen med deres overordnede udgifter.
- En forenklet rude til redigering af udgifter.
- Nydesignede fejl-, advarsels- og politikmeddelelser er med til at sikre, at du har den rigtige kontekst til at forstå, hvad problemet er, og hvordan du løser det. Microsoft har fjernet mange meddelelser, der blev vist, før brugerne havde mulighed for at udføre deres opgaver og løse problemerne, f.eks. meddelelsen om ufuldstændig specifikation.
- En ny side til angivelse af, hvilke felter der kræves af din organisation, hvilke felter der er valgfrie, og hvilke felter der ikke skal registreres. Denne side hjælper med at reducere det antal felter, som brugerne skal angive.
- Et nyt udseende for udgiftsrapporter, så rapporterne ikke længere ser ud, som om de er designet til regnskabsmedarbejdere.

Når du vil aktivere den nye oplevelse, skal du bruge arbejdsområdet **Administration af funktioner** til at aktivere funktionen **Udgiftsrapporter nyfortolkede**. Når du aktiverer denne funktion, udføres følgende handlinger:

- Det eksisterende udgiftsarbejdsområde erstattes med det nye arbejdsområde.
- Der tilføjes et nyt menupunkt for synlighed af udgiftsfelter.
- Der fjernes ingen eksisterende menupunkter for udgiftsrapporter (den eksisterende side) eller udgiftsrapportfelter.
- Arbejdsgange og eventuelle godkendelser fører stadig til den eksisterende side med udgiftsrapporter.

## <a name="getting-started-video-for-new-users"></a>Introduktionsvideo for nye brugere

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Videoen [Udgiftsoplevelse i Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (vist ovenfor) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

## <a name="new-features"></a>Nye funktioner

| Ny funktion | Beskrivelse |
|---|----|
| Synlighed af udgiftsfelt | På en konfigurationsside kan du angive, hvilke felter der skal deaktiveres for en organisation, hvilke felter der skal bruges, og hvilke felter der anbefales. |
| Obligatoriske felter | Ved hjælp af den nye simple konfiguration kan du gøre nogle felter obligatoriske uden at skulle bruge politikstrukturen. |
| Valgfrie felter | Der tilføjes endnu en side med valgfrie felter. På denne måde vil medarbejderne ikke opfatte det, som om de skal angive felterne, men felterne er stadig lettilgængelige. |
| Tilføje ikke-tilknyttede kvitteringer | Muligheden for at tilføje ikke-tilknyttede kvitteringer i udgiftsrapporter er mere synlig i arbejdsområdet og i udgiftsrapporten. |
| Forbedrede meddelelser | Der er bedre synlighed i udgiftslinjer, der har advarsler eller fejl. |
| Reduktion af meddelelser på meddelelseslinjen| Antallet af infolog-meddelelser er blevet reduceret, og der gjort en indsats for at forhindre, at der i mange tilfælde vises dublerede meddelelser. |
| Grupperede almindelige handlinger | Grænsefladen er blevet ryddet og har fået tilføjet en ny handlingsknap til de fleste almindelige handlinger på linjeniveau og en ellipseknap (...) til overskrifter og andre mindre hyppige handlinger. |
| Nyt arbejdsområde til øget synlighed | Et nyt arbejdsområde samler funktioner og links, der giver brugerne mulighed for at flytte til forskellige områder. |
| Tilføje eksisterende udgifter og kvitteringer under oprettelse af udgifter | Når du opretter udgiftsrapporter, kan du tilføje alle eller udvalgte udgifter og kvitteringer. |
| Valutakursberegner | Der er tilføjet en valutakursberegner, hvor du kan beregne valutakursen for udlæg til transaktioner med flere valutaer. |
| Gemme og tilføje nye udgiftslinjer | Knapperne **Gem** og **Ny** er tilgængelige, når der angives nye udgifter, så du hurtigt kan angive udgiftslinjer. |
| Bedre synlighed på opdelte og specificerede linjer | Specificerede og opdelte linjer føjes direkte til listen over udgifter for at øge synligheden og gøre det nemt at afgøre, om der er fejl relateret til politik eller andre fejl. |
| Vise kvitteringer under specifikation | Kvitteringer kan vises under specifikation. |

Den første version fokuserer på scenarier med udgiftsregistrering. I et eventuelt scenario til gennemgang eller godkendelse af udgiftsrapporter vil den eksisterende udgiftspostside fortsat blive anvendt.

Følgende funktioner findes på den eksisterende side, men endnu ikke på den nye side. Disse funktioner bliver introduceret igen i en række kommende versioner:

- Godkendelser
- Godkendelser af kreditorer og muligheden for at redigere regnskabet
- Flere indgangspunkter
- Integration af rejserekvisition
- Dataenhed for synlighed af udgiftsfelt
- Post for diætudgifter
- Arbejdsgang på linjeniveau
- Understøttelse af foreløbige godkendere
- Avanceret specifikation
