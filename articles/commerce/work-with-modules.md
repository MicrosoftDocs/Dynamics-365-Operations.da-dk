---
title: Arbejde med moduler
description: Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
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
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 301eb6206fb9e02c3aa7d3c07cf368ba800a1ab9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411097"
---
# <a name="work-with-modules"></a>Arbejde med moduler

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Moduler er logiske byggeklodser, der udgør sidestrukturen, og de har forskellige formål og omfang. Nogle moduler er containere på højt niveau, hvis eneste formål er at opbevare og organisere andre moduler (underordnede moduler). Andre moduler, f.eks. et enkelt modul til billedplacering, har et meget specifikt formål. Andre moduler som f.eks. et karruselmodul falder et sted mellem disse to kategorier.

Dynamics 365 Commerce-webstedet indeholder som standard et modulbibliotek, der giver dig mulighed for at få de fleste grundlæggende e-handelsscenarier. Du bør oprette et e-handels-websted, der dækker alt, ved at bruge disse moduler. Du kan dog også tilpasse disse moduler eller opbygge nye, tilpassede moduler til specifikke behov. Hvis du vil bygge brugerdefinerede moduler, kan du få hjælp til at oprette et tilpasset modulbibliotek i et SDK (Software Development Kit) til moduldesign.

## <a name="container-modules-and-slots"></a>Containermoduler og pladser

Som tidligere nævnt er nogle moduler designet til at rumme underordnede moduler. Disse moduler kaldes *containere*, og de giver mulighed for hierarkier af indlejrede moduler. Containermoduler indeholder *pladser*. Pladser bruges til at håndtere layoutet og formålet med underordnede moduler i containeren. Et eksempel er et grundlæggende sidecontainermodul (et modul på øverste niveau for en side), der definerer flere vigtige pladser:

- En sidehovedplads
- En undersidehovedplads
- En hovedplads
- En sidefodsplads
- En undersidefodsplads

Modulets udvikler definerer disse pladser og bestemmer, hvilke underordnede moduler og hvor mange underordnede moduler der kan placeres direkte i det. F.eks. understøtter sidehovedpladsen måske kun ét modul af typen **Sidehovedmodul**, mens brødtekstpladsen understøtter et ubegrænset antal moduler af enhver type (undtagen andre sidecontainermoduler).

I oprettelsesværktøjerne behøver sideforfattere ikke at vide på forhånd, hvilke moduler der kan anbringes på hver plads. Når en sideforfatter vælger en plads og derefter prøver at vælge et modul, der skal føjes til den, vises en filtreret visning af modultyper, der understøttes for den pågældende plads.

## <a name="content-modules"></a>Indholdsmoduler

Indholdsmoduler har indhold og medieelementer, f.eks. tekst (f.eks. overskrifter, afsnit og links) eller aktivreferencer (f.eks. billeder, video og PDF-filer). Typiske indholdsmodultyper omfatter indholdsblok, tekstblok og kampagnebannermoduler. Moduler af disse tre typer kan indeholde tekst eller medier, og de kræver ingen underordnede moduler for at gøre noget synligt på en side.

Størstedelen af typiske, daglige side- og indholdsoprettelsesaktiviteter omfatter indholdsmoduler, primært fordi disse moduler definerer det faktiske indhold, der gengives i de overordnede containermoduler. Mange indholdsmoduler er tilgængelige, og disse moduler er typisk de sidste stykker, du skal føje til sidens hierarki af indlejrede moduler.

I følgende illustration vises, hvordan moduler er indlejret i de overordnede containermodulpladser.

![Indlejring af moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Tilføje eller fjerne moduler

I følgende procedurer beskrives, hvordan du kan tilføje og fjerne moduler.

### <a name="add-a-module"></a>Tilføje et modul

Hvis du vil tilføje et modul på en plads eller container på en side, skal du følge disse trin.

1. Vælg en container eller en plads, som et underordnet modul kan føjes til, i dispositionsruden til venstre eller direkte i hovedlærredet.

    > [!NOTE]
    > Moduldesigneren definerer listen over de modultyper, der kan føjes til en bestemt modulplads. Skabelonoprettere kan derefter begrænse de tilladte modulindstillinger for at sikre konsistent optimering af søgemaskiner og redigeringseffektivitet for alle de sider, der er bygget ud fra en bestemt skabelon. Dialogboksen **Tilføj modul** filtreres automatisk, når et modul føjes til en plads, så der kun vises moduler, der understøttes i den valgte container eller plads. Listen over tilladte moduler bestemmes af sidens skabelon eller definitionen af containerens modul.

1. Hvis du bruger dispositionsruden, skal du vælge ellipsen (**...**) ud for modulnavnet og derefter vælge **Tilføj modul**. Hvis du bruger kontrolelementerne direkte i lærredet, skal du vælge plussymbolet (**+**) i en tom plads eller ved siden af det aktuelt valgte modul og derefter vælge **Tilføj modul**.

    > [!NOTE]
    > Hvis containeren eller pladsen ikke understøtter nye underordnede moduler, er indstillingen **Tilføj modul** ikke tilgængelig.

1. Vælg et modul, der skal tilføjes på siden, i dialogboksen **Tilføj modul**.

    > [!TIP]
    > **Indholdsblok** er en god modultype, som begyndere kan arbejde med.

1. Vælg **OK** for at føje det valgte modul til den valgte container eller plads på siden.

### <a name="remove-a-module"></a>Fjerne et modul

Hvis du vil fjerne et modul fra en plads eller container på en side, skal du følge disse trin.

1. Vælg ellipseknappen (**...**) i dispositionsruden til venstre ud for navnet på det modul, der skal fjernes, og vælg derefter symbolet med papirkurven. Du kan også vælge papirkurvesymbolet på værktøjslinjen i det valgte modul på hovedlærredet.
1. Når du bliver bedt om at bekræfte, at du vil fjerne modulet, skal du vælge **OK**.

## <a name="move-a-module-to-a-new-position"></a>Flytte et modul til en ny position

Hvis du vil flytte et modul til en ny position på siden, skal du bruge en af følgende metoder.

### <a name="move-a-module-using-the-outline-pane"></a>Flytte et modul ved hjælp af dispositionsruden

Hvis du vil flytte et modul ved hjælp af dispositionsruden, skal du følge disse trin.

1. Markér og hold fast i det modul, du vil flytte, i dispositionsruden, og træk derefter modulet til en ny placering i dispositionen. Den blå linje i konturen og på lærredet angiver, hvor modulet kan placeres.
1. Slip modulet på den nye placering.

### <a name="move-a-module-directly-within-the-canvas"></a>Flytte et modul direkte i lærredet

Hvis du vil flytte et modul direkte i lærredet, skal du følge disse trin.

1. Vælg det modul, du vil flytte, i lærredet. 
1. Vælg enten et symbol for opadgående eller nedadgående pil på værktøjslinjen for modulet, og træk derefter pilen til en ny placering på siden. Den blå linje i lærredet og konturen angiver, hvor modulet kan placeres. Hvis et modul ikke kan flyttes op eller ned, vil pilesymbolet være nedtonet. 
1. Slip modulet på den nye placering.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Flytte et modul ved hjælp af ellipsemenuen

Hvis du vil flytte et modul ved hjælp af ellipsemenuen, skal du følge disse trin.

1. Vælg et modul enten i dispositionen eller på lærredet.
1. Vælg ellipsen (**...**) ud for navnet på modulet i dispositionsruden eller på værktøjslinjen for modulet på lærredet.
1. Hvis modulet kan flyttes op eller ned inden for containeren eller pladsen, kan du se indstillingerne for **Flyt op** eller **Flyt ned**. Vælg den ønskede indstilling for flytning for at flytte modulet op eller ned i forhold til dets sidestillede.

## <a name="configure-modules"></a>Konfigurere moduler

I følgende procedurer beskrives, hvordan du kan konfigurere indholds- og containermoduler.

### <a name="configure-a-content-module"></a>Konfigurere et indholdsmodul

Hvis du vil konfigurere et indholdsmodul på en side, skal du følge disse trin.

1. Udvid træet i dispositionsruden til venstre, og vælg et indholdsmodul (f.eks. **Indholdsblok**). Eller vælg modulet i hovedlærredet.
1. Angiv egenskaber for de ønskede kontrolelementer til moduler i ruden Egenskaber for modul til højre.
1. Vælg **Gem** på kommandolinjen. Dette vil også opdatere eksemplet på lærredet.

### <a name="edit-module-text-properties"></a>Redigere tekstegenskaber for modul

Tekstegenskaber for modul, der ikke er skrivebeskyttet, kan redigeres direkte i lærredet.

Benyt følgende fremgangsmåde for at redigere egenskaber for modultekst.

1. Vælg tekstkontrolelementet på lærredet, og placer derefter markøren på det sted, hvor du vil redigere teksten.
1. Indtast tekstindholdet.
1. Vælg et vilkårligt sted uden for tekstindholdet for at fortsætte med at redigere andet indhold.

### <a name="inline-image-selection"></a>Valg af indbygget billede

Modulbilleder, der ikke er skrivebeskyttet, kan ændres direkte i lærredet.

Hvis du vil vælge et nyt billede for et indholdsmodul, skal du følge disse trin.

1. Dobbeltklik på billedet på lærredet. Dette vil åbne vinduet med medievælgeren.
1. Find og vælg et nyt billede, du vil bruge, og vælg derefter **OK**. Det nye billede gengives nu på lærredet.

### <a name="configure-a-container-module"></a>Konfigurere et containermodul

Hvis du vil konfigurere et containermodul på en side, skal du følge disse trin.

1. Vælg et containermodul på siden (f.eks. et karrusel- eller flydende containermodul).
1. Udvid de indlejrede kontrolelementer i ruden Egenskaber til højre ved at vælge overskrifterne, og angiv eventuelle nødvendige kontrolværdier.
1. Vælg ellipseknappen i dispositionsruden til venstre ud for navnet på enten containeren eller pladser inde i containeren, og vælg derefter **Tilføj modul**. Føj derefter underordnede moduler til den valgte container. Du kan finde flere oplysninger i afsnittet [Arbejde med moduler](#add-a-module) tidligere i dette emne.
1. Hvis der findes flere underordnede moduler som sidestillede i en overordnet container, kan du ændre deres visningsrækkefølge i den overordnede container. Vælg ellipseknappen for et modul, og brug derefter knapperne pil op og pil ned.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Arbejde med skabeloner](work-with-templates.md)

[Arbejde med forudindstillede layout](work-with-layouts.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Føje et containermodul til en side](add-container-module.md)

[Arbejde med publiceringsgrupper](publish-groups.md)

