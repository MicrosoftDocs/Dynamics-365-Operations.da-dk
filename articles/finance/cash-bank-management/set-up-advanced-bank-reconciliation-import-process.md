---
title: Konfigurere importprocessen for avanceret bankafstemning
description: Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Microsoft Dynamics 365 Finance. I denne artikel beskrives, hvordan du konfigurerer importfunktionen for dine kontoudtog fra banken.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60195962e50817b4d85840a2464848db6e666f46
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716012"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Konfigurere importprocessen for avanceret bankafstemning

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Denne funktion udfases i september 2022, og nye brugere skal bruge elektronisk rapportering. Der er yderligere oplysninger i [Konfigurere importprocessen for avanceret bankafstemning vha. elektronisk rapportering](../accounts-payable/import-bai2-er.md).


Med den avancerede bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Dynamics 365 Finance. I denne artikel beskrives, hvordan du konfigurerer importfunktionen for dine kontoudtog fra banken. 

Konfigurationen for import af bankkontoudtog varierer afhængigt af formatet på dit elektroniske bankkontoudtog. Finance understøtter tre standardformater for bankkontoudtog: ISO20022, MT940 og BAI2.

## <a name="set-time-zone-preference"></a>Angive foretrukken tidszone
Når du konfigurerer importindstillingerne for bankkontoudtog, kan det være vigtigt at overveje tidszonen for dato- og klokkeslætsdata i de filer med bankkontoudtog, der skal importeres. Standarden er at antage, at eventuelle dato- og klokkeslætsværdier er i UTC (Coordinated Universal Time), så der ikke anvendes tidszonekonvertering, når du importerer dataene. 

Der findes en indstilling, der angiver, at der skal bruges en tidszone til import af data. Denne indstilling er tilgængelig i feltet **Foretrukket tidszone** på hver side med **oplysninger om kildedataformat** (**Arbejdsområdet Datastyring > Konfigurer datakilder > Vælg et dataformat > oversigtspanelet Internationale indstillinger**). Denne tidszoneindstilling, som du angiver, gælder for alle de Importer, der bruger det pågældende kildedataformat. Du kan oprette lige så mange datakildeformater, der er brug for til at importere data fra flere tidszoner.  

Denne tidszone kan være den samme som brugerens eller firmaets tidszone, så du skal være sikker på, hvilken tidszone dato- og klokkeslætsdataene bruger. Vi anbefaler, at du overvejer følgende punkter, når du angiver en indstilling for tidszone. 

 - Denne tidszoneindstilling gælder for alle de importer, der bruger det pågældende kildedataformat. Du kan oprette lige så mange datakildeformater, der er brug for, til at importere data fra flere tidszoner. 
 
 - Indstillingen for tidszone skal være den lokale tidszone for dato- og klokkeslætsdataene i importfilen. 
 
 - Tidszonen for dato- og klokkeslætsdata er muligvis ikke den samme som brugerens eller firmaets tidszone.
 
 - Brugerne kan justere deres egen tidszone ved hjælp af deres **Brugerindstillinger**.

Bemærk, at følgende handlinger kan hjælpe med at minimere mulige dato- og tidskonflikter, når du importerer bankkontoudtog. 

 - Undgå at ændre tidszoneindstillingerne for eventuelle bankkonti, hvor der allerede er importeret bankkontoudtog. Hvis du ændrer tidszoneindstillingen, kan det påvirke rækkefølgen af nye kontoudtog i forhold til eksisterende kontoudtog på grund af tidszonejustering. 
 
 - Gennemse alle de importer, der bruger det valgte datakildeformat. Den tidszoneindstilling, der er angivet for formatet, gælder for alle de importprojekter, der bruger det pågældende format. Få bekræftet, at tidszoneindstillingen er passende for alle de importprojekter, der bruger det pågældende format.

## <a name="sample-files"></a>Eksempelfiler
For alle tre formater skal du have filer, der oversætter det elektroniske bankkontoudtog fra det oprindelige format til et format, der kan bruges af Finance. Du kan finde de nødvendige ressourcefiler under noden **Ressourcer** i Application Explorer i Microsoft Visual Studio. Når du har fundet filerne, skal du kopiere dem til en enkelt kendt placering, så du nemmere kan overføre dem under konfigurationsprocessen.

| Ressourcenavn                                           | Filnavn                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoudtogsformater og tekniske layout
Nedenfor vises eksempler på avancerede definitioner af teknisk layout for bankafstemnings importfil og tre relaterede eksempelfiler på bankkontoudtog: [Import af fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Teknisk layoutdefinition                             | Eksempelfil med bankkontoudtog          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Konfigurere importen af ISO20022-bankkontoudtog
Først skal du definere behandlingsgruppen for bankkontoudtogsformatet for ISO20022-bankkontoudtog ved hjælp af dataenhedsstrukturen.

1.  Gå til **Arbejdsområder** &gt; **Datastyring**.
2.  Klik på **Importer**.
3.  Angiv et navn for formatet, f.eks. **ISO20022**.
4.  Indstil feltet **Kildedataformat** til **XML-element**.
5.  Indstil feltet **Enhedsnavn** til **Bankkontoudtog**.
6.  Hvis du vil overføre importfiler, skal du klikke på **Overfør**, og derefter søge efter og vælge filen **SampleBankCompositeEntity.xml**, som du gemte tidligere.
7.  Når enheden Bankkontoudtog er blevet overført, og tilknytningen er fuldført, skal du klikke på handlingen **Vis tilknytning** for enheden.
8.  Enheden Bankkontoudtog er en sammensat enhed, der består af fire separate enheder. På listen skal du vælge **BankStatementDocumentEntity**, og derefter klikke på handlingen **Vis tilknytning**.
9.  Klik på **Ny** under fanen **Transformationer**.
10. For løbenummer 1 skal du klikke på **Overfør fil** og vælge filen **ISO20022XML-to-Reconciliation.xslt**, du gemte tidligere. **Bemærk:** Transformationsfiler er udviklet til standardformatet. Da bankerne ofte afviger fra dette format, skal du muligvis opdatere transformationsfilen, som skal knyttes til dit bankkontoudtogsformat. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Klik på **Ny**.
12. For løbenummer 2 skal du klikke på **Overfør fil** og vælge filen **BankReconciliation-to-Composite.xslt**, du gemte tidligere.
13. Klik på **Anvend transformeringer**.

Når formatbehandlingsgruppen er oprettet, er næste trin at definere regler for bankkontoudtogsformatet for ISO20022-bankkontoudtog.

1.  Gå til **Kontant- og bankstyring** &gt; **Opsætning** &gt; **Konfiguration af avanceret bankafstemning** &gt; **Bankkontoudtogsformat**.
2.  Klik på **Ny**.
3.  Angiv et kontoudtogsformat, f.eks **ISO20022**.
4.  Angiv et navn til formatet.
5.  Indstil feltet **Behandlingsgruppe** til den gruppe, du definerede tidligere, f.eks. **ISO20022**.
6.  Marker afkrydsningsfeltet **XML-fil**.

Det sidste trin er at aktivere Avanceret bankafstemning og angive kontoudtogsformatet på bankkontoen.

1.  Gå til **Kontant- og bankstyring** &gt; **Bankkonti**.
2.  Vælg bankkontoen, og åbn for at få vist detaljerne.
3.  På fanen **Afstemning** skal du vælge indstillingen **Ja** for **Avanceret bankafstemning**.
4.  Indstil feltet **Kontoudtogsformat** til det format, du oprettede tidligere, f.eks. **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Konfigurere importen af MT940-bankkontoudtog
Først skal du definere behandlingsgruppen for bankkontoudtogsformatet for MT940-bankkontoudtog ved hjælp af dataenhedsstrukturen.

1.  Gå til **Arbejdsområder** &gt; **Datastyring**.
2.  Klik på **Importer**.
3.  Angiv et navn for formatet, f.eks. **MT940**.
4.  Indstil feltet **Kildedataformat** til **XML-element**.
5.  Indstil feltet **Enhedsnavn** til **Bankkontoudtog**.
6.  Hvis du vil overføre importfiler, skal du klikke på **Overfør**, og derefter søge efter og vælge filen **SampleBankCompositeEntity.xml**, som du gemte tidligere.
7.  Når enheden Bankkontoudtog er blevet overført, og tilknytningen er fuldført, skal du klikke på handlingen **Vis tilknytning** for enheden.
8.  Enheden Bankkontoudtog er en sammensat enhed, der består af fire separate enheder. På listen skal du vælge **BankStatementDocumentEntity**, og derefter klikke på handlingen **Vis tilknytning**.
9.  Klik på **Ny** under fanen **Transformationer**.
10. For løbenummer 1 skal du klikke på **Overfør fil** og vælge filen **MT940TXT-to-MT940XML.xslt**, du gemte tidligere.
11. Klik på **Ny**.
12. For løbenummer 2 skal du klikke på **Overfør fil** og vælge filen **MT940XML-to-Reconciliation.xslt**, du gemte tidligere. **Bemærk:** Transformationsfiler er udviklet til standardformatet. Da bankerne ofte afviger fra dette format, skal du muligvis opdatere transformationsfilen, som skal knyttes til dit bankkontoudtogsformat. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Klik på **Ny**.
14. For løbenummer 3 skal du klikke på **Overfør fil** og vælge filen **BankReconciliation-to-Composite.xslt**, du gemte tidligere.
15. Klik på **Anvend transformeringer**.

Når formatbehandlingsgruppen er oprettet, er næste trin at definere regler for bankkontoudtogsformatet for MT940-bankkontoudtog.

1.  Gå til **Kontant- og bankstyring** &gt; **Opsætning** &gt; **Konfiguration af avanceret bankafstemning** &gt; **Bankkontoudtogsformat**.
2.  Klik på **Ny**.
3.  Angiv et kontoudtogsformat, f.eks **MT940**.
4.  Angiv et navn til formatet.
5.  Indstil feltet **Behandlingsgruppe** til den gruppe, du definerede tidligere, f.eks. **MT940**.
6.  Indstil feltet **Filtype** til **txt**.

Det sidste trin er at aktivere Avanceret bankafstemning og angive kontoudtogsformatet på bankkontoen.

1.  Gå til **Kontant- og bankstyring** &gt; **Bankkonti**.
2.  Vælg bankkontoen, og åbn for at få vist detaljerne.
3.  På fanen **Afstemning** skal du vælge indstillingen **Ja** for **Avanceret bankafstemning**.
4.  Når du bliver bedt om at bekræfte dit valg og aktivere avanceret bankafstemning, skal du klikke på **OK**.
5.  Indstil feltet **Kontoudtogsformat** til det format, du oprettede tidligere, f.eks. **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Konfigurere importen af BAI2-bankkontoudtog
Først skal du definere behandlingsgruppen for bankkontoudtogsformatet for BAI2-bankkontoudtog ved hjælp af dataenhedsstrukturen.

1.  Gå til **Arbejdsområder** &gt; **Datastyring**.
2.  Klik på **Importer**.
3.  Angiv et navn for formatet, f.eks. **BAI2**.
4.  Indstil feltet **Kildedataformat** til **XML-element**.
5.  Indstil feltet **Enhedsnavn** til **Bankkontoudtog**.
6.  Hvis du vil overføre importfiler, skal du klikke på **Overfør**, og derefter søge efter og vælge filen **SampleBankCompositeEntity.xml**, som du gemte tidligere.
7.  Når enheden Bankkontoudtog er blevet overført, og tilknytningen er fuldført, skal du klikke på handlingen **Vis tilknytning** for enheden.
8.  Enheden Bankkontoudtog er en sammensat enhed, der består af fire separate enheder. På listen skal du vælge **BankStatementDocumentEntity**, og derefter klikke på handlingen **Vis tilknytning**.
9.  Klik på **Ny** under fanen **Transformationer**.
10. For løbenummer skal du klikke på **Overfør fil** og vælge filen **BAI2CSV-to-BAI2XML.xslt**, du gemte tidligere.
11. Klik på **Ny**.
12. For løbenummer 2 skal du klikke på **Overfør fil** og vælge filen **BAI2XML-to-Reconciliation.xslt**, du gemte tidligere. **Bemærk:** Transformationsfiler er udviklet til standardformatet. Da bankerne ofte afviger fra dette format, og du muligvis skal opdatere transformationsfilen, som skal knyttes til dit bankkontoudtogsformat. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Klik på **Ny**.
14. For løbenummer 3 skal du klikke på **Overfør fil** og vælge filen **BankReconciliation-to-Composite.xslt**, du gemte tidligere.
15. Klik på **Anvend transformeringer**.

Når formatbehandlingsgruppen er oprettet, er næste trin at definere regler for bankkontoudtogsformatet for BAI2-bankkontoudtog.

1.  Gå til **Kontant- og bankstyring** &gt; **Opsætning** &gt; **Konfiguration af avanceret bankafstemning** &gt; **Bankkontoudtogsformat**.
2.  Klik på **Ny**.
3.  Angiv et kontoudtogsformat, f.eks **BAI2**.
4.  Angiv et navn til formatet.
5.  Indstil feltet **Behandlingsgruppe** til den gruppe, du definerede tidligere, f.eks. **BAI2**.
6.  Indstil feltet **Filtype** til **txt**.

Det sidste trin er at aktivere Avanceret bankafstemning og angive kontoudtogsformatet på bankkontoen.

1.  Gå til **Kontant- og bankstyring** &gt; **Bankkonti**.
2.  Vælg bankkontoen, og åbn for at få vist detaljerne.
3.  På fanen **Afstemning** skal du vælge indstillingen **Ja** for **Avanceret bankafstemning**.
4.  Når du bliver bedt om at bekræfte dit valg og aktivere avanceret bankafstemning, skal du klikke på **OK**.
5.  Indstil feltet **Kontoudtogsformat** til det format, du oprettede tidligere, f.eks. **BAI2**.

## <a name="test-the-bank-statement-import"></a>Teste import af bankkontoudtog
Det sidste trin er at kontrollere, at du kan importere dine kontoudtog.

1.  Gå til **Kontant- og bankstyring** &gt; **Bankkonti**.
2.  Vælg den bankkonto, som funktionen Avanceret bankafstemning er aktiveret for.
3.  På fanen **Afstem** skal du klikke på **Bankkontoudtog**.
4.  På siden **Bankkontoudtog** skal du klikke på **Importér kontoudtog**.
5.  Indstil feltet **Bankkonto** til det valgte bankkonto. Feltet **Kontoudtogsformat** indstilles automatisk baseret på indstillingen på bankkontoen.
6.  Klik på **Gennemse**, og vælg din elektroniske bankkontofil.
7.  Klik på **Overfør**.
8.  Klik på **OK**.

Hvis importen gennemføres, modtager du en meddelelse om, at kontoudtoget blev importeret. Hvis importen ikke lykkes, skal du finde jobbet i arbejdsområdet **Datastyring** i **Jobhistorik**. Klik på **Detaljer om udførelse** for jobbet for at åbne siden **Udførelsesoversigt**, og klik derefter på **Vis udførelseslog** for at få vist importfejl.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
