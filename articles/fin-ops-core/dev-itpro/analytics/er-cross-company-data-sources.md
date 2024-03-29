---
title: Datakilder på tværs af firma i elektronisk rapportering (ER)
description: Denne artikel beskriver, hvordan du kan bruge datakilder på tværs af firmaer i elektronisk rapportering (ER).
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
ms.openlocfilehash: ec96533dd2da933d5275adadedc9a92a33e47a38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277720"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Datakilder på tværs af firma i elektronisk rapportering (ER)

[!include[banner](../includes/banner.md)]

Du kan designe ER-formater for at oprette udgående dokumenter i forskellige formater. Når et dokument er oprettet, kalder et ER-format datakilder, der er konfigureret i en tilsvarende ER-modeltilknytning. Hvis du vil konfigurere adgang til tabeller i programmet for at hente poster, kan du bruge ER-datakilder af typen **Tabelposter**. Når adgangstabellen er en delt tabel (dvs. en tabel, hvor data gemmes uden et firma-id), returnerer datakilden alle poster. Når adgangstabellen er en firmaafhængig tabel (dvs. en tabel, hvor data gemmes pr. firma), returnerer denne datakilde kun de poster, der er gemt for det aktuelle firma (dvs. den firmakontekst, som ER-formatet kører under).

Hver datakilde af typen **Tabelposter** i en modeltilknytning kan nu markeres som en datakilde på tværs af firmaer. Derfor kan du bruge datakilder af typen **Tabelposter** til at få adgang til data på tværs af firmaer i programtabeller.

Hvis du markerer en datakilde som værende på tværs af firmaer, bruges følgende funktionsmåde:

- Hvis en datakilde refererer til en delt tabel undtagen CompanyInfo, returnerer datakilden alle poster, der findes i referencetabellen. 
- Hvis en datakilde refererer til tabellen CompanyInfo, også selvom CompanyInfo er en delt tabel, returnerer datakilden de poster, der indeholder identifikatoren for et firma, fra det angivne område.
- Hvis tabellen er firmaafhængig, returnerer datakilden posterne fra den referencetabel, der indeholder id'et for et firma, fra det angivne område.

I dialogboksen til systemforespørgsel, når indstillingen **Spørg efter forespørgsel** er aktiveret for alle datakilder, der er markeret som værende på tværs af firmaer, kan du manuelt vælge et eller flere firmaer, der skal medtages, under fanen **Regnskabsafgrænsning**.

> [!IMPORTANT]
> Ligesom andre filtre bevares firmafilteret som den sidste anvendte værdi for forespørgsler, når du kører et ER-format. Filteret ændres ikke automatisk, hvis du ændrer værdien på tværs af firmaer for en datakilde. Hvis du vil bruge en anden på tværs af firmaer-værdi til en anden datakilde, skal du slette den tilsvarende brugerspecifikke markering.

For hver datakilde, der er markeret som værende på tværs af firmaer, kan du vælge de poster, du vil, ved hjælp af **FILTER**- og **WHERE**-funktionerne i ER-udtryk. Feltet **dataAreaID** kan også bruges som firma-id. I øjeblikket er feltet **dataAreaID** begrænset til følgende typer betingelser, når **FILTER**-funktionen anvendes:

- Kun de betingelser, der har en enkelt **dataAreaID**-feltsammenligning, understøttes.
- Der tillades kun sammenligninger med udtryk, der ikke afhænger af listeelementer i poster.

Derfor er følgende udtryk gyldigt.

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Området indeholder som standard alle firmaer i det aktuelle program. Det kan dog være begrænset. Du kan begrænse omfanget af dataadgang på tværs af firmaer for et enkelt ER-format ved at tildele et bestemt organisationshierarki til formatet. Når et hierarki er defineret for et ER-format, returneres kun poster for juridiske enheder, der vises i det tildelte hierarki, selvom formatet kalder datakilder på tværs af firmaer. Når en reference til et hierarki, der ikke længere findes, er defineret for et ER-format, anvendes standardområdet, og formatet kalder datakilder på tværs af firmaer. I denne situation returneres poster for alle firmaer i programmet.

Bemærk, at når indstillingen **Brug kladde** er aktiveret for den tildelte til et enkelt organisationshierarki for ER-formatet, bruges de juridiske enheder fra kladdeversionen af dette hierarki, til at identificere området for datakilder på tværs af firmaer. Hvis kladdeversionen ikke findes, bruges de juridiske enheder fra den senest udgivne version af dette organisationshierarki, til denne.

Bemærk, at når indstillingen **Brug kladde** er deaktiveret for den tildelte til et enkelt organisationshierarki for ER-formatet, bruges de juridiske enheder fra den senest udgivne version af dette organisationshierarki, til at identificere området for datakilder på tværs af firmaer. Ikrafttrædelsesdatoer for organisationshierarkier understøttes endnu ikke i ER-strukturen.

Hierarkiet kan tildeles til et format på en bestemt side, der kan åbnes fra ER-arbejdsområdet eller ved hjælp af menupunktet **Virksomhedsadministration \> \> Elektronisk rapportering** Filter med juridisk enhed for formater. For at få adgang til siden skal rettigheden **Vedligehold filtre med juridisk enhed for formater** (ERMaintainFormatMappingLegalEntityFilters) være tildelt til en bruger. Områdebegrænsningen for hierarkibaserede juridiske enheder for formatet anvendes sammen med den begrænsning, som brugeren manuelt kan angive i dialogboksen til systemforespørgsler. Skæringspunktet mellem disse begrænsninger bruges, når formatet køres.

Hvis du vil vide mere om denne funktion, kan du afspille opgaveguiden **ER Åbne poster for firmaafhængige tabeller i en tilstand på tværs af firmaer**, som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10677), og som kan hentes fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Denne opgaveguide fører dig gennem processen med at konfigurere en ER-modeltilknytning og et ER-format for at få adgang til programtabeller i på tværs af firmaer-tilstand.

Hent følgende filer for at fuldføre opgaveguiden:

- [ER-modelkonfiguration - CrossCompanyDataAccessModel.xml](https://download.microsoft.com/download/4/2/5/4258f891-7054-4821-aedd-3721ba25fdd5/CrossCompanyDataAccessModel.xml)
- [ER-formatkonfiguration - CrossCompanyDataAccessFormat.xml](https://download.microsoft.com/download/3/2/1/321deb75-3ba9-4323-99bf-207a52c60b5c/CrossCompanyDataAccessFormat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
