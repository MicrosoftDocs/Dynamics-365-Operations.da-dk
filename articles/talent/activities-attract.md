---
title: Tilføj aktiviteter til en ansættelsesproces
description: Dette emne indeholder oplysninger om de forskellige typer aktiviteter, du kan tilføje til en ansættelsesproces i Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833271"
---
# <a name="add-activities-to-a-hiring-process"></a>Tilføj aktiviteter til en ansættelsesproces

[!include [banner](includes/banner.md)]

Aktiviteter kan tilføjes som en del af ansættelsesprocessen i Microsoft Dynamics 365 Talent: Attract. Aktiviteter kan føjes til en processkabelon, eller de kan føjes direkte til ansættelsesprocessen i jobbet. Når et job er defineret, vælges en processkabelon, og de aktiviteter, der er medtaget i skabelonen, anvendes på jobbet. Hvis der ikke er valgt en skabelon, bruges standardskabelonen. Ansættelsesprocessen kan også ændres i jobbet, når skabelonen er anvendt.

> [!NOTE] 
> Processkabeloner er tilgængelige i tilføjelsesprogrammet til omfattende ansættelser. Yderligere oplysninger finder du under [Hvilken version af Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Aktiviteten Jobkandidat

Aktiviteten Jobkandidat styrer, om jobkandidater kan føjes til et job. Som standard kan jobkandidater føjes til et job. Hvis du vil deaktivere Jobkandidat-aktiviteten, skal du indstille **Aktivér jobkandidater** til **Fra**. Når Jobkandidat-aktiviteten er aktiveret, kan ansættelsesansvarlige tilføje og få vist jobkandidater, og fanen **Jobkandidater** vises i jobbet.

> [!NOTE]
> For at give mulighed for at føje kandidater til et job fra LinkedIn, skal du indstille **Aktivér jobkandidater** til **Til**.

## <a name="application-activity"></a>Aktiviteten Ansøgning

Aktiviteten Ansøgning er påkrævet i ansættelsesprocesskabelonen. Hvis du vil sende e-mails til kandidater, når de indsender deres ansøgning eller bliver føjet til stadiet Ansøgning, skal du indstille **Send mail til kandidat** til **Til**.

## <a name="interview-schedule-and-feedback-activity"></a>Samtaleplanlægning og tilbagemeldingsaktivitet

Denne aktivitet består af tre komponenter: Anmodning om kandidatens tilgængelighed, Tidsplan og Tilbagemelding. Brug samtaleaktiviteten i jobskabelonen, hvis du vil medtage en anmodning om kandidatens tilgængelighed, tidsplan og tilbagemelding som led i processen i stedet for at bruge dem hver for sig som en del af ansættelsesprocessen. Yderligere oplysninger finder du i [Samtaleplanlægning og tilbagemelding](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Power Apps-aktivitet

Med Power Apps-aktiviteten kan du integrere en Microsoft Power Apps-app i din ansættelsesproces. Appen kan være påkrævet for alle ansøgere, kun interne ansøgere, kun eksterne ansøgere eller ingen ansøgere. Hvis appen er markeret som obligatorisk, skal den fuldføres, før stadiet kan fremrykkes. For at blive betragtet som fuldført skal feltet **JobApplicationStatus** angives til **Fuldført**. Feltet findes i JobApplicationActivity-enheden, og Power Apps-appen skal derfor opdatere dette felt, før stadiet kan avanceres. Hvis appen ikke er markeret som obligatorisk, er aktiviteten et valgfrit trin, og stadiet kan fremrykkes, selvom appen ikke er fuldført.

Hvis du vil gemme Power Apps-aktiviteten i forbindelse med ansættelsesprocessen, skal du angive et Power Apps-id. Du kan finde Power Apps-id'et ved at gå til [Power Apps](https://web.powerapps.com), vælge **Apps** og derefter vælge **Oplysninger**.

Power Apps-aktiviteten er som standard tilgængelig for den ansættelsesansvarlige, rekrutteringsmedarbejderen og deres delegerede. Hvis du vælger indstillingen **Tillad, at der føjes deltagere til denne aktivitet**, kan der føjes flere deltagere fra ansættelsesteamet til en ansøgning, der bruger Power Apps-aktiviteten. En organisation har f.eks. oprettet en Power Apps-app, der er et bibliotek over samtalespørgsmål til tekniske roller. Organisationen ansætter nu en ny softwareudvikler og har føjet Power Apps-aktiviteten til ansættelsesprocessen for rollen Softwareudvikler. Hvis indstillingen **Tillad, at der føjes deltagere til denne aktivitet** er valgt, kan en rekrutteringsmedarbejder eller ansættelsesansvarlig, der får vist en ansøger til rollen som softwareudvikler, føje interviewere til Power Apps-aktiviteten. Personerne kan derefter se appen, der indeholder samtalespørgsmålene.

> [!NOTE]
> Power Apps-aktiviteten er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse. Yderligere oplysninger finder du under [Hvilken version af Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>YouTube-aktivitet

Med YouTube-aktiviteten kan du dele en YouTube-video som en del af ansættelsesprocessen. For at gemme YouTube-aktiviteten i ansættelsesprocessen skal du angive URL-adressen på YouTube-videoen. Du kan vælge at vise indholdet til **Ansættelsesteamet**, **Kun interne kandidater**, **Kun eksterne kandidater** eller **Alle kandidater**. Ligesom tilfældet er med Power Apps-aktiviteten, kan du give tilladelse til, at deltagerne i ansættelsesteamet bliver føjet til aktiviteten. Hvis du vælger at vise indholdet til kandidaterne, bliver videoen alene vist som en del af kandidatoplevelsen og ikke i forbindelse med ansættelsesprocessen.

> [!NOTE]
> YouTube-aktiviteten er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse. Yderligere oplysninger finder du under [Hvilken version af Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Aktiviteten Webindhold

Med aktiviteten Webindhold kan du integrere onlineindhold i ansættelsesprocessen. For at gemme Webindhold-aktiviteten i ansættelsesprocessen skal du angive URL-adressen til indholdet. Du kan vælge at vise indholdet til **Ansættelsesteamet**, **Kun interne kandidater**, **Kun eksterne kandidater** eller **Alle kandidater**. Ligesom tilfældet er med Power Apps- og YouTube-aktiviteter, kan du give tilladelse til, at deltagerne i ansættelsesteamet bliver føjet til aktiviteten. Hvis du vælger at vise indholdet til kandidaterne, bliver webindholdet alene vist som en del af kandidatoplevelsen og ikke i forbindelse med ansættelsesprocessen. Du kan selv vælge størrelsen på det viste indhold.

> [!NOTE]
> Aktiviteten Webindhold er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse. Yderligere oplysninger finder du under [Hvilken version af Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Aktiviteten Microsoft Forms

Med Microsoft Forms-aktiviteten kan du integrere en Microsoft Forms-aktivitet i din ansættelsesproces. Med Microsoft Forms kan du oprette quizzer, undersøgelser og puljer. For at gemme Microsoft Forms-aktiviteten i ansættelsesprocessen skal du angive URL-adressen til formularen. Du kan vælge at vise indholdet til **Ansættelsesteamet**, **Kun interne kandidater**, **Kun eksterne kandidater** eller **Alle kandidater**. Ligesom tilfældet er med Power Apps-, YouTube- og webindholdsaktiviteter, kan du give tilladelse til, at deltagerne i ansættelsesteamet bliver føjet til aktiviteten. Hvis du vælger at vise indholdet til kandidaterne, bliver formularen alene vist som en del af kandidatoplevelsen og ikke i forbindelse med ansættelsesprocessen.

Forfattere kan ændre deres indstillinger, så brugere uden for deres organisation kan svare på deres undersøgelse eller quiz, i Microsoft Forms. I dette tilfælde kan brugerne sende svar anonymt. Hvis du vil se, hvem der har udfyldt din undersøgelse eller quiz, kan du kræve, at svarpersonerne skriver deres navn som en del af undersøgelsen eller quizzen.

> [!NOTE]
> Aktiviteten Microsoft Forms er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse. Yderligere oplysninger finder du under [Hvilken version af Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Tilbudsaktivitet

Ansættelsesprocesskabelonen kræver tilbudsaktiviteten. For at anvende den integrerede Offer Management-app skal **Start Offer Management-appen, når der vælges "Forbered tilbud"** være angivet til **Til**. Hvis denne funktion er slået fra, fremgår kandidaten ikke af tilbudsappen, og du vil derfor være nødt til at ajourføre dig med en kandidats tilbudsaktivitet manuelt. Hvis du ønsker at definere, hvorvidt den ansættelsesansvarlige kan forberede tilbuddet til kandidaten i tilbudsappen, skal indstillingen **Ansættelsesansvarlige kan forberede tilbud** være angivet til **Til**. Hvis der er knyttet flere stillinger til jobbet, kan du beslutte, hvorvidt du ønsker at forberede flere tilbud til det samme stillingsnummer. Hvis du blot ønsker at tillade ét tilbud pr. stilling pr. job, skal **Tillad, at stillinger kan genbruges i job** være angivet til **Fra**.

> [!NOTE]
> Den integrerede Offer Management-app er kun tilgængelig sammen med tilføjelsesprogrammet Omfattende ansættelser. Yderligere oplysninger finder du under [Hvilken version af Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).


