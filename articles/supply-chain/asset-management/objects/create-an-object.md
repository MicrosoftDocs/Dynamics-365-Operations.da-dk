---
title: Oprette et aktiv
description: Dette emne beskriver, hvordan du opretter et aktiv i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e9c2b81e97a7b08dfdb596fbf6822ac94c7358dccd0b92c0677467dbc0c2e26
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721505"
---
# <a name="create-an-asset"></a>Oprette et aktiv

[!include [banner](../../includes/banner.md)]

 

Dette emne beskriver, hvordan du opretter et aktiv i Styring af aktiver.

1. Klik på **Styring af aktiver** > **Almindeligt** > **Aktiver** > **Alle aktiver** eller **Aktive aktiver**.
2. Klik på knappen **Nyt**.
3. I dialog **Opret aktiver** skal du indsætte data vedrørende **Aktiv** (aktiv-id'et) og navnet på aktivet. Vælg dato og klokkeslæt for aktivet i feltet **Gyldig**. Fra denne dato kan du installere aktivet på et arbejdssted samt flytte og erstatte aktivet i en aktiv struktur.
4. I feltet **Aktivtype** skal du vælge aktivtypen for aktivet (obligatorisk felt). Vælg om nødvendigt **Aktivproducent** og **Aktivmodel** for aktivet. Hvis der kun er oprettet ét produkt, vælges det pågældende produkt automatisk i feltet **Aktivproducent**. De valg, der er tilgængelige i felterne **Aktivproducent** og **Aktivmodel**, afhænger af opsætningen i [Aktivproducenter og -modeller](../setup-for-objects/product-and-model.md).
5. I gruppen **Overordnede aktiv** er feltet **Aktiv** tomt som standard. Hvis det er nødvendigt, kan du vælge et overordnet aktiv, og derefter udfyldes alle felter i gruppen **Overordnet aktiv** automatisk.
    >[!NOTE]  
    >Når du vælger et overordnet aktiv, er der to eller tre tilgængelige faner: Fanen **Mine aktiver** indeholder aktiver, der er relateret til de arbejdssteder, som du (den vedligeholdelsesarbejder, som er logget på systemet) kan allokeres til. Hvis der ikke er konfigureret noget arbejdssted for en vedligeholdelsesarbejder i formen [Vedligeholdelsesarbejdere og arbejdsgrupper](../setup-for-objects/workers-and-worker-groups.md), vil fanen **Mine aktiver** ikke være synlig. Fanen **Aktive aktiver** indeholder en liste over alle aktiver med status som "Aktiv" for aktivers livscyklus. Fanen **Aktiv visning** viser en trævisning af arbejdssteder og aktiver, der er installeret på disse steder.

6. Det standardarbejdssted, du har oprettet, foreslås for aktivet i **Aktiv**-gruppen > feltet **Arbejdssted**. Vælg et andet arbejdssted, hvis det er nødvendigt.

    >[!NOTE]
    >Når du har oprettet et aktiv, kan du installere det på et andet arbejdssted, hvis det er nødvendigt. Kun aktiver på øverste niveau (aktiver uden et aktuelt overordnet aktiv) kan installeres på et arbejdssted. Det betyder, at du installerer det øverste niveau samt eventuelle underordnede aktiver på det valgte arbejdssted. Læs mere om at installere aktiver på arbejdssteder under [Introduktion til arbejdssteder](../functional-locations/introduction-to-functional-locations.md).

7. Klik på **OK**.
8. Vælg aktivet på listen **Alle aktiver**, og klik på knappen **Rediger** for at føje yderligere oplysninger til aktivet.

## <a name="general-information"></a>Generelle oplysninger

Det arbejdssted, som aktivet er relateret til, vises i feltet **Arbejdssted**. Hvis aktivet er et overordnet aktiv, vises antallet af underordnede, der er relateret til aktivet, i feltet **Underordnet**. Hvis aktivet er et underordnet aktiv for et eksisterende aktiv, vises id'et for det overordnede aktiv i feltet **Overordnet**.

Du kan redigere oplysninger om **Aktivproducent** og **Aktivmodel** på aktivet, som bruges til at administrere reservedele, alternative reservedele og jobtypestandarder. Se [Aktivproducenter og -modeller](../setup-for-objects/product-and-model.md) for at få flere oplysninger. Du kan også tilføje oplysninger om **Modelår** og **Serienummer**, hvis det er nødvendigt.

**Aktuel livscyklustilstand** bruges til at definere, om aktivet er aktivt eller inaktivt. Når du opretter et aktiv, angives fasen altid til den første fase i aktivfasegruppen. Når du er klar til at aktivere et aktiv, skal du klikke på **Opdater aktivtilstand** og vælge den livscyklustilstand, du har defineret som "aktivt aktiv", og klikke på **OK**.

**Bemærk:** Når et aktiv er indstillet til "inaktiv", er det ikke længere muligt at oprette arbejdsordrer for aktivet. Du kan heller ikke planlægge forebyggende vedligeholdelsesopgaver for et inaktivt aktiv.

Felterne **Serviceniveau** og **Kritikalitet** vedrører arbejdsordrer, som er oprettet for aktivet. Felterne viser de **Serviceniveau**- og **Kritikalitet**-tal, som er beregnet for aktivets aktuelle opsætning. Se [Serviceniveauer for aktiv](../setup-for-objects/object-priorities.md) og [Kritikalitetstyper for aktiver](../setup-for-objects/object-criticalities.md) vedrørende opsætningen af disse værdier.

## <a name="asset"></a>Aktiv

Du kan vælge en **Ressource** til aktivet. Ressourcevalget bestemmer, hvilken kalender der bruges til planlægning af arbejdsordre. Ressourcevalg bruges ofte til anlægsaktiver. Ressourcer og ressourcegrupper konfigureres i **Virksomhedsadministration** > **Ressourcer** > **Ressourcegrupper** eller **Ressourcer**.

I feltet **Nummer på anlægsaktiv** kan du vælge et anlægsaktiv, der skal relateres til aktivet. Dette er relevant, hvis dit aktiv er relateret til et investeringsprojekt.

- Hvis aktivet er relateret til et anlægsaktiv, kan du oprette en arbejdsordretype, der skal bruges til arbejdsordrer i forbindelse med et investeringsprojekt. 
- Oplysninger om anlægsaktiver for et aktiv er relateret til modulet **Anlægsaktiver** i Dynamics 365 Supply Chain Management. Det betyder, at du i **Anlægsaktiver** > **Anlægsaktiver** > **Anlægsaktiver** kan se en oversigt over de projekter i Styring af aktiver, der kan relateres til et anlægsaktiv, ved at vælge aktivet på listen og se indholdet i **Relaterede oplysninger**-ruden > **Tilknyttede projekter**-sektionen .


## <a name="details"></a>Oplysninger

I feltet **Aktiv fra** vises den dato, hvor du opdaterede tilstanden for aktivlivscyklus til en aktiv tilstand (se [Tilstande for aktivlivscyklus](../setup-for-objects/object-stages.md) med hensyn til opsætning af tilstande for aktivlivscyklus). Hvis aktivet ikke længere er aktivt, og du har opdateret tilstanden for aktivlivscyklus til en inaktiv livscyklustilstand, vises den første dato, hvor aktivet er inaktivt, i feltet **Aktiv til**. Hvis det er nødvendigt, kan du ændre disse datoer manuelt.

Hvis det er nødvendigt, kan du indsætte en forventet dato for udskiftning af aktivet i feltet **Erstatningsdato**. Der kan indsættes en anslået værdi for udskiftning af aktivet i feltet **Erstatningsværdi**. Eksempel: Du kan bruge erstatningsoplysninger til at sammenligne dem med omkostningerne ved at vedligeholde et aktiv og derefter træffe en beslutning om at købe et nyt aktiv, hvis vedligeholdelsesomkostningerne på det eksisterende aktiv stiger hurtigt.

## <a name="notes"></a>Kommentarer

Du kan tilføje noter, der er relateret til aktivet, i oversigtspanelet **Noter**. Klik på knappen **Tilføj tidsstempel**, før du skriver noten, hvis du vil tilføje brugeroplysninger og et dato-/tidsstempel i noten.

## <a name="attributes"></a>Egenskaber

I dette oversigtspanel kan du angive værdier for aktivattributter. Disse attributter kan bruges til at beskrive egenskaber eller karakteristika, der er relevante for aktivet, f.eks størrelse, vægt eller maskinkonfiguration.

Klik på **Tilføj linje**, og vælg attributtypen. Indsæt derefter den **Værdi**, der er relateret til attributtypen, og gem posten.

>[!NOTE] 
>Du kan få en oversigt over aktivattributtyper og deres relation til aktiverne i **Aktivattribut** og **Oversigt over aktivattribut**. Du kan få flere oplysninger under [Oversigt over aktivattribut](../objects/object-specification-overview.md).

## <a name="vendor"></a>Leverandør

I oversigtspanelet **Kreditor** skal du vælge en kreditorkonto for aktivet. Hvis der er givet en leverandørgaranti, kan du også indsætte garantioplysninger her.

## <a name="address"></a>Adressering

I oversigtspanelet **Adresse** kan du indsætte udstyrets adresse. Hvis der ikke er indsat en adresse på aktivet, bruger aktivet adressen på et overordnet aktiv, hvis det overordnede aktiv har en adresse. Hvis der ikke er knyttet en adresse til aktivet eller nogen overordnede i aktivhierarkiet, kan adressen på det arbejdssted, hvor aktivet er installeret, bruges. Hvis dette arbejdssted ikke har en relateret adresse, bruges adressen på det overordnede arbejdssted på aktivet.

## <a name="asset-management-plans"></a>Planer for aktivstyring

Vedligeholdelsesplaner bruges til planlægning af forebyggende vedligeholdelsesopgaver med jævne mellemrum på aktivet. I dette oversigtspanel kan du oprette vedligeholdelsesplanlinjer for det valgte aktiv. Vedligeholdelsesrunder kan konfigureres for forskellige aktiver, hvor du skal udføre en lignende opgave med jævne mellemrum. Under fanen **Vedligeholdelsesplaner for arbejdssted** vises de vedligeholdelsesplaner, der er relateret til det arbejdssted, hvor aktivet er installeret.

>[!NOTE]
>Hvis du sletter en vedligeholdelsesplanlinje eller en vedligeholdelsesrunde, der er relateret til et aktiv i **Alle aktiver**, sletter du også automatisk alle vedligeholdelsesplaner med statussen "Oprettet", der er oprettet på baggrund af den pågældende vedligeholdelsesplan eller vedligeholdelsesrunde.

## <a name="functional-location-maintenance-plans"></a>Vedligeholdelsesplaner for arbejdssted

I dette oversigtspanel vises de vedligeholdelsesplaner, der er relateret til det arbejdssted, hvor aktivet er installeret.

## <a name="maintenance-rounds"></a>Vedligeholdelsesrunder

I dette oversigtspanel kan du tilføje eller fjerne vedligeholdelsesrunder, der er relateret til aktivet.

## <a name="financial-dimensions"></a>Økonomiske dimensioner

Du kan vælge økonomiske dimensioner til aktivet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]