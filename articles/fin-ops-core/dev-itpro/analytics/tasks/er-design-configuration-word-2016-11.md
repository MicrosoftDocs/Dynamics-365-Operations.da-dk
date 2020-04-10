---
title: Designe ER-konfigurationer til at generere rapporter i Word-format
description: Følgende trin beskriver, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapporteringsformat til at generere rapporter som Microsoft Word-filer.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 208b1be20a8833afbf4929a7ceda706aeb5bda3b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142080"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Designe ER-konfigurationer til at generere rapporter i Word-format

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapporteringsformater (ER) til at generere rapporter som Microsoft Word-filer. Disse trin kan udføres i GBSI-virksomheden.

For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "Oprette en ER-konfiguration til generering af rapporter i OPENXML-format". På forhånd skal du også hente og gemme følgende skabeloner lokalt for eksempelrapporten:

- [Skabelon for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266)
- [Bundet skabelon for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266)


Denne procedure er beregnet til en funktion, der blev tilføjet i Microsoft Dynamics 365 for Operations version 1611.


## <a name="select-the-existing-er-report-configuration"></a>Vælg den eksisterende ER-rapportkonfiguration
1. Gå i **navigationsruden til Moduler > Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**. Sørg for, at konfigurationsprovideren 'Litware, Inc.'. er markeret som aktiv.  
2. Klik på **Rapporteringskonfigurationer**. Vi genbruger den eksisterende ER-konfiguration, der oprindeligt er udviklet til at generere rapporten i OPENXML-formatet.  
3. Udvid "Betalingsmodel" i træet.
4. Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.
5. Klik på Designer.

## <a name="replace-the-excel-template-with-the-word-template"></a>Erstat Excel-skabelonen med Word-skabelonen

Aktuelt bruges Excel-dokumentet som en skabelon til at generere outputtet i OPENXML-format. Vi importerer rapportens skabelon i Word-format.

1. Klik på **Vedhæftede filer**. Erstat den eksisterende Excel-skabelon med Word-skabelonen, som du downloadede tidligere, SampleVendPaymDocReport.docx. Bemærk, at denne skabelon kun indeholder layoutet på det dokument, vi vil generere som ER-output.  
2. Klik på **Slet**.
3. Klik på **Ja**.
4. Klik på **Ny**.
5. Klik på **Fil**.
6. Klik på **Gennemse**. Naviger til og vælg SampleVendPaymDocReport.docx, som du tidligere downloadede. Klik på **OK**. Vælg den skabelon, du downloadede i det forrige trin.  
7. Indtast eller vælg en værdi i feltet **Skabelon**.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Udvid Word-skabelonen ved at tilføje en brugerdefineret XML-del
1. Klik på **Gem**. I tillæg til at lagre konfigurationsændringer opdaterer handlingen Gem også den vedhæftede Word-skabelon. Strukturen på det designede format overføres til det vedhæftede Word-dokument som en ny brugerdefineret XML-del med navnet "Rapport". Bemærk, at den vedhæftede Word-skabelon ikke kun indeholder layoutet på det dokument, vi vil generere som ER-output, den indeholder også strukturen af data, som ER udfylder i denne skabelon på kørselstidspunktet.  
2. Klik på **Vedhæftede filer**.
    + Nu skal du binde elementerne i den brugerdefinerede XML-del "Rapport" til Word-dokumentdelene.  
    + Hvis du har kendskab til Word-dokumenter, der kan designes som formularer, der indeholder indholdskontrolelementer, der er bundet til elementer i brugerdefinerede XML-dele – kan du afspille alle trin i den næste underopgave for at oprette et sådant dokument. Du kan finde flere oplysninger under [Oprette formularer, som brugere udfylder eller udskriver i Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US). Ellers skal du springe alle trin i den næste underopgave over.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Få Word med brugerdefineret XML-del til at udføre databindinger

Åbn dette dokument i Word, og gør følgende:  
1. Åbn fanen Udvikler i Word (tilpas båndet, hvis det endnu ikke er aktiveret).
2. Vælg XML-tilknytningsrude.
3. Vælg den brugerdefinerede del "Rapport" i opslaget.
4. Udfør tilknytningen af elementerne i den markerede brugerdefinerede XML-del og indholdskontrolelementerne i Word-dokumentet.  5 Gem det opdaterede Word-dokument på et lokalt drev.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Upload Word-skabelonen med brugerdefineret XML-del bundet til indholdskontrolelementer
1. Klik på **Slet**.
2. Klik på **Ja**. Tilføj en ny skabelon. Hvis du udførte trinnene i den tidligere underopgave, skal du markere det Word-dokument, som du har klargjort og gemt lokalt. Ellers skal du vælge MS Word-skabelonen SampleVendPaymDocReportBounded.docx, som du tidligere downloadede.  
3. Klik på **Ny**.
4. Klik på **Fil**.
5. Klik på **Gennemse**. Naviger til og vælg SampleVendPaymDocReportBounded.docx, som du tidligere downloadede. Klik på **OK**.
6. Vælg det dokument i feltet **Skabelon**, som du downloadede i det forrige trin.
7. Klik på **Gem**.
8. Luk siden.

## <a name="execute-the-format-to-create-word-output"></a>Udfør formatet for at oprette Word-output
1. Klik på **Konfigurationer** i **handlingsruden**.
2. Klik på **Brugerparametre**.
3. Vælg Ja i feltet **Indstillinger for kørsel**.
4. Klik på **OK**.
5. Klik på **Rediger**.
6. Vælg Ja i feltet **Udkast til kørsel**.
7. Klik på **Gem**.
8. Luk siden.
9. Luk siden.
10. Gå i **navigationsruden** til **Moduler > Kreditorer > Betalinger > Betalingskladde**.
11. Klik på **Linjer**.
12. Markér eller fjern markeringen af alle rækker på listen.
13. Klik på **Betalingsstatus**.
14. Klik på **Ingen**.
15. Klik på **Generer betalinger**.
16. Klik på **OK**.
17. Klik på **OK**. Analysér det genererede output. Bemærk, at det oprettede output vises i Word-format og indeholder oplysninger om de behandlede betalinger.  

