---
title: Fejl ved certificeringsstien ved oprettelse af appforbindelse
description: Hvis Warehouse Management-appen viser fejlen "Trust anker til certificeringsstien ikke fundet", kan du bruge denne side til at løse eller løse problemet.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475907"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Tillidsanker til certificeringsstien blev ikke fundet ved oprettelse af appforbindelse

## <a name="symptoms"></a>Symptomer

Når du forsøger at oprette forbindelse til Supply Chain Management, kan du få vist følgende fejlmeddelelse i appen Warehouse Management:

> java.security.cert.certPathValidatorException: Tillidsanker for certificeringsstien blev ikke fundet.

Dette problem kan påvirke enheder med følgende egenskaber:

- **OS-version**: Android 4.4.x (f.eks. Zebra TC55). Der er ingen problemer med de seneste Android-versioner.
- **Placering af Supply Chain Management**: Sky
- **Forbindelsestilstand**: Klientprogram eller certifikat

## <a name="possible-cause"></a>Mulig årsag

Microsoft kan have opdateret de SSL-servercertifikater, der bruges af Supply Chain Management. Som følge heraf kan rodcertifikatet og/eller et af mellemcertifikaterne være ændret, så det nye certifikat ikke findes på listen over pålidelige systemcertifikater for den mobile enhed. Nyere versioner af opdaterer automatisk Android-listerne over betroede certifikater, men Android 4.4.x gør det ikke.

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at benytte en af følgende fremgangsmåder:

- Brug den løsning, der er beskrevet i næste afsnit, til at opdatere hver relevant enhed.
- Det *kan være* muligt at kontakte Zebra eller Google for at få en opdatering af systembetroede certificeringsmyndighed (CA). Det har vi dog ikke bekræftet.
- Hvis det er muligt, kan du overveje at erstatte ældre enheder med enheder, der kører en nyere version af Android (hvor betroede CA-certifikater opdateres automatisk).

### <a name="workaround"></a>Løsning

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>Trin 1: Eksportere det nye rodcertifikat fra Supply Chain Management

Sådan henter du det nye rodcertifikat manuelt via din internetbrowser:

1. Log på Dynamics Supply Chain Management, og åbn forsiden.

1. Vælg låseikonet på adresselinjen i browseren for at åbne dialogboksen **Lokalitet er sikker**.
1. Vælg **Certifikat (gyldigt)** i dialogboksen for at åbne **certifikatvinduet** for det pågældende certifikat.
1. Åbn fanen **Certificeringssti** i vinduet **Certifikat**.
1. Vælg det øverste certifikat, der vises i hierarkiet. (dette er rodcertifikatet).
1. Åbn fanen **Certifikat** i vinduet **Detaljer**.
1. Klik på knappen **Kopier til fil** nederst under fanen **Detaljer**.
1. **Certifikateksport-guide** åbnes. Vælg **Næste** for at fortsætte.
1. Siden **Eksportfilformat** åbnes. Vælg **DER-kodet binær X.509 (.CER)**. Vælg **Næste** for at fortsætte.
1. Siden **Filer, der skal eksporteres**, åbnes ved at angive et filnavn og en placering. Vælg **Næste** for at fortsætte.
1. Siden **Udførslen af guiden Eksport af certifikat** åbnes, som viser resultatet af eksporten. Vælg **Udfør**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>Trin 2: Installere det hentede certifikat på de berørte enheder

Du kan installere det hentede certifikat på følgende måde:

1. Overfør det certifikat, du hentede i forrige trin, til den enhed, du vil opdatere. Du kan f.eks. bruge et SD-kort eller en netværksforbindelse til at gøre filen tilgængelig for enheden.
1. Åbn sikkerhedsindstillingerne for enheden, og vælg menuindstillingen for installation af et certifikat fra en fil. (De nøjagtige trin til dette varierer afhængigt af enheden og OS-versionen.)
1. Det nye certifikat skal nu vises under fanen **Bruger** for betroede certifikater.
1. Gentag denne procedure for hver berørt enhed.
