---
title: Importere filer i XML-format med valgfrie attributter
description: Dette emne giver oplysninger om design af ER-formater, der angiver XML-attributter til fortolkning af indgående elektroniske dokumenter i XML-format.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 10795c90cb90961c17a4326b71ed43dc72039f2b
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117419"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Importere filer i XML-format med valgfrie attributter

[!include [banner](../includes/banner.md)]

Du kan designe ER-formater for at parse indgående elektroniske dokumenter i XML-format. Visse attributter af XML-elementer kan angives i designet ER-format som valgfrie. Det giver dig mulighed for at håndtere indgående filer med og uden sådanne XML-attributter korrekt. Derefter kan du bruge indholdet fra disse filer til at opdatere programdata.

Hvis du vil vide mere om denne funktion, skal du udføre trinnene i [(RCS) – Importere filer i XML-format med valgfrie attributter](tasks/import-files-xml-format-optional-attributes.md), der er en del af 7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677). Du kan hente denne opgaveguide og tilknyttede eksempelfiler i [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).


| Indholdsbeskrivelse       | Fil                                                         |
|---------------------------|--------------------------------------------------------------|
| Eksempelfil i XML-format | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Opgaveguide                | RCS Importere filer i XML-format med valgfrie attributter.axtr |


Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan designe konfiguration af ER-format til at importere filer i XML-format, der indeholder valgfrie attributter. For at fuldføre disse trin skal du først fuldføre trinnene i proceduren [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md). Før du går i gang, kan du hente og gemme filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml lokalt i Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).

1. Gå til **Organisationsadministration** > **Arbejdsområder** > **Elektronisk rapportering**.
2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis denne konfigurationsudbyder ikke vises, skal du fuldføre trinnene i emnet [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Klik på **Rapporteringskonfigurationer**.

## <a name="create-a-new-data-model-configuration"></a>Opret en ny datamodelkonfiguration
1. Klik på **Opret konfiguration** for at åbne dialogboksen.
2. Gå til feltet **Navn**, og skriv "Model til at importere xml-fil".
3. Klik på **Opret konfiguration**.
4. Klik på **Designer**.
5. Klik på **Ny** for at åbne dialogboksen Fjern.
6. Skriv "Rod" i feltet **Navn**.
7. Klik på **Tilføj**.
8. Klik på **Ny** for at åbne dialogboksen Fjern.
9. Skriv "Liste" i feltet **Navn**.
10.    Vælg **Liste over poster** i feltet **Varetype**.
11.    Klik på **Tilføj**.
12.    Klik på **Ny** for at åbne dialogboksen Fjern.
13.    Skriv 'Kode' i feltet **Navn**.
14.    Vælg **Streng** i feltet **Varetype**.
15.    Klik på **Tilføj**.
16.    Klik på **Gem**.
17.    Luk siden.
18.    Klik på **Skift status**.
19.    Klik på **Fuldfør**.
20.    Klik på **OK**.

## <a name="create-a-format-for-data-import"></a>Opret et format til dataimport
1. Klik på **Opret konfiguration** for at åbne dialogboksen.
2. Gå til feltet **Ny**, og indtast "Format baseret på datamodel Model til at importere xml-fil".
3. Gå til feltet **Navn**, og skriv "Format til at importere xml-fil". 
4. Vælg **Ja** i feltet **Understøtter dataimport**.
5. Klik på **Opret konfiguration**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Designe et format til parsing af en indgående fil i XML-format
1. Klik på **Designer**.
2. Klik på **Tilføj rod** for at åbne dialogboksen.
3. Vælg **XML\Element** i træet.
4. Skriv "Rod" i feltet **Navn**.
5. Klik på **OK**.
6. Klik på **Tilføj** for at åbne dialogboksen.
7. Vælg **XML\Element** i træet.
8. Skriv 'Dokument' i feltet **Navn**.
9. Vælg **Én mange** i feltet **Multiplicitet**.
10.    Klik på **OK**.
11.    Vælg **rod\layout** i træet.
12.    Klik på **Tilføj** for at åbne dialogboksen.
13.    Vælg **XML\Attribut** i træet.
14.    Skriv "Id" i feltet **Navn**.
15.    Klik på **OK**.
16.    Klik på **Gem**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Udform en formattilknytning for at gemme oplysninger, der fortolkes, i datamodellen
1.    Klik på **Knyt format til model**.
2.    Klik på **Ny**.
3.    Indtast eller vælg en værdi i feltet **Definition**.
4.    Skriv "Tilknytning" i feltet **Navn**.
5.    Klik på **Gem**.
6.    Klik på **Designer**.
7.    Udvid **Format** i træet.
8.    I træet skal du udvide **format\root: XML Element(root)**.
9.    I træet skal du vælge **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
10.    Klik på **Bind**.
11.    I træet skal du udvide **format\root: XML Element(root)\document: XML Element 1..* (dokument)**.
12.    I træet skal du vælge **format\root: XML Element(root)\document: XML Element 1..* (dokument)\id**.
13.    I træet skal du udvide **List = format.root.document**.
14.    I træet skal du vælge **List = format.root.document\Code**.
15.    Klik på **Bind**.
16.    Klik på **Gem**.
17.    Luk siden.

## <a name="run-format-mapping"></a>Kør formattilknytning
1. Klik på **Kør**.
2. Klik på **Gennemse**, og vælg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes xml**.
3. Klik på **OK**.

> [!NOTE]
> Den valgte fil er ikke importeret, da formatdesignet forudsætter, at attributten "id"' findes for elementet "dokument", men den importerede fil indeholder ikke denne attribut.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Rediger formatstrukturen for at håndtere XML-attribut som valgfri
1. Luk siden.
2. I træet skal du udvide **root\document**.
3. I træet skal du vælge **root\document\id**.
4. Vælg **Ja** i feltet **Tom streng for manglende attribut**.
5. Klik på **Gem**.

## <a name="run-format-mapping-to-test-changes"></a>Kør formattilknytning for at teste ændringer
1. Klik på **Knyt format til model**.
2. Klik på **Kør**.
3. Klik på **Gennemse**, og vælg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes xml**.
4. Klik på **OK**.
5. Gennemse den genererede fil. Bemærk, at den samme fil er blevet importeret, da formatdesignet nu anser attributten "id" for elementet "dokument" som valgfrit.
