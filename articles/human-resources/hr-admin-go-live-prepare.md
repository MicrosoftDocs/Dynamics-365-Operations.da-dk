---
title: Forberedelse af udgivelse med Human Resources
description: Denne side indeholder en vejledning i, hvordan du kan forberede en udgivelse med Dynamics 365 Human Resources.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ece4875b69d3cf797ab90e54f0cc0fda317cc931
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359647"
---
# <a name="prepare-for-human-resources-go-live"></a>Forberedelse af udgivelse med Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du kan forberede en udgivelse af et Dynamics 365 Human Resources-projekt ved hjælp af Microsoft Dynamics Lifecycle Services (LCS). 

Denne grafik viser faserne i udgivelsesprocessen. 

![Udgivelsesproces.](./media/hr-admin-go-live-prepare-process.png)

I følgende tabel vises alle trinnene i processen, den forventede varighed og hvem, der er ansvarlig for aktionen.

| Fase | Handling | Varighed/hvornår | Hvem | Noter |
| --- | --- | --- | --- |--- |
| 1 | Opdatere udgivelsesdato i LCS | Senest 2-3 måneder forinden | Partner/kunde | Milepælsdatoerne skal holdes opdateret løbende. |
| 2 | Fuldføre og sende tjekliste | Når test af brugeraccept (UAT) er fuldført | Partner/kunde | Følg instruktionerne i [Udgivelsesvurdering med FastTrack](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projektvurdering (FastTrack) | FastTrack-arkitekt* | Arkitekten leverer en vurdering, når tjeklisten er modtaget, og fortsætter gennemgangen, indtil eventuelle spørgsmål er besvaret, og afhjælpninger er udført. |
| 4 | Projektworkshop (FastTrack) | FastTrack-arkitekt* | |
| 5 | Import af datapakke | Afhænger af projektet | Partner/kunde | Følg instruktionerne i [Oversigt over datastyring](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).|
| 6 | Produktionsklar | Når alle foregående trin er fuldført | Partner/kunde | Partner/kunde kan overtage styringen med produktionsmiljøet.|
| 7 | Efterkalkulationsaktiviteter | Afhænger af projektet | Partner/kunde | |
| 8 | Udgivelse | Afhænger af projektet | Kunde | |

> [!IMPORTANT]
> *Trin 3 og 4 fuldføres kun for kunder, der er berettiget til FastTrack.

## <a name="completing-the-lcs-methodology"></a>Fuldførelse af LCS-metoden

En stor milepæl i hvert implementeringsprojekt er overgangen (cutover) til produktionsmiljøet. Fuldførelsen af et trin består af to dele: 

- Udfør det faktiske arbejde, f.eks. en fit-gab-analyse eller test af brugeraccept (UAT). 
- Markér det tilsvarende trin i LCS-metoden som fuldført. 

Det er en god ide at udføre trinnene i metoden, efterhånden som implementeringen skrider frem. Vent ikke til sidste øjeblik. Det er naturligvis i kundens interesse, at implementeringen udføres korrekt. 

## <a name="uat-for-your-solution"></a>Test af brugeraccept (UAT) af løsningen

Under UAT-fasen skal du teste alle de forretningsprocesser, du har implementeret, og alle de tilpasninger, du har foretaget, i et sandkassemiljø i implementeringsprojektet. Du skal overveje følgende, når du fuldfører UAT-fasen, for at sikre, at udgivelsen udføres korrekt: 

- Det anbefales, at UAT-processen begynder med et rent og nyt miljø, hvor dataene fra DIN GOLD-konfiguration kopieres til miljøet, før UAT-processen startes. Det anbefales, at du bruger produktionsmiljøet som GULD-miljø, indtil du går i gang med at producere på et bestemt tidspunkt.
- Testsager omfatter alle krav. 
- Test ved hjælp af overførte data. Dette skal omfatte data som f.eks. arbejdere, job og stillinger. Medtag også startsaldi, f.eks. orlovs- og fraværsperiodiseringer. Endelig skal du inkludere åbne posteringer, f.eks. aktuelle tilmeldinger til frynsegoder. Fuldfør testen med alle typer data, også selvom datasættet ikke er færdiggjort. 
- Test ved hjælp af de korrekte sikkerhedsroller (standardroller og brugerdefinerede roller), der er tildelt til brugere. 
- Sørg for, at løsningen overholder alle firma- og branchespecifikke lovgivningsmæssige krav. 
- Dokumenter alle funktioner, og få godkendelser fra kunden. 

## <a name="mock-go-live"></a>Go-live-test

Før du går i gang, skal du udføre en go-live-test for at teste de trin, der er nødvendige for at ændre eksisterende systemer til det nye system. Du skal udføre din go-live i et sandkassemiljø og medtage alle trin i overgangsplanen.

- Det anbefales, at du bruger produktionsmiljøet som GOLD-konfigurationsmiljø, indtil det går i gang.
- Sørg for, at du har en effektiv styringsproces på plads for at beskytte produktionsmiljøet mod utilsigtede posteringer eller opdateringer før opdateringen.
- Når du er klar til at udføre UAT eller go-live, skal du opdatere sandkassemiljøet fra produktionsmiljøet. Yderligere oplysninger finder du i [Kopiér en forekomst](hr-admin-setup-copy-instance.md).
- Test hvert trin i din overgangsplan i sandkassemiljøet, og valider derefter sandkassemiljøet ved at udføre kontroller på stedet eller udføre test fra UAT-scriptene i miljøet.
  - Test bør omfatte alle dataoverflytninger, herunder de transformationer, der skal bruges til udgivelse.
  - Processen skal omfatte en overgang i praksis af ældre systemer.
  - Sørg for at medtage eventuelle trin i integrationsovergangen eller eksterne systemtrin i din overgang.
- Hvis du oplever problemer i forbindelse med overgangen, kan der blive brug for endnu en overgang. Derfor anbefales det, at du planlægger to overgange i projektplanen.

## <a name="fasttrack-go-live-assessment"></a>Udgivelsesvurdering med FastTrack

Kunder, der er kvalificerede til FastTrack og bruger en FastTrack-løsningsarkitekt, skal fuldføre en udgivelsesgennemgang med Microsoft FastTrack. Du kan finde flere oplysninger i  [Microsoft FastTrack](/dynamics365/fasttrack/). 

Cirka otte uger før udgivelsen beder FastTrack-teamet dig om at udfylde en [Kontrolliste før udgivelse](https://go.microsoft.com/fwlink/?linkid=2146013).

Projektlederen eller et ledende projektmedlem skal udfylde kontrollisten i fasen før udgivelsen af projektet. Kontrollisten fuldføres typisk fire til seks uger før den foreslåede udgivelsesdato, når UAT er fuldført eller næsten er fuldført. 

Når du har fuldført kontrollisten, skal du sende den via e-mail til din FastTrack-løsningsarkitekt. Medtag altid en primær interessent fra kunden og implementeringspartneren i e-mailen. 

Når du har sendt kontrollisten, gennemgår FastTrack-løsningsarkitekten projektet og giver en vurdering med en beskrivelse af de potentielle risici, de bedste fremgangsmåder og anbefalinger til, hvordan projektudgivelsen kan lykkes. I nogle tilfælde kan løsningsarkitekten fremhæve risikofaktorer og bede om en afhjælpningsplan. 

## <a name="see-also"></a>Se også

[Ofte stillede spørgsmål om udgivelse](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
