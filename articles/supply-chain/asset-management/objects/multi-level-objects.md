---
title: Aktiver på flere niveauer
description: Denne artikel forklarer, hvordan du opretter og sletter aktiver på flere niveauer.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b13db8b8b12aaef2e067f9a55eb8754333eb16b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017139"
---
# <a name="multi-level-assets"></a>Aktiver på flere niveauer

[!include [banner](../../includes/banner.md)]

 

Denne artikel forklarer, hvordan du opretter og sletter aktiver på flere niveauer. Du kan oprette aktiver og relaterede under aktiver i en hierarkisk træstruktur. På denne måde kan du vise relationer og afhængigheder mellem aktiver. Vedligeholdelsesjob kan relateres til alle niveauer i træstrukturen. Der kan også oprettes statistikker for et individuelt niveau eller en sum af alle niveauer for underaktiver.

På listesiden **Alle aktiver** (**Styring af aktiver** \> **Aktiver** \> **Alle aktiver**) viser kolonnen **Aktiver** aktiverne i hierarkisk orden. Kolonnen **Overordnet** viser den relaterede overordnede. Hvis der derudover allerede er oprettet aktiver og underaktiver, vises aktiverne i en træstruktur i sektionen **Aktivtræ** i ruden **Relaterede oplysninger**.

Du kan finde flere oplysninger om, hvordan du opretter et aktiv i [Opret et aktiv](../objects/create-an-object.md). Hvis du vil oprette et underaktiv, skal du vælge det overordnede aktiv i feltet **Overordnet aktiv** på oversigtspanelet **Generelt**.

## <a name="copy-an-asset-or-asset-structure"></a>Kopiér et aktiv eller en aktivstruktur

Hvis din virksomhed har flere ensartede aktivstrukturer, kan du bruge kopieringsfunktionen i Styring af aktiver til hurtigt at oprette dem.

1. Vælg **Styring af aktiver** \> **Aktiver** \> **Alle aktiver**.
2. På listesiden **Alle aktiver** skal du vælge, hvilket aktiv, der skal kopieres. Hvis du for eksempel vil kopiere hele aktivstrukturen, herunder underaktiver, skal du vælge et overordnet aktiv.
3. Vælg **Kopiér aktiv**. I sektionen **Kopiér fra** er feltet **Aktiv** angivet til det aktiv, du valgte på listesiden.
4. Angiv navnet på det nye aktiv i feltet **Aktiv** i sektionen **Kopiér til**.
5. Hvis det aktiv, du opretter, skal være en del af en eksisterende aktivstruktur, skal du i feltet **Aktiv** i sektionen **Overordnet aktiv** vælge et overordnet ID.
6. Vælg **OK**. Den nye aktivstruktur fremgår af listesiden **Alle aktiver**. Alle aktivattributter, vedligeholdelsesplaner og vedligeholdelsesrunder, der er relateret til det aktiv, du kopierede, overføres til det nye aktiv eller aktivstruktur.

Når du kopierer en aktivstruktur, har underaktiverne i den nye struktur samme navn som de underaktiver, du kopierede. Når kopieringsproceduren er fuldført, kan du nemt ændre navnet og andre indstillinger for et aktiv. Vælg aktivet på listesiden **Alle aktiver**, og vælg derefter knappen **Rediger**.

> [!NOTE]
> Når du kopierer et aktiv eller en aktivstruktur, nulstilles livscyklussen for de nye aktiver til den tilstand, du definerede som den oprindelige livscyklustilstand for aktiver. Arbejdsstedet nulstilles til arbejdsstedsstandarden.

## <a name="delete-an-asset-or-asset-structure"></a>Slet et aktiv eller en aktivstruktur

Hvis et aktiv har relaterede underaktiver, kan du kun slette det, hvis der ikke er registreret nogen vedligeholdelsesanmodninger, arbejdsordrejobs, fejlregistreringer eller tilstandsvurderinger på nogen af aktiverne.

1. På listesiden **Alle aktiver** skal du vælge, hvilket aktiv, der skal slettes.
2. Vælg **Slet**.

> [!NOTE]
> Hvis du ikke kan slette et aktiv ved hjælp af denne procedure, er en anden måde at håndtere sletningen på at konfigurere en livscyklustilstand for et aktiv til dette formål. Du kan eksempelvis konfigurere en **Kasseret** eller **Slettet** livscyklustilstand på siden **Livscyklustilstand for aktiv**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]