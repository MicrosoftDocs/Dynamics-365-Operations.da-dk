---
title: Arbejde med skabeloner
description: Dette emne beskriver, hvordan du kan arbejde med skabeloner i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a3fc4259a76f6edcfaa0b8f6e08292477c6c0835
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411093"
---
# <a name="work-with-templates"></a>Arbejde med skabeloner


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du kan arbejde med skabeloner i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Som nævnt i [Oversigt over skabeloner og layout](templates-layouts-overview.md) definerer skabeloner det sæt indstillinger, der er tilgængelige for downstream-forfattere. Skabeloner er nyttige for en virksomheds webudviklerteam af flere årsager, og velstrukturerede skabeloner kan hjælpe med alle følgende mål:

- Gøre det lettere at oprette en indholdsredigeringsroller fra dag til dag.

    - Filtrere modulindstillinger, så det kun er relevante moduler, der vises for en bestemt sidesektion. (F.eks. kan en marketingsektion i en skabelon konfigureres til at filtrere irrelevante moduler fra, der aldrig bør bruges i den pågældende kontekst, og som kun komplicerer indholdsoprettelsesopgaver, hvis de vises).
    - Konfigurere standardmodulindstillinger som en hjælp til at forbedre effektiviteten under oprettelsen.
    - Definere standardsidefragmenter for at forbedre effektiviteten under oprettelsen. (F.eks. vises sidehoved- og sidefodsfragmenter i en skabelon automatisk på alle downstream-sider).

- Fastholde virksomhedens brands på websteder ved at definere et godkendt sæt indstillinger for modularrangement og -konfiguration.

    > [!TIP] 
    > Vellykkede e-handels-websteder giver kunderne velkendte, repeterbare og brandbaserede brugeroplevelsesmønstre (UX). Ved hjælp af skabelonerne kan du styre konsistensen på tværs af webstedet.

- Forbedre SEO-resultater gennem optimering af søgemaskiner ved at sikre gentagne og programmatisk definerede sidedefinitioner og metadata.

> [!NOTE]
> Selvom skabeloner er designet til at styre konsistensen på tværs af et sted, kan de teoretisk være konfigureret, så de ikke gennemtvinger konsistens. Brand- og webstedsadministratorer kan definere et hvilket som helst variationsniveau for siderne på deres websted. En skabelon kan f.eks. være helt åben, så indholdsforfattere kan oprette ethvert sidedesign, som de ønsker. I dette tilfælde gælder ingen af fordelene på den foregående liste.

## <a name="modify-a-template"></a>Redigere en skabelon

Skabeloner redigeres ved hjælp af skabeloneditoren.

Benyt en af følgende fremgangsmåder for at åbne skabeloneditoren:

- Vælg **Skabeloner** i navigationsruden på dit websted, og vælg derefter den skabelon, der skal redigeres.
- Vælg topnoden i dispositionstræet til venstre i sideeditoren for en eksisterende side. Vælg derefter **Rediger skabelon** i egenskabsruden til højre.

I dispositionstræet til venstre vises de modulindstillinger og -strukturer, der er tilgængelige for underordnede layout og sider. Når du vælger et modul i dispositionstræet, kan du se skabelonegenskaberne for det valgte modul i egenskabsruden til højre. Nogle af disse egenskaber er unikke for skabelonredigering. Egenskaberne er beskrevet i følgende tabel.

| Egenskabsbetegnelse | Beskrivelse |
|---|---|
| Min. forekomster | Denne egenskab definerer det mindste antal forekomster for det valgte modul. Hvis f.eks. værdien er angivet til **1**, kræves modulet for en downstream-forfatter, hvorimod modulet er valgfrit, hvis værdien er angivet til **0** (nul). |
| Maks. forekomster | Denne egenskab definerer det maksimale antal forekomster for det valgte modul. Hvis f.eks. værdien er angivet til **1**, kan modulet kun tilføjes én gang. |
| Min. moduler (containere) | For moduler, der indeholder andre moduler (dvs. *containermoduler*), definerer denne egenskab minimumantallet af samlede moduler, der skal tilføjes som underordnede. Til f.eks. et modul med karrusel kan værdien være angivet til et antal, der er større end 1. |
| Maks. moduler (containere) | For containermoduler definerer denne egenskab det maksimale antal samlede moduler, der skal tilføjes som underordnede. Til f.eks. et modul med karrusel kan værdien være angivet til et antal, der er mindre end 10. |
| Låst | Der vises et **Låst** boolesk kontrolelement ud for alle egenskaber for kernemoduler. Den tillader, at forfatteren af skabelonen låser en modulindstilling i skabelonen. En modulindstilling, der er låst, kan ikke tilsidesættes af underordnede layout eller sider. Den bliver en centralt redigerbar egenskabsværdi for alle de layout og sider, der bruger skabelonen. |

## <a name="create-a-new-template"></a>Opret en ny skabelon

Følg disse trin for at oprette en ny skabelon.

1. Vælg **Skabeloner** i navigationsruden på dit websted for at åbne skabelonfremviseren.
1. Vælg **Ny skabelon**.
1. Indtast et navn og en beskrivelse for skabelonen i dialogboksen til oprettelse af skabeloner. De værdier, du angiver, vises for forfattere, når de opretter nye sider. Angiv derfor metadata, der vil være nyttige for sideforfattere. Du kan f.eks. indtaste **Brug denne skabelon til at oprette generelle marketingsider** som beskrivelse. Disse metadata kan redigeres senere.
1. Vælg **OK** for at oprette den nye skabelon og åbne skabeloneditoren. I skabeloneditoren vises et dispositionstræ til venstre og en egenskabsrude til højre.
1. Udvid noderne i dispositionstræet, og vælg pladsen **HTML-hoved**.
1. Hvis der endnu ikke findes nogen moduler på denne plads, skal du vælge ellipseknappen (**...**) og derefter vælge **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge **Oversigt over standardside** og derefter vælge **OK**.
1. Vælg det nye modul i dispositionstræet, og angiv derefter de standardindstillinger, der skal konfigureres automatisk for alle underordnede sider i skabelonen, i egenskabsruden. Hvis du ikke ønsker nogen standardindstillinger, skal du lade værdierne være tomme.
1. Vælg pladsen **Brødtekst** i dispositionstræet, vælg ellipseknappen (...), og vælg derefter **Tilføj modul**.
1. Vælg et sidecontainermodul (der er måske kun én indstilling), og vælg derefter **OK**.

Under det nye sidecontainermodul kan du se et nyt sæt pladser (**Sidehoved**, **Hoved** osv.). Her kan du tilføje og konfigurere modulindstillinger, der vil være tilgængelige for forfattere, når de opretter sider ud fra denne skabelon. Hvis du ikke føjer nogen moduler til en plads, understøttes alle tilgængelige modultyper på den pågældende plads.

Skabelonen er nu teknisk gyldig, og den kan gemmes, checkes ind og bruges til at oprette nye sider. De næste tre afsnit beskriver dog nogle andre standardindstillinger, som du måske vil konfigurere først.

## <a name="add-a-header-and-a-footer"></a>Tilføje et sidehoved og en sidefod

Hvis webstedet allerede har et sidehovedfragment, skal du udføre disse trin for at føje et sidehoved og en sidefod til en skabelon.

1. Udvid **Brødtekst**-pladsen og dets underordnede sidemodul i dispositionstræet.
1. Vælg **Sidehoved**-pladsen.
1. Vælg ellipseknappen ud for **Sidehoved**-pladsen, og vælg derefter **Tilføj fragment**.
1. Søg efter og vælg dit websteds sidehovedfragment, og vælg derefter **OK**.

Alle de sider, der bruger skabelonen, arver nu dette sidehovedfragment.

Hvis dit websted endnu ikke har et sidehovedfragment, kan du se [Oprette et fragment](work-with-fragments.md#create-a-fragment) for at få oplysninger om, hvordan det oprettes, og derefter fuldføre den forrige procedure.

## <a name="change-the-template-theme"></a>Ændre skabelontemaet

Hvis du vil angive standardtemaet for alle sider, der bruger en skabelon, skal du benytte følgende fremgangsmåde.

1. Udvid **Brødtekst**-pladsen i dispositionstræet til venstre.
1. Vælg sidecontainermodulet i **Brødtekst**-pladsen (f.eks. **Standardside**).
1. Vælg et tema i feltet **Tema** i egenskabsruden til højre.

Som standard vil alle nye sider nu bruge det valgte tema. Hvis du vil forhindre, at sider tilsidesætter denne indstilling på layout- eller sideniveau, skal du angive det booleske kontrolelement **Låst** til **Sand**.

## <a name="add-a-script-to-a-template"></a>Føje et script til en skabelon

Du kan føje HTML-baserede **&lt;script&gt;**-elementer, der indeholder JavaScript, til skabelonen. På denne måde kan du levere standardscriptfunktioner til HTML hoved-, brødtekststart- og brødtekstslutafsnit på siderne.

Hvis du vil tilføje et script i en skabelon, skal du følge disse trin.

1. I dispositionstræet til venstre skal du vælge den plads, hvor du vil tilføje elementet **&lt;script&gt;** (f.eks. HTML-hoved, brødtekststart- og brødtekstslutafsnit).
1. Vælg ellipseknappen (...) til pladsen, og vælg derefter **Tilføj modul**.
1. Vælg et scriptmodul (f.eks. **Eksternt script** eller **Indbygget script**) i dialogboksen **Tilføj modul**.
1. Skriv dit script i egenskabsruden til højre i det relevante kontrolelement til scriptegenskaber (f.eks. **Indbygget script** eller **Scriptkoder**).
1. Angiv evt. andre valgfrie indstillinger, du vil konfigurere, i egenskabsruden.

> [!TIP]
> Hvis du vil genbruge nogle af dine scriptmoduler til andre skabeloner, kan du konvertere dem til fragmenter. På denne måde hjælper du med at gøre oprettelsesprocessen mere effektiv, og du centraliserer opdateringsprocessen. Du kan finde oplysninger om, hvordan du konverterer et scriptmodul til et fragment, under [Gemme en eksisterende modulkonfiguration som et fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Gemme, checke ind, se forhåndsvisning af og publicere en skabelon

Hvis du vil gemme en skabelon og checke den ind, skal du følge disse trin.

1. Vælg **Gem** øverst i skabeloneditoren. Gemte ændringer påvirker ikke downstream-sider, før de er checket ind.
1. Vælg **Afslut redigering**. Dine ændringer er nu synlige for downstream-arbejdsgange.

Hvis du vil se ændringerne på forhånd, skal du enten åbne en eksisterende side, der bruger skabelonen, eller oprette en ny side ud fra skabelonen.

Når du har set ændringerne af skabelonen, skal du følge et af disse trin for at publicere skabelonen til dit aktive websted:

* Gå til **Skabeloner**, vælg skabelonen, og vælg derefter **Publicer**.
* Vælg layoutnavnet for at åbne layouteditoren, og vælg derefter **Publicer**.
* Publicer en side, der refererer til den ikke-publicerede skabelon. Skabelonen publiceres automatisk.

> [!WARNING]
> Når en skabelon eller et andet CMS-element (indholdsstyringssystem) publiceres, kan det ses på internettet. Publicer ikke dokumenter eller aktiver, før du er klar til at gøre dem offentlige. Dokumentversioner, der er blevet gemt og checket ind, men som ikke er publiceret, kan kun findes af brugere, der er godkendt af systemet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Arbejde med forudindstillede layout](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]