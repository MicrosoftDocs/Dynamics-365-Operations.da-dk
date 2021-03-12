---
title: Angive standardbeskrivelser til automatisk bogføring
description: Dette emne forklarer, hvordan du kan konfigurere den standardtekst, der bruges til at beskrive de regnskabsposter, der bogføres automatisk i finans. Du kan angive standardbeskrivelsesteksten ved hjælp af en fritekst eller ved at vælge faste variabler.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1b73b104ed8a8a015cb97dcf3055a648cfb083d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994734"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Angive standardbeskrivelser til automatisk bogføring

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan konfigurere den standardtekst, der bruges til at beskrive de regnskabsposter, der bogføres automatisk i finans. Du kan angive standardbeskrivelsesteksten ved hjælp af en fritekst eller ved at vælge faste variabler.

> [!NOTE]
> For visse transaktionstyper kan du i nogle lande/områder medtage tekst fra felter i Microsoft Dynamics AX-databasen, der er relateret til disse transaktionstyper. Du kan finde en liste over transaktionstyperne og lande og områder i afsnittet [Valgfrit: Føje anden tekst til standardbeskrivelser](#optional-add-other-text-to-default-descriptions) senere i dette emne.

## <a name="set-up-default-descriptions"></a>Konfigurere standardbeskrivelser

1. Gå til **Virksomhedsadministration** \> **Opsætning** \> **Standardbeskrivelser**.
2. Gå til handlingsruden, og vælg **Ny**.
3. I feltet **Beskrivelse** skal du vælge den type transaktion, der skal oprettes en standardbeskrivelse til.
4. I feltet **Sprog** skal du vælge det sprog, som denne beskrivelse gælder for.
5. Indtast standardbeskrivelsen i feltet **Tekst**. Du kan skrive tekst i feltet, eller du kan bruge en eller flere af følgende fritekstvariabler:

    - **%1** – Tilføj transaktionsdatoen.
    - **%2** – Tilføj en identifikator, der svarer til den dokumenttype, der bogføres i finansmodulet. I forbindelse med transaktionstyper, der er knyttet til fakturaer, tilføjer variablen **%2** f.eks. fakturanummer.
    - **%3** – Tilføj en identifikator, der er relateret til den dokumenttype, der bogføres i finansmodulet. I forbindelse med transaktionstyper, der er knyttet til fakturaer, tilføjer variablen **%3** f.eks. debitorkontonummer.

## <a name="optional-add-other-text-to-default-descriptions"></a>Valgfrit: Føje anden tekst til standardbeskrivelser

For visse transaktionstyper kan du i nogle lande/områder medtage tekst i standardbeskrivelser, der kommer fra felter i dine data, der er relateret til disse transaktionstyper. Følgende lister viser de transaktionstyper og lande/områder, hvor denne indstilling er tilgængelig.

**Posteringstyper**

Du kan føje anden tekst til standardbeskrivelser for transaktionstyper, der vedrører følgende dokumenttyper:

- Debitorfakturaer
- Kreditnotaer til kunden
- Debitorkontantbetalinger
- Kreditorbetalinger
- Salgsordrer
- Indkøbsordrer
- Lagerkladder
- Varedisponering
- Anlægsaktiver

**Lande og områder**

Denne indstilling er kun tilgængelig for følgende lande og områder:

- Brasilien
- Kina
- Tjekkiet
- Østeuropa
- Ungarn
- Indien
- Japan
- Litauen
- Letland
- Polen
- Rusland

### <a name="add-text-to-default-descriptions"></a>Føje tekst til standardbeskrivelser

Når du har fuldført trinnene i afsnittet [Konfigurere standardbeskrivelser](#set-up-default-descriptions) tidligere i dette emne, skal du følge disse trin for at føje anden tekst til standardbeskrivelserne.

1. Vælg **Tilføj** i oversigtspanelet **Parametre**.
2. I feltet **Referencetabel** skal du vælge den databasetabel, hvorfra der skal føjes parameterdata til beskrivelsen.
3. I feltet **Referencefelt** skal du vælge det felt, hvorfra der skal føjes parameterdata til beskrivelsen.
4. Gentag trin 1-3 for at tilføje flere parametre.
