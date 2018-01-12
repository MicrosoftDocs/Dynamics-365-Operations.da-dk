---
title: Parametre for udgiftsstyring
description: "Følgende parametre styrer funktionsmåden i Udgiftsstyring."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8ca9e80d6d2b87fcdd10ebb9d32bd0a2b2d15614
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="expense-management-parameters"></a>Parametre for udgiftsstyring
-----------------------------

Parametrene styrer den generelle funktionsmåde i Udgiftsstyring.

### <a name="general"></a>Almindelig

| **Felt**                                                | **Beskrivelse**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardsats for kørsel**                             | Angiv refusionssatsen for udgifter til kørsel. Satsen skal ganges med den kørsel, der er angivet for udgiften ved beregning af det beløb, der refunderes for rejseudgiften.                       |
|**Personlige udgifter betalt af**                             | Vælg, hvem der er ansvarlig for betaling af de transaktionsbeløb på kreditkort, der kategoriseres som personlige.                                                                                                     |
|**Få vist hele udgiftsrapporten ved detailudledning**               | Vælg denne indstilling for at få vist alle udgifter for en udgiftsrapport, når du får vist detaljer i det oprindelige dokument for et bestemt bilag, der blev genereret, da udgiftsrapporten blev bogført.              |
|**Rejser skal forudgodkendes**                 | Markér denne indstilling for at kræve, at der sendes og godkendes en rejserekvisition, før en medarbejder kan sende en udgiftsrapport.                                                                    |
|**Tillad, at fordelinger redigeres, før de bogføres**            | Vælg, om fordelingerne af en udgiftsrapport skal kunne ændres før bogføringen.                                                                                                                 |
|**Evaluer politikker for udgiftsstyring**                     | Vælg, hvornår udgifterne evalueres for at finde ud af, om en udgiftspolitik er overtrådt. Udgifter kan kontrolleres for overtrædelser, når udgiftsregistrering angives og gemmes, eller når udgiften sendes til godkendelse. Politikreglerne for påkrævede kvitteringer bliver kontrolleret, når udgiftslinjen er gemt.                   |
|**Tillad interne udgiftslinjer**                         | Vælg, om du vil tillade angivelse af udgifter for andre juridiske enheder i en udgiftsrapport.                                                                                                          |
|**Tillad redigering af valutakursen for kreditkortudgifter** | Vælg denne indstilling, hvis du vil tillade, at brugeren redigerer valutakursen for importerede kreditkortudgifter.                                                                        |
|**Felter, som skal vises, i hierarki med flere niveauer**                  | Vælg, hvilke godkenderfelter der skal vises, når tildelingstypen i arbejdsgangen for udgiftsrapporten er indstillet til hierarki, og valget af hierarki er indstillet til Hierarki for godkendelse i flere niveauer af udgifter. Når hierarki for godkendelse i flere niveauer bruges til arbejdsgangen, vises og redigeres de valgte felter i udgiftsrapporten. |
|**Angiv medarbejderens kreditkortnummer (opdatering fra juli 2017)**     | Vælg, om et nummer med 15 eller 16 tegn kan angives og gemmes i feltet **Kort-ID** på siden **Kreditkort** for en medarbejder.                                                                          |

### <a name="financial"></a>Økonomisk

| **Felt**                                                            | **Beskrivelse**     |
|----------------------------------------------------------------------|------------------------------------|
|**Navn på finanskassekladde**                                         | Vælg navnet på den finanskladde, som godkendte udgiftsrapporter bogføres til.            |
|**Aktivér momsopkrævning fra udgifter**                                  | Vælg denne indstilling for at aktivere udgift med momsopkrævning for berettigede udgifter. Denne indstilling kan ikke aktiveres, hvis Amerikansk moms og importmomsregler er aktiveret.      |
|**Bogfør kontantforskud med det samme**                                     | Vælg denne indstilling for at bogføre et godkendt kontantforskud, når processen Betal og overfør er fuldført. Hvis denne indstilling ikke er valgt, genererer Betal og overfør-processen en ikke-bogført finanskladde. |
|**Ret regnskabsdato under bogføring**                             | Vælg denne indstilling for at opdatere regnskabsdatoen, når du bogfører udgifter, hvis den aktuelle periode på hold eller lukket. Regnskabsdatoen indstilles til den næste åbne periode.   |
|**Tillad gruppering af transaktioner baseret på den modkonto, der er angivet i betalingsmetoden**      | Vælg denne indstilling for at opsummere udgiftsposteringerne for en udgiftsrapport baseret på den modkonto, der er angivet i betalingsmåden for udgifterne.   
|**Inkl. moms**                                                   | Vælg denne indstilling for at inkludere moms i udgiftsbeløb som standard.             |
|**Frigiv behæftelse ved lukning af rejserekvisitioner**            | Vælg denne indstilling for at frigive behæftede midler, når en godkendt rejserekvisition lukkes.                                                                                   |
|**Tillad indsendelse af rejserekvisition ved budgetoverskridelse af budgetregister og projektbudget** | Vælg denne indstilling for at give medarbejdere mulighed for at sende rejserekvisitioner til godkendelse, der enten overskrider det tilladte budget, der er angivet i budgetregisteret, eller det tilladte budget for et projekt.            |
|**Tillad indsendelse af udgiftsrapport ved budgetoverskridelse af budgetregister og projektbudget**    | Vælg denne indstilling for at give medarbejdere mulighed for at sende udgiftsrapporter til godkendelse, der enten overskrider det tilladte budget, der er angivet i budgetregisteret, eller det tilladte budget for et projekt.                |
|**Tillad godkendelse af udgiftsrapporter kun ved budgetoverskridelse af budgetregister**                | Vælg denne indstilling for at give godkendere mulighed for at godkende udgiftsrapporter, der overskrider det tilladte budget, der er angivet i budgetregisteret.                                                                       |

### <a name="per-diem"></a>Diæter

| **Felt**                             | **Beskrivelse**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimumstimer for diæter**           | Angiv min. standardantal timer, som en medarbejder skal arbejde på en dag, for at det udløser en diæt til rejserelaterede udgifter.  Denne værdi bruges kun som en standardværdi for feltet Minimumstimer på diætsatsniveau.                                                                                      |
|**Måltidsprocent**                          | Angiv standardprocenten for diæter for måltider, der bruges på den første og sidste dag af den rejserelaterede udgift, når feltet **Beregn fradrag for måltider efter** er indstillet til enten **Måltidstype pr. dag** eller **Antal måltider pr. dag**. Arbejdsdagen for den første og sidste dag kan være kortere end for en standardarbejdsdag. Diætbeløbet for disse dage kan derfor være forskelligt fra standardbeløbet. Hvis procentdelen er indstillet til 0, fradrag for den første og sidste dag være 0,00. |
|**Hotelprocent**                        | Angiv standardprocenten for diæter til hoteller for den første og sidste dag i den rejserelaterede udgift. Arbejdsdagen for den første og sidste dag kan være kortere end for en standardarbejdsdag. Diætbeløbet for disse dage kan derfor være forskelligt fra standardbeløbet. Hvis procentdelen er indstillet til 0, fradrag for den første og sidste dag være 0,00.                                              |
|**Andre procenter**                        | Angiv standardprocenten for diæter til diverse udgifter for den første og sidste dag i den rejserelaterede udgift. Arbejdsdagen for den første og sidste dag kan være kortere end for en standardarbejdsdag. Diætbeløbet for disse dage kan derfor være forskelligt fra standardbeløbet. Hvis procentdelen er indstillet til 0, fradrag for den første og sidste dag være 0,00.                                                                                                     |
|**Reduktion i procenten for morgenmad** | Angiv det beløb, som diæten reduceres med for morgenmad. Hvis en medarbejder f.eks. får morgenmaden betalt på anden vis, kan du vælge at reducere diætbeløbet med 10 %.                               |
|**Reduktion i procenten for frokost**    | Angiv det beløb, som diæten reduceres med for frokost. Hvis en medarbejder f.eks. får frokosten betalt på anden vis, kan du vælge at reducere diætbeløbet med 15 %.                                       |
|**Reduktion i procenten for aftensmad**   | Angiv det beløb, som diæten reduceres med for aftensmad. Hvis en medarbejder f.eks. får aftensmaden betalt på anden vis, kan du vælge at reducere diætbeløbet med 25 %.                                     |
|**Beregn fradrag for måltider efter**         | Vælg, hvordan systemet skal beregne diæter for fradrag for måltid ved at vælge, om fradraget er baseret på måltidstypen pr. rejse eller pr. dag, eller om det er baseret på antallet af måltider, der er tilladt pr. dag.|
|**Afrunding af diæter**                  | Vælg den afrundingstype, der bruges til udgifter til diæter. Hvis du vælger normal afrunding, rundes enhver diætudgift, der består af et beløb på 0,50, op til 1,00, og enhver diætudgift, der består af et beløb, der er mindre end 0,50, rundes ned til 0,00.                                                                                              |
|**Udfør beregning af diæter baseret på**         | Vælg, om et diætbeløb skal baseres på en kalenderdag eller en 24-timersperiode.       |

### <a name="fax-cover-pages"></a>Faxforsider

| **Felt**                      | **Beskrivelse**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instruktioner**                   | Angiv de instruktioner, som medarbejdere skal følge, når de opretter en forside til en fax, der bruges til at sende kvitteringer, der er relateret til en udgiftsrapport. Klik på knappen **Oversættelser** for at angive den sprogspecifikke tekst, der skal vises baseret på brugerens sprog. |
|**Bruger-ID (stregkodeoplysninger)** | Vælg denne indstilling for at gemme en medarbejders entydige id i den stregkode, der bruges på forsiden af faxen.                 |
|**Stregkode**                      | Vælg den stregkode, der bruges på forsiden af faxen. Stregkoder, 39 og 128 understøttes i Udgiftsstyring.               |

### <a name="anti-corruption"></a>Antikorruption

| **Felt**                             | **Beskrivelse**      |
|---------------------------------------|------------------------------------------------------------------------|
|**Vis antikorruptionsattest**   | Vælg denne indstilling for at få vist antikorruptionsteksten, når du opretter en ny udgiftsrapport. Derefter kan du aktivere specifikke udgiftskategorier, der kræver, at antikorruptionsattesten er valgt i udgiftsrapporten. F.eks. kan en gavekategori, der er relateret til en udgift i forbindelse med en regeringsembedsmænd, kræve, at medarbejderen bekræfter, at udgiften overholder firmaets politik vedrørende regeringsembedsmænd. |
|**Meddelelse til afsender om antikorruption** | Angiv den tekst, medarbejderen ser, når der oprettes en ny udgiftsrapport. Klik på knappen **Oversættelser** for at angive den sprogspecifikke tekst, der skal vises baseret på brugerens sprog.         |
|**Meddelelse til godkender om antikorruption**  | Angiv den tekst, godkenderen ser, når der oprettes en ny udgiftsrapport. Klik på knappen **Oversættelser** for at angive den sprogspecifikke tekst, der skal vises baseret på brugerens sprog.        |

