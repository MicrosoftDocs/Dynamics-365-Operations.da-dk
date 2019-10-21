---
title: (RCS) Importere filer i XML-format med valgfrie attributter
description: Dette emne indeholder oplysninger om, hvordan en bruger kan designe ER-formatkonfiguration til at importere filer i XML-format, der indeholder valgfrie attributter.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182180"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Importere filer i XML-format med valgfrie attributter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan designe konfiguration af ER-format til at importere filer i XML-format, der indeholder valgfrie attributter. Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin. Før du går i gang, kan du hente og gemme filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml lokalt i [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).

1.  Gå til **Alle arbejdsområder** > **Elektronisk rapportering**.
2.  Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret en konfigurationsudbyder, og markér den som aktiv](er-configuration-provider-mark-it-active-2016-11.md).
3.  Klik på **Rapporteringskonfigurationer**.

## <a name="create-a-new-data-model-configuration"></a>Opret en ny datamodelkonfiguration
1.  Klik på **Opret konfiguration** for at åbne dialogboksen.
2.  Gå til feltet **Navn**, og skriv "Model til at importere xml-fil".
3.  Klik på **Opret konfiguration**.
4.  Klik på **Designer**.
5.  Klik på **Ny** for at åbne dialogboksen Fjern.
6.  Skriv "Rod" i feltet **Navn**.
7.  Klik på **Tilføj**.
8.  Klik på **Ny** for at åbne dialogboksen Fjern.
9.  Skriv "Liste" i feltet **Navn**.
10. Vælg **Liste over poster** i feltet **Varetype**.
11. Klik på **Tilføj**.
12. Klik på **Ny** for at åbne dialogboksen Fjern.
13. Skriv 'Kode' i feltet **Navn**.
14. Vælg **Streng** i feltet **Varetype**.
15. Klik på **Tilføj**.
16. Klik på **Gem**.
17. Luk siden.
18. Klik på **Skift status**.
19. Klik på **Fuldfør**.
20. Klik på **OK**.

## <a name="create-a-format-for-data-import"></a>Opret et format til dataimport
1.  Klik på **Opret konfiguration** for at åbne dialogboksen.
2.  Gå til feltet **Ny**, og indtast "Format baseret på datamodel Model til at importere xml-fil".
3.  Gå til feltet **Navn**, og skriv "Format til at importere xml-fil".
4.  Vælg **Ja** i feltet **Understøtter dataimport**.
5.  Klik på **Opret konfiguration**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Designe et format til parsing af en indgående fil i XML-format
1.  Klik på **Designer**.
2.  Klik på **Tilføj rod** for at åbne dialogboksen.
3.  Vælg **XML\Element** i træet.
4.  Skriv "Rod" i feltet **Navn**.
5.  Klik på **OK**.
6.  Klik på **Tilføj** for at åbne dialogboksen.
7.  Vælg **XML\Element** i træet.
8.  Skriv 'Dokument' i feltet **Navn**.
9.  Vælg **Én mange** i feltet **Multiplicitet**.
10. Klik på **OK**.
11. Vælg **rod\layout** i træet.
12. Klik på **Tilføj** for at åbne dialogboksen.
13. Vælg **XML\Attribut** i træet.
14. Skriv "Id" i feltet **Navn**.
15. Klik på **OK**.
16. Klik på **Gem**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Udform en formattilknytning for at gemme oplysninger, der fortolkes, i datamodellen
1. Klik på **Knyt format til model**.
2. Klik på **Ny**.
3. Indtast eller vælg en værdi i feltet **Definition**.
4. Klik op linket i den valgte række på listen.
5. Skriv "Tilknytning" i feltet **Navn**.
6. Klik på **Gem**.
7. Klik på **Designer**.
8. Udvid **Format** i træet.
9. I træet skal du udvide **format\root: XML Element(root)**.
10. I træet skal du vælge **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
11. Klik på **Bind**.
12. I træet skal du udvide **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
13. I træet skal du vælge **format\root: XML Element(root)\document: XML Element 1..* (dokument)\id**.
14. I træet skal du udvide **List = format.root.document**.
15. I træet skal du vælge **List = format.root.document\Code**.
16. Klik på **Bind**.
17. Klik på **Gem**.
18. Luk siden.
 
## <a name="run-format-mapping"></a>Kør formattilknytning
1. Klik på **Kør**.
2. Klik på **Gennemse**, og vælg **IncomingDocumentToLearnHowToHandleOptionalAttributes xml**.
3. Klik på **OK**.

> [!NOTE]
> Den valgte fil er ikke importeret, da formatdesignet forudsætter, at attributten "id"' findes for elementet "Dokument", men den importerede fil indeholder ikke denne attribut.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Rediger formatstrukturen for at håndtere XML-attribut som valgfri
1. Luk siden.
2. I træet skal du udvide **root\document**.
3. I træet skal du vælge **root\document\id**.
4. Vælg **Ja** i feltet **Tom streng for manglende attribut**.
5. Klik på **Gem**.
 
## <a name="run-format-mapping-to-test-changes"></a>Kør formattilknytning for at teste ændringer
1. Klik på **Knyt format til model**.
2. Klik på **Kør**.
3. Klik på **Gennemse**, og vælg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Klik på **OK**.
5. Gennemse den genererede fil. 

> [!NOTE]
> Den samme fil er blevet importeret, da formatdesignet nu anser attributten "id" for elementet "Document" som valgfrit.
