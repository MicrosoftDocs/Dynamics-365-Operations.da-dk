---
title: Oprette og sende en onboardingguide ved hjælp af Dynamics 365 Talent - Onboard
description: Dette emne forklarer, hvordan du bruger Microsoft Dynamics 365 Talent - Onboard-appen til at oprette en onboardingguide for dine nyansatte. Denne opgave er et vigtigt første skridt i en totalstrategi for styring af menneskelig kapital (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2371d86165390503312c2848842acf4745a8ed7a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898242"
---
# <a name="create-and-send-an-onboarding-guide"></a>Oprette og sende en onboardingguide

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboard giver dig mulighed for at oprette onboardingguider ud fra skabeloner, du har oprettet selv, fra skabeloner, der er tilgængelige i et galleri, eller fra bunden.

Når du har oprettet en onboardingguide, kan du sende den til en nyansat. Alternativt kan du sende den til flere nyansatte, som du angiver i en Microsoft Excel-fil, som du downloader fra Onboard-appen.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Oprette en onboardingguide ud fra en skabelon og sende den til en enkelt nyansat

1. Vælg **Skabeloner** i menuen til venstre.
2. Under **Mine skabeloner** skal du vælge den skabelon, du vil oprette som onboardingguide til den nyansatte.
3. Rediger skabelonen, som du ønsker det. Husk at gemme dit arbejde jævnligt.
4. Når du er færdig med at redigere skabelonen, skal du vælge **Opret guide**.

    [![Oprettelse af en onboardingguide ud fra en skabelon](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. I vinduet **Opret en guide** skal du under **Hvem onboarder du?** indtaste den nyansattes navn eller mailadresse. Hvis den nyansatte endnu ikke er i systemet, skal du vælge **Tilføj nu** og indtaste medarbejderens oplysninger.

    ![[Indtastning af oplysninger til onboarding-guiden](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. Under **Hvornår starter de?** skal du vælge en startdato.
7. Hvis onboardingguiden automatisk skal sendes til den nyansatte på en bestemt dato, skal du sørge for, at indstillingen **Planlæg en automatisk afsendelsesdato** er aktiveret, og vælg derefter den automatiske afsendelsesdato. For at sende guiden straks skal du deaktivere indstillingen **Planlæg en automatisk afsendelsesdato**.
8. Vælg **Udført**.
9. Når du er færdig med at redigere onboardingguideen, skal du vælge **Send** i øverste højre hjørne. Udfør derefter ét af følgende trin:

    - Hvis du vil sende den nyansatte et link til onboardingguiden, skal du vælge **kopiér et link** og derefter vælge **Kopiér**.
    - Hvis du vil tilpasse mailen for onboardingguiden, før du sender den, skal du vælge **Tilpas mailen, før du sender den**, vælge **Næste**, tilpasse mailen, som du ønsker, og derefter vælge **Send**.
    - Hvis du vil sende mailen uden at tilpasse den, skal du vælge **Næste** og derefter vælge **Send**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Oprette en onboardingguide ud fra en skabelon og sende den til flere nyansatte

Onboard giver dig mulighed for at sende en onboardingguide til flere nyansatte på samme tid.

1. Vælg **Skabeloner** i menuen til venstre.
2. Under **Mine skabeloner** skal du vælge den skabelon, du vil oprette som onboardingguide til de nyansatte.
3. Rediger skabelonen, som du ønsker det. Husk at gemme dit arbejde jævnligt.
4. Når du er færdig med at redigere skabelonen, skal du vælge **Opret guide**.
5. I vinduet **Opret en guide** skal du vælge **Skal du onboarde flere personer på én gang?**.

    [![Oprettelse af en onboardingguide til flere nyansatte](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Vælg **skabelon til nyansatte**.
7. Når .xlsx-filen er downloadet, skal du vælge **Åbn**, indtast medarbejdernes oplysninger i Excel-projektmappen og gemme projektmappen.

    [![Download af Excel-skabelonen for at sende onboardingguiden til flere nyansatte](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Før du kan redigere projektmappen, skal du vælge **Aktivér redigering** i Excel.
    > 
    > [![Aktivering af redigering](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Træk Excel-projektmappen til det angivne område i vinduet **Opret flere guider**, eller klik hvor som helst i dette område for at søge efter filen på din computer.

    [![Trækning af den redigerede projektmappe](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Når du er færdig med at redigere onboardingguideen, skal du vælge **Send** i øverste højre hjørne. Udfør derefter ét af følgende trin:

    - Hvis du vil sende de nyansatte et link til onboardingguiden, skal du vælge **kopiér et link** og derefter vælge **Kopiér**.
    - Hvis du vil tilpasse mailen for onboardingguiden, før du sender den, skal du vælge **Tilpas mailen, før du sender den**, vælge **Næste**, tilpasse mailen, som du ønsker, og derefter vælge **Send**.
    - Hvis du vil sende mailen uden at tilpasse den, skal du vælge **Næste** og derefter vælge **Send**.

## <a name="create-a-guide-without-using-a-template"></a>Oprette en guide uden at bruge en skabelon

Du behøver ikke altid at oprette en guide ud fra en skabelon. Hvis du foretrækker det, kan du i stedet oprette en guide fra bunden.

1. I menuen til venstre skal du vælge **Guider** og derefter vælge **Tilføj**-knappen (plustegnet \[**+**\]).
2. I vinduet **Opret en guide** skal du under **Hvem onboarder du?** indtaste den nyansattes navn eller mailadresse. Hvis den nyansatte endnu ikke er i systemet, skal du vælge **Tilføj nu** og indtaste medarbejderens oplysninger.

    ![[Indtastning af oplysninger til onboarding-guiden](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. Under **Hvornår starter de?** skal du vælge en startdato.
4. Hvis onboardingguiden automatisk skal sendes til den nyansatte på en bestemt dato, skal du sørge for, at indstillingen **Planlæg en automatisk afsendelsesdato** er aktiveret, og vælg derefter den automatiske afsendelsesdato. For at sende guiden straks skal du deaktivere indstillingen **Planlæg en automatisk afsendelsesdato**.
5. Vælg **Udført**.

## <a name="save-a-guide-as-a-template"></a>Gemme en guide som en skabelon

Du kan gemme en onboardingguide som en skabelon. På denne måde kan du spare tid, når du skal oprette flere onboardingguider senere.

1. Vælg **Guider** i menuen til venstre.
2. Vælg **Mere**-knappen (ellipsen \[**...**\]) til den guide, du vil oprette en skabelon ud fra, og vælg derefter **Gem som skabelon**.

    ![[At gemme en onboardingguide som en skabelon](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. I vinduet **Gem som en ny skabelon** skal du indtaste et navn til din nye skabelon og derefter vælge **Gem**.

## <a name="next-steps"></a>Næste trin

- [Redigere onboardingguider og -skabeloner](./onboard-edit-guides-templates.md)
- [Dele indhold med andre bidragydere](./onboard-share-template.md)
- [Se status for opgaver og onboarding af medarbejdere](./onboard-view-status.md)
- [Oprette ansættelsesteam i Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Se også

- [Prøve eller købe appen Onboard](https://dynamics.microsoft.com/talent/onboard/)
- [Nyheder eller ændringer i Dynamics 365 Talent](./whats-new.md)
- [Frigivelsesplaner](https://docs.microsoft.com/business-applications-release-notes/index)
- [Få support til Microsoft Dynamics 365 Talent](./talent-support.md)
