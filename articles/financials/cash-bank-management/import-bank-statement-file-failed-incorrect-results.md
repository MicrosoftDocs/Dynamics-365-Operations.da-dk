---
title: Fejlfinding af filimport af bankkontoudtog
description: "Det er vigtigt, at bankkontoudtogsfilen fra banken svarer til det layout, som Microsoft Dynamics 365 for Finance and Operations, Enterprise edition understøtter. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4feb77bf0031494dfd456c23c632a264c96f0e43
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a>Fejlfinding af filimport af bankkontoudtog

[!include[banner](../includes/banner.md)]


Det er vigtigt, at bankkontoudtogsfilen fra banken svarer til det layout, som Microsoft Dynamics 365 for Finance and Operations, Enterprise edition understøtter. På grund af strenge standarder for bankkontoudtog fungerer de fleste integrationer korrekt. Men nogle gange kan udtogsfilen ikke importeres eller giver forkerte resultater. Normalt skyldes disse problemer små forskelle i bankkontoudtogsfilen. Denne artikel forklarer, hvordan du løser disse forskelle og løser problemerne.

<a name="what-is-the-error"></a>Hvad er fejlen?
------------------

Når du forsøger at importere en bankkontoudtogsfil, skal du gå til jobhistorikken for Datastyring og se udførelsesoplysningerne for at finde fejlen. Fejlen gør det lettere at udpege kontoudtoget, balancen eller kontoudtogslinjen. Det er dog ikke sandsynligt, at du får tilstrækkelige oplysninger til at identificere det felt eller element, der er årsag til problemet.

## <a name="what-are-the-differences"></a>Hvad er forskellene?
Sammenlign layoutdefinitionen for bankfiler med Finance and Operations-importdefinitionen, og bemærk eventuelle forskelle i felter og elementer. Sammenlign bankkontoudtogsfilen med den relaterede Finance and Operations-eksempelfil. I ISO20022-filerne bør eventuelle forskelle være lette at se.

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
8.  Åbn menuen, og klik på **XML** &gt; **Start fejlfinding af XSLT**.

### <a name="format-the-xslt-output"></a>Formatér XLST-outputtet

Når transformationen er i gang, oprettes der en outputfil, som du kan se i Visual Studio. Brug Ctrl+A, Ctrl+K og Ctrl+D til hurtigt at formatere outputfilen.

### <a name="adjust-the-transformation"></a>Justere transformationen

Juster transformationen for at få det relevante felt eller element i bankkontoudtogsfilen. Derefter skal du knytte feltet eller elementet til det relevante Finance and Operations-element.

### <a name="debitcredit-indicator"></a>Indikator for debet/kredit

Nogle gange kan debiteringer importeres som kreditter, og kreditter kan importeres som debet. Du kan løse dette problem ved at ændre den relevante XSLT. Hvis bankkontoudtog kommer fra flere banker, skal du kontrollere, at de alle bruger samme fremgangsmåde for debet/kredit, eller oprette separate transformationer.

-   BAI2XML-til-Reconciliation.xlst GetAmountCreditDebitIndicator-skabelon
-   ISO20022XML-til-Reconcilation.xslt GetCreditDebit-skabelon
-   MT940XML-til-Reconcilation.xslt GetCreditDebitIndicator-skabelon

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoudtogsformater og tekniske layout
Følgende tabel viser eksempler på de tekniske layoutdefinitioner for importfiler til avanceret bankafstemning og tre relaterede eksempelfiler på bankkontoudtog. Du kan hente filer eksempelfilerne og tekniske layout her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Teknisk layoutdefinition                             | Eksempelfil med bankkontoudtog          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |






