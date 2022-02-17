---
title: Køre brugerdefinerede X++ scripts med nul nedetid
description: I dette emne beskrives, hvordan du uploader og kører pakker, der kan implementeres, og som indeholder brugerdefinerede X++ scripts, uden at skulle ophæve systemet.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fcd0a472fa5116ca0b3a59561b6eeb72181a9113
ms.sourcegitcommit: 44e6875e974a3a1b3e1d7a24c1a3cff3d3697cdc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2022
ms.locfileid: "8088338"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Køre brugerdefinerede X++ scripts med nul nedetid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Med denne funktion kan du overføre og køre implementeringspakker, der indeholder tilpassede X++ scripts uden at skulle gennemgå Microsoft Dynamics Lifecycle Services (LCS) eller ophæve systemet. Du kan derfor rette mindre datauoverensstemmelser uden at få forstyrrende nedetid.

Fordelen ved at bruge et X++ script til at rette mindre datauoverensstemmelser er, at systemet automatisk justerer alle relaterede tabeller efter behov, når scriptet køres. Denne metode er med til at sikre korrektionsintegriteten og er med til at minimere risikoen for introduktion af nye uoverensstemmelser.

> [!IMPORTANT]
> Denne funktion anvendes kun til rettelse af mindre datauoverensstemmelser. Den må ikke bruges til følgende formål eller andre formål:
>
> - Dataindsamling
> - Skemaændringer
> - Overflytning af data eller andre processer, der kører længe
> - Rettelse af data, der kan rettes via andre metoder, f.eks. almindelige forretningsprocesser, værktøjer til datakonsistens eller andre værktøjer til selvbetjening
>
> Funktionen giver autoriserede brugere mulighed for at ændre enheder og deres poster direkte uden at skulle køre den forretningslogik, der er knyttet til disse enheder. Disse ændringer kan forårsage problemer med dataintegriteten. Din organisation kan derfor kræve, at du får godkendelse og underskrift fra interne og eksterne revisorer (eller andre tilsvarende personer), før og/eller efter at du kører et script. Af hensyn til overholdelse af angivne standarder skal ændringer, der påvirker visse karakteristika, også offentliggøres i eksterne rapporter (f.eks. regnskaber) eller rapporteres til offentlige myndigheder. Din organisation er eneansvarlig for eventuelle ændringer, der foretages af dens data via denne funktion, enhver godkendelse og underskrift eller offentliggørelse af disse ændringer samt overholdelse af de gældende love. Du bærer hele risikoen ved at bruge funktionen.

Alle de pakker, der kan implementeres, og som overføres til systemet, gennemgår en obligatorisk arbejdsproces. Som en sikkerhedsforanstaltning og for at hjælpe med at sikre opdelingen af opgaver, må den bruger, der overfører en pakke, der kan installeres, ikke godkende den i forbindelse med de næste trin i arbejdsprocessen. En anden bruger skal godkende den. Når pakken er godkendt, vil den bruger, der har overført den, dog få tilladelse til at udføre de resterende trin.

Systemet kræver, at alle installerbare pakker gennemgår en testkørsel. Før scriptet får lov til at køre på produktionsdata, skal en bruger validere, at outputtet er korrekt, ved at vælge **Acceptér testlog**. Hvis outputtet ikke er korrekt, skal brugeren markere pakken som mislykket ved at vælge **Afbryd**. I dette tilfælde kan scriptet ikke køre på produktionsdata.

Alle overførte pakker gemmes i systemet og gennemgår en defineret arbejdsproces for hændelser. For hver hændelse opbevarer systemet en log, der indeholder et tidsstempel og id'et for den person, der udførte hændelsen. På denne måde sikrer systemet, at der er et revisionsspor.

Som følgende illustration viser, indeholder systemet detaljer om, hvordan hver installerbare pakke blev kørt i X++, og hvilke enheder der blev berørt.

![Siden Scriptdetaljer.](media/script-details.png "Siden Scriptdetaljer")

## <a name="assign-duties-to-users-to-control-access"></a>Tildele opgaver til brugere for at kontrollere adgang

Denne funktion har følgende opgaver. Administratorer kan bruge disse opgaver som en hjælp til at styre adgangen til funktionen.

- **Vedligehold brugerdefinerede scripts** – Denne opgave giver mulighed for at overføre, teste, kontrollere og køre tilpassede X++ scripts i miljøer (test af brugeraccept \[UAT\] og produktion).
- **Godkend brugerdefinerede scripts** – Denne opgave giver mulighed for at godkende et overført brugerdefineret X++-script. Godkendelse er et obligatorisk trin, før et script kan testes, kontrolleres og køres.

For at minimere risikoen for skadelige handlinger skal hvert script udtrykkeligt godkendes af en anden bruger end den bruger, der har overført det. Før du kan bruge denne funktion i organisationen, skal en administrator tildele de foregående opgaver til mindst to relevante og højt betroede brugere. Selvom en enkelt bruger kan have begge opgaver, kan den pågældende bruger stadig ikke godkende egne scripts.

## <a name="create-a-deployable-package"></a>Oprette en installerbar pakke

Funktionen kræver en almindelig installerbar pakke, der kan oprettes i Visual Studio. Du kan finde flere oplysninger under [Oprette installerbare pakker med modeller](../deployment/create-apply-deployable-package.md).

Den pakke, der kan implementeres, skal indeholde nøjagtigt én kørselsbar X++-klasse. Det skal med andre ord have én klasse, der omfatter en metode med følgende signatur.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Navnet på hovedmetoden skal være små bogstaver.

## <a name="code-example"></a>Kodeeksempel

Følgende kodeeksempel viser, hvordan en pakke, der kan installeres, kan struktureres.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Bedste praksis

Følgende liste indeholder en beskrivelse af nogle af de bedste fremgangsmåder for vellykket skrivning, implementering og kørsel af et script. Listen er ikke udtømmende, og den skal betragtes som blot vejledende.

- **Du skal** skrive en meddelelse om succes i slutningen af scriptet. På denne måde kan du se, at scriptet kørte uden undtagelser.
- **Du skal** tilføje eksplicit håndtering af transaktionsområdet.
- **Du skal** bruge eksisterende forretningslogik, f.eks. `update()`-metoder, men **du må ikke** gå uden om forretningslogik ved hjælp af metoderne `doUpdate()`, `doInsert()` og `doDelete()`. Denne fremgangsmåde er med til at sikre, at afhængige data håndteres korrekt. Risikoen for yderligere uoverensstemmelser i data vil også blive væsentligt reduceret.
- **Du skal** vurdere firmakonteksten. Denne metode viser almindelige fejl, når der køres et script. Den vil f.eks. vise, om scriptet køres i det forkerte firma.
- **Du skal** sikre dig, at antallet af berørte poster svarer til dine forventninger. Denne metode vil vise, om data uventet flyttes i systemet, mens scriptet blev forberedt.
- **Du skal** bruge entydige klassenavne til hvert script (f.eks. ved at medtage en reference til et arbejdselement i navnet). Med denne metode undgås problemer med navne, når du uploader scriptet. Hvis der kræves en ny gentagelse af et script, skal du give det et nyt navn.
- **Du skal** teste de enkelte script i et ikke-produktionsmiljø først. Test for den tilsigtede effekt og for utilsigtede sideeffekter på relaterede data. Du skal sikre, at alle de forretningsprocesser, der kan påvirkes, kan fuldføres korrekt efterfølgende.

## <a name="upload-and-run-a-deployable-package"></a>Uploade og køre en pakke, der kan installeres

Brug følgende procedure til at uploade og køre et script.

1. I din Finans- og driftsapp skal du gå til **Systemadministration \> Periodiske opgaver \> Database \> Brugerdefinerede scripts**.
1. Vælg **Overfør**.
1. Vælg den pakke, der kan installeres, og som er oprettet som beskrevet tidligere i dette emne. Du bliver bedt om at angive formålet med scriptet.
1. Scriptet skal nu godkendes af en anden bruger end den bruger, der har uploadet det. Godkenderen skal følge disse trin:

    1. Gå til **Systemadministration \> Periodisk \> Database \> Brugerdefinerede scripts**.
    1. Vælg det script, du vil godkende, og vælg derefter **Detaljer**.
    1. I handlingsruden under fanen **Procesarbejdsgang** skal du i gruppen **Start** vælge **Godkend** eller **Afvis**. Hvis du vælger **Godkend**, markeres scriptet som godkendt og låses op til test. Hvis du vælger **Afvis**, er scriptet låst. I begge tilfælde registreres hændelsen, og en kopi af scriptet bevares i systemet.

1. Scriptet skal testes for at sikre, at det gør, hvad det er tiltænkt at gøre. Testeren kan være den samme som uploaderen eller godkenderen, eller det kan være en tredje bruger, der har de nødvendige tilladelser. Testeren skal følge disse trin:

    1. Gå til **Systemadministration \> Periodisk \> Database \> Brugerdefinerede scripts**.
    1. Vælg det script, du vil teste, og vælg derefter **Detaljer**.
    1. I handlingsruden under fanen **Procesarbejdsgang** skal du i gruppen **Test** vælge **Kør test**. Scriptet køres i en midlertidig transaktion, som automatisk afbrydes, mens der indsamles forskellige logfiler og SQL-sætninger.
    1. Når scriptet er kørt færdigt, kan du gennemse logfilerne og kontrollere, at resultaterne opfylder dine forventninger. Udfør ét af følgende trin:

        - Hvis du er tilfreds med testresultatet, skal du vælge **Acceptér testlog** i **Test**-gruppen under fanen **Procesarbejdsgang** i handlingsruden for at tillade, at scriptet køres. Hændelsesloggen afspejler det faktum, at scriptet er blevet testet, og det angiver, hvem der har testet det og hvornår.
        - Hvis du ikke er tilfreds med testresultatet, skal du vælge **Afbryd** i **Slut**-gruppen under fanen **Procesarbejdsgang** i handlingsruden for at forhindre, at scriptet køres. Systemet opbevarer en kopi af scriptet sammen med en log over dets historik.

1. Når du er sikker på, at scriptet lever op til dine forventninger, skal du vælge **Kør** i gruppen **Kør** under fanen **Procesarbejdsgang** i handlingsruden for at køre det. Denne kommando gør samme ting som den forrige testkørsel, men transaktionen bliver bekræftet til slut.
1. Når scriptet er kørt færdig, skal du kontrollere resultatet og bekræfte, at scriptet har fungeret efter din hensigt. Udfør ét af følgende trin:

    - Hvis du er tilfreds med resultatet, skal du vælge **Løst formål** i **Slut**-gruppen under fanen **Procesarbejdsgang** i handlingsruden. Hændelsesloggen afspejler det faktum, at scriptet er kørt korrekt, og det angiver, hvem der har verificeret det og hvornår. Scriptet gemmes, men er nu låst og kan ikke køres igen.
    - Hvis du ikke er tilfreds med resultatet, skal du vælge **Uløst formål** i **Slut**-gruppen under fanen **Procesarbejdsgang** i handlingsruden. Hændelsesloggen afspejler det faktum, at scriptet ikke har opfyldt det tiltænkte formål, og det angiver, hvem der har kørt det og hvornår. Scriptet gemmes, men er nu låst og kan ikke køres igen. Men scripthandlingen fortrydes ikke automatisk af systemet. Du skal muligvis skrive, importere og køre et nyt script for at fortryde den effekt, som det mislykkede script havde på systemet.

Dit valg i det sidste trin definerer scriptets sluttilstand. Du kan gentage processen efter behov.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Uploade og køre en pakke, der kan installeres, via LCS

I stedet for at implementere den pakke, der kan installeres, via brugergrænsefladen i din Finans- og driftsapp, som det beskrives i forrige afsnit, kan du uploade den til LCS og bruge den almindelige procedure til at udrulle den. Yderligere oplysninger finder du i [Installere installerbare pakker fra kommandolinjen](../deployment/install-deployable-package.md).

Selvom der er færre begrænsninger i denne tilgang, giver den mindre fejlbeskyttelse. Da den kræver genstart af alle servere, medfører det desuden en vis nedetid.
