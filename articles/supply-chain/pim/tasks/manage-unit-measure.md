---
title: Administrere måleenheder
description: Denne artikel beskriver, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.
author: t-benebo
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e2c21756b270ef7d914dc74a0cf61727953206a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863905"
---
# <a name="manage-units-of-measure"></a>Administrere måleenheder

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.

## <a name="open-the-units-page"></a>Åbne siden Enheder

Hvis du vil oprette og arbejde med de måleenheder, der er tilgængelige i systemet, skal du gå til **Organisationsadministration \> Opsætning \> Enheder \> enheder**.

I de resterende afsnit i denne artikel beskriver, hvad du kan gøre på siden **Enheder**.

## <a name="create-standard-units-and-conversions"></a>Oprette standardenheder og -omregninger

Hvis systemet ikke allerede indeholder de mest almindelige måleenheder for det metriske system og/eller det amerikanske målesystem (USCS), kan guiden Enhedsopsætning hjælpe dig med hurtigt at komme i gang med grundlæggende enhedsdefinitioner og -omregninger. Hvis du vil fuldføre guiden, skal du vælge **Guide til oprettelse af enhed** i handlingsruden og derefter følge instruktionerne på skærmen.

## <a name="create-or-edit-a-unit-of-measure"></a>Oprette eller redigere en måleenhed

Benyt følgende fremgangsmåde for at oprette eller redigere en måleenhed.

1. Udfør ét af følgende trin:

    - Hvis du vil redigere en eksisterende enhed, skal du vælge den i listeruden.
    - Vælg **Ny** i handlingsruden for at oprette en ny enhed.

1. Angiv følgende felter i postens hoved:

    - **Enhed** – Angiv det id eller symbol, der skal bruges til at referere til enheden på systemsproget. Dette id eller symbol er normalt en almindelig forkortelse for enheden, f.eks. *stk.* for hver eller *cm* for centimeter.
    - **Beskrivelse** – Indtast et beskrivende navn for enheden i systemsproget. Dette navn er normalt det fulde navn på enheden som f.eks. *Hver* eller *Centimeter*.

1. I oversigtspanelet **Generelt** skal du indstille følgende felter:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Enhedsklasse** – Vælg den egenskab, som enheden måler (f.eks. længde, område, masse eller antal).
    - **Enhedssystem** – Vælg det målingssystem, som enheden tilhører (*Metriske enheder* eller *Amerikanske måleenheder*).
    - **Basisenhed** – Angiv denne indstilling til *Ja*, hvis du vil bruge den aktuelle enhed som basisenhed for enhedsklassen. I så fald skal du kun angive omregningsfaktoren mellem basisenheden og hver ekstra enhed i enhedsklassen. Derefter kan systemet omregne alle enheder i enhedsklassen. Derfor er det lettere at konfigurere omregninger.

        Hvis gallon f.eks. er basisenheden for enhedsklassen *Volumen*, skal du kun konfigurere omregningsfaktorer fra quart til gallon og fra pint til gallon. Systemet kan derefter også omregne quart til pint.

        Du kan kun have én basisenhed pr. enhedsklasse.

    - **Systemenhed** – Angiv denne indstilling til *Ja*, hvis du vil bruge den aktuelle enhed som antaget enhed for alle uspecificerede målinger i enhedsklassen. Hvis et felt, der bruges til at angive et antal, f.eks. ikke tillader, at der angives en enhed (eller hvis brugeren ikke vælger en enhed), bruger systemet den enhed, der er angivet som systemenhed for enhedsklassen *Antal*. Du kan kun have én systemenhed pr. enhedsklasse.
    - **Decimalpræcision** – Angiv det antal decimaler, som værdier, der er angivet for den aktuelle enhed eller omregnet til den, skal afrundes til.

1. Vælg **Gem** i handlingsruden.

## <a name="define-unit-translations"></a>Definer enhedsoversættelser

Hvis du vil definere oversættelser for id'et eller symbolet og beskrivelsen af en måleenhed, skal du følge disse trin.

1. Opret eller vælg den enhed, der skal oprettes oversættelser for.
1. Vælg **Enhedstekster** i handlingsruden.

    Siden **Enhedstekster** vises. Du kan bruge denne side til at definere oversættelser for id'et eller symbolet for den valgte enhed. Disse oversættelser kan derefter bruges på eksterne dokumenter på kundespecifikke eller leverandørspecifikke sprog.

1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Sprog** skal du vælge det sprog, som du vil oversætte enhedens id eller symbol til.
1. Angiv oversættelsen af enheds-id'et eller symbolet på det valgte sprog i feltet **Tekst**.
1. Vælg **Gem** i handlingsruden.
1. Luk siden.
1. Vælg **Oversatte enhedsbeskrivelser** i **Handlingsrude**.

    Siden **Oversatte enhedsbeskrivelser** vises. Du kan bruge denne side til at definere sprogspecifikke beskrivelser af den valgte enhed.

1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Sprog** skal du vælge det sprog, som du vil oversætte enhedsbeskrivelsen til.
1. Angiv oversættelsen af enhedsbeskrivelsen på det valgte sprog i feltet **Beskrivelse**.
1. Vælg **Gem** i handlingsruden.
1. Luk siden.

## <a name="define-unit-conversion-rules"></a>Definer omregningsregler for enhed

Hvis du vil definere regler for omregninger mellem måleenheder, skal du benytte følgende fremgangsmåde.

1. Opret eller vælg den enhed, du vil definere omregningsregler for.
1. Vælg **Enhedsomregninger** i handlingsruden.

    Siden **Enhedsomregninger** åbnes. Du kan bruge denne side til at definere regler for omregning af den valgte enhed til og fra andre enheder i enhedsklassen.

1. Vælg en af følgende faner, afhængigt af den type omregning, som du vil konfigurere:

    - **Standardomregninger** – Konfigurer standardomregningsregler for alle produkter.
    - **Omregninger i klasser** – Konfigurer produktspecifikke omregningsregler for enheder i samme enhedsklasse.
    - **Omregninger mellem klasser** – Konfigurer produktspecifikke omregningsregler for enheder på tværs af enhedsklasser.

1. Udfør ét af følgende trin:

    - Vælg **Ny** på værktøjslinjen for at oprette en ny omregning.
    - Hvis du vil redigere en eksisterende omregning, skal du markere omregningen i gitteret og derefter vælge **Rediger** på værktøjslinjen.

1. Angiv følgende felter i den viste dialogboks med rullepanel:

    - **Produkt** – Vælg det specifikke produkt, som omregningen gælder for. Dette felt er kun tilgængeligt ved omregninger i og mellem klasser.
    - **Formellayout** – Lad dette felt være angivet til *Simpel* for at angive en simpel omregning, der har en enkelt faktor. Angiv den til *Avanceret* for at konfigurere en mere kompleks ligning. Formatet for avancerede ligninger varierer, afhængigt af enhedsklassen.
    - **Fra enhed** – Dette felt viser den valgte enhed. Normalt skal du ikke ændre værdien. (Hvis du ændrer værdien, skal du åbne Siden **Enhedsomregninger** for den valgte enhed for at få vist den nye omregning, når du har gemt den.)
    - **Til enhed** – Vælg den enhed, der skal omregnes til.
    - **Afrunding** – Vælg, hvordan brøkdele skal afrundes baseret på værdien for **Decimalpræcision** for den valgte enhed (*Til nærmeste*, *Op* eller *Ned*).
    - **Omregningsformel** – Brug de resterende felter øverst i dialogboksen med rullelisten til at angive formlen for omregning mellem de to enheder. De tilgængelige felter varierer, afhængigt af enhedsklassen og det formellayout, du har valgt.

1. Vælg **OK**.
1. Luk siden.

> [!TIP]
> Du kan også konfigurere enhedsomregninger pr. produktvariant. Du kan finde flere oplysninger i [Måleenhedsomregning pr. produktvariant](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
