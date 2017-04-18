---
title: Bankens kontoudtog fil import fejlfinding
description: "Det er vigtigt, at bankkontoudtogsfilen fra banken, svarer til det layout, der understøtter Microsoft Dynamics 365 for operationer. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: 9717cf2f36033efe8465906324966242977c6eb2
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-file-import-troubleshooting"></a>Bankens kontoudtog fil import fejlfinding

Det er vigtigt, at bankkontoudtogsfilen fra banken, svarer til det layout, der understøtter Microsoft Dynamics 365 for operationer. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.

<a name="what-is-the-error"></a>Hvad er fejlen?
------------------

Når du forsøger at importere en bankkontoudtogsfil, skal du gå til jobhistorikken for Datastyring og se udførelsesoplysningerne for at finde fejlen. Fejlen gør det lettere at udpege kontoudtoget, balancen eller kontoudtogslinjen. Det er dog ikke sandsynligt, at du får tilstrækkelige oplysninger til at identificere det felt eller element, der er årsag til problemet.

## <a name="what-are-the-differences"></a>Hvad er forskellene?
Sammenlign bank fil Layoutdefinitionen til Microsoft Dynamics 365 operationer import definition, og Bemærk eventuelle forskelle i de felter og elementer. Sammenlign bankkontoudtogsfilen relaterede prøven Dynamics 365 for fil operationer. Eventuelle forskelle skal være let at se, i ISO20022-filerne.

## <a name="transformations"></a>Transformationer
Ændringen foretages typisk i en af tre transformationer. Hver transformation er skrevet for en bestemt standard.

| Ressourcenavn                                         | Filnavn                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_til\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_til\_afstemning\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_til\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Fejlfinding af transformationer
### <a name="adjust-the-bai2-and-mt940-files"></a>Justere BAI2- og MT940-filerne

BAI2- og MT940-filerne er tekstbaserede filer og kræver en justering for at aktivere fejlfinding af Extensible Stylesheet Language Transformations (XSLT). Denne justering foretages, når en fil importeres.

1.  Opret en XML-fil, og kopiér følgende tekst ind i den.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopiér indholdet af bankkontoudtogsfilen og indsæt det i XML-filen, så det erstatter **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Foretage fejlfinding af XSLT-transformationen

Få flere oplysninger under <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Start Microsoft Visual Studio.
2.  Opret en konsolansøgning.
3.  Åbn den relevante XSLT-transformation.
4.  Klik på XLST-transformationen og dens egenskabsside.
5.  Angiv input til lokationen for bankkontoudtogsfilen.
6.  Definer en lokation og et filnavn til outputtet.
7.  Angiv de nødvendige pausepunkter.
8.  Klik på menuen **XML**&gt;**starte fejlfinding af XSLT-**.

### <a name="format-the-xslt-output"></a>Formatér XLST-outputtet

Når transformationen er i gang, oprettes der en outputfil, som du kan se i Visual Studio. Brug Ctrl+A, Ctrl+K og Ctrl+D til hurtigt at formatere outputfilen.

### <a name="adjust-the-transformation"></a>Justere transformationen

Juster transformationen for at få det relevante felt eller element i bankkontoudtogsfilen. Derefter knytte dette felt eller element til den relevante Dynamics 365 for operationer element.

### <a name="debitcredit-indicator"></a>Indikator for debet/kredit

Nogle gange kan debiteringer importeres som kreditter, og kreditter kan importeres som debet. Du kan løse dette problem ved at ændre den relevante XSLT. Hvis bankkontoudtog kommer fra flere banker, skal du kontrollere, at de alle bruger samme fremgangsmåde for debet/kredit, eller oprette separate transformationer.

-   BAI2XML-til-Reconciliation.xlst GetAmountCreditDebitIndicator-skabelon
-   ISO20022XML-til-Reconcilation.xslt GetCreditDebit-skabelon
-   MT940XML-til-Reconcilation.xslt GetCreditDebitIndicator-skabelon

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoudtogsformater og tekniske layout
Følgende tabel viser eksempler på de tekniske layoutdefinitioner for importfiler til avanceret bankafstemning og tre relaterede eksempelfiler på bankkontoudtog. Du kan hente filer for eksempel og tekniske layout her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Teknisk layoutdefinition                             | Eksempelfil med bankkontoudtog          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |



