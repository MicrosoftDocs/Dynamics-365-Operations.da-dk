---
title: Analyse af aktivfejl
description: I dette emne beskrives analyse af aktivfejl i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 67ccbb742bb4e2283c30b4dec055d137b4a51e40
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216407"
---
# <a name="asset-fault-analysis"></a>Analyse af aktivfejl

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver kan du analysere registreringer af aktivfejl for at få et overblik over det samlede antal registrerede fejl i en bestemt periode. Fejlregistreringer kan analyseres fra forskellige perspektiver, f.eks. med fokus på aktiver, aktivtyper, arbejdssteder, fejlsymptomer eller fejltyper.

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Analyse af aktivfejl**.

2. I dialogboksen **Analyseberegning af aktivfejl** kan du bruge feltet **Niveau** til at angive, hvor detaljeret aktivfejllinjerne skal være i forbindelse med arbejdssteder. 

    Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktivfejllinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
        
    Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle aktivfejllinjer på alle de arbejdsstedsniveauer, de er relateret til.

3. Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver, fejldatoer, fejlårsager og fejlrettelser i oversigtspanelet **Poster, der skal indgå**.

4. Klik på **OK** for at starte beregningen.

5. Klik på en eller flere af knapperne **Sammenlæg pr.** under fanen **Analyse af aktivfejl** for at få vist detaljeringsniveauet. Aktiverede knapper er fremhævet. Aktivér eller deaktiver knapper ved at klikke på dem.

6. Klik på **Opdater beregninger** for at få vist dine valg på skærmen. 

>[!NOTE]
>Når du aktiverer eller deaktiverer knappen **Sammenlæg pr.**, skal du huske at klikke på knappen **Opdater beregninger**. Dette er nødvendigt, da en stor mængde data behandles, mens du genberegner fejlsandsynlighed.

## <a name="examples"></a>Eksempler

Der er mange måder at analysere fejlregistreringer på. Denne sektion har fem eksempler på, hvordan forskellige datavalg giver mere indsigt og detaljer ved analyse af registreringer af aktivfejl.

### <a name="group-by-symptoms"></a>Sammenlæg pr. symptomer

I skærmbilledet herunder er det kun knappen **Symptom**, der er valgt.

- Der er foretaget fejlregistrering af tre fejlsymptomer: "Air leak", "Blown fuse" og "Equipment jammed".  
- I kolonnen **Sandsynlighed %** giver alle procenter en sum af 100 %. Sandsynlighed er baseret på alle **Symptom**-registreringer i denne fejlanalyse.

![Figur 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Sammenlæg pr. symptomer og tidsperiode

I skærmbilledet nedenfor tilføjes **År** og **Måned** for at vise, hvordan du kan få vist fejlregistreringer i løbet af en valgt periode.

- Fejlsymptomerne vises nu som registreringer pr. år/måned.  
- Hvis du tilføjer alle procentsatser for hver måned i kolonnen **Sandsynlighed %**, bliver de sammenlagt 100 %. Sandsynlighed er baseret på **Symptom**-registreringerne i denne fejlanalyse. Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlsymptom, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlsymptom.

![Figur 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Sammenlæg pr. flere symptomer og aktiver

Kombinationen af aktiver og en aktivtype bruges som udgangspunkt for de beregninger, der vises i de tre skærmbilleder nedenfor, som øges i detaljeringsgraden.  

Generelt vil knapperne i handlingsrudegrupper **Gruppér efter dato**, **Gruppér efter aktiv**, **Gruppér efter arbejdssted** samt knappen **Fejl** (fejl-id) normalt indeholde perioder eller aktivrelationer. Knapperne **Symptom**, **Område**, **Type**, **Årsag** og **Afhjælpning** er de kategoriseringer, der bruges i fejlstyring til at analysere registreringer af aktivfejl og udpege problematiske områder.  

**Sammenlæg pr. symptom, aktiv og aktivtype**

I skærmbilledet nedenfor blev **Aktiv** og **Aktivtype** tilføjet for at give flere oplysninger om fejlregistreringer.

- Fejlsymptomerne er nu opdelt i kombinationerne **Aktiv** / **Aktivtype** / **Symptom**.  
- Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for henholdsvis kombinationen **Aktiv** / **Aktivtype** / **Symptom**, bliver de hver især sammenlagt 100 %. Sandsynlighed er baseret på **Symptom**-registreringer i denne fejlanalyse. Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlsymptom, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlsymptom.

![Figur 3](media/08-controlling-and-reporting.png)

**Sammenlæg pr. to symptomer, aktiv og aktivtype**

I skærmbilledet nedenfor er **Område** lagt til **Symptom**, **Aktiv** og **Aktivtype** for at give flere oplysninger om fejlregistreringer.

- Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for kombinationen af **Aktiv** / **Aktivtype** / **Symptom** på et aktiv, bliver de hver især sammenlagt 100 %. Sandsynlighed er baseret på kombinationen af **Symptom** og **Område** i denne fejlanalyse. Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlområde, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlområde.  

![Figur 4](media/09-controlling-and-reporting.png)

**Sammenlæg pr.tre symptomer, aktiv og aktivtype**

I skærmbilledet nedenfor er **Type** tilføjet, og den mest detaljerede beregning vises i dette eksempel.
 
- Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for kombinationen af **Aktiv** / **Aktivtype** / **Symptom** på et aktiv, bliver de hver især sammenlagt 100 %. Sandsynlighed er baseret på kombinationen af **Symptom**, **Område** og **Type** i denne fejlanalyse. Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på en fejltype, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for denne fejltype.

![Figur 5](media/10-controlling-and-reporting.png)


>[!NOTE]
>Du kan få vist en oversigt over alle fejlregistreringer, der er oprettet på arbejdsordrer og vedligeholdelsesanmodninger, ved at klikke på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl**. Vælg en registrering af aktivfejl på siden **Aktivfejl**, og udvid ruden **Relaterede oplysninger** for at få vist oplysninger om den relaterede arbejdsordre eller vedligeholdelsesanmodning.

