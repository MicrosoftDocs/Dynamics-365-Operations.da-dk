---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien i Finans og Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: eaf9433ad2d9ccf3d3c5632d0f2d4fe772ff8bde
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592664"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien 

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du kommer i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien. Procedurer i dette emne fører dig gennem de konfigurationstrin, der er landeafhængige i RCS (Regulatory Configuration Services), og supplerer de trin, der er beskrevet i [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til den brasilianske NF-r (BR) elektroniske fakturafunktion

Hvis du vil konfigurere funktionen NF-e (BR) elektronisk fakturering, kræver det, at de specifikke trin er udført. Nogle af parametrene fra konfigurationerne er udgivet med standardværdier, så de skal gennemses og opdateres, så de passer bedre til din forretningsoperation.

### <a name="prerequisites"></a>Forudsætninger

Før du fuldfører proceduren i dette afsnit, skal du oprette brasiliansk NF-e (BR) Elektronisk faktureringsfunktion i din organisation, som beskrevet i afsnittet **Opret en elektronisk fakturering under din organisationsudbyder** emnet [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
2. På siden **Funktioner for elektronisk fakturering** skal du kontrollere, at den **Brasiliansk NF-e (BR)** elektroniske fakturafunktion, du har oprettet, er valgt.
3. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
4. Vælg **Send** i gitteret under fanen **Opsætninger**, og vælg derefter **Rediger**.
5. Vælg handlingen **(Forhåndsvisning) Signer xml-dokument** i feltet **Handling** på fanen **Handlinger**.
6. Vælg **Certifikatnavn** i feltet **Parametre**, og angiv navnet på det certifikat, der er tilknyttet parameteren Key vault i feltet **Værdi**.
7. Vælg handlingen **(Forhåndsvisning) Kald brasiliansk SEFAZ-tjeneste** i feltet **Handlinger** på fanen **Handlinger**.
8. Vælg parameteren **URL-adresse** i feltgruppen **Parametre**.
9. Gennemse og opdater URL-adressen for de webtjenester, der er udgivet af SEFAZ-dokumentationen for din tilstand, i feltet **Værdi**, og vælg derefter **Gem**.
10. Under fanen **Anvendelsesregler** i feltgruppen **Opsætning af anvendelighedsregel** kan du gennemse og opdatere feltkriterierne for **Tilstand** efter behov for samme tilstand, som URL-adressen til webtjenesterne refererer til.
11. Vælg **Gem**, og luk siden.
12. Du kan konfigurere programopsætningen under [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til ansøgningsopsætning for den brasilianske NF-r (BR) elektroniske fakturafunktion

Hvis du vil konfigurere ansøgningsopsætningen for funktionen NF-e (BR) elektronisk fakturering, kræver det, at de specifikke trin er udført. Fuldfør disse trin, før du implementerer funktionen Elektronisk fakturering i dit servicemiljø for tilføjelsesprogram til elektronisk fakturering.

### <a name="prerequisites"></a>Forudsætninger

Før du fuldfører proceduren i dette afsnit, skal du oprette og initiere ansøgningskonfigurationen til brasiliansk NF-e (BR) Elektronisk faktureringsfunktion som beskrevet i afsnittet **Konfigurere opsætning af applikationen** i emnet [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
2. På siden **Funktioner til elektronisk fakturering** skal du kontrollere, at den **Brasiliansk NF-e (BR)** elektroniske fakturafunktion er valgt.
3. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
4. På fanen **Opsætninger** skal du vælge **Opsætning af ansøgning** og i feltet **Tilsluttet ansøgning** skal du vælge den ansøgning, du vil installere.
5. Vælg **Regnskabsdokumentnotat** i feltet **Tabelnavn**.
6. Vælg **Svartyper**, og vælg derefter **Ny**.
7. Angiv "Svar" i feltet **Svartype** som fast værdi, og indtast "Beskrivelse" i feltet **Beskrivelse**.
8. Vælg **Afventer** i feltet **Indsendelsesstatus**.
9. I feltet **Modeltilknytning** skal du vælge **Modeltilknytning fra svarmeddelelse** med **(Forhåndsversion) Format til import af svarmeddelelse** og derefter vælge **Gem**.
10. Vælg **Ny** og i feltet **Svartype** skal du angive "ResponseData" som fast værdi, og indtast "Beskrivelse" i feltet **Beskrivelse**.
11. Vælg **Afventer** i feltet **Indsendelsesstatus**.
12. I feltet **Modeltilknytning** skal du vælge **Import af svardata** med **(Forhåndsversion) NF-e import af svardataformat (BR)** og derefter vælge **Gem**.
13. Hvis du vil implementere funktionen Elektronisk fakturering, skal du se [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til den brasilianske NFS-e ABRASF Curitiba (BR) elektroniske fakturafunktion

Hvis du vil konfigurere funktionen brasiliansk NFS-e ABRASF Curitiba (BR) elektronisk fakturering, kræver det, at de specifikke trin er udført. Nogle af parametrene fra konfigurationerne er udgivet med standardværdier, så de skal gennemses og opdateres, så de passer bedre til din forretningsoperation.

### <a name="prerequisites"></a>Forudsætninger

Før du gennemfører proceduren i dette afsnit, skal du oprette en funktion til brasiliansk NFS-e ABRASF Curitiba (BR) elektronisk fakturering i organisationen. Dette er beskrevet i afsnittet **Konfigurer elektronisk fakturering** i emnet [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
2. På siden **Funktioner til elektronisk fakturering** skal du kontrollere, at den **Brasiliansk NFS-e ABRASF Curitiba (BR)** elektroniske fakturafunktion, du har oprettet, er valgt.
3. Kontroller, at versionen **Kladde** er valg under fanen **Versioner**, og vælg **Overfør** på fanen **Opsætninger**.
4. Vælg **Rediger**, og vælg fanen **Handlinger** i feltgruppen **Handlinger**, vælg den første forekomst af **(Forhåndsversion) Underskriv xml-dokument**.
5. Vælg **Certifikatnavn** i feltgruppen **Parametre**.
6. Angiv navnet det certifikat, der er tilknyttet parameteren Key vault, i feltet **Værdi**.
7. I feltgruppen **Handlinger** skal du vælge den anden forekomst af **(Forhåndsvisning) Signér xml-dokument**.
8. Vælg **Certifikatnavn** i feltgruppen **Parametre**.
9. Angiv navnet det certifikat, der er tilknyttet parameteren Key vault, i feltet **Værdi**.
10. Vælg handlingen **(Forhåndsvisning) Kald brasiliansk SEFAZ-tjeneste** i feltet **Handlinger** på fanen **Handlinger**.
11. Vælg parameteren **URL-adresse** i feltgruppen **Parametre**.
12. Gennemse og opdater URL-adressen for de webtjenester, der er udgivet af momsafdelingen for byen Curitiba i feltet **Værdi**, og vælg derefter **Gem**.
13. Vælg **Forespørg** i gitteret under fanen **Opsætninger**, og vælg derefter **Rediger**.
14. Vælg handlingen **(Forhåndsvisning) Kald brasiliansk SEFAZ-tjeneste** i feltet **Handlinger** på fanen **Handlinger**.
15. Vælg parameteren **URL-adresse** i feltgruppen **Parametre**.
16. Gennemse og opdater URL-adressen for de webtjenester, der er udgivet af momsafdelingen for byen Curitiba i feltet **Værdi**.
17. Vælg **Gem**, og luk derefter siden.
18. Du kan konfigurere programopsætningen under [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til ansøgningsopsætningen for den brasilianske NFS-e ABRASF Curitiba (BR) elektroniske fakturafunktion

Hvis du vil konfigurere programopsætningen for NFS-e ABRASF Curitiba (BR) Elektronisk fakturering, skal du fuldføre de specifikke trin, før du implementerer funktionen elektronisk fakturering i det tjenestemiljø, hvor du kan fakturere elektronisk fakturering.

### <a name="prerequisites"></a>Forudsætninger

Før du fuldfører proceduren i dette afsnit, skal du oprette og initiere en brasiliansk NFs-e ABRASF Curitiba (BR) Elektronisk faktureringsfunktion som beskrevet i afsnittet **Konfigurere opsætning af applikationen** i emnet [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md).

1. I RCS i arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.
2. På siden **Funktioner til elektronisk fakturering** skal du kontrollere, at den **Brasiliansk NFS-e ABRASF Curitiba (BR)** elektroniske fakturafunktion er valgt.
3. Kontroller, at versionen **Kladde** er valg under fanen **Versioner**, og vælg **Ansøgningsopsætning** på fanen **Opsætninger**.
4. I feltet **Tilknyttet ansøgning** skal du vælge den ansøgning, du vil implementere.
5. I feltet **Tabelnavn** skal du kontrollere, at sidehovedet på regnskabsdokumentet er valgt.
6. Vælg **Svartyper**, og vælg derefter **Ny**.
7. Angiv "ABRASFCuritibaSubmitResponse" i feltet **Svartype** som fast værdi, og indtast "Beskrivelse" i feltet **Beskrivelse**.
8. Vælg **Afventer** i feltet **Indsendelsesstatus**.
9. I feltet **Modeltilknytning** skal du vælge **Import af svarmeddelelse** med **(Forhåndsversion) NFS-e ABRASF Curitiba import af svarmeddelelse (BR)** og derefter vælge **Gem**.
10. Vælg **Ny** og i feltet **Svartype** skal du angive "ABRASFCuritibaSubmitResponseData" som fast værdi, og indtast "Beskrivelse" i feltet **Beskrivelse**.
11. Vælg **Afventer** i feltet **Indsendelsesstatus**.
12. I feltet **Modeltilknytning** skal du vælge **Import af svardata** med **(Forhåndsversion) NFS-e ABRASF import af svardataformat (BR)** og derefter vælge **Gem**.
13. Vælg **Ny** og i feltet **Svartype** skal du angive "ABRASFCuritibaInquireResponse", og indtast "Beskrivelse" i feltet **Beskrivelse**.
14. Vælg **Afventer** i feltet **Indsendelsesstatus**.
15. I feltet **Modeltilknytning** skal du vælge **Import af svarmeddelelse** med **(Forhåndsversion) NFS-e ABRASF Curitiba import af svarmeddelelse (BR).**
16. Vælg **Gem**, og vend tilbage til emnet [Kom i gang med tilføjelsesprogrammet Elektronisk fakturering](e-invoicing-get-started.md) for at installere Elektronisk faktureringsfunktion.

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Aktivering af funktionerne **NF-e Federal - Brasiliansk elektronisk faktura (BR)** og **NFS-e - Brasiliansk (by) elektroniske fakturatjeneste** kan evt. kræve, at der sendes begrænsede data, herunder organisationsmomsregistrerings-id. Disse data vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer til denne skattemyndighed i det foruddefinerede format, der kræves til integration med myndighedernes webtjeneste. Som administrator kan du aktivere eller deaktivere funktionerne for den elektroniske **NF-e Federal - Brasiliansk elektronisk faktura (BR)** og **NFS-e - Brasiliansk (by) elektroniske fakturatjeneste**. Dette beskrives i følgende trin: 

1. Gå til **Organisationsadministration** > **Konfiguration** > **Elektroniske dokumentparametre**. 
2. Under fanen **Funktioner** skal du markere den række, der indeholder funktionen **NF-e Federal - Brasiliansk elektronisk faktura (BR)** eller **NFS-e - Brasiliansk (by) elektroniske fakturatjeneste**, og vælge funktionen. De data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionerne med Erklæring om beskyttelse af personlige oplysninger i dokumentationen for den lande- eller områdespecifikke funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Tilføjelsesprogrammet til oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Introduktion til tilføjelsesprogrammet til serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Introduktion til tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
