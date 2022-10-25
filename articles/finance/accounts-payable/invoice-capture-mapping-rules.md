---
title: Tilknytningsregler for løsningen Invoice Capture
description: Denne artikel indeholder oplysninger om opsætning af tilknytningsregler i løsningen Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691176"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Tilknytningsregler for løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tilknytningsregler henter grundlæggende masterdata fra Microsoft Dynamics 365 Finance eller ERP-systemet (Enterprise Resource Planning). Når der er oprettet tilknytningsregler, afledes de oplysninger, der kræves for at oprette kreditorfakturaer i Finance. Når der bruges tilknytningsregler, kontrollerer kreditorassistenten status i stedet for at udfylde alle de manglende feltværdier manuelt.

Der findes fire typer tilknytningsregler:

- Juridisk enhed
- Leverandørkonto
- Vare
- Udgiftstype

## <a name="manage-mapping-rules-by-using-the-app"></a>Administrere tilknytningsregler ved hjælp af appen

Hvis du vil administrere tilknytningsregler ved hjælp af appen, skal du vælge **Opsætning**. Fanen **Opsætning af tilknytningsregel** indeholder fire muligheder:

- Juridisk enhed 
- Leverandørkonto 
- Varetilknytning 
- Udgiftstype

Du kan f.eks. vælge indstillingen **Tilknytningsregler for juridisk enhed**. Den juridiske enheds kode identificeres ved hjælp af firmaets navn, adresse og momsregistreringsnummer. For en regel, der hedder **LE-USPM**, hvis firmanavnet indeholder teksten "Contoso Robotics USA", er koden for den juridiske enhed **USPM**.

På siden vises alle aktive tilknytningsregler. Hvis du vil have vist de inaktive tilknytningsregler, skal du vælge **Aktive tilknytningsregler for juridisk enhed** og derefter vælge **Inaktive tilknytningsregler for juridisk enhed**.

De følgende handlinger er tilgængelige for tilknytningsregler.

### <a name="create-a-mapping-rule"></a>Oprette en tilknytningsregel

Du kan bruge to metoder til at oprette en tilknytningsregel:

- Vælg **Ny** for at oprette en ny tilknytningsregel. Angiv derefter oplysninger om tilknytningsreglen. Værdien **Regelnavn** skal være entydig for hver type tilknytningsregel.
- Hvis du vælger en eksisterende tilknytningsregel, bliver knappen **Kopiér** tilgængelig. Vælg den, og vælg derefter **OK** i dialogboksen. Der oprettes en tilknytningsregel ved at duplikere den valgte regel.

### <a name="edit-a-mapping-rule"></a>Redigere en tilknytningsregel

Hvis du vil redigere en tilknytningsregel, skal du markere et felt og ændre værdien.

### <a name="activatedeactivate-mapping-rules"></a>Aktivere/deaktivere tilknytningsregler

Hvis du vil deaktivere en eller flere tilknytningsregler, skal du markere dem på siden **Aktive tilknytningsregler** og derefter vælge **Deaktiver**. Reglerne flyttes fra siden **Aktive tilknytningsregler** til siden **Inaktive tilknytningsregler**.

Hvis du vil aktivere tilknytningsregler, skal du markere dem på siden **Inaktive tilknytningsregler** og derefter vælge **Aktivér**.

### <a name="remove-mapping-rules"></a>Fjerne tilknytningsregler

Hvis du vil fjerne tilknytningsregler, skal du vælge dem og derefter vælge **Slet**.

### <a name="check-for-conflicts"></a>Kontrollere for konflikter

Hvis to tilknytningsregler har samme værdier for **Juridisk enhed** og **Kreditorkonto**, men forskellige værdier for **Varenavn**, registreres der en konflikt, og tilknytningsreglen oprettes eller opdateres ikke.

## <a name="importexport-mapping-rules-from-excel"></a>Importere/eksportere tilknytningsregler fra Excel

Et Excel-tilføjelsesprogram kan bruges til at administrere regler i en batch. Der findes følgende indstillinger:

- Download en Excel-skabelon.
- Eksportér til Excel.
- Importér fra Excel.

### <a name="download-an-excel-template"></a>Download en Excel-skabelon

Hvis du vil downloade en Excel-skabelon, skal du vælge **Download skabelon**. Vælg de felter, der skal medtages i skabelonen.

### <a name="export-to-excel"></a>Eksportér til Excel

Du kan eksportere på to måder:

- Vælg **Åbn i Excel Online** for at åbne filen i Excel. Du kan derefter redigere filen online. Vælg **Gem**, når du er færdig. Alle dine ændringer gemmes på siden **Tilknytningsregel**.
- Vælg **Download regneark** for at downloade en Excel-fil, der indeholder tilknytningsregler. Du kan derefter redigere filen. Når du er færdig, skal du vælge **Importér fra Excel** for at uploade det opdaterede regneark.

### <a name="import-from-excel"></a>Importér fra Excel

1. Vælg **Importér fra Excel** for at importere data fra en XLSX-fil. Du kan også importere fra kommaseparerede værdier (CSV) eller XML-filer. Før du importerer, skal du beslutte, om dubletter er tilladt.
2. Vælg **Gennemse tilknytning** for at gennemse tilknytningen af attributter og finde ud af, om den er korrekt. Du kan redigere tilknytningsrelationen.
3. Når du er færdig, skal du vælge **Udfør import** for at starte importen.
4. Du kan vælge **Spor proces** for at spore status for importprocessen.

    Importstatus opdateres fra **Udfør** til **Parsing**, derefter til **Transformering** og til sidst til **Fuldført**.

Når importprocessen er fuldført, vises statistik for succeser, delvise fejl, fejl og samlet behandlet.
