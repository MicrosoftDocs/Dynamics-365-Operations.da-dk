---
title: Flytte, erstatte og installere aktiver
description: Dette emne forklarer, hvordan du flytter, erstatter og installerer aktiver i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 022ffc59b1b64913fedaf550f3fdb32141a94031
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020273"
---
# <a name="move-replace-and-install-assets"></a>Flytte, erstatte og installere aktiver

[!include [banner](../../includes/banner.md)]

 

Dette emne forklarer, hvordan du flytter, erstatter og installerer aktiver i Styring af aktiver. Du kan oprette individuelle aktiver, der ikke har relationer til andre aktiver, eller du kan oprette en aktivstruktur, der omfatter et overordnet aktiv (aktiv på øverste niveau) og relaterede underordnede aktiver (underaktiver). I Styring af aktiver er der tre metoder til at flytte og ændre placeringen af et aktiv:

- **Flyt** – flyt et aktiv til en anden aktivstruktur eller til et andet sted i samme aktivstruktur.
- **Erstat** – fjern midlertidigt et aktiv fra en aktivstruktur, så det kan repareres eller renoveres, og føj derefter det renoverede aktiv til aktivstrukturen igen. Du kan også permanent erstatte et brugt aktiv med et nyt aktiv.
- **Installer** – installer et overordnet aktiv og eventuelle relaterede underordnede aktiver på et arbejdssted.

> [!NOTE]
> Det aktiv, du flytter, erstatter eller installerer, kan være relateret til et andet arbejdssted. I så fald kan aktivet muligvis bruge arbejdsstedets økonomiske dimensioner. På siden **Arbejdsstedstyper** konfigurerer du håndteringen af arbejdsstedernes økonomiske dimensioner.

## <a name="move-asset"></a>Flyt aktiv

Anvend funktionen **Flyt aktiv** for at flytte et aktiv til enten en anden aktivstruktur eller til et andet sted i samme aktivstruktur. Du kan også flytte et aktiv ud af en aktivstruktur, så det bliver et selvstændigt aktiv uden strukturrelationer.

> [!NOTE]
> Brug ikke denne funktion, hvis aktiverne repareres eller udskiftes midlertidigt. Brug i stedet funktionen **Erstat aktiv**, som beskrives senere i dette emne.

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**.
2. Vælg hvilket aktiv, du ønsker at flytte, på listen. Hvis aktivet har underordnede aktiver, flytter du også disse aktiver.
3. Vælg **Flyt aktiv** for at flytte det.
4. Hvis du vil flytte aktivet, så det bliver en del af en aktivstruktur, skal du vælge det nye overordnede aktiv i feltet **Overordnet aktiv**. Hvis du flytter et underordnet aktiv, og du vil gøre det til et selvstændigt aktiv uden strukturrelationer, skal du lade feltet **Overordnet aktiv** være tomt.
5. Feltet **Effektiv** er angives til den aktuelle dato og tidspunkt. Du kan dog vælge en anden dato og et andet klokkeslæt, som flytningen af aktivet skal være gyldig fra.
6. Vælg **OK**.

## <a name="replace-asset"></a>Erstat aktiv

Brug funktionen **Erstat aktiv** i forbindelse med reparationer, renovering eller permanent udskiftning af et udslidt aktiv med et nyt aktiv. Denne funktion bruges til at erstatte underordnede aktiver i en aktivstruktur. I forbindelse med overordnede aktiver (altså aktiver, der i øjeblikket ikke har et overordnet aktiv), udføres denne udskiftning på et arbejdssted. Du finder flere oplysninger om, hvordan du erstatter overordnede aktiver på et arbejdssted i [Installer aktiver på arbejdssteder](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Hvis et værksted er relateret til din produktionsafdeling, kan du oprette arbejdssteder såsom **Værksted**, **Skrot** og **Lager** til håndtering af reparationen og udskiftningen af aktiverne.

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**.
2. Du skal vælge det underordnede aktiv, der skal erstattes, på listen. Hvis aktivet har underordnede aktiver, erstatter du også disse aktiver.
3. Vælg **Erstat aktiv**.

    Feltet **Strukturændring** viser den seneste dato og tidspunkt for, hvor det valgte aktiv og de tilknyttede underordnede aktiver blev flyttet i aktivstrukturen.

4. I sektionen **Valgt aktiv** i feltet **Målarbejdssted** skal du vælge det arbejdssted, som du ønsker at flytte aktivet til. Vælg eksempelvis stedet **Værksted** eller **Skrot**.

    I sektionen **Overordnet aktiv** viser feltet **Effektiv** den seneste dato og tidspunkt for, hvornår det overordnede aktiv og de relaterede underordnede aktiver blev installeret eller flyttet over på det aktuelle arbejdssted.

5. I sektionen **Nyt aktiv** i feltet **Aktiv** skal du vælge det aktiv, der skal indsættes som en midlertidig eller permanent erstatning for det valgte aktiv. Dette aktiv kan i øjeblikket være placeret på et andet arbejdssted, såsom **Lager**.
7. I sektionen **Gyldig fra** angives som standard den aktuelle dato og tidspunkt i feltet **Gyldig**. Du kan dog vælge en anden dato og et andet klokkeslæt, som erstatningen af aktivet skal være gyldig fra.
8. Vælg **OK**.

## <a name="install-asset"></a>Installer aktiv

Brug funktionen **Installer aktiv** til at installere en aktivstruktur på et arbejdssted.

> [!NOTE]
> Vælg altid et overordnet aktiv. Det overordnede aktiv og de relaterede underordnede aktiver flyttes til det valgte arbejdssted.

1. Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver** eller **Aktive aktiver**.
2. Vælg det overordnede aktiv, du vil installere på et andet arbejdssted, på listen.
3. Vælg **Installer aktiv**.

    Sektionen **Attributter** viser de aktivattributter, der er angivet for det overordnede aktiv.

4. I feltet **Arbejdssted** vælges det nye sted.
5. Feltet **Effektiv** er angives til den aktuelle dato og tidspunkt. Du kan dog vælge en anden dato og et andet klokkeslæt, som installationen af aktivstrukturen skal være gyldig fra.
6. Vælg **OK**.
