---
title: Understøtte parameteriserede kald af ER-datamodeller
description: Denne artikel forklarer, hvordan du implementerer parameteriserede kald af ER-datamodeller (elektronisk rapportering).
author: kfend
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
ms.openlocfilehash: 5be189c19d963991ec012de189bbf7b721b88fef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275982"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Understøtte parameteriserede kald af ER-datamodeller

[!include [banner](../includes/banner.md)]

For at generere forretningsdokumenter skal du konfigurere en [ER-løsning](general-electronic-reporting.md) (elektronisk rapportering), der indeholder følgende ER-komponenter:

- **[Format](er-overview-components.md#format-component)** – Denne komponent angiver strukturen i et forretningsdokument.
- **Formattilknytning** – Denne komponent styrer, hvordan et forretningsdokument udfyldes under kørslen.
- **[Modeltilknytning](er-overview-components.md#model-mapping-component)** – Denne komponent angiver, hvad dataene trækker ud fra programmet til en formattilknytning.
- **[Datamodel](er-overview-components.md#data-model-component)** – Denne komponent sender oplysninger mellem de enkelte komponenter.

Når du kører et ER-format, køres alle formatelementer med udgangspunkt i rodformatelementet. Når et formatelement, der køres, indeholder en binding til en [datakilde](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents), køres datakilden for at levere de forventede data og bruge dem til at udfylde formatelementet. Når datakilden for *Model*-typen kaldes, kaldes den relevante modeltilknytning for at trække data ud af programmet på baggrund af indstillingerne for modeltilknytning.

Tidligere kunne disse modeltilknytningskald ikke parameteriseres, så de var afhængige af logikken i det format, der køres. Kun følgende dataflow blev understøttet.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Formatelement<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;anmodning&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;&lt;
</td>
<td><b>Formattilknytning</b><br>
Datakilde<br>
&nbsp;
</td>
<td>
<i>Datamodel</i><br>
&gt;&nbsp;anmodning&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;&lt;
</td>
<td>
<b>Modeltilknytning</b><br>
Datakilde<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;anmodning&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;&lt;
</td>
<td>
<b>Tabellen</b><br>
Post<br>
Felt
</td>
</tr>
</tbody>
</table>

Men i version 10.0.15 og senere kan du konfigurere datamodelfelter, der kun kan kaldes, når værdierne for de konfigurerede parametre er angivet. Når et sådant felt konfigureres og kaldes fra en formatkomponent, skal de påkrævede parametre angives i en formatbinding som argumenter i kaldet. I disse tilfælde kan værdierne for argumenterne angives på grundlag af formatspecifikke værdier. Du kan derfor bruge **dynamisk kørselsparameterisering** til datamodelkald for at understøtte følgende dataflow.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Formatelement&nbsp;1<br>
<br>
Formatelement&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;anmodning&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;anmodning&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Formattilknytning</b><br>
Datakilde&nbsp;1<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Datamodel</i><br>
&gt;&nbsp;field1&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;værdi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Modeltilknytning</b><br>
Datakilde&nbsp;1<br>
<br>
Datakilde&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;anmodning&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;anmodning&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;værdi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tabel&nbsp;1</b><br>
Post&nbsp;1<br>
Felt&nbsp;1<br>
<b>Tabel&nbsp;2</b><br>
Post&nbsp;2<br>
Felt&nbsp;2
</td>
</tr>
</tbody>
</table>

Den nye funktionalitet giver dig mulighed for at parameterisere kaldet til ethvert datamodelfelt i [*Post*](er-formula-supported-data-types-composite.md#record)- eller [*Postliste*](er-formula-supported-data-types-composite.md#record-list)-typen. Følgende datatyper understøttes til parametrene i et datamodelfelt:

- [Boolesk](er-formula-supported-data-types-primitive.md#boolean)
- [Container](er-formula-supported-data-types-composite.md#container)
- [Dato](er-formula-supported-data-types-primitive.md#date)
- [Dato/klokkeslæt](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Heltal](er-formula-supported-data-types-primitive.md#integer)
- [Kommatal](er-formula-supported-data-types-primitive.md#real)
- [Streng](er-formula-supported-data-types-primitive.md#string)

Du kan angive hver parameter i et datamodelfelt, hvor der kan angives et argument som en enkelt værdi af den definerede datatype og [*listen*](er-formula-supported-data-types-composite.md#record-list) over disse værdier.

> [!NOTE]
> Standardværdien for parameteren i et datamodelfelt understøttes ikke. Hvis du føjer en parameter til et felt i en datamodel, og versionen af den pågældende datamodel allerede er frigivet og udgivet, skal du [rebasere](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) alle tilsvarende modeltilknytninger og -formater til den nye version af denne model, da denne datamodel ikke er bagudkompatibel.

Du kan konfigurere de parameteriserede datamodelfelter, så modeltilknytningskald bliver formatspecifikke. Denne metode kan hjælpe dig med at reducere antallet af modeltilknytninger, der skal konfigureres for mange formater af en enkelt datamodel. Du kan også bruge denne metode til at forbedre ydeevnen af udførelsen af dine formater og reducere den tid, der kræves til at generere forretningsdokumenter. Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i denne artikel.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Eksempel: Bruge parameteriserede kald af ER-datamodeller

I følgende fremgangsmåde forklares det, hvordan en bruger i rollen Systemadministrator eller Elektronisk rapporteringsudvikler kan designe en ER-løsning, der indeholder en datamodel, en modeltilknytning og en ER-formatkomponent, der er konfigureret til at kalde en modeltilknytning fra et format ved at angive et argument for kaldet, hvis værdi er beregnet ved kørsel ved hjælp af formlen i det kørende format. 

Disse trin kan udføres i **DEMF**-virksomheden. Der kræves ingen kodeændringer. 

I dette eksempel opretter du de krævede ER-[konfigurationer](general-electronic-reporting.md#Configuration) for **Litware, Inc.**- eksempelvirksomheden. Sørg for, at konfigurationsudbyderen for eksempelfirmaet **Litware, Inc.** (`http://www.litware.com`) er angivet for ER-strukturen og er markeret som **Aktiv**. Hvis denne konfigurationsudbyder ikke er angivet, eller hvis den ikke er markeret som **Aktiv**, skal du følge trinnene i emnet [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Forretningsscenarie

Du har en ER-løsning, der omfatter et format, du kan køre for at generere et elektronisk dokument til revisionsbrug. Dette format indeholder momstransaktioner, der er relateret til salgsordrer og indkøbsordrer, og som indeholder de nødvendige oplysninger som f.eks. posteringsdato og momsværdi. Fra og med det nye regnskabsår er strukturen i dette dokument ændret. Du skal nu indsende et udvidet dokument, der indeholder flere detaljer (navne) for alle parter (debitorer og kreditorer), hvis posteringer vises i genererede rapporter. Du skal derfor ændre ER-løsningen, så den genererer dokumenter, der overholder dette nye krav.

### <a name="configure-the-er-framework"></a>Konfigurere ER-strukturen

Følg trinnene i [Konfigurere ER-strukturen](er-quick-start2-customize-report.md#ConfigureFramework) for at konfigurere det minimale sæt af ER-parametre. Du skal fuldføre denne opsætning, før du begynder at bruge ER-strukturen til at designe en ny ER-løsning.

### <a name="design-a-domain-specific-data-model"></a>Designe en domænespecifik datamodel

Du skal oprette en ny ER-konfiguration, der indeholder den påkrævede komponent til datamodellen. Denne datamodel vil senere blive brugt som en datakilde, når du designer et ER-format til at generere en revisionsrapport.

Følg disse trin for at importere den påkrævede datamodel fra en XML-fil, der leveres af Microsoft.

1. Download filen [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Gå til siden **Konfigurationer**, og vælg **Kurs** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Sample audit model.version.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

    ![Importeret ER-datamodelkonfiguration på siden Konfigurationer.](./media/er-data-model-parameterized-calls-imported-model.png)

I følgende illustration vises den redigerbare version af den konfigurerede datamodel på siden **Datamodeldesigner**.

![ER-datamodellens struktur på datamodeldesignersiden.](./media/er-data-model-parameterized-calls-model1.png)

Aktuelt er modellen designet til kun at vise momstransaktioner, der har de nødvendige oplysninger.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Designe en modeltilknytning for den konfigurerede datamodel

Som bruger i rollen Udvikler af elektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for modeltilknytning til datamodellen for eksempelrevision. Denne komponent implementerer den konfigurerede datamodel for Microsoft Dynamics 365 Finance og er specifik for denne app. Du skal konfigurere komponenten for modeltilknytning for at angive de applikationsobjekter, der skal bruges til at udfylde den konfigurerede datamodel med applikationsdata under kørsel. For at fuldføre denne opgave skal du vide, hvordan datastrukturen i momsforretningsdomænet er implementeret i Finans.

Følg disse trin for at importere den påkrævede modeltilknytning fra en XML-fil, der leveres af Microsoft.

1. Download filen [Sample audit model mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Gå til siden **Konfigurationer**, og vælg **Kurs** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Sample audit model mapping.version.1.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

    ![Importeret konfiguration af ER-modeltilknytning på siden Konfigurationer.](./media/er-data-model-parameterized-calls-imported-mapping.png)

I følgende illustration vises den redigerbare version af den konfigurerede modeltilknytning på siden **Modeltilknytningsdesigner**.

![ER-modeltilknytningens struktur på siden Modeltilknytningsdesigner.](./media/er-data-model-parameterized-calls-mapping1.png)

Aktuelt er modeltilknytningen designet til kun at vise momstransaktioner, der har de nødvendige oplysninger. Disse oplysninger hentes fra programtabellen `TaxTrans` ved hjælp af de konfigurerede ER-datakilder `TaxTrans` og `TaxTransFiltered`.

### <a name="design-a-new-format"></a>Designe et nyt format

Som bruger med rollen Funktionel konsulent i elektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for format. Du skal konfigurere formatkomponenten til at udfylde genererede rapporter med momstransaktioner, der har alle de nødvendige oplysninger.

Følg disse trin for at importere det påkrævede format fra en XML-fil, der leveres af Microsoft.

1. Download filen [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml), og gem den på din lokale computer.
2. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
3. I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.
4. Gå til siden **Konfigurationer**, og vælg **Kurs** \> **Indlæs fra XML-fil** i handlingsruden.
5. Vælg **Gennemse**, og find og vælg derefter filen **Sample audit format.version.1.1.xml**.
6. Vælg **OK** for at importere konfigurationen.

    ![Importeret ER-formatkonfiguration på siden Konfigurationer.](./media/er-data-model-parameterized-calls-imported-format.png)

I følgende illustration vises den redigerbare version af det konfigurerede format på siden **Formatdesigner**.

![ER-formatets struktur på siden Formatdesigner.](./media/er-data-model-parameterized-calls-format1.png)

ER-formatet er konfigureret til at generere en rapport som en tekstfil i csv-format (kommaseparerede værdier).

### <a name="run-the-imported-format"></a>Kør det importerede format

1. Vælg konfigurationen af **eksempelrevisionsformatet** på siden **Konfigurationer**, og vælg derefter **Kør** i handlingsruden.
2. Vælg **Filter** i dialogboksen **Parametre for elektronisk rapport** under fanen **Poster, der skal medtages**.
3. Angiv betingelserne for valg af momstransaktioner for bilag **PIV-110000004** og **INV-10000001**.
4. Vælg **OK**.
5. Vælg **OK**.
6. Gennemse det genererede dokument, der indeholder momstransaktioner for de valgte bilag.

    ![Eksempelvisning af det genererede dokument med momstransaktioner.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Regulere den importerede ER-løsning

Ifølge det nye krav skal det dokument, du skal indsende, indeholde navnene på de debitorer og kreditorer, hvis transaktioner er medtaget. Du skal derfor ændre den importerede ER-løsning, så den genererer et dokument, der overholder dette nye krav.

Beslut, hvordan du vil implementere de nødvendige ændringer af de importerede ER-komponenter.

Den indlysende metode er at implementere følgende ændringer:

- Tilføj det nye datamodelfelt `Transaction.Party.Name` af typen *Streng* i datamodellen.
- I modeltilknytningen skal du konfigurere bindingen for det nye datamodelfelt ved at bruge tilgængelige tabelrelationer for at få adgang til den relevante post i programtabellen `DirPartyTable` og hente værdien af feltet `Name` fra den.

Selvom denne metode vil fungere, kan det medføre problemer med ydeevnen i SQL-databasen, da `TaxTrans` er transaktionstabellen, og den kan derfor indeholde et stort antal poster. I dette tilfælde skal antallet af kald til `DirPartyTable` være lig med antallet af poster i tabellen `TaxTrans`, som kan forårsage problemer med ydeevnen.

Du kan også implementere følgende ændringer:

- Tilføj den nye rod `Party` og det nye felt `Party.Name` i datamodellen .
- I modeltilknytningen skal du tilføje en ny datakilde , der kan knytte alle de poster i tabeller, der bruges i tabelrelationer, til at få adgang til den relevante post i programtabellen `DirPartyTable` med start fra tabellen `TaxTrans`.

Selvom denne metode vil fungere, kan det medføre problemer med forbruget af hukommelse. Selv når en ny [JOIN](er-join-data-sources.md)-datakilde køres som en enkelt SQL-anmodning til programdatabasen for at forhindre problemer med databasens ydeevne, skal resultatet hentes til hukommelsen på programserveren. Da antallet af poster og antallet af felter i disse poster er meget stort, kan denne metode forårsage meget stort hukommelsesforbrug. En kørselsundtagelse med ikke mere hukommelse kan endog opstå.

Du kan implementere ændringerne, når et kørende format indsamler i hukommelsen de entydige identifikationskoder for debitorer og kreditorer for alle momstransaktioner, der vil blive vist i en genereret rapport. Da det kun er entydige koder, der skal opbevares, er det endelige sæt koder ikke stort nok til at påvirke forbruget af hukommelse. Sættet med koder overføres derefter til modeltilknytning som argumentet for et andet kald af datakilden for *Model*-typen. På baggrund af dette kald kører modeltilknytningen en ny ER-datakilde, der opretter en enkelt SQL-anmodning til programdatabasen om kun at hente poster fra tabellen `DirPartyTable` for de parter, hvis koder findes i det angivne sæt af koder.

### <a name="adjust-the-imported-data-model"></a>Regulere den importerede datamodel

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude vælge **Eksempelrevisionsmodel**.
3. I oversigtspanelet **Versioner** skal du vælge version **2**, der har status af **Kladde**.
4. Vælg oversigtspanelet **Konfigurationskomponenter**.
5. Vælg **Designer** for at åbne datamodellen til redigering.
6. Sørg for, at feltet `Root` er markeret, og vælg derefter **Ny** på siden **Datamodel**.
7. Følg disse trin i rulledialogboksen:

    1. Vælg indstillingen **Underordnet for en aktiv node** i feltgruppen **Ny node som**.
    2. I feltet **Navn** skal du angive **Part**.
    3. Vælg **Liste over poster** i feltet **Varetype**.
    4. Vælg **Tilføj** for afslutte tilføjelsen af det nye felt.

8. Sørg for, at feltet `Root.Party` er markeret, og vælg derefter **Parametre** under fanen **Node**.
9. Følg disse trin i dialogboksen **Parametre**:

    1. Vælg **Ny** under fanen **Parametre**.
    2. I feltet **Navn** skal du angive **PartyRefRecId**.
    3. I **Type**-feltet skal du vælge **Int64**.
    4. Markér afkrydsningsfeltet **Liste**.
    5. Vælg **OK** for at afslutte angivelsen af parametrene.

    > [!NOTE]
    > Du har lige konfigureret datamodelfeltet `Root.Party` som et felt, der kaldes, når der angives en værdi i parameteren **PartRefRecId**. Denne værdi skal findes på listen over poster, der indeholder et `Value`-felt af datatypen *Int64*.

    ![Dialogboksen Parametre.](./media/er-data-model-parameterized-calls-model2a.png)

10. Kontrollér, at feltet `Root.Party` stadig er valgt, og vælg derefter **Ny**.
11. Følg disse trin i rulledialogboksen:

    1. Vælg indstillingen **Underordnet for en aktiv node** i feltgruppen **Ny node som**.
    2. Angiv **Navn** i feltet **Navn**.
    3. Vælg **Streng** i feltet **Varetype**.
    4. Vælg **Tilføj** for afslutte tilføjelsen af det nye felt.

12. Vælg **Gem**, og luk derefter siden **Datamodel**.

    ![ER-datamodellens struktur er justeret på datamodeldesignersiden.](./media/er-data-model-parameterized-calls-model2b.png)

13. I oversigtspanelet **Versioner** skal du for version **2** vælge **Skift status** \> **Fuldfør**. Vælg derefter **OK**.

    > [!NOTE]
    > Ændringerne i datamodellen gemmes i den anden revision af datamodelkomponenten **Eksempelrevisionsmodel**, som findes i den anden version af ER-konfigurationen **Eksempelrevisionsmodel**.

![Opdateret ER-datamodelkonfiguration på siden Konfigurationer.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Justere den importerede modeltilknytning

1. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Eksempelrevisionsmodel**.
2. Vælg **Modeltilknytning af eksempelrevision**, og vælg derefter i oversigtspanelet **Versioner** den anden tilknytningsversion, der er baseret på den første datamodelversion (version **1.2**), og som har statussen **Kladde**.
3. Vælg **Rebaśer**.
4. I feltet **Målversion** skal du bevare version **2** af basismodellen **Eksempelrevisionsmodel**.
5. Vælg **OK** for at rebasere og justere modeltilknytningen med de seneste datamodelændringer.

    Bemærk, at versionsnummeret for din redigerbare modeltilknytning er ændret fra **1.2** til **2.2** for at angive, at den anden modelversion aktuelt bruges som base.

6. Vælg **Designer**.
7. Vælg **Designer** på siden **Tilknytning af model til datakilde** for den aktuelle modeltilknytning.
8. Benyt følgende fremgangsmåde for at tilføje en ny datakilde for at få adgang til programtabellen `DirPartyTable`:

    1. Vælg **Dynamics 365 for Operations \> Tabelposter** i ruden **Datakildetyper**.
    2. Vælg **Tilføj rod** i ruden **Datakilder**.
    3. I feltet **Navn** skal du angive **PartyTable**.
    4. Indtast **DirPartyTable** i feltet **Tabel**.
    5. Vælg **OK** for at tilføje den nye datakilde.

9. Benyt følgende fremgangsmåde for at tilføje en ny datakilde til `DirPartyTable`-anmodningsposter baseret på den angivne liste over postidentifikationskoder:

    1. I ruden **Datakildetype** skal du vælge **Generelt \> Tom container**.
    2. Vælg **Tilføj rod** i ruden **Datakilder**.
    3. Angiv **Data** i feltet **Navn**.
    4. Vælg **OK** for at tilføje den nye datakilde.
    5. Vælg datakilden **Data** i ruden **Datakilder**.
    6. Vælg **Funktioner \> Beregnet felt** i ruden **Datakildetype**.
    7. Vælg **Tilføj** i ruden **Datakilder**.
    8. Angiv **DirParty** i feltet **Navn**.
    9. Vælg **Rediger formel**.
    10. Vælg **Parametre** på siden **Formeldesigner**.
    11. Følg disse trin i dialogboksen **Parametre**:

        1. Vælg **Ny** under fanen **Parametre**.
        2. Angiv **DirPartyId** i feltet **Navn**.
        3. I **Type**-feltet skal du vælge **Int64**.
        4. Markér afkrydsningsfeltet **Liste**.
        5. Vælg **OK**.

        > [!NOTE]
        > Du har lige konfigureret dette beregnede felt, så det under kørslen accepterer argumenterne for en enkelt parameter , der er konfigureret som en postliste, der indeholder et enkelt `Value`-felt af typen *Int64*.

    12. Angiv følgende udtryk i feltet **Formel**:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Du har lige konfigureret det beregnede felt `DirParty` til kun at hente `DirPartyTable`-poster, hvor postidentifikationskoderne er medtaget på den `DirPartyId`-liste, der vises som argument, når feltet `DirParty` kaldes.

        ![Formel til hentning af partnavne fra programtabellen på formeldesignersiden.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Vælg **Gem**, og luk derefter siden **Formeldesigner**.
    14. Vælg **Gem**, og vælg derefter **OK** for at afslutte tilføjelsen af den nye datakilde.

10. Benyt følgende fremgangsmåde for at forbinde den nye datakilde med det nye datamodelfelt, så datamodellen bruges til at vise partnavne:

    1. I ruden **Datamodel** skal du vælge datamodelfeltet `Root.Party`.
    2. Vælg **Rediger** i ruden **Datamodel**.
    3. På siden **Formeldesigner** skal du i feltet **Formel** angive udtrykket `Data.DirParty(PartyRefRecId)`.
    4. Vælg **Gem**, og luk derefter siden **Formeldesigner**.

        > [!NOTE]
        > Du har lige konfigureret bindingen til at kalde den konfigurerede `Data.DirParty`-datakilde og angive listen over postidentifikationskoder, der vil blive angivet i formatet, når datamodelfeltet `Root.Party` kaldes.

    5. I ruden **Datamodel** skal du vælge datamodelfeltet `Root.Party.Name`.
    6. Vælg **Rediger** i ruden **Datamodel**.
    7. På siden **Formeldesigner** skal du i ruden **Datakilde** udvide **Data \> DirParty** og vælge **Navn**.
    8. Vælg **Tilføj datakilde**.
    9. Vælg **Gem**, og luk derefter siden **Formeldesigner**.

    ![ER-modeltilknytningens justerede struktur på siden Modeltilknytningsdesigner.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Vælg **Gem**, og luk siden **Modeltilknytningsdesigner**.
12. Luk siden **Tilknytning af model til datakilde**.
13. I oversigtspanelet **Versioner** skal du for version **2.2** vælge **Skift status \> Fuldfør**. Vælg derefter **OK**.

### <a name="adjust-the-imported-format"></a>Justere det importerede format

1. På siden **Konfigurationer** skal du vælge **Eksempelrevisionsformat**.
2. I oversigtspanelet **Versioner** skal du vælge version **1.2**, der har status af **Kladde**.
3. Vælg **Rebaśer**.
4. I feltet **Målversion** skal du bevare version **2** af basismodellen **Eksempelrevisionsmodel**.
5. Vælg **OK** for at rebasere og justere formatet med de seneste datamodelændringer.
6. Vælg **Designer**.
7. Vælg **Udvid/skjul** i formatstrukturtræet i venstre rude på siden **Formatdesigner**.
8. Benyt følgende fremgangsmåde for at tilføje et nyt formatelement for at indsamle postidentifikationskoder for parter, hvis transaktioner vises i genererede rapporter.

    1. Vælg sekvenselementet **Report.Row.Trans** i formatstrukturtræet.
    2. Vælg **Tilføj**.
    3. I dialogboksen **Tilføj** skal du vælge **Datakilde \> Vare**.
    4. I dialogboksen **Komponentegenskaber** skal du i feltet **Navn** angive **Id**.
    5. Vælg **Int64** i feltet **Datatype**.
    6. Vælg **OK**.

    > [!NOTE]
    > Et element til **Datakilde \> Vare** kan kun bruges til at udføre interne beregninger og datatransformation inden for området af det kørende format. Når du tilføjer dette formatelement, ændrer du derfor ikke indholdet af et genereret dokument.

9. Benyt følgende fremgangsmåde for at tilføje nye formatelementer til indtastning af partnavne i genererede rapporter:

    1. Vælg sekvenselementet **Report.Row**.
    2. Vælg **Tilføj**.
    3. I dialogboksen **Tilføj** skal du vælge **Tekst \> Sekvens**.
    4. I dialogboksen **Komponentegenskaber** skal du i feltet **Navn** angive **Part**.
    5. Vælg **OK**.
    6. Vælg sekvenselementet **Report.Row.Party**.
    7. Vælg **Tilføj**.
    8. I dialogboksen **Tilføj** skal du vælge **Tekst \> Streng**.
    9. I dialogboksen **Komponentegenskaber** skal du i feltet **Navn** angive **Navn**.
    10. Vælg **OK**.

10. Benyt følgende fremgangsmåde for at tilføje en ny datakilde for at indsamle postidentifikationskoder for parter, hvis transaktioner vises i genererede rapporter:

    1. Under fanen **Tilknytning** skal du vælge **Tilføj rod**.
    2. I dialogboksen **Tilføj datakilde** skal du vælge **Funktioner \> Dataindsamling**.
    3. Angiv **PartyIds** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for dataindsamling**.
    4. Vælg **Int64** i feltet **Varetype**.
    5. Vælg **OK**.

11. Benyt følgende fremgangsmåde for at tilføje en ny binding for at indsamle postidentifikationskoder for parter, hvis transaktioner vises i genererede rapporter:

    1. Vælg datavareelementet **Report.Row.Trans.Id** i formatstrukturtræet.
    2. Vælg **Rediger formel**.
    3. Angiv udtrykket `PartyIds.Collect(model.Transaction.Party.RecId)` på siden **Formeldesigner**.
    4. Vælg **Gem**, og luk derefter siden **Formeldesigner**.

12. Benyt følgende fremgangsmåde for at tilføje nye bindinger til indtastning af partnavne i genererede rapporter:

    1. Vælg sekvenselementet **Report.Party** i formatstrukturtræet.
    2. Vælg **Rediger formel**.
    3. Angiv udtrykket `model.Party(PartyIds.Result)` på siden **Formeldesigner**.
    4. Vælg **Gem**, og luk derefter siden **Formeldesigner**.
    5. Vælg sekvenselementet **Report.Party.Name** i formatstrukturtræet.
    6. Under fanen **Tilknytning** skal du vælge datamodelfeltet `model.Party.Name`.
    7. Vælg **Bind**.

    ![ER-formatets justerede struktur på siden Formatdesigner.](./media/er-data-model-parameterized-calls-format2.png)

13. Vælg **Gem**, og luk siden **Formatdesigner**.
14. Luk siden **Tilknytning af model til datakilde**.
15. I oversigtspanelet **Versioner** skal du for version **2.2** vælge **Skift status** \> **Fuldfør**. Vælg derefter **OK**.

### <a name="run-the-adjusted-format"></a>Kør det justerede format

1. Vælg **Eksempelrevisionsformat** på siden **Konfigurationer**, og vælg derefter **Kør** i handlingsruden.
2. Vælg **Filter** i dialogboksen **Parametre for elektronisk rapport** under fanen **Poster, der skal medtages**.
3. Angiv betingelserne for valg af momstransaktioner for bilag **PIV-110000004** og **INV-10000001**.
4. Vælg **OK**.
5. Vælg **OK**.
6. Gennemse det genererede dokument, der indeholder momsposteringer på de valgte bilag, samt navnene på den tilsvarende debitor og kreditor.

    ![Eksempelvisning af det genererede dokument med momstransaktioner og partnavne.](./media/er-data-model-parameterized-calls-output2.png)

7. Gå til **Kreditor** \> **Kreditorer** \> **Alle kreditorer**, og gennemse oplysningerne i det valgte **PIV-110000004**-bilag, herunder kreditornavnet.

    ![Gennemgå oplysninger om købsbilag på siderne Alle kreditorer og Fakturakladde.](./media/er-data-model-parameterized-calls-review1.gif)

8. Gå til **Debitor** \> **Debitorer** \> **Alle debitorer**, og gennemse oplysningerne i det valgte **INV-10000001**-bilag, herunder debitornavnet.

    ![Gennemgå oplysninger om salgsbilag på siderne Alle debitorer og Bogført moms.](./media/er-data-model-parameterized-calls-review2.gif)

Du kan få flere oplysninger om denne udførelse af ER-løsningen ved at bruge den indbyggede [ER-performancesporing](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt](er-calculated-field-type.md)
- [Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)
- [Bruge datakilder for DATAINDSAMLING i elektroniske rapporteringsformater](er-data-collection-data-sources.md)
- [ER-funktionen ValueInLarge](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
