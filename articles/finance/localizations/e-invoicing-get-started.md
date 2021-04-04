---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 56227e031f8205836bcae9ce26006fc8091c2863
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592544"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Kom i gang med tilføjelsesprogrammet til elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering.

Følgende tabel indeholder funktionerne for elektronisk fakturering og de forretningsdokumenter, de kan anvendes på.

| Funktionsnavn                         | Forretningsdokument |
|--------------------------------------|-------------------|
| Østrigske elektroniske fakturaer (AT)    | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Belgisk elektronisk faktura (BE)      | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Brasiliansk NF-e (BR)                  | <p>Regnskabsdokumentmodel 55</p><p>Rettelsesbrev</p> |
| Brasiliansk NFS-e ABRASF Curitiba (BR) | Serviceregnskabsdokument |
| Dansk elektronisk faktura (DK)       | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Egyptisk elektronisk faktura (EG)     | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Estisk elektronisk faktura (EE)     | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Finsk elektronisk faktura (FI)       | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Fransk elektronisk faktura (FR)       | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Tysk elektronisk faktura (DE)       | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| FatturaPA (IT)                       | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Mexicansk CFDI Interfactura (MX)       | <p>Salgsfaktura</p><p>Følgeseddel</p><p>Lageroverførsel</p><p>Betalingstillæg</p> |
| Hollandsk elektronisk faktura (NL)        | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Norsk elektronisk faktura (NO)    | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| Spansk elektronisk faktura (ES)      | <p>Salgsfaktura</p><p>Projektfaktura</p> |
| PEPPOL Elektronisk faktura            | <p>Salgsfaktura</p><p>Projektfaktura</p> |

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Konfigurere din Regulatory Configuration Service (RCS) og dit Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-miljø, så du kan sende til tilføjelsesprogrammet Elektronisk fakturering.
- Opret et servicemiljø, og udgiv det til tilføjelsesprogrammet Elektronisk fakturering. Du kan finde flere oplysninger i [Introduktion til administration af tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started-service-administration.md).
- Oprette en tilsluttet applikation. Du kan finde flere oplysninger i [Introduktion til administration af tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started-service-administration.md).
- Oprette en konfigurationsudbyder til organisationen. Få flere oplysninger i [Oprette konfigurationsudbyder og markere som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importere en funktion til elektronisk fakturering fra Microsoft-konfigurationsudbyder. 

1. Logge på din RCS-konto (Regulatory Configuration Service).
2. I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
3. Vælg **Import**, og vælg derefter **Synkroniser**.
4. Filtrer kolonnen **Konfigurationsudbyder** efter termen **Microsoft**.
5. Vælg navnet på en funktion til elektronisk fakturering i tabellen i starten af dette emne, og vælg derefter **Import**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Opret en funktion til tilføjelsesprogrammet til elektronisk fakturering for din organisationsudbyder.

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
2. Vælg **Tilføj** > **Baseret på eksisterende funktion**, og indtast navnet på den elektroniske faktureringsfunktion i feltet **Navn** .
3. Angiv en beskrivelse af funktionen i feltet **Beskrivelse**.
4. I feltet **Basisfunktionfeltet** skal du vælge den importerede funktion til elektronisk fakturering fra Microsoft-konfigurationsudbyderen.
5. Vælg **Opret funktion**.

## <a name="configure-the-electronic-invoicing-feature"></a>Konfigurere funktioner til elektronisk fakturering

Afhængigt af landet eller området kan funktionen til elektronisk fakturering kræve yderligere konfiguration. 

De specifikke trin finder du i dokumentationen "Kom i gang", som findes i dit land eller område.

## <a name="configure-the-application-setup"></a>Konfigurere opsætning af applikationen

1. Vælg den funktion til elektronisk fakturering, du har oprettet.
2. Kontroller, at **Kladde**-versionen er valgt under fanen **Version**.
3. Under fanen **Opsætning af applikation** skal du vælge **Opsætninger**.

    > [!NOTE]
    > Kontroller, at organisationen er angivet som **Aktiv** konfigurationsudbyder. Yderligere oplysninger findes i [Oprette konfigurationsudbyder og markere som aktive.](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. Vælg **Funktionsopsætning**, og vælg derefter **Tilknyttet program**.
5. Vælg **Tilføj** i sektionen **Elektroniske dokumenttyper**.
6. For hvert forretningsdokument, som funktionen understøtter, skal du vælge og angive en værdi for **Tabelnavn** i henhold til følgende tabel.

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

7. For hvert forretningsdokument, som funktionen understøtter, skal du vælge og angive en værdi for **Kontekst** i henhold til følgende tabel.

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

8. For hvert forretningsdokument, som funktionen understøtter, skal du vælge og angive en værdi for **Tilknytning af forretningsdokument** i henhold til følgende tabel.

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

Afhængigt af landet eller området kan funktionen til elektronisk fakturering kræve yderligere konfiguration.

De specifikke trin finder du i dokumentationen "Kom i gang", som findes i dit land eller område.

## <a name="deploy-the-electronic-invoicing-feature"></a>Implementere funktioner til elektronisk fakturering

1. Vælg den version af funktionen Elektronisk fakturering, du vil implementere, under fanen **Versioner**.
2. Vælg **Skift status** \> **Fuldfør**.
3. Vælg **Skift status** \> **Publicer**.
4. Vælg **Implementer**.
5. Angiv indstillingen **Implementer til tilknyttet applikation** til **Ja**.
6. Vælg den forbindelse, der er knyttet til din forekomst af Finans eller Supply Chain Management, på siden **Tilknyt applikation**.
7. Angiv indstillingen **Implementer til servicemiljø** til **Ja**.
8. Vælg det servicemiljø for elektronisk fakturering, hvor du vil implementere funktionen Elektronisk fakturering, i feltet **Servicemiljø**.
9. I feltet **Fra dato** skal du vælge den dato, hvor funktionen Elektronisk fakturering skal være gældende i tilføjelsesprogrammet Elektronisk fakturering.
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

- [Tilføjelsesprogrammet til oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Introduktion til tilføjelsesprogrammet til serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien](e-invoicing-bra-get-started.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Mexico](e-invoicing-mex-get-started.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien](e-invoicing-ita-get-started.md)
- [Elektroniske fakturaer til kunder i Egypten](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
