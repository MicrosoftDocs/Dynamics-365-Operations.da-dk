---
title: Konfigurer momsrapporteringskoder
description: Momsrapporteringskoderne refererer til et feltnummer, der er angivet i en momsrapport.
author: twheeloc
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff5a5622fa63b6058b9e768f1fd1bc776a48962
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734833"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Konfigurer momsrapporteringskoder

[!include [banner](../../includes/banner.md)]

**Momsrapporteringskoder** refererer til et feltnummer, der er angivet i en momsrapport. De bruges i landespecifikke rapportlayout. De anvendes også i momsafregning pr. kode i rapport. Denne rapport viser momsbeløb for en opsummeringsperiode for hver enkelt rapporteringskode. Når du har oprettet **Momsrapporteringskoder**, kan du referere til disse koder i oversigtspanelet **Rapportopsætning**, som då får adgang til fra siden **Momskode**. 

Denne registrering anvender demofirmaet DEMF.

1. Gå i **Navigationsrude** til **Moms > Opsætning > Moms > Momsrapporteringskoder**.
2. Klik på **Ny**.
3. Vælg det rapportlayout, som rapporteringskoden hører til. Dette layout bruges til at filtrere de tilgængelige rapporteringskoder til en salgsmomskode. Hver salgsmomskode tilhører en afregningsperiode, der tilhører en momsmyndighed, som bruger et rapportlayout.  
4. Angiv et tal i feltet **Rapporteringskode**.
5. Angiv en beskrivelse, der skal vises i rapporter, i feltet **Rapporttekst**.
6. Angiv en beskrivelse til interne formål i feltet **Kort beskrivelse**.
7. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
