---
title: Konfigurere en mailkanal
description: Denne artikel forklarer, hvordan du konfigurerer en mailkanal til modtagelse af elektroniske fakturaer.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 19339cbcc59e93289609690363b0dd9195a66f6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279864"
---
# <a name="configure-an-email-channel"></a>Konfigurere en mailkanal

[!include [banner](../includes/banner.md)]

Konfigurer en mailkontokanal, hvis du med funktionen Elektronisk fakturering har oprettet import af elektroniske kreditorfakturaer fra vedhæftede filer, der modtages via mail.

1. Vælg den funktion til elektronisk fakturering, du har oprettet, i RCS (Regulatory Configuration Service). Sørg for at vælge den version, der har status af **Kladde**.
2. Vælg **Tilføj** på fanen **Opsætninger**.
3. Vælg indstillingen **Brugerdefineret opsætning**, i feltgruppen **Ny** i dialogboksen **Opret funktionsopsætning**.
4. I feltgruppen **Opsætningstype** skal du vælge indstillingen **Datakanal**.
5. Angiv **Indgående mail** i feltet **Vælg datakanal**.
6. Vælg **Opret**.
7. Vælg den linje, du oprettede, og vælg derefter **Rediger**.
8. Angiv følgende obligatoriske felter i afsnittet **Parametre** under fanen **Datakanal**.

    | Felt                | Beskrivelse |
    |----------------------|-------------|
    | Datakanal         | Angiv et entydigt navn til identifikation af datakanalen. Navnet må højst være på 10 tegn. Der vil blive refereret til det i anvendelighedsreglerne og i tilknyttede programmer under kommunikationsprocessen. |
    | Serveradresse       | Angiv serveradressen på kontoudbyderens mail. Serveradressen til udbyderen `https://outlook.live.com` er f.eks. imap-mail.outlook.com. |
    | Serverport          | Angiv nummeret på den port, som bruges af mailkontoudbyderen. Serverporten for udbyderen `https://outlook.live.com` er f.eks. 993. |
    | Brugernavnhemmelighed     | Vælg navnet på Microsoft Azure Key Vault-hemmeligheden, der indeholder id'et for mailbrugerkontoen. Denne hemmelighed skal oprettes i Key Vault og konfigureres i dit servicemiljø. |
    | Hemmelighed for brugeradgangskode | Vælg navnet på den Key Vault-hemmelighed, der indeholder adgangskoden til mailbrugerkontoen. |
    | Timeout              | Angiv den maksimale tidsgrænse i millisekunder (ms), som systemet skal vente på et svar. Standardværdien er 10.000 ms (10 sekunder). |
    | Hovedmappe          | Angiv den mailimportkilde eller den mappe, som tjenesten skal behandle mail fra. |
    | Arkivmappe       | Angiv den mappe, hvor de behandlede mails skal gemmes. Hvis du ikke angiver denne mappe, oprettes den automatisk. |
    | Fejlmappe         | Angiv den mappe, som systemet skal flytte mail til, hvis behandlingen mislykkes. Hvis du ikke angiver denne mappe, oprettes den automatisk. |
    | Maks. meddelelsesstørrelse     | Angiv den maksimale størrelse i byte på en enkelt meddelelse, der behandles. Standardværdien er 20.000.000 byte. |
    | Maks. meddelelsesantal   | Angiv det maksimale antal meddelelser, der skal behandles i en enkelt handling. Hvis du ikke vil begrænse antallet af meddelelser, skal du angive værdien til **0** (nul). |
    | Fra filter          | Angiv en streng, der skal filtreres efter afsenderadresse. Det er kun mails, hvor afsenderadressen svarer til filteret, der behandles. Dette felt er valgfrit. Hvis du vil angive flere afsenderadresser, skal du bruge semikolon (;) som separator. |
    | Emnefilter       | Angiv en streng, der skal filtreres efter emne. Det er kun mails, hvor emnet svarer til filteret, der behandles. Dette felt er valgfrit. En simpel maske som f.eks. **\*smth\*.ext** understøttes, hvor hver stjerne (\*) repræsenterer nul eller flere forekomster af et tegn. |
    | Datofilter          | Angiv en dato for at definere den maksimale alder i dage for de meddelelser, der behandles. Dette felt er valgfrit. Standardværdien er 30 dage. |
    | Behandlingstilstand      | <p>Vælg en af følgende indstillinger for at angive, om alle vedhæftede filer i en mail kan behandles sammen, eller om hver vedhæftede fil skal behandles separat:</p><ul><li><b>Efter vedhæftet fil</b> – Der oprettes et nyt elektronisk dokument for hver vedhæftede fil i mailen. Hvis en mail f.eks. indeholder flere filer, der indeholder e-fakturadata, vil hver fil blive betragtet som en ny e-faktura i systemet.</li><li><b>Efter mail</b> – Én vedhæftet fil betragtes som en grundlæggende vedhæftet fil, og der oprettes én elektronisk faktura i systemet. Andre vedhæftede filer kan bruges som supplerende filer.</li></ul> |

9. Tilføj oplysningerne om filfiltre i afsnittet **Filter for vedhæftede filer**. Der behandles kun vedhæftede filer, der opfylder det definerede filter. F.eks. vil **\*.xml** filtrere efter vedhæftede filer med filtypenavnet .xml. Navnet på den vedhæftede fil bruges i Dynamics 365 Finance eller Dynamics 365 Supply Chain Management under opsætningen.

    - Hvis du angiver feltet **Behandlingstilstand** til **Efter mail** i det forrige trin, kan du tilføje flere filtre her. Navnet identificerer det specifikke dokument.
    - Hvis du angiver feltet **Behandlingstilstand** til **Efter vedhæftet fil**, kan du kun tilføje ét filter.

10. Gennemse og opdater kriterierne under fanen **Anvendelighedsregler**, hvis det er nødvendigt. Værdien i feltet **Kanal** skal være lig med den værdi, du angav i feltet **Datakanal** i trin 8.
11. Vælg **Gem**, og luk siden.
