---
title: Økonomiske dimensioner
description: I dette emne beskrives de forskellige typer økonomiske dimensioner, og hvordan de er oprettet.
author: aprilolson
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0715d3e4e4cb167c55d9c7d98cdf599187bf3b43
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176934"
---
# <a name="financial-dimensions"></a>Økonomiske dimensioner

[!include [banner](../includes/banner.md)]

I dette emne beskrives de forskellige typer økonomiske dimensioner, og hvordan de er oprettet.

Du kan bruge siden **Økonomiske dimensioner** til at oprette økonomiske dimensioner, som du kan bruge som kontosegmenter i kontoplaner. Der er to typer økonomiske dimensioner: brugerdefinerede dimensioner og enhedsunderstøttede dimensioner. Brugerdefinerede dimensioner deles på tværs af juridiske enheder, og værdierne angives og vedligeholdes af brugerne. For enhedsunderstøttede dimensioner defineres værdierne andre steder i systemet, f.eks. i enheden Debitorer eller Butikker. Nogle enhedsunderstøttede dimensioner deles på tværs af juridiske enheder, mens andre enhedsunderstøttede dimensioner er firmaspecifikke.

Når du har oprettet de økonomiske dimensioner, skal du bruge siden **Økonomiske dimensionsværdier** til at tildele hver økonomisk dimension yderligere egenskaber.

Du kan bruge økonomiske dimensioner til at repræsentere juridiske enheder. Du behøver ikke at oprette de juridiske enheder i Dynamics 365 Finance. Økonomiske dimensioner kan dog ikke opfylde juridiske enheders handlings- eller forretningsmæssige behov. Funktionen for regnskab mellem enheder i Finance er kun udviklet til at håndtere de regnskabsposter, der oprettes ved hver transaktion.

Før du kan konfigurere økonomiske dimensioner som juridiske enheder, skal du evaluere forretningsprocesserne på følgende områder for at afgøre, om denne installation vil fungere for organisationen:

- Lagerbeholdning
- Salg og køb mellem økonomiske dimensioner og juridiske enheder
- Beregning og rapportering af salgsmoms
- Driftsrapportering

Her er nogle begrænsninger:

- Du kan kun bruge salgsmomsfunktioner til juridiske enheder, ikke til økonomiske dimensioner.
- Nogle rapporter medtager ikke økonomiske dimensioner. Hvis du vil rapportere pr. økonomisk dimension, kan det derfor være nødvendigt at redigere rapporterne.

## <a name="custom-dimensions"></a>Brugerdefinerede dimensioner

For at oprette en brugerdefineret økonomisk dimension skal du i feltet **Brug værdier fra** vælge **Brugerdefineret dimension**.

Du kan også angive en kontomaske for at begrænse mængden og typen af oplysninger, som kan angives for dimensionsværdier. Du kan skrive tegn, der forbliver ens for hver dimensionsværdi, f.eks. bogstaver eller en bindestreg (-). Du kan også angive nummertegn (\#) og &-tegn (&) som pladsholdere for tegn, som ændres, hver gang der oprettes en dimensionsværdi. Brug et nummertegn (\#) som pladsholder for et tal, og tegnet (&) som pladsholder for et bogstav. Feltet til formatmasken er kun tilgængeligt, hvis du har valgt **Brugerdefineret dimension** i feltet **Brug værdier fra**.

**Eksempel**

Hvis du vil begrænse dimensionsværdien til bogstaverne "CC", en bindestreg og tre tal, skal du angive **CC-\#\#\#** som formatmaske.

## <a name="entity-backed-dimensions"></a>Enhedsunderstøttede dimensioner

For at oprette en enhedsunderstøttet økonomisk dimension skal du i feltet **Brug værdier fra** vælge en systemdefineret enhed, den økonomiske dimension skal baseres på. Der oprettes derefter økonomiske dimensionsværdier ud fra denne enhed. Hvis du f.eks. vil oprette dimensionsværdier for projekter, skal du vælge **Projekter**. Der oprettes derefter en dimensionsværdi for hvert projektnavn. Siden **Økonomiske dimensionsværdier** viser værdierne for enheden. Hvis disse værdier er firmaspecifikke, viser siden også firmaet.

## <a name="activating-dimensions"></a>Aktivering af dimensioner

Når du aktiverer en økonomisk dimension, opdateres tabellen, så den omfatter navnet på den økonomiske dimension. Slettede dimensioner fjernes. Du kan angive dimensionsværdier, før du aktiverer en økonomisk dimension. Men en økonomisk dimension ikke forbruges overalt, før den aktiveres. Du kan f.eks. ikke føje en økonomiske dimension til kontostruktur, før den økonomiske dimension er blevet aktiveret. Når du vælger **Aktivér**, opdateres alle dimensioner, og statusændringer vises.

## <a name="translations"></a>Oversættelser

På siden **Oversættelse af tekst** kan du skrive tekst til den valgte økonomiske dimension på forskellige sprog. På siden **Oversættelse af hovedkonto** kan du skrive tekst til den hovedkontoen på forskellige sprog. 

## <a name="legal-entity-overrides"></a>Tilsidesættelser af juridisk enhed

Ikke alle dimensioner gælder for alle juridiske enheder. Desuden kan nogle dimensioner være relevante for kun en bestemt periode. I disse tilfælde kan du bruge sektionen **Tilsidesættelser af juridisk enhed** til at angive de firmaer, dimensionen bør suspenderes for, ejeren, og den periode, hvor dimensionen er aktiv.

## <a name="deleting-financial-dimensions"></a>Slette økonomiske dimensioner

Af hensyn til vedligeholdelsen af dataenes referenceintegritet kan økonomiske dimensioner sjældent slettes. Hvis du forsøger at slette en økonomisk dimension, evalueres følgende kriterier:

- Er den økonomiske dimension blevet anvendt på bogførte eller ikke-bogførte posteringer eller i nogen form for kombination af dimensionsværdier?
- Bruges den økonomiske dimension i en aktiv kontostruktur, en avanceret regelstruktur eller et sæt økonomiske dimensioner?
- Er den økonomiske dimension en del af et standardintegrationsformat for økonomiske dimensioner?
- Er den økonomiske dimension konfigureret som en standarddimension?

Hvis et af kriterierne er opfyldt, kan du ikke slette den økonomiske dimension.

## <a name="default-dimension-values"></a>Standarddimensionsværdier

Du kan bruge værdier fra masterposter, f.eks. debitor og kreditor, som standardværdier i nye dimensioner. Når der oprettes nye dimensioner, angives masterpost-id'et i dimensionsværdierne for disse masterposter. Når du f.eks. opretter en ny debitor, angives debitor-id i debitordimensionen. Når du opretter salgsordrer, fakturaer eller andre dokumenter, der kræver et debitor-id, bruges de eksisterende standardregler, og debitor-id føjes til dokumentet.

Denne funktion styres af en indstilling i dimensionen. Denne indstilling hedder **Kopiér værdier til denne dimension i hvert nyt DimensionName, der oprettes**, hvor **DimensionName** er navnet på dimensionen. Funktionen er som standard slået fra. Men den kan aktiveres til enhver tid.

Hvis der allerede findes poster for dimensionen, opdateres masterposter, når du aktiverer funktionen. Men eksisterende dokumenter og transaktioner opdateres ikke.

Hvis du bruger en skabelon til at oprette en masterpost, skal du kontrollere, at skabelonværdien for masterdimensionen er tom. F.eks. hvis du vil opretter debitorer fra en skabelon, skal du sikre, at debitordimensionen i skabelonen er tom. Standardværdien for debitordimensionen fra det nye debitornummer bruges, når du opretter den nye debitor.  

## <a name="derived-dimensions"></a>Afledte dimensioner

Du kan konfigurere en dimension, så oplysninger til andre dimensioner angives automatisk, når du angiver denne dimension i et dokument. Hvis du f.eks. angiver bærer 10, kan en værdi på **20** angives automatisk i afdelingsdimensionen.

Du kan oprette afledte værdier på dimensionssiden.

1. Vælg en dimension, og vælg derefter **Afledte dimensioner**.

    Siden **Afledte dimensioner** indeholder et gitter. Det valgte dimensionssegment er den første kolonne i gitteret.

2. Tilføj de segmenter, der skal afledes. Hvert segment vises som en kolonne.

Angiv kombinationer af dimensioner, der skal afledes af dimensionen i den første kolonne. Hvis du f.eks. vil bruge bærer,som den dimension, som afdelingen og sted afledes fra, skal du angive bærer 10, afdeling 20 og sted 30. Når du derefter angiver bærer 10 i en masterpost eller på en transaktionsside, bliver afdeling 20 og sted 30 angivet som standard.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Tilsidesættelse af eksisterende værdier med afledte dimensioner
 
Den afledte dimensionsproces tilsidesætter som standard ikke eksisterende værdier for afledte dimensioner. Hvis du f.eks. angiver bærer 10, og ingen anden dimension er angivet, angives afdeling 20 og sted 30 som standard. Men hvis du ændrer bæreren, ændres de værdier, der allerede er fastlagt, ikke. Derfor kan du oprette standarddimensioner for masterposter, og disse dimensioner ændres ikke af afledte dimensioner.

Du kan ændre funktionaliteten af afledte dimensioner for at tilsidesætte eksisterende værdier ved at markere afkrydsningsfeltet **Erstat eksisterende dimensionsværdier med afledte værdier** på siden **Afledte dimensioner**. Hvis dette felt er markeret, kan du angive en dimension med afledte dimensionsværdier, og de afledte dimensionsværdier tilsidesætter derefter de værdier, der allerede findes. Hvis du i det foregående eksempel angiver bærer 10, og ingen anden dimension er angivet, angives afdeling 20 og sted 30 som standard. Hvis værdierne allerede var afdeling 50 og sted 60, bliver værdierne dog nu ændret til afdeling 20 og sted 30.
 
Afledte dimensioner med denne indstilling erstatter ikke automatisk de eksisterende standardværdier for dimensioner, når standarddimensionsværdier anvendes. Dimensionsværdier bliver kun tilsidesat, når du indtaster en ny dimensionsværdi på en side, og der findes afledte værdier for den pågældende dimension på siden.

### <a name="preventing-changes-with-derived-dimensions"></a>Forhindre ændringer med afledte dimensioner
 
Når du bruger **Tilføj segment "** på siden **Afledte dimensioner** til at tilføje et segment som en afledt dimension, er der angivet en indstilling nederst på siden **Tilføj segment**, som du kan bruge til at undgå ændringer af dimensionen, når den er afledt på en side. Standardindstillingen er deaktiveret, så den forhindrer ikke, at de afledte dimensionsværdier bliver ændret. Vælg indstillingen **Ja**, hvis du vil forhindre, at dimensionen ændres, når den er afledt. F.eks. hvis værdien for dimensionen Afdeling er afledt fra værdien for dimensionen Bærer, kan værdien Afdeling ikke ændres, hvis indstillingen **Forhindre ændringer** er **Ja**. 
 
Indstillingen forhindrer ikke ændringer, hvis dimensionsværdien er gyldig, men ikke findes på listen over afledte dimensioner. F.eks. hvis Afdeling 20 er afledt af Bærer 10, og du angiver Bærer 10, kan du ikke redigere Afdeling 20. Men hvis du angiver Bærer 20, og det ikke er på listen over afledte dimensioner for Bærer, kan du redigere værdien for Afdeling. 
 
I alle tilfælde valideres kontoværdien og alle dimensionsværdier stadig mod kontostrukturerne, når de afledte dimensionsværdier er anvendt. Hvis du bruger afledte dimensioner, og de ikke valideres, når de bruges på en side, skal du ændre de afledte dimensionsværdier på siden med afledte dimensioner, før du kan bruge dem i transaktioner. 
 
Når du ændrer dimensioner i oversigtspanelet **Regnskabsdimensioner**, kan den dimension, der er markeret for at forhindre ændringer, ikke redigeres. Hvis du angiver en konto og dimensioner i det segmenteret postkontrolelement på en side, kan dimensionerne redigeres. Men når du flytter fremhævningen fra det segmenterede postkontrolelement og flytter til et andet felt eller foretager handlinger, valideres kontoen og dimensionerne mod listen over afledte dimensioner og kontostrukturerne for at sikre, at du har angivet de relevante værdier. 

### <a name="derived-dimensions-and-entities"></a>Afledte dimensioner og enheder

Du kan oprette de afledte dimensionssegmenter og -værdier ved hjælp af enheder.

- Enheden Afledte dimensioner opretter de styrende dimensioner og segmenter, der bruges til disse dimensioner.
- Med den afledte dimensionsværdienhed kan du importere de værdier, der skal afledes for hver styrende dimension.

Når du bruger en enhed til at importere data, og den pågældende enhed importerer dimensioner, anvendes de afledte dimensionsregler under importen, medmindre enheden specifikt tilsidesætter disse dimensioner.

Du kan finde flere oplysninger under følgende emner:

- [Definere økonomiske dimensioner](tasks/define-financial-dimensions.md)
- [Vedligeholde standardskabeloner for økonomiske dimensioner](tasks/maintain-financial-dimension-default-templates.md)
