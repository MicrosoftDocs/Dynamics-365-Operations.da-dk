---
title: Aktiviteter i processerne
description: "Dette emne indeholder oplysninger om de forskellige typer aktiviteter, der kan bruges i ansættelsesprocessen."
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: da-dk
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a>Aktiviteter i ansættelsesprocesserne

[!include[banner](../includes/banner.md)]

Aktiviteter kan tilføjes som en del af ansættelsesprocessen i Microsoft Dynamics 365 for Talent: Attract. Aktiviteter kan føjes til en processkabelon, eller de kan føjes direkte til ansættelsesprocessen i jobbet. Når et job er defineret, vælges en processkabelon, og de aktiviteter, der er medtaget i skabelonen, anvendes på jobbet. Hvis der ikke er valgt en skabelon, bruges standardskabelonen. Ansættelsesprocessen kan også ændres i jobbet, når skabelonen er anvendt.

> [!NOTE] 
> Processkabeloner er tilgængelige i tilføjelsesprogrammet til omfattende ansættelser.

## <a name="prospect-activity"></a>Aktiviteten Jobkandidat

Aktiviteten Jobkandidat styrer, om jobkandidater kan føjes til et job. Som standard kan jobkandidater føjes til et job. Hvis du vil deaktivere Jobkandidat-aktiviteten, skal du indstille **Aktivér jobkandidater** til **Fra**. Når Jobkandidat-aktiviteten er aktiveret, kan ansættelsesansvarlige tilføje og få vist jobkandidater, og fanen **Jobkandidater** vises i jobbet.

## <a name="application-activity"></a>Aktiviteten Ansøgning

Aktiviteten Ansøgning er påkrævet i ansættelsesprocesskabelonen. Hvis du vil sende e-mails til kandidater, når de indsender deres ansøgning eller bliver føjet til stadiet Ansøgning, skal du indstille **Send mail til kandidat** til **Til**.

## <a name="scheduler-activity"></a>Aktiviteten Planlægger

Aktiviteten Planlægger er valgfri. Denne aktivitet består af to komponenter: Kandidatens tilgængelighed og Tidsplan. I komponenten Kandidatens tilgængelighed kan du bruge e-mail til at anmode om en kandidats tilgængelighed. Komponenten Planlægger giver mulighed for at planlægge samtaler med kandidaten og ansættelsesteamet. Følgende indstillinger kan konfigureres i aktiviteten Planlægger: **Anmod om kandidatens tilgængelighed**, **Onlinemøde** og **Send mail til kandidat**.

- Hvis du vil sende e-mails til kandidater for at anmode om deres tilgængelighed, skal du indstille **Anmod om kandidatens tilgængelighed** til **Til**. Hvis du vælger **Fra** i indstillingen, vises dette trin ikke i ansættelsesprocessen for jobbet.
- For at streame live eller have et telefonmøde via Skype for Business skal du indstille feltet **Onlinemøde** til **Skype for Business**. Det korrekte **Deltag i Skype-møde**-link tilføjes derefter i samtalemødeindkaldelsen, der sendes til interviewere.
- Hvis du vil sende e-mails til kandidater for at færdiggøre tidsplanen, skal du indstille **Send mail til kandidat** til **Til**. Hvis du vælger **Fra** i indstillingen, modtager kandidaterne først samtaletidsplanen, når de logger på kandidatportalen.

## <a name="feedback-activity"></a>Aktiviteten Tilbagemelding

Aktiviteten Tilbagemelding er valgfri. Med denne aktivitet kan deltagerne i samtalen angive anbefalinger for en ansøger. De kan også angive eventuelle feedbackkommentarer, de har. Hvis du aktiverer indstillingen **Overtag tilbagemeldingsdeltagere fra ansættelsesteam**, angives rekrutteringsmedarbejder, den ansættelsesansvarlige og interviewerne automatisk i aktiviteten Tilbagemelding. Organisationer kan tillade, at interviewere får vist tilbagemeldinger fra andre, før de sender deres egen feedback. Organisationer kan også tillade, at interviewere redigerer deres tilbagemeldinger, når de sender dem.

## <a name="interview-activity"></a>Aktiviteten Samtale

Aktiviteten Samtale er valgfri. Denne aktivitet består af tre komponenter: Kandidatens tilgængelighed, Tidsplan og Tilbagemelding. I komponenten Kandidatens tilgængelighed kan du bruge e-mail til at anmode om en kandidats tilgængelighed. Komponenten Planlægger giver mulighed for at planlægge samtaler med kandidaten og ansættelsesteamet. Følgende indstillinger kan konfigureres i aktiviteten Planlægger: **Anmod om kandidatens tilgængelighed**, **Onlinemøde** og **Send mail til kandidat**.

- Hvis du vil sende e-mails til kandidater for at anmode om deres tilgængelighed, skal du indstille **Anmod om kandidatens tilgængelighed** til **Til**. Hvis du vælger **Fra** i indstillingen, vises dette trin ikke i ansættelsesprocessen for jobbet.
- For at streame live eller have et telefonmøde via Skype for Business skal du indstille feltet **Onlinemøde** til **Skype for Business**. Det korrekte **Deltag i Skype-møde**-link tilføjes derefter i samtalemødeindkaldelsen.
- Hvis du vil sende e-mails til kandidater for at færdiggøre tidsplanen, skal du indstille **Send mail til kandidat** til **Til**. Hvis du vælger **Fra** i indstillingen, modtager kandidaterne først samtaletidsplanen, når de logger på kandidatportalen.

I komponenten Tilbagemelding kan personer angive anbefalinger for en ansøger. De kan også angive eventuelle feedbackkommentarer, de har. Hvis du aktiverer indstillingen **Overtag tilbagemeldingsdeltagere fra ansættelsesteam**, angives rekrutteringsmedarbejder, den ansættelsesansvarlige og interviewerne automatisk i komponenten Tilbagemelding. Organisationer kan tillade, at interviewere får vist tilbagemeldinger fra andre, før de sender deres egen feedback. Organisationer kan også tillade, at interviewere redigerer deres tilbagemeldinger, når de sender dem.

## <a name="powerapps-activity"></a>Aktiviteten PowerApps

Med aktiviteten PowerApps kan du integrere en Microsoft PowerApps-app i din ansættelsesproces. Appen kan være påkrævet for alle ansøgere, kun interne ansøgere, kun eksterne ansøgere eller ingen ansøgere. Hvis appen er markeret som obligatorisk, skal den fuldføres, før stadiet kan fremrykkes. Hvis appen ikke er markeret som obligatorisk, er aktiviteten et valgfrit trin, og stadiet kan fremrykkes, selvom appen ikke er fuldført.

Hvis du vil gemme aktiviteten PowerApps i forbindelse med ansættelsesprocessen, skal du angive et PowerApps-id. Du kan finde PowerApps-id'et ved at gå til [PowerApps](https://web.powerapps.com), vælge **Apps** og derefter vælge **Oplysninger**.

Hvis du vælger indstillingen **Tillad, at der føjes deltagere til denne aktivitet**, kan der tilføjes flere bidragydere til et program, der bruger aktiviteten PowerApps. En organisation har f.eks. oprettet en PowerApps-app, der er et bibliotek over samtalespørgsmål til tekniske roller. Organisationen ansætter nu en ny softwareudvikler og har tilføjet PowerApps-aktiviteten til ansættelsesprocessen for rollen Softwareudvikler. Hvis indstillingen **Tillad, at der føjes deltagere til denne aktivitet** er valgt, kan en rekrutteringsmedarbejder eller ansættelsesansvarlig, der får vist en ansøger til rollen som Softwareudvikler, føje personer til aktiviteten PowerApps. Personerne kan derefter se appen, der indeholder samtalespørgsmålene.

> [!NOTE]
> Aktiviteten PowerApps er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.

## <a name="youtube-activity"></a>YouTube-aktivitet

Med YouTube-aktiviteten kan du dele en YouTube-video som en del af ansættelsesprocessen. For at gemme YouTube-aktiviteten i ansættelsesprocessen skal du angive URL-adressen på YouTube-videoen. Hvad angår PowerApps-aktiviteten, kan du tillade, at deltagerne bliver føjet til aktiviteten. Hvis du vælger indstillingen **Vis kun til kandidaten**, vises videoen kun som en del af kandidatoplevelsen. Den vises ikke i ansættelsesprocessen i Attract.

> [!NOTE]
> YouTube-aktiviteten er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.

## <a name="web-content-activity"></a>Aktiviteten Webindhold

Med aktiviteten Webindhold kan du integrere onlineindhold i ansættelsesprocessen. For at gemme Webindhold-aktiviteten i ansættelsesprocessen skal du angive URL-adressen til indholdet. Hvad angår PowerApps- og YouTube-aktiviteterne, kan du tillade, at deltagerne bliver føjet til aktiviteten. Hvis du vælger indstillingen **Vis kun til kandidaten**, vises indholdet kun som en del af kandidatoplevelsen. Den vises ikke i ansættelsesprocessen i Attract. Du kan vælge størrelsen på det indhold, der vises.

> [!NOTE]
> Aktiviteten Webindhold er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.

## <a name="microsoft-forms-activity"></a>Aktiviteten Microsoft Forms

Med aktiviteten Microsoft Forms kan du integrere en Microsoft Forms-formular i din ansættelsesproces. Med Microsoft Forms kan du oprette quizzer, undersøgelser og puljer. For at gemme Microsoft Forms-aktiviteten i ansættelsesprocessen skal du angive URL-adressen til formularen. Hvad angår PowerApps-, YouTube- og Webindhold-aktiviteterne, kan du tillade, at deltagerne bliver føjet til aktiviteten. Hvis du vælger indstillingen **Vis kun til kandidaten**, vises formularen kun som en del af kandidatoplevelsen. Den vises ikke i ansættelsesprocessen i Attract.

Forfattere kan ændre deres indstillinger, så brugere uden for deres organisation kan svare på deres undersøgelse eller quiz, i Microsoft Forms. I dette tilfælde kan brugerne sende svar anonymt. Hvis du vil se, hvem der har udfyldt din undersøgelse eller quiz, kan du kræve, at svarpersonerne skriver deres navn som en del af undersøgelsen eller quizzen.

> [!NOTE]
> Aktiviteten Microsoft Forms er kun tilgængelig i forbindelse med tilføjelsesprogrammet til omfattende ansættelse.

