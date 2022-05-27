---
title: Synkronisere dispositionskoder
description: Dette emne forklarer synkronisering af dispositionskoder for intern handel
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 27b587e576900f2b7f7fed7ee2a27a282306f0fe
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671752"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Synkronisere interne dispositionskoder

[!include [banner](../../includes/banner.md)]

For at understøtte interne returneringer giver Microsoft Dynamics 365 Supply Chain Management dig mulighed for at knytte dispositionskoder, der er defineret eksternt, til de tilsvarende interne dispositionskoder. Når der defineres en intern kæde, skal dispositionshandlingerne i de to firmaer, der er knyttet til hinanden, være de samme. Hvis de ikke er de samme, lykkes synkroniseringen ikke.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Om dispositionskoder ved trebenede direkte returneringer

Dispositionskoder synkroniseres fra den interne salgsordrelinje til den oprindelige salgsordrelinje. Synkronisering har dog kun én umiddelbar effekt på den oprindelige salgsordrelinje. Denne effekt er, at linjetillæg slettes på baggrund af dispositionskoden og det tillæg, der er defineret i firma A. Firma A er det firma, der opretter returordren.

I en trebenet direkte leverancekæde understøttes alle dispositionshandlinger på den interne salgsordrelinje. Hvis et produkt returneres til kunden, skal du dog bekræfte, at leveringsadressen i returordren svarer til kundens leveringsadresse, som er angivet i den oprindelige ordre.

> [!NOTE]
> Dispositionskoder findes ikke for indkøbsordrer. Synkronisering af dispositionskoder fra den interne salgsordre til den oprindelige salgsordre skal derfor ske fra salgsordre til salgsordre.

## <a name="replacing-returned-items"></a>Erstatte returvarer

Hvis en returvare erstattes, og der allerede er oprettet en erstatningsordre i firma B, kan en dispositionskode ikke vælges, og der oprettes ingen yderligere erstatningsordre i firma A.

## <a name="rules-for-intercompany-direct-deliveries"></a>Regler for direkte leveringer ved intern handel

Følgende generelle regler gælder for oprindelige returordrer i scenarier, der involverer direkte levering ved intern handel:

- Hvis den underliggende dispositionshandling på den oprindelige salgsordrelinje er Kredit og Kasseres, Kredit eller Returner til kunde, anvendes dispositionshandlingen Kredit. Men handlingskoden Returner til kunde angiver nettobeløbet til 0 (nul) på den eksisterende linje og på den linje, der netop er synkroniseret med salgsordren, ved den interne salgsordre. Derudover synkroniseres kassationslinjer aldrig. Når der føjes en linje til en intern salgsordre ved intern handel, synkroniseres den aldrig for en salgsordre, der indeholder et positivt antal og dispositionshandlingen Kassér (f.eks. Kredit og Kasseres eller Erstat og Kasseres).
- En underliggende dispositionshandling for Kredit og Erstat eller Kasseres og Erstat tilsidesættes ikke. Den behandles som en dispositionshandling for Kredit og Erstat eller Kasseres og Erstat. Denne regel gælder også, selvom der ikke er oprettet en kassationslinje i Firma A, og der ikke er oprettet en genanskaffelsesordre i Firma B (det firma, der modtager returvaren). En erstatningsordre oprettes kun i firma A, når der udføres en opdatering af følgesedlen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
