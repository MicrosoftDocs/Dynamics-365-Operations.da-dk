---
title: Arbejde med moduler
description: Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
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
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914788"
---
# <a name="work-with-modules"></a>Arbejde med moduler

Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a>Oversigt

Moduler er logiske byggeklodser, der udgør sidestrukturen, og de har forskellige formål og omfang. Nogle moduler er containere på højt niveau, hvis eneste formål er at opbevare og organisere andre moduler (underordnede moduler). Andre moduler, f.eks. et enkelt modul til billedplacering, har et meget specifikt formål. Andre moduler som f.eks. et karruselmodul falder et sted mellem disse to kategorier.

Dynamics 365 Commerce-webstedet indeholder som standard et startsæt med modulbibliotek, der giver dig mulighed for at få de fleste grundlæggende e-handelsscenarier. Du bør oprette et e-handels-websted, der dækker alt, ved at bruge disse moduler. Du kan dog også tilpasse disse moduler eller opbygge nye, tilpassede moduler til specifikke behov. Hvis du vil bygge brugerdefinerede moduler, kan du få hjælp til at oprette et tilpasset modulbibliotek i et SDK (Software Development Kit) til moduldesign.

## <a name="container-modules-and-slots"></a>Containermoduler og pladser

Som tidligere nævnt er nogle moduler designet til at rumme underordnede moduler. Disse moduler kaldes *containere*, og de giver mulighed for hierarkier af indlejrede moduler. Containermoduler indeholder *pladser*. Pladser bruges til at håndtere layoutet og formålet med underordnede moduler i containeren. Et eksempel er et grundlæggende sidecontainermodul (et modul på øverste niveau for en side), der definerer flere vigtige pladser:

- En sidehovedplads
- En brødtekstplads
- En sidefodsplads

Modulets udvikler definerer disse pladser og bestemmer, hvilke underordnede moduler og hvor mange underordnede moduler der kan placeres direkte i det. F.eks. understøtter sidehovedpladsen måske kun ét modul af typen **Sidehovedmodul**, mens brødtekstpladsen understøtter et ubegrænset antal moduler af enhver type (undtagen andre sidecontainermoduler).

I oprettelsesværktøjerne behøver sideforfattere ikke at vide på forhånd, hvilke moduler der kan anbringes på hver plads. Når en sideforfatter vælger en plads og derefter prøver at vælge et modul, der skal føjes til den, vises en filtreret visning af modultyper, der understøttes for den pågældende plads.

## <a name="content-modules"></a>Indholdsmoduler

Indholdsmoduler har indhold og medieelementer, f.eks. tekst (f.eks. overskrifter, afsnit og links) eller aktivreferencer (f.eks. billeder, video og PDF-filer). Eksempler på typiske indholdsmodultyper er **Hero**, **Funktion** og **Banner**. Moduler af disse tre typer kan indeholde tekst eller medier, og de kræver ingen underordnede moduler for at gøre noget synligt på en side.

Størstedelen af typiske, daglige side- og indholdsoprettelsesaktiviteter omfatter indholdsmoduler, primært fordi disse moduler definerer det faktiske indhold, der gengives i de overordnede containermoduler. Mange indholdsmoduler er tilgængelige, og disse moduler er typisk de sidste stykker, du skal føje til sidens hierarki af indlejrede moduler.

I følgende illustration vises, hvordan moduler er indlejret i de overordnede containermodulpladser.

![Indlejring af moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Tilføje eller fjerne moduler

I følgende procedurer beskrives, hvordan du kan tilføje og fjerne moduler.

### <a name="add-a-module"></a>Tilføje et modul

Hvis du vil tilføje et modul på en plads eller container på en side, skal du følge disse trin.

1. Vælg en container eller en plads, som et underordnet modul kan føjes til, i dispositionsruden til venstre.

    > [!NOTE]
    > Moduldesigneren definerer listen over de modultyper, der kan føjes til en bestemt modulplads. Skabelonoprettere kan derefter begrænse de tilladte modulindstillinger for at sikre konsistent optimering af søgemaskiner og redigeringseffektivitet for alle sider, der er bygget ud fra en bestemt skabelon.

1. Vælg ellipseknappen (**...**) til modulet, og vælg derefter **Tilføj modul**. Dialogboksen **Tilføj modul** vises. Denne dialogboks filtreres automatisk, så der kun vises moduler, der understøttes i den valgte container eller plads. Listen over moduler bestemmes af sidens skabelon eller definitionen af containerens modul.

    > [!NOTE]
    > Hvis containeren eller pladsen ikke understøtter nye underordnede moduler, er indstillingen **Tilføj modul** ikke tilgængelig.

1. Søg efter og vælg et modul, der skal tilføjes på siden, i dialogboksen.

    > [!TIP]
    > **Funktion** og **Hero** er egnede modultyper, som begyndere kan arbejde med.

1. Vælg **OK** for at føje det valgte modul til den valgte container eller plads på siden.

### <a name="remove-a-module"></a>Fjerne et modul

Hvis du vil fjerne et modul fra en plads eller container på en side, skal du følge disse trin.

1. Vælg ellipseknappen i dispositionsruden til venstre ud for navnet på det modul, der skal fjernes, og vælg derefter knappen med papirkurven.
1. Når du bliver bedt om at bekræfte, at du vil fjerne modulet, skal du vælge **OK**.

## <a name="configure-modules"></a>Konfigurere moduler

I følgende procedurer beskrives, hvordan du kan konfigurere indholds- og containermoduler.

### <a name="configure-a-content-module"></a>Konfigurere et indholdsmodul

Hvis du vil konfigurere et indholdsmodul på en side, skal du følge disse trin.

1. Vælg en indholdsmodultype i dispositionsruden til venstre (f.eks. **Funktion**, **Hero** eller **Banner**).
1. Udvid de indlejrede kontrolelementer i ruden Egenskaber til højre ved at vælge overskrifterne, og angiv eventuelle nødvendige kontrolværdier.
1. Hvis ruden Egenskaber indeholder afsnittet **Datakonfiguration**, skal du vælge det for at udvide det. Gå ellers til trin 5.
1. Hvis knappen **Tilføj datakilde** ikke er markeret, skal du markere den og derefter vælge de indholdselementer, der skal tilføjes.
1. Angiv indstillinger for nødvendige eller ønskede kontrolelementer til moduler.
1. Vælg **Gem**.

### <a name="configure-a-container-module"></a>Konfigurere et containermodul

Hvis du vil konfigurere et containermodul på en side, skal du følge disse trin.

1. Vælg et containermodul på siden (f.eks. et karrusel- eller flydende containermodul).
1. Udvid de indlejrede kontrolelementer i ruden Egenskaber til højre ved at vælge overskrifterne, og angiv eventuelle nødvendige kontrolværdier.
1. Vælg ellipseknappen i dispositionsruden til venstre ud for navnet på enten containeren eller pladser inde i containeren, og vælg derefter **Tilføj modul**. Føj derefter underordnede moduler til den valgte container. Du kan finde flere oplysninger i proceduren [Tilføje et modul](#add-a-module) tidligere i dette emne.
1. Hvis der findes flere underordnede moduler som sidestillede i en overordnet container, kan du ændre deres visningsrækkefølge i den overordnede container. Vælg ellipseknappen for et modul, og brug derefter knapperne pil op og pil ned.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Arbejde med skabeloner](work-with-templates.md)

[Arbejde med forudindstillede layout](work-with-layouts.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Føje et containermodul til en side](add-container-module.md)

[Føje moduler for indholdsplacering til en side](add-content-placement-modules.md)

[Arbejd med publiceringsgrupper](publish-groups.md)

