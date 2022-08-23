---
title: Tilsluttede programmer
description: Denne artikel beskriver, hvordan du konfigurerer tilsluttede programmer i elektronisk fakturering.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f908caa902e4747d324480e3a5108b443d385ea7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277325"
---
# <a name="connected-applications"></a>Tilsluttede programmer

[!include [banner](../includes/banner.md)]

Tilsluttede programmer er de forekomster af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management, som du muligvis vil have kontakt til via Regulatory Configuration Service (RCS). Via de tilsluttede programmer kan du konfigurere en del af funktionen Globalisering i Finans eller Supply Chain Management, så scenariet til elektronisk fakturering fungerer.

Når du implementerer funktionen Globalisering, kan de opsætningsoplysninger, der gælder for dit Finans- eller Supply Chain Management-program, udgives direkte fra RCS til det relevante tilsluttede program.

Det er nyttigt, at Finans- eller Supply Chain Management-parametrene er tilgængelige i RCS, når du har flere programmiljøer, f.eks. test af brugeraccept (UAT) og produktionsmiljøer, og du vil sikre, at opsætningen er konsistent ved at udrulle de samme parametre i forskellige miljøer.

## <a name="create-a-connected-application"></a>Opret en tilsluttet applikation.

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Elektronisk fakturering**.
3. På siden **Miljøopsætning** skal du vælge **Tilsluttede programmer** i handlingsruden.
4. Vælg **Ny** for at oprette en tilsluttet applikation.
5. Angiv navnet på den applikation, der skal tilsluttes i feltet **Navn**.
6. Vælg **Dynamics 365 Finance** i feltet **Type**.
7. Angiv URL-adressen til det miljø, der skal tilsluttes, i feltet **Program**.
8. Angiv miljøets lejer i feltet **Lejer**.
9. Vælg **Gem**.
10. Vælg **Check-forbindelse** i handlingsruden for at teste forbindelsen til miljøet. Luk derefter siden.

## <a name="link-connected-applications-to-environments"></a>Sammenkæd tilknyttede applikationer med miljøer

1. På siden **Miljøopsætning** skal du vælge **Ny** for at tildele et tilsluttet program til et miljø.
2. Vælg en tilsluttet applikation i feltet **Tilsluttet applikation**.
3. Vælg et servicemiljø i feltet **Servicemiljø**.
4. Vælg **Gem**, og luk derefter siden.
