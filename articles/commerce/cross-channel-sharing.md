---
title: Aktivere og bruge deling på tværs af kanaler
description: Dette emne beskriver, hvordan du aktiverer og bruger funktionen til deling på tværs af kanaler i Microsoft Dynamics 365 Commerce-webstedsgenerator.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: de317c2fae4607f5b8b887dd5e866d812043dcd3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799511"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Aktivere og bruge deling på tværs af kanaler

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du aktiverer og bruger funktionen til deling på tværs af kanaler i Microsoft Dynamics 365 Commerce-webstedsgenerator.

Med deling på tværs af kanaler kan forhandlere genbruge og dele indhold mellem flere forskellige kanaler af et websted. Denne egenskab er nyttig, når der er et kompatibelt basissprog for webstedskanaler, eller når der er mange forskellige indholdsobjekter til fælles.

Deling af på tværs af kanaler fungerer ved at aktivere en standardkanal, der søger efter tilgængeligt indhold, når der ikke findes en kanalspecifik version af det ønskede indhold. Indhold, der er beregnet til at blive delt mellem kanaler, oprettes i standardkanalen. Dette indhold kan lokaliseres for enhver landestandard, der bruges på en webstedskanal.

## <a name="when-to-use-cross-channel-sharing"></a>Hvornår du skal bruge deling på tværs af kanaler

Deling på tværs af kanaler er nyttig, når flere kanaler på et enkelt websted kan dele indhold. En forhandler, der har flere mærker og udstillingsvinduer, der er grupperet under et enkelt websted, kan f.eks. dele noget indhold på nogle eller alle udstillingsvinduer. Dette delte indhold kan være sider til vilkår og betingelser, betalingsbetingelser, leveringsmetoder og ofte stillede spørgsmål.

Deling på tværs af kanaler understøtter også fragmenter. Derfor kan der oprettes en indholdsside med kanalspecifikke fragmenter som indhold på tværs af kanaler. I dette tilfælde vil det meste af indholdet blive delt mellem kanalerne, men kanalspecifikke fragmenter på en side med krydskanaler gengives kun, når der anmodes om dem fra den tilsvarende udstillingsvinduekanal.

Websteder, der kun har én kanal, eller websteder, der har flere kanaler, der ikke kan dele indhold, vil ikke være omfattet af deling på tværs af kanaler.

## <a name="enable-cross-channel-sharing"></a>Aktivere deling på tværs af kanaler

Deling på tværs af kanaler aktiveres på webstedsniveau. Denne handling er envejs. Det vil sige, at når deling på tværs af kanaler er aktiveret, kan den med andre ord ikke deaktiveres.

Udfør følgende trin for at aktivere deling af på tværs af kanaler i Commerce-webstedsgenerator.

1. Gå til **Webstedsindstillinger \> Funktioner**.
1. Angiv indstillingen for funktionen **På tværs af kanal** til **Aktiveret**.

    ![Indstillingen på tværs af kanaler er indstillet til aktiveret i Commerce -webstedsgenerator](./media/enabling-cross-channel-sharing.png)

Når du har aktiveret deling på tværs af kanaler, vises oplysninger om tværkanal i afsnittet **Kanaler** i **Webstedsindstillinger \> Funktioner** som eksemplet i følgende illustration viser.

![Kanaloplysninger, der er synlige, efter at deling på tværs af kanaler er aktiveret](./media/channels-cross-channel.png)

Når du har aktiveret deling via flere kanaler, vil feltet **Kanal** i øverste højre hjørne af Commerce-webstedsgenerator medtage en **Onlinebutik på tværs af kanaler**, som du kan bruge til at administrere krydskanalindhold som vist i følgende illustration.

![Indstillingen Onlinebutik på tværs af kanaler i feltet Kanaler, efter at deling på tværs af kanaler er aktiveret](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Oprette og bruge indhold på tværs af kanaler

Du kan oprette og bruge indhold på tværs af kanaler på flere måder. Du kan f.eks. oprette krydskanalfragmenter, oprette krydskanalsider, der bruger krydskanal- og kanalspecifikt indhold, og tilsidesætte krydskanalfragmenter med kanalspecifikke versioner af fragmenter.

### <a name="create-a-cross-channel-fragment"></a>Oprette et krydskanalfragment

Udfør følgende trin for at oprette et krydskanalfragment i Commerce-webstedsgenerator.

1. Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. Vælg modulet **Kampagnebanner** i dialogboksen **Nyt fragment**, og angiv derefter et navn under **Fragmentnavn** (f.eks. **Banner på tværs af kanaler**). Vælg derefter **OK**.
1. Vælg **Tilføj meddelelse** i ruden Egenskaber i modulet **Kampagnebanner**, og vælg derefter **Meddelelse**.
1. Angiv **Krydskanal** under **Tekst** i dialogboksen **Meddelelse**, og vælg **OK**. 
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

Dette krydskanalfragment kan bruges på krydskanal- eller kanalspecifikke sider, der oprettes på en webstedskanal.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Oprette en side på tværs af kanaler, der bruger krydskanalindhold

Sider på tværs af kanaler kan bruges på en hvilken som helst kanal på dit websted. Du kan derfor oprette en side med delt indhold én gang og foretage efterfølgende opdateringer på et enkelt sted. En side med **Vilkår og betingelser** for krydskanal , der har URL-adressen `/toc`, kan f.eks. deles mellem alle kanalerne på et websted. Hvis basis-URL-adresserne for stedkanalerne er `www.fabrikam.com/brand1` og `www.fabrikam.com/brand2`, vil den samme krydskanals delte **Vilkår og betingelser**-side være tilgængelige fra både URL-adresser på `www.fabrikam.com/brand1/toc` og `www.fabrikam.com/brand2/toc`. Hvis siden **Vilkår og betingelser** skal opdateres senere, skal du kun opdatere den ene delte side.

Hvis du vil oprette en side til flere kanaler i Commerce-webstedsgenerator, der bruger indhold på tværs af kanaler, skal du følge disse trin.

1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge en skabelon som f.eks. **Marketing**.
1. Under **Sidenavn** skal du angive et sidenavn (f.eks. **Krydskanalside**).
1. Angiv en URL-adresse til siden under **Sidens URL-adresse** (f.eks. **examplepage**), og vælg derefter **OK**.
1. Vælg pladsen **Hoved** på den nye side, vælg ellipsen (**...**), og vælg derefter **Tilføj fragment**.
1. Vælg det krydskanalfragment, du har oprettet tidligere, og som har et kampagnebanner, i dialogboksen **Tilføj fragment**, og vælg derefter **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Du skulle kunne se kampagnebanneret "Krydskanal".
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Oprette en kanalspecifik side, der bruger krydskanalindhold

Ved at bruge krydskanalindhold på kanalspecifikke sider kan du oprette et delt indholdsfragment én gang og derefter bruge det på kanalspecifikke sider. Denne "ene kilde" er nyttig til delt indhold som f.eks. vilkår og betingelser, betalingsbetingelser eller kontaktoplysninger.

Hvis du vil oprette en kanalspecifik side i Commerce-webstedsgenerator, der bruger indhold på tværs af kanaler, skal du følge disse trin.

1. I en bestemt kanal, f.eks. **Fabrikam-udvidet onlinebutik**, skal du gå til **Sider** og derefter vælge **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge en skabelon som f.eks. **Marketing**.
1. Under **Sidenavn** skal du angive et sidenavn (f.eks. **Kanalspecifik side**).
1. Angiv en URL-adresse til siden under **Sidens URL-adresse** (f.eks. **channelspecificpage**), og vælg derefter **OK**.
1. Vælg pladsen **Hoved** på den nye side, vælg ellipsen (**...**), og vælg derefter **Tilføj fragment**.
1. Vælg **Onlinebutik på tværs af kanaler** under **Kanal** i dialogboksen **Tilføj fragment**. Det krydskanalfragment, du har oprettet tidligere, vises på listen. Vælg det, og vælg derefter **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Du skulle kunne se kampagnebanneret "Krydskanal".
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Oprette en kanalspecifik version af en krydskanalside

Deling på tværs af kanaler understøtter tilsidesættelse af krydskanalindhold. F.eks. vil alle undtagen én af dine webstedskanaler dele det samme indhold. Denne ene webstedskanal kræver andet indhold. Hvis du vil implementere det andet indhold for den, kan du tilsidesætte krydskanalindholdet med kanalspecifikt indhold ved at oprette en kanalspecifik version af krydskanalsiden.

Hvis du vil oprette en kanalspecifik version af en krydskanalside i Commerce-webstedsgenerator, skal du følge disse trin.

1. I feltet **Kanal** i øverste højre hjørne skal du vælge **Onlinebutik på tværs af kanaler**.
1. Åbn den krydskanalside, du har oprettet tidligere.
1. Vælg den kanal, der skal have specifikt indhold, i feltet **Kanal** øverst til højre. I sideeditoren vises en meddelelse, hvor du bliver bedt om at oprette en ny sidevariant.
1. Vælg **Opret sidevariant**.
1. På pladsen **Hoved** på sidevarianten skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Kampagnebanner** og derefter **OK**.
1. Vælg **Tilføj meddelelse** i ruden Egenskaber i modulet **Kampagnebanner**, og vælg derefter **Meddelelse**.
1. Angiv **Kanalspecifik** under **Tekst** i dialogboksen **Meddelelse**, og vælg **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Du skulle kunne se kampagnebanneret "Kanalspecifik".
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

Hvis du nu bruger kanalens grundlæggende URL-adresse og går til URL-adressen for krydskanalsiden på det pågældende websted, vises det kanalspecifikke indhold i stedet for krydskanalindholdet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Metoder til at tilføje indhold](add-manage-content.md)

[Ordliste til sidemodel](page-elements-overview.md)

[Dokumenttilstande og -livscyklus](document-states-overview.md)

[Arbejde med publiceringsgrupper](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
