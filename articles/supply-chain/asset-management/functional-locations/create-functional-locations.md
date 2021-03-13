---
title: Oprette arbejdssteder
description: Dette emne beskriver, hvordan du opretter et arbejdssted i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b5b81d7c318ba0a195dbc6324d700ccb8d39bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018215"
---
# <a name="create-functional-locations"></a>Oprette arbejdssteder

[!include [banner](../../includes/banner.md)]

 

Dette emne beskriver, hvordan du opretter et arbejdssted i Styring af aktiver.

Når du opretter en arbejdsstedsstruktur, skal du være opmærksom på, at når du har oprettet et arbejdssted, kan du ikke flytte det fra det oprindelige sted. Det betyder, at du nøje bør overveje strukturen af dine arbejdssteder, før du begynder at oprette dem i Styring af aktiver. Hvis du fortryder et arbejdssted, kan du slette det, forudsat at det endnu ikke er taget i brug.

Hvis du vil kunne arbejde med arbejdssteder, skal du starte med at oprette to "kategorier" af arbejdssteder:

- Opret *ét* standardarbejdssted uden underlokationer. Dette arbejdssted bruges kun som standardsted for aktiver, når du opretter nye aktiver.  
- Opret de arbejdsstedsstrukturer, der kræves til administration af vedligeholdelsesjob i dit firma.

## <a name="create-a-default-functional-location"></a>Oprette et standardarbejdssted

Når du bruger arbejdssteder, skal du starte med at oprette et standardsted, der skal bruges, når du opretter nye aktiver. Dette arbejdssted er det, du vælger i **Styring af aktiver** > **Opsætning** > **Parametre til aktivstyring** > **Aktiver**-link > feltet **Standardarbejdssted**. Standardarbejdsstedet kan bruges, når du opretter nye aktiver, og du endnu ikke har oprettet en arbejdsstedstruktur for disse aktiver.

1. Vælg **Styring af aktiver** > **Almindeligt** > **Arbejdssteder** > **Alle arbejdssteder**.  
2. Vælg **Nyt** i **Alle arbejdssteder**.
3. Indsæt et id i feltet **Arbejdssted**, for eksempel "0000" eller "Standard", for at angive, at dette er et særligt arbejdssted.
4. Angiv et navn til standardarbejdsstedet i feltet **Navn**.
5. Du må *ikke* vælge en overordnet i feltet **Overordnet**. Lad dette felt være tomt.
6. I feltet **Arbejdsstedstype** skal du vælge den arbejdsstedstype, der skal bruges til standardarbejdsstedet. Du finder flere oplysninger om, hvordan du konfigurerer typer af arbejdssteder, i [Arbejdsstedstyper](../setup-for-functional-locations/functional-location-types.md).
7. Vælg **OK**. Du bør ikke føje yderligere data til dette arbejdssted, da det kun bruges som et midlertidigt sted for nye aktiver, indtil du installerer aktiverne på de arbejdssteder, der bruges af din virksomhed.

## <a name="create-functional-locations"></a>Oprette arbejdssteder

Følgende procedure beskriver, hvordan du opretter de arbejdssteder, der kræves til vedligeholdelsesstyring i din virksomhed.

1. Vælg **Styring af aktiver** > **Almindeligt** > **Arbejdssteder** > **Alle arbejdssteder**. Du kan oprette et arbejdssted fra gittervisning eller detaljevisning.
2. Vælg knappen **Nyt**.
3. Indsæt et id i feltet **Arbejdssted**.
4. Angiv et navn til arbejdsstedet i feltet **Navn**.
5. Hvis arbejdsstedet er en underlokation i en struktur, skal du vælge det overordnede sted i feltet **Overordnet**.
6. Vælg en type i feltet **Arbejdsstedstype**.
7. Vælg **OK**.
8. Vælg arbejdsstedet, og klik på knappen **Rediger** for at tilføje yderligere oplysninger.

>[!NOTE]
>Afhængigt af din opsætning af livscyklustilstande for arbejdssteder skal du muligvis oprette alle underlokationer for et arbejdssted og derefter ændre livscyklustilstanden for arbejdsstedet, før du kan begynde at installere aktiver. Du kan finde flere oplysninger om installation af aktiver under [Installere aktiver på arbejdssteder](../functional-locations/install-objects-on-functional-locations.md). Se [Livscyklustilstande for arbejdssted](../setup-for-functional-locations/functional-location-stages.md) for at få mere at vide om opsætning af livscyklustilstande for arbejdssteder.

I detaljevisning kan du se oversigtspaneler, hvor du kan tilføje og redigere oplysninger om arbejdsstedet.

## <a name="general-information"></a>Generelle oplysninger

Dette afsnit indeholder en oversigt over overordnede og underordnede oplysninger i arbejdsstedsstrukturen. I afsnittet **Detaljer** kan du se antallet af aktivattributter, vedligeholdelsesplaner og aktiver, der er relateret til arbejdsstedet. I sektionen **Lager** kan du vælge lokationen og lagerstedet, som arbejdsstedet er relateret til. Lokation og lagersted bruges i forbindelse med arbejdsordrevares budgetter. Når du opretter et varebudget, bruges lokations- og lagerstedsoplysninger fra aktivets arbejdssted automatisk. I afsnittet **Livscyklustilstand** vises oplysninger om livscyklustilstanden for arbejdsstedet.

## <a name="installed-assets"></a>Installerede aktiver

Du kan finde flere oplysninger om installation af aktiver under [Installere aktiver på arbejdssteder](../functional-locations/install-objects-on-functional-locations.md). Du kan bruge knappen **Vis** i dette oversigtspanel til at få vist flere felter i oversigtspanelet. Felterne **Gyldigt fra** og **Underordnet aktiv** kan vises i gitteret.

## <a name="asset-attribute-requirements"></a>Krav til attribut for aktiv

I dette oversigtspanel kan du tilføje specifikke attributkrav for de aktiver, du installerer på arbejdsstedet. Disse krav er kun til informationsformål. De forhindrer dig ikke i at installere aktiver med andre attributkrav. Vælg **Tilføj linje**, og vælg attributtypen. Derefter indsætter du den relevante **Værdi**, vælger en tærskel i feltet **Tærskelkriterier** og gemmer posten.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Vedligeholdelsesplaner og vedligeholdelsesrunder

Her kan du tilføje vedligeholdelsesplaner og vedligeholdelsesrunder for arbejdsstedet, herunder en startdato. De aktiver, der er installeret på et arbejdssted, kan have andre konfigurerede vedligeholdelsesplaner. Alle vedligeholdelsesplaner og vedligeholdelsesrunder kan bruges til planlægning af aktivkalenderposter for et arbejdssted og dets aktuelt installerede aktiver.

>[!NOTE]
>Hvis du opdaterer opsætningen af aktivtyper, aktivmærker og aktivmodeller på vedligeholdelsesplaner i **Alle arbejdssteder** detaljevisning > oversigtspanelet **Vedligeholdelsesplaner**, når du har planlagt vedligeholdelsesplaner, bliver eksisterende poster i vedligeholdelsesplanen, der er relateret til dette arbejdssted, automatisk slettet. Hvis du vil oprette nye planlægningsposter, der svarer til den opdaterede opsætning af vedligeholdelsesplanen på arbejdsstedet, skal du køre en ny tidsplan for vedligeholdelsesplanen for dette arbejdssted. 

## <a name="address"></a>Adressering

Indsæt arbejdsstedets adresse i oversigtspanelet **Adresse**. Adresser på arbejdssteder nedarves, hvilket betyder, at hvis der ikke er defineret en adresse for en underlokation, bruges adressen på det overordnede sted.

## <a name="workers"></a>Arbejdere

I dette oversigtspanel kan du tilføje arbejdere, der er tilknyttet arbejdsstedet, og du kan vælge et primært arbejdssted for arbejderen. 

## <a name="attributes"></a>Egenskaber

I dette oversigtspanel kan du angive værdier for arbejdsstedsattributter. Disse attributter kan bruges til at beskrive egenskaber eller karakteristika, der er relevante for arbejdsstedet, for eksempel strukturelle egenskaber, bygningstype, områdebeskrivelser eller placering over eller under jorden.

Vælg **Tilføj linje**, og vælg attributtypen. Indsæt derefter den **Værdi**, der er relateret til attributtypen, og gem posten.

## <a name="financial-dimensions"></a>Økonomiske dimensioner

Du kan vælge økonomiske dimensioner til arbejdsstedet. [Arbejdsstedstyper](../setup-for-functional-locations/functional-location-types.md) kan konfigureres til at tillade automatisk opdatering af økonomiske dimensioner fra et arbejdssted. Det betyder, at aktiver, der er installeret på en økonomisk dimension, automatisk henter de økonomiske dimensioner for arbejdsstedet. Dette er nyttigt, hvis du vil have forskellige bærere, afhængigt af stederne.

Når data vedrørende **Lokation**, **Lagersted** **Adresse** og **Økonomiske dimensioner** opdateres på et overordnet arbejdssted, kan de relaterede underlokationer opdateres i overensstemmelse hermed, hvis du foretager dette valg under opdateringen. Der åbnes en dialogboks, som giver dig opdateringsindstillingerne.

## <a name="copy-a-functional-location-structure"></a>Kopiere en arbejdsstedsstruktur

Hvis din virksomhed har flere arbejdssteder med lignende stedstrukturer, kan du bruge kopieringsfunktionen i Styring af aktiver til hurtigt at oprette en række lignende stedhierarkier. Når du kopierer et bestemt arbejdssted eller en hel struktur, har det sted eller den nye struktur samme navn som den, du kopierede. Når kopieringsproceduren er udført, kan du nemt ændre navnet eller andre indstillinger på det nye arbejdssted, forudsat at den livscyklustilstand for arbejdssted, der er valgt for det nye arbejdssted, tillader det.

1. I **Alle arbejdssteder** skal du vælge det arbejdssted, du vil kopiere. Vælg f.eks. en toplokation (overordnet), hvis du vil kopiere hele arbejdsstedsstrukturen, herunder underlokationer.
2. Vælg knappen **Kopiér arbejdsstedsstruktur**. Det sted, du har valgt på listesiden, vises i feltet **Kopiér fra**.
3. Indsæt navnet på det nye sted i feltet **Nyt arbejdssted**.
4. I feltet **Overordnet, der skal indsættes under** skal du kun indsætte et overordnet id, hvis det sted, du opretter, skal være en del af en eksisterende arbejdsstedsstruktur.
5. Klik på **OK**. Den nye arbejdsstedsstruktur vises i **Alle arbejdssteder**.

>[!NOTE]
>Når du kopierer en arbejdsstedsstruktur, angives livscyklustilstande for arbejdssted i den nye struktur til den "første tilstand", du har oprettet for arbejdssteder. Om du kan omdøbe eller slette et arbejdssted ved hjælp af knapperne **Omdøb** og **Slet** i **Alle arbejdssteder**, afhænger af den aktuelle livscyklustilstand for arbejdsstedet.

## <a name="delete-a-functional-location"></a>Slette et arbejdssted

Et arbejdssted med relaterede underlokationer kan slettes, hvis der ikke er installeret aktiver på nogen af de arbejdssteder, du forsøger at slette, og hvis den aktuelle livscyklustilstand for arbejdsstedet tillader det.

1. I **Alle arbejdssteder** skal du vælge det arbejdssted, du vil slette.
2. Hvis det er nødvendigt, skal du opdatere arbejdsstedet til en livscyklustilstand for arbejdssted, der tillader sletning af et arbejdssted.
3. Vælg **Slet**.

>[!NOTE]
>Hvis du ikke kan slette et arbejdssted, kan du i stedet håndtere sletningen ved at konfigurere en livscyklustilstand for arbejdssted til dette formål. Du kan for eksempel oprette et "skrottet" eller "slettet" stadie, som ikke bør være et aktivt stadie, i formen **Livscyklustilstande for arbejdssted**.
