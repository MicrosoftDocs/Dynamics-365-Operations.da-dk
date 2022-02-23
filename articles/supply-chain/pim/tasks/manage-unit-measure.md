---
title: Administrere måleenhed
description: Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8d9b6f18fdc1c47d6a695ca6a2330f6f02fc1bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424484"
---
# <a name="manage-unit-of-measure"></a>Administrere måleenhed

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder. Du kan gennemgå denne procedure ved at bruge demodataene eller dine egne data.

1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Vedligeholdelse af frigivet produkt**.
2. Klik på **Enheder**.

## <a name="create-a-unit-of-measure"></a>Opret en måleenhed
1. Klik på **Ny**.
2. I feltet **Enhed** skal du angive en værdi. Angiv det id eller symbol, der skal bruges i forbindelse med måleenheden.  
3. Indtast en værdi i feltet **Beskrivelse**. Indtast et beskrivende navn for måleenheden i systemsproget.  
4. I feltet **Enhedsklasse** skal du vælge en indstilling. Enhedsklassen definerer, hvilken logisk gruppering, f.eks. område, masse eller mængde, måleenheden er del af.  
5. I feltet **Decimalpræcision** skal du indtaste et tal. Angiv antallet af decimaler, som den omregnede måleenhed skal afrundes til, når der er fuldført en beregning for måleenheden.  
6. Klik på **Gem**.

## <a name="define-unit-translations"></a>Definer enhedsoversættelser
1. Klik på **Enhedstekster** i **Handlingsrude**.
2. Klik på **Ny**. Brug enhedstekst til at oprette en oversættelse af id'et eller et symbol, der repræsenterer måleenheden, til brug på eksterne dokumenter på debitor- eller kreditorspecifikke sprog.  
3. I feltet **Sprog** skal du indtaste eller vælge en værdi.
4. I feltet **Tekst** skal du indtaste en værdi.
5. Klik på **Gem**.
6. Luk siden.
7. Klik på **Oversatte enhedsbeskrivelser** i **Handlingsrude**.
8. Klik på **Ny**. Definer sprogspecifikke beskrivelser af måleenheden.  
9. I feltet **Sprog** skal du indtaste eller vælge en værdi.
10. Indtast en værdi i feltet **Beskrivelse**.
11. Klik på **Gem**.
12. Luk siden.

## <a name="define-unit-conversion-rules"></a>Definer omregningsregler for enhed
1. Klik på **Enhedsomregninger** i **Handlingsrude**. Definer regler for konvertering af måleenheden til og fra andre enheder i den valgte enhedsklasse.  
2. Klik på **Ny** for at åbne dialogboksen Fjern.
3. Angiv et tal i feltet **Faktor**. Omregningsfaktor mellem Fra enhed og Til enhed. Omregningsfaktoren fra centimeter til meter er f.eks. 100, fordi der går 100 centimeter på 1 meter.  
4. Indtast eller vælg en værdi i feltet **Til enhed**.
5. Vælg en indstilling i feltet **Afrunding**. Definer, hvordan den omregnede værdi skal afrundes.  
6. Klik på **OK**.
7. Luk siden.

