---
title: Konfigurere opslagsdatakilder til at bruge ER-programspecifikke parametre
description: Denne artikel forklarer, hvordan du kan konfigurere opslagsdatakilder i elektroniske rapporteringsformater (ER) til at bruge ER-programspecifikke parametre.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 193f185e0b7a7183f98bf9aff3fd3e1c4589fb58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892531"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Konfigurere opslagsdatakilder til at bruge ER-programspecifikke parametre 

[!include[banner](../includes/banner.md)]

De ER-programspecifikke parametre til [Elektronisk rapportering](general-electronic-reporting.md) gør det muligt for digt at konfigurere datafiltreringen i et ER-format, så den er baseret på et sæt abstrakte regler. Dette sæt regler kan konfigureres til at bruge de datakilder af typen **Opslag**, der er tilgængelige i et ER-format. Du kan derefter angive de rigtige regler ud over ER-komponentdesigneren ved hjælp af den brugergrænseflade (UI), der genereres automatisk på basis af indstillingerne for datakilden **Opslag** for det tilsvarende ER-format og de aktuelle oplysninger om den juridiske enhed. I den sidste ende får du adgang til de angivne regler i ER-formatets **Opslag**-datakilde, når dette ER-format udføres.

> [!NOTE]
> Brug de konfigurerede datakilder i det redigerbare ER-format for at angive, hvilke programdata der skal bruges til at konfigurere rigtige regler.

Brug [ER-operationsdesigneren](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) til at få datakilden af **Opslag**-typen ind i dit ER-format. Datakilden skal konfigureres til at beskrive, hvordan abstrakte regler ser ud, herunder følgende:

   - Parametersættet for en bestemt datatype, hvis værdi er leveret til angivelse af en enkelt regel.
   - Værditypen for en bestemt datatype, der returneres af en enkelt regel, når denne regel blandt andet betragtes som den mest relevante.

Du kan konfigurere følgende typer **Opslag**-datakilder afhængigt af den type værdi, der returneres af en konfigureret regel:

   - Brug typen **Datamodel\Opslag**, når en modelfasttekstværdi skal returneres.
   - Brug **Dynamics 365 Operations\Opslag**-typen, når en programfasttekstværdi eller en [udvidet datatype](../extensibility/extensible-edts.md) for en programværdi skal returneres.
   - Brug typen **Formatfasttekst\Opslag**, når en formatfasttekstværdi skal returneres.

I følgende illustration vises, hvordan en formatfasttekst kan konfigureres i ER-eksempelformat.

   ![Visning af en formatfasttekst som grundlag for den konfigurerede opslagsdatakilde.](./media/er-lookup-data-sources-img1.gif)

I følgende illustration vises de formatkomponenter, der er konfigureret til at rapportere forskellige typer moms i en anden sektion af en genereret rapport.

   ![Viser formatsektionerne for at rapportere forskellige typer moms separat.](./media/er-lookup-data-sources-img2.png)

I følgende illustration vises, hvordan ER-operationsdesigneren tillader tilføjelse af en datakilde af typen **Formatfasttekst\Opslag**.  Den tilføjede datakilde er konfigureret som en returnering af en værdi af `List of taxation levels`-formatfasttekst.

   ![Tilføjelse af en ER-datakilde af typen Formatfasttekst\Opslag.](./media/er-lookup-data-sources-img3.gif)

I følgende illustration vises, hvordan den tilføjede datakilde er konfigureret til at bruge feltet **Kode** i **Model.Data.Tax**-postlisten for **Model**-datakilden som en parameter, der skal angives for hver konfigureret regel.

![Konfigurere parametre for den tilføjede datakilde for typen Formatfasttekst\Opslag.](./media/er-lookup-data-sources-img4.gif)

Den tilføjede `Model.Data.Tax`-datakilde er konfigureret til at angive en momskode for hver konfigureret regel ved at åbne poster i **TaxTable**-programtabellen.

   ![Gennemgang af enkeltfirmas opslagsdatakilde for typen Formatfasttekst\Opslag.](./media/er-lookup-data-sources-img5.gif)

Du kan oprette opslagsregler for det valgte ER-format i brugergrænsefladen, der automatisk justeres efter strukturen i den konfigurerede datakilde. I øjeblikket kræver denne brugergrænseflade, at du for hver regel både angiver den returnerede værdi som `List of taxation levels`-formatfasttekstværdi og momskoden som en parameter.

   ![Konfigurere regler for den konfigurerede datakilde.](./media/er-lookup-data-sources-img6.gif)

I følgende illustration vises, hvordan `Model.Data.Summary.LevelByLookup`-datakilden for typen **Beregnet felt** kan konfigureres til at kalde den konfigurerede **Opslag**-datakilde, der leverer de påkrævede parametre. For at behandle dette kald under kørslen gennemgår ER listen over konfigurerede regler i den definerede rækkefølge for at finde den første regel, der opfylder de leverede betingelser. I dette eksempel er det reglen, der indeholder den momskode, der svarer til den angivne momskode. Som følge heraf findes den mest relevante regel, og den fasttekstværdi, der er konfigureret for den fundne regel, returneres af denne datakilde.

> [!NOTE]
> En undtagelse opstår, når der ikke findes nogen gældende regel. Du kan forhindre disse undtagelser ved at konfigurere flere regler i slutningen af regellisten, så du kan håndtere sager, når der ikke er angivet en konfigureret værdi. Brug indstillingerne **\*Ikke tom**\* og **\*Tom**\* i overensstemmelse hermed.  
>
> ![Tilføje en datakilde for at kalde den konfigurerede opslagsdatakilde.](./media/er-lookup-data-sources-img7.png)

Når du angiver indstillingen **På tværs af firma** til **Ja** for den opslagsdatakilde, der kan redigeres, føjer du en ny påkrævet **Firma**-parameter til parametersættet for denne datakilde. Værdien af parameteren **Firma** skal angives ved kørsel, når opslagsdatakilden kaldes. Når firmakoden angives under kørslen, bruges de regler, der er konfigureret for dette firma, til at finde den regel, der passer bedst, og den tilsvarende værdi returneres. I følgende illustration vises, hvordan du kan gøre dette, og hvordan parametersættet for den redigerbare datakilde ændres.

   ![Gennemgang af flere firmaers opslagsdatakilde for typen Formatfasttekst\Opslag.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Vælg hvert firma separat for at konfigurere regelsættet for denne opslagsdatakilde i det redigerbare ER-format. En undtagelse opstår under kørslen, når opslag på tværs af firmaer kaldes med koden for det firma, som opslagsindstillingen ikke er fuldført for.
>
> Sørg for at give tilladelser til en bruger, der kører ER-formatet med datakilden **Opslag** på tværs af firmaer, for at få adgang til data fra alle de firmaer, der findes i området for denne datakilde. Ellers sker der en undtagelse på kørselstidspunktet.

Fra og med version 10.0.19 er de udvidede funktioner i **Opslag**-datakilderne tilgængelige. Når du angiver indstillingen **Udvidet** til **Ja** for den opslagsdatakilde, der kan redigeres, konverteres den konfigurerede opslagsdatakilde til den strukturerede datakilde, der indeholder de ekstra egenskaber, så det konfigurerede sæt regler analyseres. Følgende illustration viser denne transformation.

   ![Gennemgang af struktureret opslagsdatakilde for typen Formatfasttekst\Opslag.](./media/er-lookup-data-sources-img9.gif)

- Underelementet **Opslag** er designet som en funktion til at finde den mest relevante regel fra sættet af konfigurerbare regler baseret på de angivne parametre.
- Underelementet **IsLookupResultSet** er designet som en funktion til at acceptere den angivne værdi af den grundlæggende fasttekstdatakilde og returnere den *Booleske* værdi af **Sand**, når regelsættet indeholder mindst én regel, som den angivne fasttekstværdi er konfigureret som en returværdi for. Denne funktion returnerer den *Booleske* værdi af **Falsk**, når der ikke er konfigureret regler for returnering af den angivne fasttekstværdi.
- Underelementet **Indstilling** er designet som en funktion, der returnerer sættet med konfigurerede regler som poster på en postliste. De returnerede værdier og parametersættet i de konfigurerede regler præsenteres i alle returnerede poster som felter af de relevante datatyper:

    - Den returnerede værdi vises som feltet **Opslagsresultat**.
    - De konfigurerede parametre vises som felter med navne på parametre (**Kode**-felt i dette eksempel).

Du kan finde flere oplysninger om, hvordan du konfigurerer **Opslag**-datakilden, i [Konfigurere ER-formater til at bruge parametre, der er angivet for hver juridiske enhed](er-app-specific-parameters-configure-format.md). Du kan få mere at vide om, hvordan du konfigurerer opslagsreglerne, i [Konfigurere parametrene for et ER-format pr. juridiske enhed](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere ER-formater til at bruge de parametre, der er angivet for den enkelte juridiske enhed](er-app-specific-parameters-configure-format.md)

[Konfigurere parametrene for et ER-format for hver juridisk enhed](er-app-specific-parameters-set-up.md)
