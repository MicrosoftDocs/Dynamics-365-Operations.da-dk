---
title: Arbejde med forudindstillinger for typografi
description: Dette emne beskriver, hvordan du kan arbejde med forudindstillede webstedstypografier i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7857920a04faaebaee44d5485f7b2ffc2e675f59e7c9dc15b2b86376207e3a2d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772124"
---
# <a name="work-with-style-presets"></a>Arbejde med forudindstillinger for typografi

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du kan arbejde med forudindstillede webstedstypografier i Microsoft Dynamics 365 Commerce-webstedsgenerator.

En forudindstillet typografi er et gemt sæt af alle tilladelige typografiværdier på tværs af et webstedstema. Den kan bruges til straks at ændre et websteds udseende fra webstedsgeneratoren. Forudindstillinger af typografier lader forfattere i Commerce-webstedsgeneratoren hurtigt ændre, få vist og aktivere et sæt typografiværdier på tværs af webstedet uden at skulle bruge overlappende typografiark (CSS – Cascading Style Sheets) eller installere temaer. Skrifttyper, knaptypografier og webstedsfarver er typiske eksempler på typografivariabler, der kan styres via forudindstillede typografier.

Det sæt typografivariabler, der er tilgængeligt på et websted, bestemmes af det tema- og modulbibliotek, der er installeret på webstedets lejer. Dynamics 365 Commerce online-SDK (Online Software Development Kit) giver udviklere mulighed for at implementere lige så mange (eller lige så få) variabler, der kan redigeres, som de skal bruge til et bestemt tema. Ved at aktivere flere typografivariabler kan en temaudvikler give endelige valg af webstedslayout i hænderne på webstedsgenerator-forfattere. Derfor kan ikke-udviklere opdatere og få vist webstedstypografier ved hjælp af værktøjssættet. Funktionen er også nyttig i forbindelse med situationer, hvor direkte ændringer af temaer eller CSS vil medføre unødvendige omkostninger.

Temaer, hvor godkendte typografivariabler er aktiveret, kræver en forudindstillet standardtypografi. De kan vælge at medtage yderligere forudindstillede indstillinger som en del af en installeret temapakke. Der kan f.eks. være installeret et tema, der indeholder en enkelt forudindstillet "modern light" standardtypografi. Alternativt kan det indeholde yderligere indstillinger for forudindstillede typografier ud over standardindstillingen, f.eks. "modern dark" "vintage light" eller "vintage dark". Disse indbyggede forudindstillede temaer oprettes af udviklere og kan bruges som udgangspunkt for nye webstedsdesign.

I webstedsgeneratoren kan forfattere vælge mellem et temas indbyggede forudindstillinger, eller de kan oprette deres egne forudindstillinger og tilpasninger ved hjælp af de aktiverede typografivariabler. En forudindstillet typografi kan vises i webstedsgeneratoren, før den aktiveres direkte på webstedet. Når en forfatters typografiændringer gennemses, kan den forudindstillede typografi angives til "aktiv" for webstedet.

## <a name="preview-a-style-preset"></a>Få vist en forudindstillet typografi

Hvis du vil have vist en forudindstillet typografi på dit websted i webstedgeneratoren, skal du følge disse trin.

1. Gå til **Webstedsindstillinger \> Design** i venstre navigationsrude.
1. På fanen **Standardtypografier** øverst i designeditoren på listen **Tilgængelige standarder** skal du vælge en standardtypografi og derefter **Vis** for at gå til Preset Editor.

    Hvis der aktuelt ikke er standarder på listen **Tilgængelige standarder**, se [Oprette en tilpasset standardtypografi](#create-a-custom-style-preset), hvis du ønsker flere oplysninger om, hvordan du opretter en tilpasset forudindstillet typografi.

    > [!NOTE]
    > Forudindstillinger, der er inkluderet i temaet, angives med et **indbygget** mærke. Disse indbyggede forudindstillinger er skrivebeskyttede. Hvis du vil kopiere en indbygget forudindstilling som en ny justerbar forudindstilling, skal du vælge ellipseknappen (**...**) for forudindstillingen og derefter **Gem som**.

1. Vælg **Forhåndsvisning** på kommandolinjen.
1. Vælg en URL-adresse på dit websted, der skal bruges til at få vist den forudindstillede typografi, og vælg derefter **OK**.
1. Vælg den kanalspecifikke og landespecifikke URL-adressevariant, du vil have vist, ved at vælge navnet på varianten. Der åbnes et nyt eksempelvindue i browseren, hvor den valgte formatindstillede typografi anvendes på den angivne side.

> [!NOTE]
> URL-adressen til forhåndsvisning er permanent og godkendt. Du kan derfor kopiere, indsætte og sende den til andre godkendte kolleger til gennemsyn, før du angiver den til "aktiv" på dit websted. URL-adressen for forhåndsvisning er også nyttig til at kontrollere typografier på forskellige enheder, i forskellige browsere og på forskellige skærmbilleder.

> [!TIP]
> Mens du redigerer en forudindstillet typografi, kan det være en god idé at lade det viste browservindue være åbent i et separat browservindue, så du hurtigt kan validere dine ændringer. Når du har gemt ændringerne i en forudindstilling, skal du opdatere det åbne forhåndsvindue i browseren for at validere brugeroplevelsen.

## <a name="create-a-custom-style-preset"></a>Oprette en tilpasset standardtypografi

Hvis du vil oprette en tilpasset standardtypografi i webstedgeneratoren, skal du følge disse trin.

1. Gå til **Webstedsindstillinger \> Design** i venstre navigationsrude.
1. På fanen **Standardtypografier** øverst oppe i designeditoren i kommandolinjen skal du vælge **Ny forudindstilling**.
1. Angiv et navn og en beskrivelse for den nye forudindstilling, og vælg derefer **Gem**. Der oprettes en ny forudindstilling, der kan tilpasses, og som bruger temaets standardværdier som udgangspunkt.

> [!NOTE]
> Du kan også oprette en ny tilpasset standardtypografi ud fra en eksisterende forudindstilling ved at vælge ellipseknappen (**...**) for den pågældende forudindstilling og derefter vælge **Gem som**. Du kan også vælge **Gem som** på kommandolinjen i Preset Editor.

## <a name="modify-global-and-module-type-style-values"></a>Ændre globale og modulære typografiværdier

Nogle af et temas typografivariabler deles af flere modultyper. Disse typografivariabler kaldes *globale* typografivariabler. Eksempler er primære webstedsfarver, standardskrifttyper og knaptypografier. Når du angiver globale variabler, kan du ændre udseendet på tværs af mange forskellige modultyper.

Nogle typografiværdier kan være entydige for en modultype, eller de kan evt. tilsidesætte en global standardværdi. Hvis et webstedstema har implementeret typografivariabler af typen modul, kan forfattere i webstedsgeneratoren tilpasse typografien for en modultype uafhængigt af de globale indstillinger. Modultypevariabler kan enten udvide eller tilsidesætte de globale typografivariabler i et tema.

> [!NOTE]
> Hierarkiet af typografiværdier på et websted fungerer på følgende måde. Typografiværdier, der vises længere til højre, overskriver de typografiværdier, der er placeret til venstre for dem.
>
> Temastandardværdier \< Globale typografiværdier \< Modulære typografiværdier \<CSS-tilsidesættelse

Udfør følgende trin for at ændre en standardstypografis globale eller modulære typeværdier i webstedsgeneratoren.

1. Gå til **Webstedsindstillinger \> Design** i venstre navigationsrude.
1. På fanen **Standardtypografier** øverst i designeditoren skal du vælge **Vis** for at sende standardtypografier til Preset Editor.
1. Vælg **Forhåndsvisning**, og følg derefter fremgangsmåden til valg af URL-adresser for at åbne en forhåndsvisning i fuldt browservindue for din forudindstilling. Lad dette browservindue for forhåndsvisning være åbent.
1. Vælg **Rediger** i øverste højre hjørne i Preset Editor.
1. Brug kontrolelementerne for typografivariabler i editoren til at ændre nogle globale typografiværdier.
1. Øverst i editoren skal du på fanen **Moduler** til højre for fanen **Global** vælge en modultype, der skal formateres.
1. Brug typografikontrolelementerne til at ændre nogle værdier for modultypen.
1. Når du er klar til at få forhåndsvist ændringerne, skal du vælge **Gem** på kommandolinjen.
1. Vend tilbage til det åbne browservindue for forhåndsvisning, og opdater det. Forhåndsvisningen i fuldt browservindue er praktisk til at kontrollere typografiændringer på forskellige pausepunkter i visninger, i forskellige browsere og på forskellige enhedsplatforme.
1. Når alle ændringer er fuldført og valideret, skal du vælge **Afslut redigering** i øverste højre hjørne af editoren.

> [!NOTE]
> Hvis du redigerer standardtypografien, der i øjeblikket er aktiv på dit websted, får du vist et blåt mærke for **Aktiv** i editoren. Dette mærke angiver, at forudindstillingen i øjeblikket er aktiv på dit websted. Hvis du ændrer den aktive forudindstilling, skal du vælge **Publicer** for at få vist disse ændringer på dit websted.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Oprette en ny forudindstillet typografi aktivt på dit direkte websted

Hvis du vil angive en standardtypografi som den nye aktive forudindstilling på dit websted, skal du følge disse trin.

- Vælg **Indstil som aktiv knap** på et af følgende steder:

    - Kommandolinjen i editoren for standardtypografier
    - Ellipsemenuen (**...**) for en hvilken som helst tilgængelig forudindstilling i hovedvisningen på fanen **Standardtypografier** ved **Webstedsindstillinger \> Design**

Værdierne for standardtypografien aktiveres på tværs af dit offentlige websted.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje et logo](add-logo.md)

[Vælge et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en favicon](add-favicon.md)

[Tilføje en velkomstmeddelelse](add-welcome-message.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
