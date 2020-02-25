---
title: ER-destinationstype for e-mail
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere en maildestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019686"
---
# <a name="EmailDestinationType">Maildestination</a>

[!include [banner](../includes/banner.md)]

Du kan konfigurere en e-maildestination for hver komponent af typen MAPPE eller FIL i et elektronisk rapporteringsformat (ER), der er konfigureret til at generere udgående dokumenter. På baggrund af destinationsindstillingen leveres et genereret dokument som en vedhæftet fil til en e-mail.

Indstil **Aktiveret** til **Ja** for at sende en outputfil via mail. Når denne indstilling er aktiveret, kan du angive e-mailmodtagere og redigere e-mailens emne og brødtekst. Du kan konfigurere konstanttekster til e-mailens emne og brødtekst, eller du kan bruge ER [formler](er-formula-language.md) til dynamisk at oprette e-mailtekster. 

Du kan konfigurere e-mailadresser for ER på to måder. Konfigurationen kan fuldføres på samme måde, som funktionen Udskriftsstyring fuldfører den, eller du kan løse en e-mailadresse ved at bruge en direkte reference til ER-konfigurationen via en formel.

[![Aktivere e-maildestination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-mailadressetyper

Når du vælger **Rediger** i felterne **Til** eller **Cc**, åbnes dialogboksen **Mail til**. Du kan derefter vælge type e-mailadresse, du vil bruge. I øjeblikket understøttes e-mailtyperne **Konfigurationsmail** og **Udskriftsstyring**.

[![Vælge e-mailtype](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Udskriftsstyring

Hvis du vælger e-mailtypen **Udskriftsstyring**, kan du angive fast e-mailadresser i feltet **Til**. 

[![Konfigurere faste e-mailadresser](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Hvis du vil bruge mailadresser, der ikke er faste, skal du vælge mailkildetypen for en fildestination. Følgende værdier understøttes: **Kunde**, **Leverandør**, **Kundeemne**, **Kontakt**, **Konkurrent**, **Arbejder**, **Ansøger**, **Mulig kreditor** og **Ikke-godkendt kreditor**. Når du har valgt en kildetype for mail, skal du bruge knappen ved feltet **Kildekonto for mail** til at åbne formularen **Formeldesigner**. Du kan bruge denne formular til at tilknytte en formel, der på kørselstidspunktet returnerer **partskontoen** for den valgte kildetype fra det behandlede dokument til e-maildestinationen.

[![Konfigurere e-mailens kildekonto](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formler er specifikke for ER-konfigurationen. Angiv en dokumentspecifik reference til en debitor- eller kreditorparttype i feltet **Formel**. I stedet for at skrive kan du finde datakildenoden, der repræsenterer debitor- eller kreditorkontoen, og derefter vælge **Tilføj datakilde** for at opdatere formlen. Hvis du f.eks. bruger konfigurationen **ISO 20022-kreditoverførsel**, er den node, der repræsenterer en kreditorkonto, `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Hvis du angiver en strengværdi som f.eks. `"DE-001"` og gemmer en formel, sendes der en e-mail til kontaktpersonen for leverandøren, **DE-001**.


[![Siden ER-formeldesigner](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![Konfigurere e-mailens kildekonto](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Konfigurationsmail

Brug denne e-mailtype, hvis den konfiguration, du bruger, har en node i datakilderne, der returnerer en **e-mailadresse**. Du kan bruge datakilder og funktioner i formeldesigneren til at få en korrekt formateret e-mailadresse. Hvis du f.eks. bruger konfigurationen **ISO 20022-kreditoverførsel**, er den node, der repræsenterer en e-mailadresse for en kreditors kontaktperson, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Konfigurere kilden til e-mailadressen](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)
