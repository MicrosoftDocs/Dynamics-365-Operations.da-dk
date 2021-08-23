---
title: Modul for indtjekning ved afhentning
description: Dette emne omhandler modulet for indtjekning ved afhentning og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f6359f41f3b97325db4fda083dc32d39839811297a96a1f2d99a93990c00afae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747459"
---
# <a name="check-in-for-pickup-module"></a>Modul for indtjekning ved afhentning

[!include [banner](includes/banner.md)]

Dette emne omhandler modulet for indtjekning ved afhentning og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.

Modulet for indtjekning ved afhentning indeholder en bekræftelsesside til kunder, der bruger Dynamics 365 Commerce-funktionerne til kunders indtjekning for at underrette en butik om deres ankomst. Med modulet for indtjekning ved afhentning kan du også konfigurere en formular, der indsamler yderligere oplysninger fra kunder for at lette ordreleveringen. Disse oplysninger omfatter en kundes parkeringspladssnummer samt mærke og model for kundens køretøj. 

## <a name="module-properties"></a>Modulegenskaber

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Bekræftelsestekst | Tekststreng | Indhold til den overskrift, som vises på siden for bekræftelse af indtjekning. |
| Vis QR-kode | **Sand** eller **Falsk** | Når denne egenskab er angivet til **Sand**, viser siden til bekræftelse af indtjekning en QR-kode, der repræsenterer ordrebekræftelsens id. |
| Overskrift for yderligere oplysninger | Tekststreng | Indhold til den overskrift, der vises, når der er konfigureret felter til yderligere oplysninger. |
| Nøgler for yderligere oplysninger | Par af ressource-id/ressourceværdi | Hver nøgle opretter et formularfelt og en tilknyttet etiket, der bruges til at indsamle yderligere oplysninger fra kunder. |
| Nøgler for yderligere oplysninger \> Ressource-id | Tekststreng | Hver oplysningsnøgle opretter et formularfelt og en tilknyttet etiket, der bruges til at indsamle yderligere oplysninger fra kunder. Denne egenskab identificerer nøglen for yderligere oplysninger. I den opgave, der er oprettet i POS, vises værdien for denne egenskab som etiketten i instruktionsfeltet. |
| Nøgler for yderligere oplysninger \> Ressourceværdi | Tekststreng | Etiketten for tekstfeltet i opgaven i POS. |
| Nøgler for yderligere oplysninger \> Påkrævet | **Sand** eller **Falsk** | Denne egenskab angiver, om debitorerne skal udfylde formularfeltet, før de kan fortsætte. Når denne egenskab er angivet til **Sand**, vises en stjerne ved siden af formularetiketten, og der udføres en null-kontrol for at forhindre debitorer i at fortsætte, hvis der ikke er angivet en værdi. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Føje modulet for indtjekning ved afhentning til en side

Modulet for indtjekning ved afhentning skal føjes til den nye side, som du opretter til bekræftelse af indtjekning. Denne side fungerer som bekræftelse af indtjekning for kunder, der vælger linket **Jeg er her** eller knappen i deres mail. 

## <a name="configure-the-additional-information-form"></a>Konfigurere formularen til yderligere oplysninger

Hvis der ikke er konfigureret nøgler for yderligere oplysninger, får kunderne som standard vist modulet for bekræftelse af indtjekning. Når bekræftelsen af indtjekning vises, oprettes der en opgave i POS for den butik, hvor ordren afhentes.

Når der er konfigureret en eller flere nøgler for yderligere oplysninger, bliver kunderne først bedt om at angive oplysninger. Når de vælger **Send**, vises bekræftelsen af indtjekning, og der oprettes en opgave i POS. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Aktivere beskeder om kunders indtjekning i POS](enable-customer-check-in.md)
