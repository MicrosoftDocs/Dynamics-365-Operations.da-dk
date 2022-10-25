---
title: Udgivelsesproces og udgivelseshistorik for planlægningsoptimering
description: Denne artikel indeholder oplysninger om frigivelsesprocessen og frigivelseshistorikken for Planlægningsoptimering.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682554"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Frigivelsesproces og frigivelseshistorik for Planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Microsoft opdaterer Planlægningsoptimering på månedsbasis. Men på baggrund af forretningsbehov frigiver vi fra tid til anden flere opdateringer mellem de planlagte frigivelser.

Hver frigivelse udgives i de individuelle områder, hvor Planlægningsoptimering er tilgængelig. Det tager typisk tre dage at behandle processen.

Mens Planlægningsoptimering opdateres, kan varedisponering køre en smule langsommere end normalt.

Miljøer, der bruger Planlægningsoptimering, modtager automatisk den seneste version. Der kræves ingen brugerhandling: Tjenesten opdateres automatisk. Men ingen større funktionsændring overføres automatisk til miljøer. Ændringer, der betragtes som større, er som standard deaktiverede, og de skal aktiveres direkte ved hjælp af [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Derfor vil ændringerne ikke blive vist i miljøet, før du har aktiveret dem.

Da der ikke vises beskeder, når Planlægningsoptimering opdateres i dit miljø, kan du gennemse produktbemærkningerne i følgende tabel for at finde ud af, hvornår ændringerne blev frigivet, og hvilke funktioner de introducerede. Denne tabel viser de ændringer, der er frigivet til Planlægningsoptimering, om disse ændringer er knyttet til en funktion fra funktionsstyring og datoen for frigivelsen.

| Ændringer | Detaljer om funktionsstyring | Udstedelsesdatoer |
|---|---|---|
| <p>[Batchdispositionskoder](../../inventory/batch-disposition-codes.md)</p><p>Medtage parametre for disponibel lagerbeholdning og lagertransaktion i behovsplaner</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet</p> | Der kræves ingen funktionsstyring | 10.- 14. oktober 2022 |
| <p>[Ressourcer, der er planlagt med kapacitetsbegrænsning](finite-capacity.md)</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet</p> | Der kræves ingen funktionsstyring | 19. - 23. september 2022 |
| Generelle forbedringer af ydeevne, kvalitet og stabilitet | Der kræves ingen funktionsstyring | 29. august - 3. september 2022 |
| <p>[Vedligeholdelse af centraliseret kalender](../supply-chain-calendars-master-planning.md)</p><p>[Forslag til optimering af eksisterende forsyning](../action-messages.md)</p><p>[Understøttelse af underleverandørarbejde](../../production-control/manage-subcontract-work-production.md)</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet</p> | Der kræves ingen funktionsstyring | 7.-11. marts 2022 |
| Understøttelse af planlægningsprioritet for produktionsordrer | Tilgængelig i version 10.0.25 som en del af funktionen med navnet *Prioritetsstyret MRP-understøttelse for planlægningsoptimering*. | 12. - 18. november 2021 |
| Generelle forbedringer af ydeevne, kvalitet og stabilitet | Der kræves ingen funktionsstyring | 12. - 18. november 2021 |
| <p>Understøttelse af beregningsformler til procestid, produktionsrute med overlap og produktionsoperationsnummer på behovsposteringer</p><p>Bedre fejlmeddelelser for produktionsplanlægning, der er knyttet til timeout, kapacitet blev ikke fundet og cyklisk rute</p><p>Forbedret konsistens ved beregning af tilgangsdatoer og afgangsdatoer på både ordreforslag og autoriserede ordrer</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet</p> | Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering* | 22.- 27. oktober 2021 |
| <p>Understøttelse af overvejelser om spildprocent ved beregning af procestid</p><p>Understøttelse af operationsnummer og materialeforbrug under planlægning</p> | Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering* | 5.- 7. oktober 2021 |
| <p>Understøttelse af jobtyper til produktionsrute: **Kø før**, **Kø efter** og **Transporttid**</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet</p> | Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering* | 25. - 30. september 2021 |
| <p>Understøttelse af behovsplaner, hvor **Planlægningsmetode** er indstillet til *Grovplanlægning*</p><p>På siden **Rutegrupper** skal du markere indstillingerne af afkrydsningsfelterne **Aktivering**, **Arbejdstid** og **Kapacitet** for rækker med **Rute-/jobtype** som *Opsætning* eller *Proces* </p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet</p> | <p>Grovplanlægning er tilgængelig i funktionsstyring fra og med version 10.0.20</p><p>Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering*</p> | 9. - 17. september 2021 |
| Generelle forbedringer af ydeevne, kvalitet og stabilitet | Der kræves ingen funktionsstyring | 25 - 30 august 2021 |
| <p>Har tilføjet feltet **Leveringstid** til ordreforslag.</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet.</p> | Der kræves ingen funktionsstyring | 12 - 17 august 2021 |
| <p>Tilføjet ressourcetypekrav for planlægning med ubegrænset kapacitet</p><p>Forbedret ressourceeffektivitet og kalendereffektivitet for planlægning med ubegrænset kapacitet</p><p>Yderligere oplysninger finder du under [Planlægning med ubegrænset kapacitet](infinite-capacity-planning.md)</p> | <p>Tilgængelig i funktionsstyring fra og med version 10.0.20</p><p>Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering*</p> | 6 - 12 juli 2021 |
| Generelle forbedringer af kvalitet | Der kræves ingen funktionsstyring | 6 - 12 juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
