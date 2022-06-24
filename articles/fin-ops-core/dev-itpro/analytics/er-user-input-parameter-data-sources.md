---
title: Bruge datakilder for BRUGERINPUTPARAMETRE til at angive parametre for en rapport
description: Denne artikel forklarer, hvordan du kan bruge datakilder for BRUGERINPUTPARAMETRE til at angive parametre for rapporter, du genererer.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 62b7a8173416a1d36a2985823d186a7a0e6a7e60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872966"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Bruge datakilder for BRUGERINPUTPARAMETRE til at angive parametre for en rapport

[!include[banner](../includes/banner.md)]

Når du designer [Elektronisk rapportering](general-electronic-reporting.md) (ER) som [modeltilknytning](er-overview-components.md#model-mapping-component) og komponenter i ER-[format](er-overview-components.md#format-component), kan du bruge datakilder fra en *BRUGERINPUTPARAMETER*-type til at finde de krævede værdier, der kan angives i dataindtastningsfelterne i dialogboksen under kørslen, før udførelsen af et ER-format begynder. Denne artikel beskriver de datakilder for *BRUGERINPUTPARAMETER*, der aktuelt understøttes.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Obligatoriske egenskaber

Du skal angive følgende egenskaber for datakilder af enhver *BRUGERINPUTPARAMETER*-type:

- Angiv det interne navn på datakilden i feltet **Navn**. Du kan bruge dette navn i andre [udtryk](er-formula-language.md) og bindinger for den konfigurerede modeltilknytning eller formatkomponent.

## <a name="optional-properties"></a><a name="optional-properties"></a>Valgfrie egenskaber

Du kan vælge at angive følgende egenskaber for datakilder af en *BRUGERINPUTPARAMETER*-type:

- I feltet **Navn** skal du angive det navn, der bruges til det relaterede felt til dataindtastning i dialogboksen under kørslen. Du kan tilføje en separat navnetekst til forskellige sprogkoder ved at aktivere feltet **Navn** og derefter vælge **Oversæt**.
- I feltet **Hjælp** skal du angive den hjælpetekst, der vises ved designtid nederst på **Formatdesigner**-siden eller **Modeltilknytningsdesigner**-siden, når der vælges en redigerbar datakilde af typen *BRUGERINPUTPARAMETER*. Denne tekst kan indeholde flere oplysninger om datakilden, som kan hjælpe brugerne med at konfigurere det format eller den modeltilknytningskomponent, der kan redigeres. Du kan tilføje forskellige hjælpetekster til forskellige sprogkoder ved at vælge **Oversæt**.

    > [!NOTE]
    > Knappen **Oversæt**, som du kan bruge til at tilføje [sprogspecifikke navne og tekster](er-design-multilingual-reports.md#format-component), bliver først tilgængelig, når du har tilføjet datakilden, gemt dine ændringer og derefter åbner datakilden igen, så den kan redigeres.

- Konfigurer et udtryk, der returnerer en *[Boolesk](er-formula-supported-data-types-primitive.md#boolean)* værdi, i feltet **Skrivebeskyttet**.

    - Hvis det konfigurerede udtryk returnerer værdien **Sand** ved kørsel, vises det relaterede dataindtastningsfelt nedtonet i dialogboksen, og værdien kan ikke ændres.
    - Hvis det konfigurerede udtryk returnerer værdien **Falsk** ved kørsel, eller hvis intet udtryk er konfigureret, er det relaterede dataindtastningsfelt tilgængeligt i dialogboksen, og værdien kan ændres.

- Konfigurer et udtryk, der returnerer værdien af den parametertype, der refereres til, i feltet **Standardværdi**. Denne værdi kan bruges til at udfylde en standardværdi for det relaterede felt til dataindtastning i dialogboksen under kørslen.

    Når du kører et ER-format, gemmes den værdi, du angiver i det relaterede dataindtastningsfelt i dialogboksen ved kørsel, i hukommelsen som den tidligere anvendte værdi. Tidligere anvendte værdier gemmes individuelt for hvert felt, kørende ER-format, aktuel bruger og aktuel organisation (firma).

    - Angiv indstillingen **Nulstil altid til standardværdi** til **Ja**, hvis den værdi, der returneres af **Standardværdi**-udtrykket, altid skal bruges som standardværdi, uanset hvilken værdi der er anvendt tidligere.
    - Angiv indstillingen **Nulstil altid til standardværdi** til **Nej**, hvis den værdi, der returneres af **Standardværdi**-udtrykket, kun skal bruges som standardværdi, når den tidligere anvendte værdi mangler.

    > [!NOTE]
    > Hvis du angiver indstillingen **Nulstil altid til standardværdi** til **Ja**, skal der konfigureres et udtryk i feltet **Standardværdi**.

- Hvis du angiver indstillingen **Tillad flere valg** til **Ja**, kan du vælge flere værdier for den konfigurerede parameter ved kørsel. Hvis du angiver det til **Nej**, kan du kun vælge en enkelt værdi.

    > [!NOTE]
    > Denne indstilling gælder ikke for alle typer af *BRUGERINPUTPARAMETER*. På designtidspunktet er der en undtagelse, som oplyser brugeren om, at den konfigurerede brugerinputparameter ikke understøtter valg af flere værdier, og at der kun kan vælges eller angives en enkelt værdi.
    >
    > Hvis du angiver indstillingen **Tillad flere valg** til **Ja**, og du har angivet et udtryk i feltet **Standardværdi**, kan det pågældende udtryk kun bruges til at angive en enkelt standardværdi.

- Vælg indstillingen **Rediger synlighed** for at angive, om den konfigurerede parameter skal vises i dialogboksen under kørslen.

    > [!NOTE]
    > Standardsynligheden af datakilder for en *BRUGERINPUTPARAMETER*-type afhænger af den ER-komponent, de findes i.
    >
    > - Hvis en datakilde er konfigureret i formatkomponenten, er den som standard synlig.
    > - Hvis en datakilde er konfigureret i modeltilknytningskomponenten, er den kun synlig, hvis datakildeværdien har indflydelse på udfaldet, når en ER-komponent køres. Du har f.eks. tilføjet en datakilde, men ikke brugt den i udtryk og bindinger fra den aktuelle modeltilknytningskomponent. I dette tilfælde vises det relevante dataindtastningsfelt som standard ikke i dialogboksen under kørslen. 

    På siden **Formeldesigner** skal du i feltet **Formel** konfigurere et udtryk, der returnerer en *boolesk* værdi.

    - Hvis det konfigurerede udtryk returnerer værdien **Sand** ved kørsel, eller hvis intet udtryk er konfigureret, er det relaterede dataindtastningsfelt synligt i dialogboksen ved kørsel.
    - Hvis det konfigurerede udtryk returnerer værdien **Falsk**, skjules det relaterede felt til dataindtastning i dialogboksen under kørslen. Når det kaldes af andre udtryk under kørslen, returnerer det standardværdien, den tidligere anvendte værdi eller standardværdien for den aktuelle datatypeværdi, afhængigt af andre indstillinger.

## <a name="type-specific-properties"></a>Typespecifikke egenskaber

### <a name="application-dependent-user-input-parameter"></a>Programafhængig brugerinputparameter

Brug datakilden af typen **Generelt** \> **Brugerinputparameter** til at få den påkrævede værdi eller de påkrævede værdier af en datatype, som er angivet for den aktuelle forekomst af programmet Microsoft Dynamics 365 Finance. Når du føjer en datakilde af denne type til en ER-komponent, skal du angive følgende egenskaber:

- I feltet **Navn på Operations-datatype (EDT, fasttekst)** skal du vælge et program [udvidet datatype (EDT)](../extensibility/extensible-edts.md) eller en programfasttekst.

> [!NOTE]
> Det anbefales , at du gennemser de udtryk, der er konfigureret i felterne **Skrivebeskyttet** og **Standardværdi**, når du ændrer referencen **Navn på Operations-datatype (EDT, fasttekst)** i en redigerbar datakilde for denne type af *BRUGERINPUTPARAMETER*.

I følgende illustration vises egenskaberne for den `$TaxRegNum`-datakilde, der blev konfigureret i ER-formatkonfigurationen **Instat XML (DE)**. Denne datakilde er konfigureret til at bruge *Beskrivelse*-EDT til at tilbyde dataindtastningsfeltet **SE-nummer** i dialogboksen under kørslen.

![Egenskaberne for en datakilde af typen BRUGERINPUTPARAMETER i dialogboksen på formatdesignersiden.](./media/er-user-input-parameter-data-sources-01.png)

I følgende illustration vises den dialogboks, der vises under kørslen, når ER-formatkonfigurationen **Instat XML (DE)** køres for at [generere](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) Intrastat-opgørelsen. Bemærk, at det konfigurerede felt **SE-nummer** er tilgængeligt for dataindtastning.

![Dialogboksen Intrastat-rapport med det kørende ER-format på Intrastat-siden.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Brugerinputparameter  for fasttekst til datamodel

Brug datakilden af typen **Datamodel** \> **Fasttekst til brugerinputparameter** for at få den ønskede værdi eller værdier af en enkelt datamodels [fasttekst](er-formula-supported-data-types-primitive.md#enumeration). Når du føjer en datakilde af denne type til en ER-komponent, skal du angive følgende egenskaber:

- Angiv en reference til basisdatamodellen i feltet **Model**.
- Angiv en reference til en fasttekst i den datamodel, der refereres til, i feltet **Modelfasttekst**.
- Vælg revisionsnummeret på den ER-datamodelkomponent, der indeholder den refererede modelfasttekst, i feltet **Version**.

    > [!TIP]
    > Når du designer, kan du lade feltet **Version** være tomt, så du kan få adgang til oversigten over fasttekster for den datamodelkomponent, der refereres til, og som findes i kladdeversionen af den tilsvarende ER-datamodelkonfiguration. På denne måde kan du samtidigt redigere kladdeversionen af modeltilknytningen eller formatkomponenten og kladdeversionen af komponenten for basisdatamodellen.
    >
    > Bemærk dog, at feltet **Version** kun kan være tomt i kladdeversionen af en modeltilknytning eller formatkomponent. Når du ændrer status for en ER-modeltilknytning eller formatkonfiguration fra **Kladde** til **Fuldført**, udfyldes dette felt automatisk med det højeste modelrevisionsnummer, der er tilgængeligt i den aktuelle finansforekomst. Hvis du introducerer en ny fasttekst eller en fasttekstværdi i kladdeversionen af basisdatamodellen og refererer til den i den redigerbare komponent til modeltilknytning eller format, skal du fuldføre kladdeversionen af konfigurationen af basisdatamodellen, før kladdeversionen af ER-modeltilknytningen eller formatkonfigurationen fuldføres. Ellers udløses undtagelsen "Stien findes ikke", når du ændrer status for modeltilknytning eller formatkonfiguration fra **Kladde** til **Fuldført**. Meddelelsen fortæller dig, at den fasttekst eller fasttekstværdi, der refereres til, mangler i basisdatamodellen.

I følgende illustration vises egenskaberne for den `$ReportDirection`-datakilde, der blev konfigureret i ER-formatkonfigurationen **Instat XML (DE) Contoso**. Konfigurationen af **Instat XML (DE) Contoso** er [afledt](general-electronic-reporting.md#Configuration) af konfigurationen **Instat XML (DE)**. Denne datakilde er konfigureret til at bruge modelfastteksten *ReportDirection* til at tilbyde det korrekte opslagsfelt i dialogboksen under kørslen.

![Egenskaberne for datakilden af typen BRUGERINPUTPARAMETER i dialogboksen på formatdesignersiden.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Brugerinputparameter  til formatfasttekst

Brug datakilden af typen **Formatfasttekst** \> **Fasttekst til brugerinputparameter** for at få den ønskede værdi eller værdier af en enkelt formatfasttekst. Når du føjer en datakilde af denne type til en ER-komponent, skal du angive følgende egenskaber:

- Udfyld feltet **Formatfasttekst** med en fasttekst i det format, der kan redigeres.

> [!NOTE]
> Datakilder af denne type kan kun konfigureres i området af den formatkomponent, der kan redigeres.

## <a name="additional-resources"></a>Yderligere ressourcer

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Starte datakildeværdier for USER INPUT PARAMETER-typen fra kildekoden](er-initiate-uip-data-source-value-from-source-code.md)
