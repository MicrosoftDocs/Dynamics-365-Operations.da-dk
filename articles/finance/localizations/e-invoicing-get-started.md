---
title: Start her med elektronisk fakturering
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: cf553f2ffecf18859b88932e68360231ca46410f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840118"
---
# <a name="get-started-with-electronic-invoicing"></a>Start her med elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering. Dette emne fører dig gennem de almindelige konfigurationstrin i RCS (Regulatory Configuration Services) og Dynamics 365 Finance, og det indeholder de trin, du skal følge for at sende forretningsdokumenter og gennemgå behandlingsresultaterne.

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Konfigurer Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) og dit Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-miljø. Du kan finde flere oplysninger i [Start her med serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md).
- Oprette en konfigurationsudbyder til organisationen. Yderligere oplysninger finder du i [Oprette en konfigurationsudbyder og markere den som aktiv](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importere en funktion til elektronisk fakturering fra Microsoft-konfigurationsudbyder. 

1. Logge på din RCS-konto (Regulatory Configuration Service).
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
3. Vælg **Import**, og vælg derefter **Synkroniser**.
4. Filtrer kolonnen **Konfigurationsudbyder** efter termen **Microsoft**.
5. Vælg navnet på en funktion til elektronisk fakturering i tabellen i starten af dette emne, og vælg derefter **Import**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Opret en funktion til tilføjelsesprogrammet til elektronisk fakturering for din organisationsudbyder.

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
2. Vælg **Tilføj** > **Baseret på eksisterende funktion**, og indtast navnet på den elektroniske faktureringsfunktion i feltet **Navn** .
3. Angiv en beskrivelse af funktionen i feltet **Beskrivelse**.
4. I feltet **Basisfunktionfeltet** skal du vælge den importerede funktion til elektronisk fakturering fra Microsoft-konfigurationsudbyderen.
5. Vælg **Opret funktion**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til den elektroniske fakturafunktion

Afhængigt af landet eller området kan funktionen til elektronisk fakturering kræve specifik konfiguration. 

De specifikke trin finder du i dokumentationen "Kom i gang", som findes i dit land eller område.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Importere modeltilknytningskonfigurationer fra elektronisk rapportering

1. Vælg i RCS arbejdsområdet **Elektronisk rapportering**.
2. På listen over **Microsoft**-konfigurationsudbydere skal du vælge **Lagre**.
3. Vælg **Global** og vælg **Åbn** i handlingsruden.
4. Importér modeltilknytningskonfigurationerne i henhold til følgende tabel ved hjælp af funktionsnavnet.

| Funktionsnavn                         | Modeltilknytningskonfiguration |
|--------------------------------------|-----------------------------|
| Østrigske elektroniske fakturaer (AT)    | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Belgisk elektronisk faktura (BE)      | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Brasiliansk NF-e (BR)                  | <p>Kontekstmodel for debitorfaktura</p><p>Regnskabsdokumenter</p><p>Svarmeddelelsesmodel</p> |
| Brasiliansk NFS-e ABRASF Curitiba (BR) | <p>Kontekstmodel for debitorfaktura</p><p>Regnskabsdokumenter</p><p>Svarmeddelelsesmodel</p> |
| Dansk elektronisk faktura (DK)       | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Egyptisk elektronisk faktura (EG)     | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p><p>Svarmeddelelsesmodel</p> |
| Estisk elektronisk faktura (EE)     | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Finsk elektronisk faktura (FI)       | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Fransk elektronisk faktura (FR)       | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Tysk elektronisk faktura (DE)       | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| FatturaPA (IT)                       | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Mexicansk CFDI Interfactura (MX)       | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p><p>Svarmeddelelsesmodel</p> |
| Hollandsk elektronisk faktura (NL)        | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Norsk elektronisk faktura (NO)    | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| Spansk elektronisk faktura (ES)      | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |
| PEPPOL Elektronisk faktura            | <p>Kontekstmodel for debitorfaktura</p><p>Fakturamodel</p> |


## <a name="configure-the-application-setup"></a>Konfigurere opsætning af applikationen

1. Vælg den funktion til elektronisk fakturering, du har oprettet.
2. Under fanen **Opsætning af applikation** skal du vælge **Opsætninger**.
3. Vælg den forbindelse, der er knyttet til din forekomst af Finance eller Supply Chain Management, i feltet **Tilknyt applikation**.
4. Vælg **Tilføj** i sektionen **Elektroniske dokumenttyper**.
5. Vælg og angiv en værdi for **Tabelnavn** i henhold til følgende tabel.

    | Funktionsnavn                         | Forretningsdokument | Tabel-label |
    |--------------------------------------|-------------------|------------|
    | Østrigske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskabsdokument</p><p>Rettelsesbrev</p> | Regnskabsdokument |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Serviceregnskabsdokument | Regnskabsdokument |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Projektfaktura | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Mexicansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverførsel</p><p>Betalingstillæg</p> | Debitorfakturajournal |
    | Hollandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |
    | PEPPOL Elektronisk faktura            | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Debitorfakturajournal</p><p>Projektfaktura</p> |

7. Vælg og angiv en kontekstværdi for hvert tabelnavn, du opretter, i henhold til følgende tabel.

    | Funktionsnavn                         | Forretningsdokument | Kontekst |
    |--------------------------------------|-------------------|---------|
    | Østrigske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskabsdokument</p><p>Rettelsesbrev</p> | <p>Kontekstmodel for debitorfaktura – regnskabsdokumentkontekst</p><p>Kontekstmodel for debitorfaktura – FD-korrektionsbrevkontekst</p> |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Serviceregnskabsdokument| Kontekstmodel for debitorfaktura – regnskabsdokumentkontekst |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Mexicansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverførsel</p><p>Betalingstillæg</p> | Kontekstmodel for debitorfaktura – debitorfakturakontekst |
    | Hollandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |
    | PEPPOL Elektronisk faktura            | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Kontekstmodel for debitorfaktura – debitorfakturakontekst</p><p>Kontekstmodel for debitorfaktura – projektfakturakontekst</p> |

8. For hvert tabelnavn og hver kontekst skal du vælge og angive en værdi for Tilknytning af forretningsdokument i henhold til følgende tabel.

    | Funktionsnavn                         | Forretningsdokument | Tilknytning af forretningsdokument |
    |--------------------------------------|-------------------|---------------------------|
    | Østrigske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Brasiliansk NF-e (BR)                  | <p>Regnskabsdokument</p><p>Rettelsesbrev</p> | <p>Tilknytning af regnskabsdokumenter – tilknytning af regnskabsdokumenter</p><p>Tilknytning af regnskabsdokumenter – tilknytning af rettelsesbrev</p> |
    | Brasiliansk NFS-e ABRASF Curitiba (BR) | Serviceregnskabsdokument | Tilknytning af regnskabsdokumenter – tilknytning af regnskabsdokumenter |
    | Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Mexicansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverførsel</p><p>Betalingstillæg</p> | Tilknytning af fakturamodel – Debitorfaktura |
    | Hollandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |
    | PEPPOL Elektronisk faktura            | <p>Salgsfaktura</p><p>Projektfaktura</p> | <p>Tilknytning af fakturamodel – Debitorfaktura</p><p>Tilknytning af fakturamodel – projektfaktura</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Landespecifik konfiguration af programopsætning

Afhængigt af landet eller området kan programopsætningen kræve specifik konfiguration. 

De specifikke trin finder du i dokumentationen "Kom i gang", som findes i dit land eller område.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Implementere funktionen Elektronisk fakturering i servicemiljøet

1. Vælg den version af funktionen Elektronisk fakturering, du vil implementere, under fanen **Versioner**.
2. Vælg **Skift status** \> **Fuldfør**.
3. Vælg **Skift status** \> **Publicer**.
4. Vælg **Implementer**.
5. Angiv indstillingen **Implementer til tilknyttet applikation** til **Nej**.
6. Angiv indstillingen **Implementer til servicemiljø** til **Ja**.
7. Vælg det servicemiljø for elektronisk fakturering, hvor du vil implementere funktionen Elektronisk fakturering, i feltet **Servicemiljø**.
8. I feltet **Fra dato** skal du vælge den dato, hvor funktionen Elektronisk fakturering skal være gældende i Elektronisk fakturering.
9. Vælg **OK**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Implementere funktionen Elektronisk fakturering i tilknyttet program

1. Vælg den version af funktionen Elektronisk fakturering, du vil implementere, under fanen **Versioner**.
4. Vælg **Implementer**.
5. Angiv indstillingen **Implementer til tilknyttet applikation** til **Ja**.
6. Vælg den forbindelse, der er knyttet til din forekomst af Finance eller Supply Chain Management, i feltet **Tilknyt applikation**.
7. Angiv indstillingen **Implementer til servicemiljø** til **Nej**.
10. Vælg **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Aktivere funktionen til elektronisk fakturering i Finance eller Supply Chain Management

1. Log på Finans eller Supply Chain Management, og kontroller, at du er i den korrekte juridiske enhed.
2. Gå til **Organisationsadministration** \> **Konfiguration** \> **Elektroniske dokumentparametre**.
3. Under fanen **Funktioner** skal du vælge den specifikke funktion for lande/område, der skal aktivere funktionen Elektronisk fakturering for Finans eller Supply Chain Management. Følgende tabel indeholder en liste over de funktioner for elektronisk fakturering, der er tilgængelige for bestemte lande/områder. 

    | Funktionsnavn                                          | Land/område  |
    |-------------------------------------------------------|-----------------|
    | Østrigske elektroniske fakturaer (AT)                     | Østrig         |
    | Belgisk elektronisk faktura (BE)                       | Belgien         |
    | CFDI Mexicansk elektronisk faktura (MX)                  | Mexico          |
    | Dansk elektronisk faktura (DK)                        | Danmark         |
    | Hollandsk elektronisk faktura (NL)                         | Nederlandene |
    | Egyptisk elektronisk faktura (EG)                      | Egypten           |
    | Estisk elektronisk faktura (EE)                      | Estland         |
    | Finsk elektronisk faktura (FI)                       | Finland         |
    | Fransk elektronisk faktura (FR)                        | Frankrig          |
    | Tysk elektronisk faktura (DE)                        | Tyskland         |
    | Italiensk elektronisk faktura (IT)                       | Italien           |
    | NF-e Federal - brasiliansk elektronisk faktura (BR)      | Brasilien          |
    | NFS-e - Brasiliansk tjeneste (by) elektronisk faktura   | Brasilien          |
    | Norsk elektronisk faktura (NO)                     | Norge          |
    | PEPPOL Elektronisk faktura                             | Globalt          |
    | Spansk elektronisk faktura (ES)                       | Spanien           |

4. Vælg **Gem**.

## <a name="issue-electronic-invoices"></a>Udstede elektroniske fakturaer

1. Gå til **Organisationsadministration** \> **Periodisk** \> **Elektroniske dokumenter** \> **Send elektroniske dokumenter**.
2. I oversigtspanelet **Medtaget post** skal du vælge **Filtrer**.
3. Vælg **Tilføj** for at føje et tabelnavn til forespørgselsfiltret.
4. Vælg den tabel, der indeholder fakturaer.

    > [!NOTE]
    > Tabelnavnet skal være vist i tabellen i afsnittet [Konfigurere applikationskonfiguration](#configure-the-application-setup) tidligere i dette emne.

5. Vælg det feltnavn fra tabellen, du vil anvende til forespørgsel.
6. Angiv tabelnavnet og feltnavnet for de kriterier, der skal forespørges på.
7. Gentag trin 5 og 6 for at føje flere felter og kriterier til forespørgslen, og vælg derefter **OK**.
8. Vælg **OK**.

## <a name="view-submission-logs"></a>Få vist indsendelseslogge

1. Gå til **Organisationsadministration** \> **Periodisk** \> **Elektroniske dokumenter** \> **Indsendelseslog for elektroniske dokumenter**.
2. Vælg den tabel, der indeholder fakturaerne, i feltet **Dokumenttype**.

    > [!NOTE]
    > Tabelnavnet skal være vist i tabellen i afsnittet [Konfigurere applikationskonfiguration](#configure-the-application-setup) tidligere i dette emne.

3. Marker en faktura i gitteret, og vælg derefter **Forespørg** \> **Indsendelsesdetaljer**.


## <a name="related-topics"></a>Relaterede emner

- [Oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Start her med serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Start her med elektronisk fakturering for Brasilien](e-invoicing-bra-get-started.md)
- [Start her med elektronisk fakturering for Mexico](e-invoicing-mex-get-started.md)
- [Start her med elektronisk fakturering for Italien](e-invoicing-ita-get-started.md)
- [Elektroniske fakturaer til kunder i Egypten](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
