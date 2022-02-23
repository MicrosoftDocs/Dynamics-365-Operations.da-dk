---
title: Integrere aktivstyring med anlægsaktiver
description: I dette emne forklares det, hvordan du kan integrere aktivstyrings- og anlægsaktivmoduler, så anlægsaktiver kan knyttes til vedligeholdelsesaktiver.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424519"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Integrere aktivstyring med anlægsaktiver

[!include [banner](../../includes/banner.md)]

Hvis du integrerer **Aktivstyring**- og **Anlægsaktiv**-moduler, kan du knytte anlægsaktiver til vedligeholdelsesaktiver. Brugere med anlægsaktiver kan derefter oprette et vedligeholdelsesaktiv ud fra et nyt eller eksisterende anlægsaktiv, og brugere af aktivstyring kan knytte et vedligeholdelsesaktiv til et eksisterende anlægsaktiv. Denne funktion gør det også nemt for brugere med anlægsaktiver at få vist de omkostninger, der blev bogført fra arbejdsordrer for relaterede vedligeholdelsesaktiver.

> [!NOTE]
> I dette emne refererer *vedligeholdelsesaktiver* til aktiver fra modulet **Aktivstyring**, og *anlægsaktiver* henviser til aktiver fra modulet **Anlægsaktiver**.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Angive en standardplacering for nye vedligeholdelsesaktiver, der oprettes ud fra anlægsaktiver (valgfrit)

Med denne valgfrie konfiguration kan du angive en standardarbejdssted for nye vedligeholdelsesaktiver, der oprettes ud fra anlægsaktiver. Du udfører typisk denne konfiguration kun én gang, hvis du overhovedet fuldfører den.

Benyt denne fremgangsmåde for at fuldføre konfigurationen.

1. Gå til **Aktivstyring \> Opsætning \> Parametre til aktivstyring**.
1. Under fanen **Anlægsaktiver** i feltet **Arbejdssted** skal du vælge standardstedet.
1. Vælg **Gem** i handlingsruden.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Arbejde med integrerede vedligeholdelsesaktiver og anlægsaktiver

Dette afsnit indeholder en samling procedurer, der viser forskellige måder, du kan arbejde med funktionerne til integreret styring af aktiver og anlægsaktiver på.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Knytte et eksisterende vedligeholdelsesaktiv til et anlægsaktiv

Knyt et eksisterende vedligeholdelsesaktiv til et anlægsaktiv ved at følge disse trin.

1. Gå til **Styring af aktiver \> Aktiver \> Alle aktiver** (eller **Aktive aktiver**).
1. Vælg et aktiv.
1. I oversigtspanelet **Anlægsaktiv** skal du vælge et eksisterende anlægsaktiv i feltet **Nummer på anlægsaktiv**.
1. Vælg **Gem** i handlingsruden.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Se det anlægsaktiv, der er tilknyttet et valgt vedligeholdelsesaktiv

Du kan se det anlægsaktiv, der er tilknyttet et valgt vedligeholdelsesaktiv, ved at følge disse trin.

1. Gå til **Styring af aktiver \> Aktiver \> Alle aktiver** (eller **Aktive aktiver**).
1. Vælg et aktiv.
1. I oversigtspanelet **Anlægsaktiv** skal du vælge linket i feltet **Nummer på anlægsaktiv**.

    Siden **Anlægsaktiver** for det valgte aktiv åbnes. (Denne side findes typisk på **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**).

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Se det vedligeholdelsesaktiv, der er tilknyttet et valgt anlægsaktiv

Du kan se det vedligeholdelsesaktiv, der er tilknyttet et valgt anlægsaktiv, ved at følge disse trin.

1. Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.
1. Vælg et aktiv.
1. Vælg **Vedligeholdelsesaktiv** i gruppen **Vis** under fanen **Styring af aktiver** i handlingsruden.

    Siden **Vedligeholdelsesaktiv** for det aktiv, der er tilknyttet det valgte anlægsaktiv, åbnes. (Denne side findes typisk på **Styring af aktiver \> Aktiver \> Alle aktiver**).

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Se vedligeholdelsesomkostninger, der er tilknyttet et anlægsaktiv

Arbejdsordrer for aktivstyring kan bogføres for vedligeholdelsesaktiver, og hver af disse arbejdsordrer har normalt en omkostning. Når et anlægsaktiv er tilknyttet et vedligeholdelsesaktiv, kan du gå direkte fra anlægsaktivet for at få vist de relaterede omkostninger.

Du kan se de vedligeholdelsesomkostninger, der er tilknyttet et valgt anlægsaktiv, ved at følge disse trin.

1. Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.
1. Vælg et aktiv.
1. Vælg **Vedligeholdelsesomkostning** i gruppen **Vis** under fanen **Styring af aktiver** i handlingsruden.

    Siden **Vedligeholdelsesomkostning** åbnes og viser de relaterede omkostninger.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Oprette et nyt vedligeholdelsesaktiv til et eksisterende anlægsaktiv

Opret et nyt vedligeholdelsesaktiv til et eksisterende anlægsaktiv ved at følge disse trin.

1. Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.
1. Vælg et aktiv.
1. Vælg **Opret vedligeholdelsesaktiv** i gruppen **Nyt** under fanen **Styring af aktiver** i handlingsruden. (Hvis denne indstilling ikke er tilgængelig, er et vedligeholdelsesaktiv muligvis allerede knyttet til det valgte anlægsaktiv).
1. Afslut oprettelsen af aktivet som beskrevet under [Oprette et aktiv](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Oprette et nyt anlægsaktiv og føje et eksisterende vedligeholdelsesaktiv til det

Opret et nyt anlægsaktiv, og føj et nyt vedligeholdelsesaktiv til det ved at følge disse trin.

1. Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Afslut oprettelsen af anlægsaktivet som beskrevet under [Oprette et anlægsaktiv](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. Vælg **Opret vedligeholdelsesaktiv** i gruppen **Nyt** under fanen **Styring af aktiver** i handlingsruden.
1. Afslut oprettelsen af aktivet som beskrevet under [Oprette et aktiv](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>Fjerne tilknytningen mellem to aktiver

I nogle tilfælde kan det være nødvendigt at fjerne tilknytningen mellem et vedligeholdelsesaktiv og dets anlægsaktiv. Hvis du f.eks. vil [oprette et nyt vedligeholdelsesaktiv](#new-maintenance-from-fixed) ud fra et anlægsaktiv, skal du først fjerne en eksisterende tilknytning.

Fjern en eksisterende tilknytning mellem et vedligeholdelsesaktiv og et anlægsaktiv ved at følge disse trin.

1. Gå til **Styring af aktiver \> Aktiver \> Alle aktiver** (eller **Aktive aktiver**).
1. Find og åbn anlægsaktivet.
1. I oversigtspanelet **Anlægsaktiv** skal du fjerne værdien fra feltet **Arbejdssted**.
1. Vælg **Gem** i handlingsruden.
