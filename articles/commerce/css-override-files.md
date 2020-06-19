---
title: Arbejd med CSS-tilsidesættelsesfiler
description: Dette emne indeholder en beskrivelse af hvorfor, hvornår og hvordan du bruger CSS-tilsidesættelsesfiler (Cascading Style Sheets) i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411241"
---
# <a name="work-with-css-override-files"></a>Arbejd med CSS-tilsidesættelsesfiler


[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af hvorfor, hvornår og hvordan du bruger CSS-tilsidesættelsesfiler (Cascading Style Sheets) i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Permanente webstedstypografier skal normalt håndteres via et websteds tema. Temaerne indeholder de grundlæggende indstillinger for CSS og typografi, der er gældende for modulerne på siderne på dit websted. Temaer oprettes ved hjælp af det online SDK (Software Development Kit) til Dynamics 365 Commerce, og implementeres på dine websteder via Microsoft Dynamics Lifecycle Services (LCS). Temafejlfindingsfunktioner og modulgrænsefladekonfigurationer i SDK hjælper webstedsudviklere med at oprette tilpassede og sammenhængende webstedsdesignpakker. Når disse designpakker installeres på et websted, kan webstedsforfatterne fokusere på at oprette, redigere og udgive indhold i stedet for at udvikle webstederne.

Som følge af et temas sædvanlige livscyklus kan afhængigheden af udviklere til at foretage typografiændringer ved hjælp af SDK- og LCS-installationspipeline være uoverkommelig i nogle scenarier. Webstedsprototyper eller hotfixes kan virke besværlige, hvis SDK'et ikke er konfigureret, eller hvis du ikke har tid til at vente på en LCS-installation.

I disse scenarier kan CSS-tilsidesættelsesfiler hjælpe. I Commerce-oprettelsesværktøjerne kan godkendte brugere uploade en CSS-fil, få den vist og derefter aktivere den for at tilsidesætte et websteds tema. Der er ikke behov for overordnet installation af SDK eller LCS. De tilsidesættelser, der er angivet i en CSS-tilsidesættelsesfil, kan være lige så små som en ændring af en enkelt teksttypografi eller så omfattende som et fuldstændigt eftersyn af varemærket.

Før du bruger CSS-tilsidesættelsesfiler, skal du være opmærksom på følgende begrænsninger:

- Der kan kun aktiveres én CSS-tilsidesættelsesfil på et websted ad gangen. Alle aktive tilsidesættelser skal derfor være indeholdt i en enkelt tilsidesættelsesfil.
- Selvom du kan få vist tilsidesættelser i Commerce-oprettelsesværktøjerne, er der ingen dedikerede fejlfindingsfunktioner, som kan hjælpe med at identificere eventuelle fejl, som skyldes tilsidesættelserne. Når du bruger CSS-tilsidesættelsesfiler har du med andre ord ikke det samme værktøjsæt, som SDK indeholder til validering af moduler og oprettelse.

Ikke desto mindre giver CSS-tilsidesættelsesfiler dig en hurtig måde, hvorpå du kan prototype et design eller implementere et hotfix, før der udvikles og implementeres en fuldstændig temaopdatering.

## <a name="create-a-css-override-file"></a>Opret en CSS-tilsidesættelsesfil

Du kan bruge et hvilket som helst IDE (integreret udviklingsmiljø), teksteditor eller kildekodeeditor til at oprette en CSS-tilsidesættelsesfil. En typisk fremgangsmåde er at bruge din browsers standard webfejlfindingsprogram til at identificere typografivælgere, egenskaber og værdier på dit eksisterende websted. De fleste browsere giver dig mulighed for at ændre værdier og få vist dem i fejlfindingsprogrammet. Når du har identificeret de ændringer, du vil foretage, kan du gemme dem i din egen CSS-fil.

## <a name="upload-a-css-override-file"></a>Overfør en CSS-tilsidesættelsesfil

Følg disse trin for at overføre en CSS-fil til dit websted i Commerce.

1. Gå til dit websted i oprettelsesværktøjerne.
1. Vælg **Design** i navigationsruden til venstre.

    > [!NOTE]
    > Afhængigt af versionen af de Commerce-oprettelsesværktøjer du bruger, skal du muligvis udvide **Indstillingerne** i navigationsruden, før du kan vælge **Design**.

1. Øverst i den primære designrude skal du vælge fanen **CSS-tilsidesættelse**, hvis den ikke allerede er valgt.
1. Vælg **Tilgængelige CSS-tilsidesættelser** skal du vælge **Overfør CSS-fil**. Der vises et Stifinder-vindue.
1. Søg i Stifinder, og vælg en CSS-fil, og vælg dernæst **Åbn**. Den overførte CSS-fil vises nu under **Tilgængelige CSS-tilsidesættelse**.

## <a name="preview-a-css-override-file"></a>Få vist en CSS-tilsidesættelsesfil

Følg disse trin for at få vist en CSS-tilsidesættelsesfil, før du gør den aktiv på dit aktive websted.

1. I navigationsruden til venstre skal du vælge **Design**og derefter på fanen **CSS-tilsidesættelse** under **Tilgængelige CSS-tilsidesættelser** finde den CSS-fil, du vil have vist.
1. Ud for CSS-filnavnet skal du vælge **Vis websted**.
1. I dialogboksen **Vælg en URL-adresse** skal du vælge URL-adressen for det websted, hvorpå du ønsker at se den anvendte tilsidesættelse, og derefter vælge **OK**.
1. Hvis der er flere varianter for den valgte URL-adresse, skal du vælge den ønskede variant i den viste dialogboks **Se variationer**.

En ny browserfane eller et nyt vindue åbnes, hvor du kan validere dine typografitilsidesættelser mod dit websted. Du kan derefter dele URL-adressen med andre godkendte Commerce-brugere til gennemsyn og feedback.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Aktivér en CSS-tilsidesættelsesfil på dit aktive websted

Når du har set og godkendt CSS-tilsidesættelsesfilen, kan du aktivere den på dit aktive websted.

> [!NOTE]
> Der kan kun aktiveres én CSS-tilsidesættelsesfil på dit websted ad gangen. Hvis du aktiverer en ny tilsidesættelsesfil, deaktiveres den forrige tilsidesættelsesfil. Sørg derfor for, at alle påkrævede tilsidesættelser findes i en enkelt CSS-tilsidesættelsesfil.

Følg disse trin for at aktivere en CSS-tilsidesættelsesfil.

1. I navigationsruden til venstre skal du vælge **Design**og derefter på fanen **CSS-tilsidesættelse** under **Tilgængelige CSS-tilsidesættelser** finde den CSS-fil, du vil aktivere.
1. Under CSS-filnavnet skal du vælge **Aktivér**. Tilsidesættelsesfilen bliver straks aktiveret på dit aktive websted.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Deaktivér en CSS-tilsidesættelsesfil på dit aktive websted

Følg disse trin for at deaktivere en CSS-tilsidesættelsesfil på dit websted.

1. I navigationsruden til venstre skal du vælge **Design**og derefter på fanen **CSS-tilsidesættelse** under **Tilgængelige CSS-tilsidesættelser** finde den CSS-fil, du vil deaktivere.
1. Under CSS-filnavnet skal du vælge **Deaktivér**. Tilsidesættelsesfilen bliver straks deaktiveret på dit aktive websted.

> [!TIP]
> Hvis du vil tilgå yderligere indstillinger for CSS-tilsidesættelsesfiler, skal du vælge ellipsen (**...**) ud for CSS-filnavnet. Indstillingerne **Download**, **Omdøb** og **Erstat** er nyttige til hurtige ændringer af en eksisterende CSS-tilsidesættelsesfil.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje et logo](add-logo.md)

[Vælge et tema for webstedet](select-site-theme.md)

[Arbejde med forudindstillinger for typografier](style-presets.md)

[Tilføje en favicon](add-favicon.md)

[Tilføje en velkomstmeddelelse](add-welcome-message.md)

[Tilføje en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)
