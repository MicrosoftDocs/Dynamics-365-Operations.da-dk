---
title: Redigere onboardingguider og -skabeloner i Dynamics 365 Talent - Onboard
description: Dette emne forklarer, hvordan du kan føje aktiviteter og andre oplysninger til onboardingguider og -skabeloner i Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897114"
---
# <a name="edit-onboarding-guides-and-templates"></a>Redigere onboardingguider og -skabeloner

[!include [banner](includes/banner.md)]

Når du har oprettet en onboardingguide eller -skabelon i Microsoft Dynamics 365 Talent: Onboard, skal du tilføje en introduktion, aktiviteter, kontakter og ressourcer. Onboard giver dig omfattende indhold i dine onboardingguider, herunder:

- YouTube-videoer
- Microsoft Sway-præsentationer
- Microsoft PowerApps-apps
- Microsoft Stream-videoer
- Microsoft Forms-formularer
- Iframes, der har webindhold

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Redigere introduktioner eller aktiviteter, der er importeret fra en skabelon

Hvis du opretter en onboardingguide ud fra en skabelon, eller hvis du importerer aktiviteter fra én skabelon til en anden, vil du bemærke **Lås**-knappen på de importerede aktiviteter. Disse kaldes *administrerede aktiviteter*.

[![Administrerede aktiviteter](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Når du vælger en administreret aktivitet, kan du se kildeskabelonen øverst i aktiviteten.

[![Administreret aktivitetskilde](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Hvis du redigerer en aktivitet i en skabelon, vil Onboard overføre ændringerne til alle skabeloner og ikke-sendte guider, der er baseret på denne skabelon. Hvis du vælger en ikke-afsendt guide, der er baseret på en skabelon, du har redigeret, og derefter vælger fanen **Aktiviteter** i guiden, vises en meddelelse om, at guiden er blevet ændret. Vælg **OK** for at lukke beskeden. 

[![Besked om ændring](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Der vises en sort prik ud for de opdaterede aktiviteter.

[![Ændret aktivitet](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Du kan ikke redigere administrerede aktiviteter uden for den oprindelige skabelon, undtagen for at tilføje en modtager, en forfaldsdato eller andre oplysninger i højre sektion af aktiviteten.

Hvis du vil redigere en administreret aktivitet, eller hvis du ikke ønsker, at en aktivitet skal modtage opdateringer fra den skabelon, den kommer fra, skal du vælge knappen **Lås** for den pågældende aktivitet. Knappen **Lås** forsvinder. Aktiviteten vil ikke længere blive administreret af den oprindelige skabelon, og den vil ikke længere modtage opdateringer fra denne skabelon. De opdateringer, du foretager i en aktivitet, påvirker ikke den oprindelige skabelon.

Hvis du sletter en aktivitet fra en guide og overfører ændringer fra den pågældende guides skabelon, vil aktiviteten forblive slettet i guiden.

> [!NOTE]
> Kontakter og ressourcer administreres ikke af skabeloner. Sektioner administreres heller ikke, så hvis du tilføjer eller redigerer en sektion i en skabelon, vil ændringerne ikke blive overført til guider eller skabeloner, der bruger den pågældende skabelon.
> 
> Hvis du føjer nye aktiviteter til en skabelon, overføres de nye aktiviteter til guider og skabeloner, der er baseret på skabelonen, og de nye aktiviteter vises øverst.

## <a name="import-activities-from-another-template"></a>Importere aktiviteter fra en anden skabelon

Du kan importere aktiviteter fra en eller flere skabeloner til en guide eller skabelon.

1. Vælg den guide eller skabelon, du vil redigere.

2. Vælg fanen **Aktiviteter**.

3. Vælg fanen **Importér** i sektionen til højre.

   [![Importere aktiviteter](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Hvis du vil have vist opgaverne som eksempel under en ny fane i browseren, skal du vælge knappen **Åbn på ny fane** i en skabelon.

   [![Importere aktiviteter](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Træk den ønskede skabelon til det sted i din guideskabelon, hvor aktiviteterne skal vises, og slip den. Fortsæt med at redigere din guide eller skabelon.

De importerede aktiviteter vil indeholde knappen **Lås**, som angiver, at disse aktiviteter administreres af den skabelon, du har importeret fra. Når du foretager ændringer i den importerede skabelon, opdateres disse aktiviteter i den skabelon, du har importeret dem til. Ændringerne overføres dog ikke automatisk til de guider, der er oprettet ud fra den skabelon, du har importeret til.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Overføre ændringer fra en skabelon til andre skabeloner eller guider

Hvis du redigerer en skabelon, der indeholder aktiviteter, som bruges i andre skabeloner eller guider, skal du overføre ændringerne, hvis du ønsker, at de skal vises i andre skabeloner eller guider.

Hvis du ikke er sikker på, om aktiviteterne i skabelonen bruges i andre skabeloner eller guider, skal du vælge fanen **Anvendt i** for at se, hvor disse aktiviteter vises.

   [![Se guider og skabelonaktiviteter, der bruges i](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Sådan overføres dine ændringer:

1. Gem ændringerne ved at vælge knappen **Gem**. Hvis du ikke gør det, bliver du bedt om at gemme ændringerne i næste trin.

2. Vælg **Overfør disse ændringer**.

   
## <a name="add-or-edit-an-introduction"></a>Tilføje eller redigere en introduktion

1. Angiv en titel til din guide og en åbningsmeddelelse under fanen **Introduktion**. Hvis du vil bruge eksempelteksten, skal du vælge **Brug denne meddelelse**.

    [![Fanen Introduktion i en Onboard-skabelon](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Brug formateringsknapperne til at fremhæve tekst, som du har brug for, eller til at tilføje billeder eller links.
3. Vælg **Gem** for at gemme dit arbejde.

## <a name="add-or-edit-activities"></a>Tilføje eller redigere aktiviteter

1. Under fanen **Aktiviteter** skal du trække elementer fra højre til redigeringsområdet.
2. Hvis du vil organisere din guide i sektioner, skal du trække elementet **Ny sektion** til redigeringsområdet og angive et navn og en valgfri beskrivelse af sektionen.

    ![[Tilføjelse af en ny sektion til en onboardingguide eller -skabelon](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Hvis du vil tilføje aktiviteter, som din nyansatte skal udføre, skal du trække elementet **Ny aktivitet** til redigeringsområdet og angive et navn og en beskrivelse for aktiviteten.

    ![[Tilføjelse af en ny aktivitet til en onboardingguide eller -skabelon](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Føje avanceret indhold til din onboardingguide:

    - Hvis du vil tilføje en YouTube-video, skal du trække **YouTube**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten og angive URL-adressen til YouTube-videoen.
    - Hvis du vil tilføje en Sway-præsentation eller et nyhedsbrev, skal du trække **Sway**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten og angive den integrerede URL-adresse til Sway-præsentationen eller -nyhedsbrevet.
    - Hvis du vil tilføje en Microsoft Power Apps-app, skal du trække **Power Apps**-elementet til redigeringsområdet, angive et navn og en beskrivelse for aktiviteten og enten vælge Power Apps-appen eller angive Power Apps-app-id.
    - Hvis du vil tilføje en Microsoft Stream-video, skal du trække **Microsoft Stream**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten og angive URL-adressen til Microsoft Stream-videoen.
    - Hvis du vil tilføje en Microsoft forms-formular, skal du trække **Microsoft Forms**-elementet til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten, angive URL-adressen til formen Microsoft Forms og angive størrelsen på skærmområdet.
    - Hvis du vil tilføje en Iframe, der har webindhold, skal du trække elementet **Webindhold (iframe)** til redigeringsområdet, angive et navn og en beskrivelse til aktiviteten, angive URL-adressen til webindholdet og angive størrelsen på skærmområdet.

    ![[Tilføjelse af rigt indhold til en onboardingguide eller -skabelon](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Valgfrit: I området til højre for hver aktivitet skal du tildele aktiviteten en bestemt person eller rolle, tilføje en forfaldsdato og kontaktperson og tildele en kategorifarve. Når du tildeler en person eller rolle en aktivitet, oprettes der en opgave for hver enkelt. Denne opgave vises i menuen **Opgaver** i Onboard.

    [![Tildeling af en aktivitet i en onboardguide eller -skabelon](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Vælg **Gem** for at gemme dit arbejde.

Hvis du vil slette en aktivitet eller sektion, skal du vælge knappen **Slet** (papirkurvssymbolet) i øverste højre hjørne af aktiviteten eller sektionen.

Hvis du vil omarrangere aktiviteter og sektioner, skal du trække dem til et nyt sted.

## <a name="add-or-edit-contacts"></a>Tilføje eller redigere kontakter

Du kan tilføje kontaktpersoner, der kan hjælpe din nyansatte med at komme godt fra start. Disse kontaktpersoner kan være rekrutteringsmedarbejdere, teammedlemmer, onboardingkammerater, vejledere, administratorer og it-supportmedarbejdere.

1. Vælg **Ny kontakt** under fanen **Kontakter**.
2. Angiv kontaktpersonens navn eller mailadresse i dialogboksen **Tilføj teammedlem**, angiv en kort beskrivelse, der forklarer, hvordan kontaktpersonen kan hjælpe den nyansatte, og vælg derefter **Tilføj**. 

    ![[Tilføjelse af kontakter til en onboardingguide eller -skabelon](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Du kan også vælge en eller flere kontaktpersoner under **Forslag**.

3. Vælg **Gem** for at gemme dit arbejde.

Hvis du vil slette en kontakt, skal du vælge knappen **Slet** (papirkurvssymbolet) til højre for kontakten.

Hvis du vil redigere en kontakt, skal du vælge knappen **Rediger** (blyantssymbolet) til højre for kontakten.

## <a name="add-or-edit-resources"></a>Tilføje eller redigere ressourcer

Du kan tilføje nyttige filer, kort og links i sektionen **Ressourcer** i din onboardingguide.

1. Vælg **Ny ressource** under fanen **Ressourcer**.
2. Udfør ét af følgende trin:

    - Hvis du vil tilføje en fil, skal du vælge fanen **Fil** og trække filen til det afsatte område. (Du kan også klikke på et vilkårligt sted i området for at søge efter filen på din computer eller vælge **Gennemse OneDrive**). Angiv et navn til filen, og vælg derefter **Tilføj**.
    - Hvis du vil tilføje et link, skal du vælge fanen **Link**, angive et navn og en adresse for linket og derefter vælge **Tilføj**.
    - Hvis du vil tilføje et kort, skal du vælge fanen **Kort**, angive et navn og en adresse for kortet og derefter vælge **Tilføj**. Onboard vil medtage et kort over den adresse, du angiver.

    ![[Tilføjelse af ressourcer til en onboardingguide eller -skabelon](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Vælg **Gem** for at gemme dit arbejde.

Hvis du vil slette en ressource, skal du vælge knappen **Slet** (papirkurvssymbolet) til højre for ressourcen.

Hvis du vil redigere en ressource, skal du vælge knappen **Rediger** (blyantssymbolet) til højre for ressourcen.

## <a name="next-steps"></a>Næste trin

- [Dele indhold med andre bidragydere](./onboard-share-template.md)
- [Se status for opgaver og onboarding af medarbejdere](./onboard-view-status.md)
- [Oprette ansættelsesteam i Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Se også

- [Prøve eller købe appen Onboard](https://dynamics.microsoft.com/talent/onboard/)
- [Nyheder eller ændringer i Dynamics 365 Talent](./whats-new.md)
- [Frigivelsesplaner](https://docs.microsoft.com/business-applications-release-notes/index)
- [Få support til Microsoft Dynamics 365 Talent](./talent-support.md)
