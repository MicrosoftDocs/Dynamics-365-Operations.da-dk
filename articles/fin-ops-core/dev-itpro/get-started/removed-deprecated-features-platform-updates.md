---
title: Fjernede eller udfasede platformfunktioner
description: Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet i platformopdateringer af Finance and Operations-apps.
author: sericks007
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6fc699907d30fff2d05e752ea055cae8d1134d9b
ms.sourcegitcommit: 3eaa71c889545318737b3bc88b05eae1a47ad2c0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/05/2020
ms.locfileid: "3433916"
---
# <a name="removed-or-deprecated-platform-features"></a>Fjernede eller udfasede platformfunktioner

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet i platformopdateringer af Finance and Operations-apps.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.12 af Finance and Operations-apps

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Udvidelser af gitter- eller gruppekontrolformularer, der indeholder ugyldige feltreferencer

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Datagruppeegenskaben for gitter- eller gruppekontrolelementer bruges til automatisk at få vist alle felterne i en feltgruppe. En gitter- eller gruppekontrol, der tilføjes som en udvidelse, kan indeholde felter, der ikke længere er defineret i feltgruppen, eller den kan mangle felter, der er defineret i feltgruppen. Dette kan medføre en inkonsistent funktionsmåde på kørselstidspunktet. Platformsopdateringer til version 10.0.12 af Finance and Operations-apps kategoriserer nu dette problem som en *compileradvarsel*. Du kan løse dette problem ved at åbne formularudvidelsen og gemme den.
| **Erstattet af en anden funktion?**   | Denne compileradvarsel erstattes af en compilerfejl i en senere opdatering. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Der introduceres en compileradvarsel i platformsopdateringer til version 10.0.12 af Finance and Operations-apps. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.11 af Finance and Operations-apps

### <a name="explicit-whitelisting-for-self-service-environments"></a>Eksplicit whitelisting til selvbetjeningsmiljøer

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Processen for IP-whitelisting er ændret. Selvbetjening understøtter ikke længere IP-whitelisting. |
| **Erstattet af en anden funktion?**   | Du kan finde flere oplysninger i [Konfiguration af betinget adgang til Azure Active Directory](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Produktområder, der er berørt**         | Sikkerhed |
| **Installationsindstilling**              | Sky |
| **Status**                         | **Udfaset:** Denne funktion er helt udfaset for installationer med selvbetjening. |

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Understøttelse af de seneste versioner af Visual Studio kræver ændringer af X++ udvidelserne til Visual Studio. Disse ændringer er ikke kompatible med Visual Studio 2015. |
| **Erstattet af en anden funktion?**   | Visual Studio 2017 erstatter Visual Studio 2015 som den installerede og påkrævede version. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Når tilgængeligheden af nye virtuelle maskiner (VM'er) med Visual Studio 2017 er annonceret, skal eksisterende VM'er med kun Visual Studio 2015 geninstalleres ved frigivelsesbølge 1 i 2021. |

### <a name="field-groups-containing-invalid-field-references"></a>Feltgrupper, der indeholder ugyldige feltreferencer

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Feltgrupper i tabellens metadatadefinitioner kan indeholde feltreferencer, der ikke er gyldige. Hvis disse feltgrupper er installeret, kan de medføre kørselsfejl i Financial Reporting og Microsoft SQL Server Reporting Services (SSRS). Platformopdatering 23 introducerede en *compileradvarsel*, der gjorde det muligt, at dette metadataproblem kunne rettes. Platformsopdateringer til version 10.0.11 af Finance and Operations-apps kategoriserer dette problem som en *compilerfejl*.<p>Følg disse trin for at løse dette problem.</p><ol><li>Fjern den ugyldige feltreference fra definitionen af tabelfeltgruppen.</li><li>Kompilér igen.</li><li>Kontrollér, at eventuelle fejl er løst.</li></ol> |
| **Erstattet af en anden funktion?**   | Denne compilerfejl erstatter permanent compileradvarslen.  |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | **Udfases:** Compileradvarslen er en compilerfejl i platformsopdateringer til version 10.0.11 af Finance and Operations-apps. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-licenser, der er oprettet ved hjælp af SHA1-hashing-algoritmen

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Den proces, man bruger til at oprette ISV-licenser (Independent Software Vendor), er blevet ændret. Du kan få flere oplysninger i afsnittet [Independent software vendor (ISV) licensing](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Erstattet af en anden funktion?**   | Ja. Brug Windows PowerShell til at oprette licenser. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | <strong>Udfases:</strong> ISV-licenser, der er oprettet ved hjælp af SHA1-hashing-algoritmen. Denne algoritme er afhænger af certifikater, der er oprettet med hjælpeprogrammet MakeCert, og dette værktøj er udfaset.<p><strong>Udfases:</strong> Brugen af SHA1 til sikkerheds- eller hashing-formål. SHA1 vil ophøre med at fungere i starten af 2021. Derfor bør den ikke længere bruges.<p><strong>Fjernet:</strong> Understøttelse af TLS (Transport Layer Security) 1.0 og TLS 1.1 indgående eller udgående anmodninger. |

## <a name="platform-update-32"></a>Platform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Ændring af anmodning om arbejdsgang indeholder ikke længere rullelisten Brugervalg
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Dette var et sikkerhedsproblem, fordi anmodningen om ændring kunne sendes til en ikke-tiltænkt bruger. Dette var også et anvendelighedsproblem, fordi den tvang brugeren til at afgøre, hvem der var arbejdsgangsigangsætteren og vælge dem manuelt.  |
| **Erstattet af en anden funktion?**   | Nr. |
| **Produktområder, der er berørt**         | Arbejdsgang |
| **Installationsindstilling**              | Alt |
| **Status**                         | Rullelisten Brugervalg blev fjernet fra dialogboksen Ændring af anmodning i platformsopdatering 32. Anmodninger om ændring af anmodninger sendes efter hensigten automatisk til igangsætteren. Du kan finde flere oplysninger om denne funktion under [Handlinger i godkendelsesprocesser i arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Link til integreret detaljeadgang understøttes ikke længere i sideinddelte dokumenter, der gengives af den skybaserede tjeneste 
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Navigations URL-adresser, der er integreret i dokumenter, der er gengivet af tjenesten, kan indeholde følsomme virksomhedsdata. Vi fjerner understøttelse af link til integreret detaljeadgang i dokumenter som en sikkerhedsforanstaltning, der beskytter kundens data yderligere. Brugerne vil også få gavn af en forbedret ydeevne, når de opretter dokumenter interaktivt, som følge af denne ændring.  |
| **Erstattet af en anden funktion?**   | Ingen |
| **Produktområder, der er berørt**         | Rapportering |
| **Installationsindstilling**              | Alt |
| **Status**                         | Denne funktion fjernes aktivt fra tjenesten.<br><br>Den moderne klient tilbyder adskillige muligheder for at lave visninger, der omfatter automatisk genererede links, som kan hjælpe dig med at navigere i programmet. Sideinddelte dokumenter, der gengives af tjenesten, anbefales til ekstern kommunikation, der sendes via mail, arkiveres og udskrives for modtagere. Vi har forbedret oplevelsen af at få vist dokumenter direkte i browseren, som giver direkte adgang til lokale printere. Du kan finde flere oplysninger i [Vis PDF-dokumenter med en integreret fremviser](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner
Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../migration-upgrade/deprecated-features.md).

