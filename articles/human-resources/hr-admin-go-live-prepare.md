---
title: Forberedelse af udgivelse med Human Resources
description: Denne side indeholder en vejledning i, hvordan du kan forberede en udgivelse med Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011407"
---
# <a name="prepare-for-human-resources-go-live"></a>Forberedelse af udgivelse med Human Resources

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du kan forberede en udgivelse af et Dynamics 365 Human Resources-projekt ved hjælp af Microsoft Dynamics Lifecycle Services (LCS). 

Denne grafik viser faserne i udgivelsesprocessen. 

![Udgivelsesproces](./media/hr-admin-go-live-prepare-process.png)

I følgende tabel vises alle trinnene i processen, den forventede varighed og hvem, der er ansvarlig for aktionen.

| Fase | Handling | Varighed/hvornår | Hvem | Noter |
| --- | --- | --- | --- |--- |
| 1 | Opdatere udgivelsesdato i LCS | Senest 2-3 måneder forinden | Partner/kunde | Milepælsdatoerne skal holdes opdateret løbende. |
| 2 | Fuldføre og sende tjekliste | Når test af brugeraccept (UAT) er fuldført | Partner/kunde | Følg instruktionerne i [Udgivelsesvurdering med FastTrack](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projektvurdering (FastTrack) | FastTrack-arkitekt* | Arkitekten leverer en vurdering, når tjeklisten er modtaget, og fortsætter gennemgangen, indtil eventuelle spørgsmål er besvaret, og afhjælpninger er udført. |
| 4 | Projektworkshop (FastTrack) | FastTrack-arkitekt* | |
| 5 | Import af datapakke | Afhænger af projektet | Partner/kunde | Følg instruktionerne i [Oversigt over datastyring](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).|
| 6 | Produktionsklar | Når alle foregående trin er fuldført | Partner/kunde | Partner/kunde kan overtage styringen med produktionsmiljøet.|
| 7 | Efterkalkulationsaktiviteter | Afhænger af projektet | Partner/kunde | |
| 8 | Udgivelse | Afhænger af projektet | Kunde | |

> [!IMPORTANT]
> *Trin 3 og 4 fuldføres kun for kunder, der er berettiget til FastTrack.

## <a name="completing-the-lcs-methodology"></a>Fuldførelse af LCS-metoden

En stor milepæl i hvert implementeringsprojekt er overgangen (cutover) til produktionsmiljøet. 

For at hjælpe med at sikre, at produktionsmiljøet bruges i forbindelse med udgivelseshandlinger, klargør Microsoft først produktionsinstansen, når implementeringen nærmer sig **driftsfasen** , når de nødvendige aktiviteter i LCS-metoden er fuldført. Yderligere oplysninger om miljøerne i dit abonnement finder du i  [licensvejledningen til Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544). 

Kunder skal fuldføre **analyse** -, **design- og udviklings** - og **test** -faserne i LCS-metoden, før knappen  **Konfigurer** , der bruges til at anmode om produktionsmiljøet, bliver tilgængelig. Når du vil fuldføre en fase i LCS, skal du først fuldføre alle nødvendige trin i den pågældende fase. Når alle trinene i en fase er fuldført, kan du fuldføre hele fasen. Du kan altid genåbne en fase senere, hvis du skal foretage ændringer. Du kan finde flere oplysninger i  [Lifecycle Services (LCS) til Finance and Operations-appskunder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs). 

Fuldførelsen af et trin består af to dele: 

- Udfør det faktiske arbejde, f.eks. en fit-gab-analyse eller test af brugeraccept (UAT). 
- Markér det tilsvarende trin i LCS-metoden som fuldført. 

Det er en god ide at udføre trinnene i metoden, efterhånden som implementeringen skrider frem. Vent ikke til sidste øjeblik. Du skal ikke blot klikke gennem alle trinene, så du kan komme frem til et produktionsmiljø. Det er naturligvis i kundens interesse, at implementeringen udføres korrekt. 

## <a name="uat-for-your-solution"></a>Test af brugeraccept (UAT) af løsningen

Under UAT-fasen skal du teste alle de forretningsprocesser, du har implementeret, og alle de tilpasninger, du har foretaget, i et sandkassemiljø i implementeringsprojektet. Du skal overveje følgende, når du fuldfører UAT-fasen, for at sikre, at udgivelsen udføres korrekt: 

- Testsager omfatter alle krav. 
- Test ved hjælp af overførte data. Disse data skal omfatte masterdata som f.eks. arbejdere, job og stillinger. Medtag også startsaldi, f.eks. orlovs- og fraværsperiodiseringer. Endelig skal du inkludere åbne posteringer, f.eks. aktuelle tilmeldinger til frynsegoder. Fuldfør testen med alle typer data, også selvom datasættet ikke er færdiggjort. 
- Test ved hjælp af de korrekte sikkerhedsroller (standardroller og brugerdefinerede roller), der er tildelt til brugere. 
- Sørg for, at løsningen overholder alle firma- og branchespecifikke lovgivningsmæssige krav. 
- Dokumenter alle funktioner, og få godkendelser fra kunden. 

## <a name="fasttrack-go-live-assessment"></a>Udgivelsesvurdering med FastTrack

Kunder, der er kvalificerede til FastTrack og bruger en FastTrack-løsningsarkitekt, skal fuldføre en udgivelsesgennemgang med Microsoft FastTrack. Du kan finde flere oplysninger i  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Cirka otte uger før udgivelsen beder FastTrack-teamet dig om at udfylde en [Kontrolliste før udgivelse](https://go.microsoft.com/fwlink/?linkid=2146013).

Projektlederen eller et ledende projektmedlem skal udfylde kontrollisten i fasen før udgivelsen af projektet. Kontrollisten fuldføres typisk fire til seks uger før den foreslåede udgivelsesdato, når UAT er fuldført eller næsten er fuldført. 

Når du har fuldført kontrollisten, skal du sende den via e-mail til din FastTrack-løsningsarkitekt. Medtag altid en primær interessent fra kunden og implementeringspartneren i e-mailen. 

Når du har sendt kontrollisten, gennemgår FastTrack-løsningsarkitekten projektet og giver en vurdering med en beskrivelse af de potentielle risici, de bedste fremgangsmåder og anbefalinger til, hvordan projektudgivelsen kan lykkes. I nogle tilfælde kan løsningsarkitekten fremhæve risikofaktorer og bede om en afhjælpningsplan. 

## <a name="see-also"></a>Se også

[Ofte stillede spørgsmål om udgivelse](hr-admin-go-live-faq.md)