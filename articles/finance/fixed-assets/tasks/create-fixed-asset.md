---
title: Oprette et anlægsaktiv
description: Dette emne forklarer, hvordan du opretter en ny anlægsaktivpost fra listesiden med anlægsaktiver.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab330c604b2485687544a7d8b3eef3a652fa2069
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985131"
---
# <a name="create-a-fixed-asset"></a>Oprette et anlægsaktiv

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du opretter en ny anlægsaktivpost fra listesiden **Anlægsaktiv**.

Systemet tildeler aktivnummeret på basis af den nummerserie, der er tildelt anlægsaktivgruppen. Hvis du bruger skabelonen for anlægsaktiver til at importere aktiver via Microsoft Excel-tilføjelsesprogrammet, eller hvis du bruger et andet importjob, opretter systemet automatisk anlægsaktivposter og øger aktivnummeret.

Hvis du vil oprette en aktivpost manuelt, skal du følge disse trin.

1. Gå til **Navigationsrude \> Moduler \> Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.
2. Gå til **handlingsruden**, og vælg **Ny**.
3. Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**. Feltet **Nummer** bruges som standard, hvis du har aktiveret funktionen **Auto-nummerer anlægsaktiver** i **Anlægsaktivparametre** og **Anlægsaktivgruppe**. Hvis ikke skal du angive et entydigt nummer, der identificerer anlægsaktivet.
4. Angiv en værdi i feltet **Navn**. Angiv yderligere oplysninger, som din virksomhed skal bruge til dette anlægsaktiv.
5. Vælg **Bøger** i **handlingsruden**.
6. Angiv en dato i feltet **Anskaffelsesdato**.
7. Angiv et tal i feltet **Anskaffelsespris**.

    - Angiv yderligere oplysninger, som din virksomhed skal bruge til denne bog.
    - Angiv yderligere oplysninger, som din virksomhed skal bruge til resterende bøger.

8. Luk siden.

Du kan også importere anlægsaktiver ved hjælp af Excel-tilføjelsesprogrammet eller ved at køre et importjob fra arbejdsområdet **Dataadministration**. Før du kører importen, skal du angive værdierne for obligatoriske felter i skabelonen.

Hvis du ikke har defineret anlægsaktivnummeret i skabelonen for Excel-tilføjelsesprogrammet eller i Dataadministration, opretter systemet et anlægsaktivnummer for hvert importerede aktiv og øger automatisk nummerserien for hver enkelt. Men hvis du importerer aktiver og definerer aktivnumre i skabelonen, øger systemet **ikke** automatisk nummerserien. I dette tilfælde skal en administrator måske opdatere nummerserien manuelt. Hvis du har defineret anlægsaktivnummeret i skabelonen til Excel-tilføjelsesprogrammet, bruger systemet det definerede anlægsaktivnummer og øger nummerserien.

> [!NOTE]                                                                                                         
> Når afskrivningen er bogført, låses felterne **Placeret i tjeneste** og **Afskrivningsdato** på siden **Kartotek**. Både feltet vil heller ikke blive opdateret fra dataenheden.

> [!WARNING]
> Anlægsaktivposten slettes ikke, hvis der er bogført posteringer i det tilknyttede kartotek, eller hvis det netop oprettede anlægsaktiv er angivet på en kladdelinje, men ikke bogført. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]