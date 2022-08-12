---
title: Fejlfinding af filimport af bankkontoudtog
description: I denne artikel beskrives, hvordan du kan løse problemer med små forskelle i bankkontoudtogsfilen.
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151754"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Fejlfinding af filimport af bankkontoudtog

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Denne funktion udfases i september 2022, og nye brugere skal bruge elektronisk rapportering.

Det er vigtigt, at kontoudtogsfilen fra banken matcher det layout, som Microsoft Dynamics 365 Finance understøtter. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.

## <a name="what-is-the-error"></a>Hvad er fejlen?

Når du forsøger at importere en bankkontoudtogsfil, skal du gå til jobhistorikken for Datastyring og se udførelsesoplysningerne for at finde fejlen. Fejlen gør det lettere at udpege kontoudtoget, balancen eller kontoudtogslinjen. Det er dog ikke sandsynligt, at du får tilstrækkelige oplysninger til at identificere det felt eller element, der er årsag til problemet.

> [!NOTE]
> Importerede bankkontoudtog må kun overlappe for et bestemt tidspunkt.  Hvis en opgørelse f.eks. slutter kl. 12:00 den 1. januar 2021, kan startdatoen for den næste opgørelse være 12:00 den 1. januar 2021.

## <a name="what-are-the-differences"></a>Hvad er forskellene?
Sammenlign layoutdefinitionen for bankfilen med finansimportdefinitionen, og bemærk eventuelle forskelle i felter og elementer. Sammenlign kontoudtogsfilen fra banken med den relaterede finanseksempelfil. I ISO20022-filerne bør eventuelle forskelle være lette at se.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Tidszoneforskelle på importerede bankkontoudtog
Dato- og klokkeslætsværdierne i importfilen kan være forskellige fra de dato- og klokkeslætsværdier, der vises i finans og drift. Hvis du vil undgå denne uoverensstemmelse, skal du angive en tidszoneindstilling på siden **Konfigurer datakilder**. Se [Konfigurere importprocessen for avanceret bankafstemning](set-up-advanced-bank-reconciliation-import-process.md) for at få flere oplysninger om angivelse af en indstilling for tidszone.

## <a name="transformations"></a>Transformationer
Ændringen foretages typisk i en af tre transformationer. Hver transformation er skrevet for en bestemt standard.

| Ressourcenavn                                         | Filnavn                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Fejlfinding af transformationer
### <a name="adjust-the-bai2-and-mt940-files"></a>Justere BAI2- og MT940-filerne

BAI2- og MT940-filerne er tekstbaserede filer og kræver en justering for at aktivere fejlfinding af Extensible Stylesheet Language Transformations (XSLT). Denne justering foretages, når en fil importeres.

1.  Opret en XML-fil, og kopiér følgende tekst ind i den.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Kopiér indholdet af bankkontoudtogsfilen og indsæt det i XML-filen, så det erstatter **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Foretage fejlfinding af XSLT-transformationen

Yderligere oplysninger finder du i <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Start Microsoft Visual Studio.
2.  Opret en konsolansøgning.
3.  Åbn den relevante XSLT-transformation.
4.  Klik på XLST-transformationen og dens egenskabsside.
5.  Angiv input til lokationen for bankkontoudtogsfilen.
6.  Definer en lokation og et filnavn til outputtet.
7.  Angiv de nødvendige pausepunkter.
8.  Åbn menuen, og klik på **XML** &gt; **Start fejlfinding af XSLT**.

### <a name="format-the-xslt-output"></a>Formatér XLST-outputtet

Når transformationen er i gang, oprettes der en outputfil, som du kan se i Visual Studio. Brug Ctrl+A, Ctrl+K og Ctrl+D til hurtigt at formatere outputfilen.

### <a name="adjust-the-transformation"></a>Justere transformationen

Juster transformationen for at få det relevante felt eller element i bankkontoudtogsfilen. Derefter skal du knytte feltet eller elementet til det relevante Finance-element.

### <a name="debitcredit-indicator"></a>Indikator for debet/kredit

Nogle gange kan debiteringer importeres som kreditter, og kreditter kan importeres som debet. Du kan løse dette problem ved at ændre den relevante XSLT. Hvis bankkontoudtog kommer fra flere banker, skal du kontrollere, at de alle bruger samme fremgangsmåde for debet/kredit, eller oprette separate transformationer.

-   BAI2XML-til-Reconciliation.xlst GetAmountCreditDebitIndicator-skabelon
-   ISO20022XML-til-Reconcilation.xslt GetCreditDebit-skabelon
-   MT940XML-til-Reconcilation.xslt GetCreditDebitIndicator-skabelon

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoudtogsformater og tekniske layout
Følgende tabel viser eksempler på de tekniske layoutdefinitioner for importfiler til avanceret bankafstemning og tre relaterede eksempelfiler på bankkontoudtog. Du kan hente eksempelfiler og tekniske layout her: [Importere fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Teknisk layoutdefinition                             | Eksempelfil med bankkontoudtog          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

