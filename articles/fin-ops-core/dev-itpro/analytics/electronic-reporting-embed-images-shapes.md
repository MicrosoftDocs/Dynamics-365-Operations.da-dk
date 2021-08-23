---
title: Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER
description: Dette emne forklarer, hvordan du bruger værktøjet elektronisk rapportering til at generere forretningsdokumenter, der har integrerede billeder og figurer.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550ecca31af48e624e292b342d909abd6eb3e87af122f736eb388524b42f1e05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730629"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER

[!include [banner](../includes/banner.md)]

Du kan bruge værktøjet Elektronisk rapportering (ER) til at designe rapporter, du kan køre for at generere påkrævede elektroniske dokumenter. Du kan bruge Microsoft Excel eller Microsoft Word-dokumenter til at angive et rapportlayout. I ER-operationsdesigneren kan du vedhæfte et Excel- eller Word-dokument som skabelon til et ER-format. Følgende navngivne elementer i den vedhæftede skabelon er knyttet til formatelementerne i ER-rapporten. Formatelementer er knyttet til datakilder. Disse elementer angiver de data, der skal indtastes i de genererede dokumenter på kørselstidspunktet.

Denne nye funktionalitet går ud over de eksisterende ER-egenskaber ved oprettelse af dokumenter i Microsoft Office-formater. Du kan finde flere oplysninger under følgende opgavevejledninger. Du kan finde disse opgavelinjer i forretningsprocessen 7.5.4.3 Acquire/Develop IT service/solution components (10677).

- Designe en ER-konfiguration til generering af rapporter i OPENXML-format
- ER Designe en konfiguration til generering af rapporter i Microsoft WORD-format

## <a name="embed-an-image-in-an-excel-document"></a>Integrere et billede i et Excel-dokument

### <a name="embed-an-image-in-an-excel-worksheet"></a>Integrere et billede i et Excel-dokument

Du skal først tilføje en pladsholder for billedet i et Excel-dokument. Åbn en Excel-projektmappe, og tilføj et billede som pladsholder for det billede, du vil tilføje senere. Brug derefter ER-værktøjet til at tilføje en ny ER-formatkonfiguration, som omfatter den rapport, du er ved at designe. Vedhæft Excel-projektmappen som en skabelon for rapportformatet, og importér derefter indholdet af projektmappen til ER-formatet. Formatdefinitionen oprettes automatisk. Den billed pladsholder, du har tilføjet, inkluderes i ER-formatdefinitionen som et **CELL**-element.

> [!NOTE]
> Du kan angive formatdefinitionen manuelt i stedet for at importere den. Når du gemmer ændringerne, valideres formatet.

Herefter skal **CELL**-elementet i ER-formatet knyttes til feltet fra formatets datakilde, der viser billedets data i binært format under kørslen. Når en ER-datamodel bruges som datakilde for et format, skal feltets datatype være [Container](er-formula-supported-data-types-composite.md#container). I øjeblikket kan et ER-datamodelfelt, der har datatypen [Container](er-formula-supported-data-types-composite.md#container), være bundet til flere typer datakilder, der returnerer billeder i binært format. Du kan få adgang til et felt i en datatabel og en fil, der er knyttet til datatabellens post, ved hjælp af Dokumentstyring.

> [!IMPORTANT]
> - Hvis du vil udfylde billed pladsholderen i det dokument, du opretter ved hjælp af Excel-skabelonen, skal ER-formatet indeholde det **CELL**-element, der henviser til det navngivet billedelement i Excel-skabelonen. Ellers vises der ikke en pladsholder til billeder i rapportens output. Hvis bindingen af et **CELL**-element ikke returnerer nogen data under kørslen, viser det dokument, der genereres, billedpladsholderen fra skabelonen. Hvis du vil skjule et billede i det dokument, du er ved at generere, skal du definere et **CELL**-element og angive, at **aktiveringsudtrykket** skal returnere værdien **FALSE**.
> - Brug et entydigt navn til hvert element i Excel-skabelonen. Disse elementer omfatter billeder og celler. Hvis du dupliker et elementnavn, vil indholdet af den rapport, der genereres, være utydeligt og uoverskueligt.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Integrere billeder i sidehovedet og sidefoden i et Excel-regneark

Brug Excel-projektmappedokumentet som skabelon til at angive layoutet for en rapport. Projektmappen kan indeholde flere regneark, som hver enkelt kan designes, så den har et sidehoved og en sidefod. Excel understøtter op til tre billeder i sidehovedet og sidefoden i hvert regneark. Billederne kan justeres til venstre, højre eller i midten.

I Finansversion 10.0.21 kan du administrere de sidehoved- og sidefodsbilleder, der genereres af en ER-løsning, der har en Excel-skabelon.

Hvis der skal vises et standardbillede i sidehovedet eller sidefoden i et genereret dokument, kan du føje et billede til sidehovedet eller sidefoden i et regneark i en ER-skabelon. Hvis du vil have adgang til dette billede i ER-formatet, skal du tilføje komponenten **Billede** under formatets [sidehoved](er-fillable-excel.md#header-component)- eller [sidefod](er-fillable-excel.md#footer-component)-komponent. Konfigurer justeringen for **billedkomponenten** efter behov. 

Du kan også bruge komponenten **Billede** til at placere et billede i sidehovedet eller sidefoden i et genereret dokument under kørslen, selvom skabelonen ikke indeholder et standardbillede. Hvis du vil angive det medieindhold, der skal sættes i sidehovedet eller sidefoden i et genereret dokument som enten et nyt billede eller en erstatning for et standardbillede, skal du knytte **billedkomponenten** til en datakilde til [containertypen](er-formula-supported-data-types-composite.md#container), der repræsenterer et billede i binært format.

Hver komponent i **sidehovedet** eller **sidefoden** kan indeholde én komponent med **billede** for hver understøttet justering: **Venstre**, **Center** og **Højre**.

**Skaler højdeegenskaben** for komponenten **Billede** giver dig mulighed for at bruge den konfigurerede binding til at styre størrelsen på et billede:

- Vælg **Original** for at bevare billedets oprindelige størrelse.
- Vælg **I forhold til** for at skalere højden på billedet i forhold til højden på det sidehoved eller den sidefod, der indeholder billedet.

    - I dette tilfælde skal højden på billedet defineres som en procentdel af det overordnede sidehoved eller den overordnede sidefod.
    - Hvis skaleringsværdien overstiger 100 procent, kan billedet overlappe dataområdet i det tilsvarende regneark.
    - Hvis højden på billedet ændres, når skaleringen anvendes, ændres bredden også, så billedets oprindelige størrelsesforhold bevares.

- Vælg **Absolut** for at ændre størrelsen på billedet i henhold til de værdier for højde og bredde (i pixel), der angives på designtid.

    - Hvis den angivne højde overstiger højden på det overordnede sidehoved eller sidefod, kan billedet overlappe dataområdet i det tilsvarende regneark.

Du kan også bruge den **aktiverede** egenskab for komponenten **Billede** til at styre synligheden af et billede, der tages i et genereret dokument ved hjælp af denne komponent.

> [!NOTE]
> Du skal bruge ER-formatdesigneren til at føje en **billedkomponent** til det er-format, der kan redigeres. Du kan ikke tilføje komponenten, når du bruger arbejdsområdet til [forretningsdokumentstyring](er-business-document-management.md) til at redigere skabelonen for et forretningsdokument.

Du kan få mere at vide om denne funktionalitet ved at følge trinnene i [Design af et ER-format for at generere en rapport i Excel-format med integrerede billeder i sidehoveder eller sidefødder](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Integrere en figur i et Excel-dokument

Du skal først tilføje en pladsholder for figuren i et Excel-dokument. Åbn en Excel-projektmappe, og vælg **Figur**, **Tekstfelt** eller **WordArt** som pladsholder for figur. Brug derefter ER-værktøjet til at tilføje en ny ER-formatkonfiguration, som omfatter den rapport, du er ved at designe. Vedhæft Excel-projektmappen som en skabelon for rapportformatet, og importér derefter indholdet af projektmappen til ER-formatet. Formatdefinitionen oprettes automatisk. Den pladsholder til figur, du har tilføjet, inkluderes i ER-formatdefinitionen som et **CELL**-element, der henviser til det navngivet Excel-figurelement.

> [!NOTE]
> Du kan angive formatdefinitionen manuelt i stedet for at importere den. Når du gemmer ændringerne, valideres formatet.

Herefter skal **CELL**-elementet i ER-formatet knyttes til feltet fra formatets datakilde, der viser billedets data i binært format under kørslen. Disse data kan konverteres til en tekststreng. Når **CELL**-elementet i ER-formatet refererer til et figurelement i Excel-skabelonen, der understøtter tekst, vises den tekst, der oprettes via denne binding ved kørsel, i en figur i det dokument, der genereres.

> [!IMPORTANT]
> - Hvis du vil bruge Excel-skabelonen, der indeholder pladsholderen til figur til at generere et nyt dokument, skal ER-formatet indeholde et **CELL**-element, der henviser til excel-elementets figur. Ellers vises der ikke en pladsholder til figuren i rapportens output. Hvis bindingen for et **CELL**-element, der henviser til det navngivet Excel-figurelement, ikke returnerer nogen data under kørslen, vil det dokument, der genereres, vise teksten til pladsholderen til formen fra Excel-skabelonen. Hvis du vil skjule en figur i det dokument, du er ved at generere, skal du definere et **CELL**-element og angive, at **aktiveringsudtrykket** skal returnere værdien **FALSE**.
> - Brug et entydigt navn til hvert element i Excel-skabelonen. Disse elementer omfatter figurer og celler. Hvis du dupliker et elementnavn, vil indholdet af den rapport, der genereres, være utydeligt og uoverskueligt.

## <a name="embed-an-image-in-a-word-document"></a>Integrere et billede i et Word-dokument
> [!IMPORTANT]
> Du kan genbruge det ER-format, der bruger en Excel-skabelon, til at oprette dokumenter, der indeholder integrerede billeder. I ER-formatet skal du kontrollere, at der er angivet et navn for det **CELL**-element, der henviser til et navngivet billedelement i Excel, og som er bundet til en datakilde, der returnerer et billede under kørslen.

Du skal først konfigurere layoutet for Word-dokumentet. Brug kontrolelementet **Billedindhold** til at oprette en pladsholder til det integrerede billede. Hvis du vil have adgang til dette kontrolelement, skal du først gøre fanen **Udvikler** synlig på Word-båndet.

Derefter skal du slette Excel-skabelonen fra ER-formatet og vedhæfte Word-skabelondokumentet. Opdater referencen til skabelonen, og gem ændringerne. Den hierarkiske struktur på det aktuelle ER-format føjes til Word-skabelonen som en ny brugerdefineret XML-del med navnet **Rapport**.

Derefter skal du gemme Word-skabelonen for det aktuelle ER-format på den lokale computer. Åbn skabelonen, og åbn ruden til **XML-tilknytning**. Find den brugerdefinerede XML-del med navnet **Rapport**, og peg derefter på **CELL**-elementet i ER-rapporten, der er bundet til en datakilde, der returnerer et billede i binært format. Knyt denne XML-del til det valgte kontrolelement med **billedindhold**, og gem ændringerne.

[![integrere billeder.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Endelig skal du slette Word-skabelonen fra ER-formatet og vedhæfte det Word-dokument, der indeholder de tilknyttede brugerdefinerede XML-dele. Opdater formatreferencen til skabelonen, og gem de ændringer, du har foretaget i dette ER-format.

## <a name="more-information"></a>Flere oplysninger
Du kan sætte dig ind i detaljerne om denne funktion ved at bruge sættet af opgavevejledninger **ER Make-rapporter i MS Office-formater med integrerede billeder**. Disse opgavevejledninger viser, hvordan du kan integrere billeder af et firmalogo og en autoriseret persons underskrift på de betalingskontroller, der genereres ved hjælp af ER-værktøjet i Excel- og Word-dokumenter.

Følgende tabel indeholder de filer, der kræves for at udføre **ER Make-rapporterne i MS Office-formater med integrerede billedopgavevejledninger**. Download og gem filerne på den lokale computer.

| Betegnelse                                          | Filnavn                   |
|------------------------------------------------------|-----------------------------|
| ER-datamodelkonfiguration                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| Konfiguration af ER-format                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Billede af firmalogo                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Signaturbillede                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternativt signaturbillede                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word-skabelon til udskrivning af betalingschecks  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel-skabelon til udskrivning af betalingschecks | [Checkskabelon.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

I følgende grafik vises et eksempel på den test, der udskrives for en betalingscheck, der genereres fra Excel-skabelonen.

[![Udskrift af betalingskontrol.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
