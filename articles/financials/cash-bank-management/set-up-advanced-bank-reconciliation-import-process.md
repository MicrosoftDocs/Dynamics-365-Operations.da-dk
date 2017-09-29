---
title: Konfigurere importprocessen for avanceret bankafstemning
description: Med funktionen Avanceret bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. I denne artikel beskrives, hvordan du konfigurerer importfunktionen for dine kontoudtog fra banken.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a4d1c81386c0ef03391f3127fa51a6b09a5142b3
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Konfigurere importprocessen for avanceret bankafstemning

[!include[banner](../includes/banner.md)]


Med funktionen Avanceret bankafstemning kan du importere elektroniske bankkontoudtog og automatisk afstemme dem med banktransaktioner i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. I denne artikel beskrives, hvordan du konfigurerer importfunktionen for dine kontoudtog fra banken. 

Konfigurationen for import af bankkontoudtog varierer afhængigt af formatet på dit elektroniske bankkontoudtog. Finance and Operations understøtter tre standardformater for bankkontoudtog: ISO20022, MT940 og BAI2.

## <a name="sample-files"></a>Eksempelfiler
For alle tre formater skal du have filer, der oversætter det elektroniske bankkontoudtog fra det oprindelige format til et format, der kan bruges af Finance and Operations. Du kan finde de nødvendige ressourcefiler under noden **Ressourcer** i Application Explorer i Microsoft Visual Studio. Når du har fundet filerne, skal du kopiere dem til en enkelt kendt placering, så du nemmere kan overføre dem under konfigurationsprocessen.

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
Nedenfor vises eksempler på avancerede definitioner af teknisk layout for bankafstemnings importfil og tre relaterede eksempelfiler på bankkontoudtog: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Teknisk layoutdefinition                             | Eksempelfil med bankkontoudtog          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

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
10. For løbenummer 1 skal du klikke på **Overfør fil** og vælge filen **ISO20022XML-to-Reconciliation.xslt**, du gemte tidligere. **Bemærk:** Finance and Operations-transformationsfiler er udviklet til standardformatet. Da bankerne ofte afviger fra dette format, skal du muligvis opdatere transformationsfilen, som skal knyttes til dit bankkontoudtogsformat. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
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
12. For løbenummer 2 skal du klikke på **Overfør fil** og vælge filen **MT940XML-to-Reconciliation.xslt**, du gemte tidligere. **Bemærk:** Finance and Operations-transformationsfiler er udviklet til standardformatet. Da bankerne ofte afviger fra dette format, skal du muligvis opdatere transformationsfilen, som skal knyttes til dit bankkontoudtogsformat. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
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
12. For løbenummer 2 skal du klikke på **Overfør fil** og vælge filen **BAI2XML-to-Reconciliation.xslt**, du gemte tidligere. **Bemærk:** Finance and Operations-transformationsfiler er udviklet til standardformatet. Da bankerne ofte afviger fra dette format, og du muligvis skal opdatere transformationsfilen, som skal knyttes til dit bankkontoudtogsformat. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
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



