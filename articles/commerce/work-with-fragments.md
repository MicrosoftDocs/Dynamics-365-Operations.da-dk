---
title: Arbejde med fragmenter
description: Denne artikel beskriver, hvorfor, hvornår og hvordan du bruger fragmenter i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 785e6f847fd1645557060356926f2dda8da22ac1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268199"
---
# <a name="work-with-fragments"></a>Arbejde med fragmenter 

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvorfor, hvornår og hvordan du bruger fragmenter i Microsoft Dynamics 365 Commerce.

Fragmenter giver en centraliseret oprettelsesoplevelse for modulkonfigurationer, der skal genbruges på hele webstedet. F.eks. konfigureres sidehoveder, sidefødder og bannere ofte som fragmenter, fordi de deles på tværs af mange sider. Du kan betragte fragmenter som miniaturewebsider, der kan indsættes på andre sider på webstedet. Fragmenter har deres egen livscyklus. Det vil sige, at de oprettes, refereres til, opdateres og slettes som uafhængige enheder i oprettelsesværktøjerne.

Når fragmenter er konfigureret, kan de bruges overalt, hvor moduler bruges i strukturen for webstedet. Der kan henvises til fragmenter på sider, i layout, i skabeloner og i andre fragmenter.

> [!NOTE]
> Fragmenter kan integreres i op til syv niveauer inde i andre fragmenter.

Hvis du f.eks. vil promovere en begivenhed på tværs af mange sider på webstedet, kan du bruge et fragment. Det første trin i oprettelsesprocessne for et nyt fragment er at vælge den type modul, du vil starte fra. I dette eksempel kan du opbygge fragmentet fra et hero-modul.

> [!NOTE]
> Fragmenter kan opbygges fra en hvilken som helst modultype.

Du kan derefter konfigurere hero-fragmentet med dit specifikke kampagneindhold. Du kan også lokalisere det efter behov. Det nye enkeltstående fragment kan derefter forbruges som et forudkonfigureret modul på hele webstedet. Du kan nemt føje det til skabeloner, til bestemte sider eller til andre fragmenter, der kan indeholde hero-moduler.

Alle de steder, hvor fragmentet tilføjes, er referencer til det centrale hero-fragment, du har oprettet. Hvis du udgiver ændringer til fragmentet, afspejles disse ændringer med det samme på alle de steder, hvor der refereres til fragmentet på tværs af webstedet. Derfor giver fragmenterne praktisk og effektiv genbrug og centraladministration af modulkonfigurationer på et websted. Ved effektivt at bruge dem kan du øge fleksibiliteten betydeligt og hjælpe med at reducere den omkostning, der er forbundet med at administrere webstedets indhold.

I følgende illustration vises, hvordan fragmenter kan bruges til at centralisere oprettelse af delte modulkonfigurationer på tværs af et e-handels-websted.

![En illustration, der viser, hvordan fragmenter kan bruges til at centralisere oprettelse af delte modulkonfigurationer på tværs af et e-handelswebsted.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Oprette et fragment

Du kan enten oprette et nyt fragment eller gemme en eksisterende modulkonfiguration som et fragment.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Gemme en eksisterende modulkonfiguration som et fragment

Hvis du vil konvertere et tidligere konfigureret modul til et fragment, der kan genbruges, skal du følge disse trin i Commerce-webstedsgenerator.

1. Åbn en side eller skabelon, der indeholder det modul, du vil konvertere til et fragment.
1. Vælg det tidligere konfigurerede modul i dispositionsruden til venstre eller direkte i den visuelle sidegenerator.
1. Vælg ellipsen (**...**) ud for navnet på modulet i enten dispositionsruden eller på værktøjslinjen for det valgte modul i den visuelle sidegenerator. 
1. Vælg **Del som fragment**. 
1. I dialogboksen **Gem som fragment** skal du angive et navn til fragmentet.
1. Vælg **OK** for at gemme modulkonfigurationen som et fragment, der kan føjes til andre sider.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Opret et nyt fragment

Udfør følgende trin for at oprette et nyt fragment i Commerce-webstedsgenerator.

1. Vælg **Fragmenter** i navigationsruden til venstre.
1. Vælg **Ny**. Der vises en **Nyt fragment**-dialogboks, hvor alle tilgængelige modultyper kan ses. Som tidligere nævnt kan fragmenter oprettes ud fra en hvilken som helst modultype.
1. Vælg en modultype til dit fragment.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Hvis du vælger en generisk containermodultype, får du størst fleksibilitet, når du skal opdatere og konfigurere dit fragment senere.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Tilføje, fjerne eller redigere fragmenter på en side

I følgende procedurer beskrives, hvordan du kan tilføje, fjerne og redigere fragmenter.

### <a name="add-a-fragment"></a>Tilføje et fragment

Udfør følgende trin for at tilføje et fragment på en side i Commerce-webstedsgenerator.

1. Vælg en container eller en plads, som underordnede moduler kan føjes til, i dispositionsruden til venstre eller direkte i den visuelle sidegenerator.
1. Vælg ellipsen (**...**) ud for navnet på containeren eller pladsen.  Hvis du bruger den visuelle sidegenerator, skal du vælge plussymbolet (**+**).  
1. Vælg **Tilføj fragment**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Hvis containeren eller pladsen ikke understøtter nye underordnede moduler, er indstillingen **Tilføj fragment** ikke tilgængelig.
    
1. Søg efter og vælg et fragment, der skal tilføjes, i dialogboksen **Vælg fragment**. Hvis der ikke vises nogen tilgængelige fragmenter, skal du muligvis først oprette et fragment ud fra en modultype, som den valgte container eller plads understøtter.
1. Vælg det ønskede fragment for at føje det til containeren eller pladsen på siden.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> De moduler, der er tilladt i en container eller plads, defineres af sidens skabelon eller modulernes egne definitioner.

### <a name="remove-a-fragment"></a>Fjerne et fragment

Hvis du vil fjerne et fragment fra en plads eller en container på en side i Commerce-webstedsgenerator, skal du følge disse trin.

1. Vælg ellipseknappen (**...**) i dispositionsruden til venstre ud for navnet på det fragment, der skal fjernes, og vælg derefter symbolet med papirkurven.  Du kan også vælge fragmentet i den visuelle sidegenerator og vælge symbolet for papirkurven på fragmentets værktøjslinje.
1. Når du bliver bedt om at bekræfte, at du vil fjerne fragmentet, skal du vælge **OK**.

> [!NOTE]
> Når du fjerner et fragment fra en side, fjerner du blot referencen til det fra den pågældende side. Du fjerner **ikke** fragmentet fra dit websted. Hvis du vil slette fragmenter på dit websted, skal du anvende brugergrænsefladen i fragmentfremviseren. Du kan kun slette fragmenter fra et websted, hvis der i øjeblikket ikke refereres til dem fra sider, skabeloner eller andre fragmenter.

### <a name="edit-a-fragment"></a>Redigere et fragment

Hvis du vil redigere fragmenter, skal du bruge fragmenteditoren. Denne restriktion er tilsigtet. Det er med til at sikre, at forfatterne ikke forveksler redigering af modulerne for en bestemt side med processen til redigering af fragmenter, der kan deles på mange sider.

Udfør følgende trin for at redigere et fragment i Commerce-webstedsgenerator.

1. Vælg **Fragmenter** i navigationsruden til venstre.
1. Vælg det fragment, du vil redigere, under **Fragmenter**.
1. Rediger fragmentets modulegenskaber og struktur efter behov. Processen minder om processen til redigering af moduler, der redigeres i sideeditorvisningen.

Du kan også redigere et fragment ved at vælge det på en side, i en skabelon eller i et overordnet fragment og derefter vælge **Rediger fragment** i ruden Egenskaber til højre.

### <a name="rename-a-fragment"></a>Omdøbe et fragment

Udfør følgende trin for at omdøbe et eksisterende fragment i webstedsgenerator.

1. Vælg **Fragmenter** i navigationsruden til venstre.
1. Vælg navnet på det fragment, du vil omdøbe.
1. Vælg **Rediger** for at begynde at redigere fragmentet. Bemærk, at du ikke kan redigere et fragment, hvis en anden allerede redigerer fragmentet.
1. Vælg blyantssymbolet ud for fragmentnavnet i ruden med egenskaber for fragment.
1. Rediger fragmentnavnet efter behov.
1. Markér afkrydsningsfeltet for at bekræfte navneændringen.
1. Vælg **Afslut redigering**.

Du kan omdøbe et oprettet fragment ved at redigere det og derefter vælge blyantssymbolet ud for fragmentnavnet i egenskabsruden.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Arbejde med skabeloner](work-with-templates.md)

[Arbejde med forudindstillede layout](work-with-layouts.md)

[Arbejde med publiceringsgrupper](publish-groups.md)

[Få vist versionshistorikken for at tilbageføre sider og fragmenter](version-history-revert.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
