---
title: Administrere robots.txt-filer
description: Dette emne beskriver, hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477702"
---
# <a name="manage-robotstxt-files"></a>Administrere robots.txt-filer

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.

Standarden for "robots exclusion standard" eller robots.txt er en standard, som websteder bruger til at kommunikere med webrobotter. Den oplyser webrobotter om alle de områder på et websted, der ikke bør besøges. Robotter bruges ofte af søgemaskiner til at indeksere websteder.

Hvis du vil udelukke robotter fra en server, skal du oprette en fil på serveren. I denne fil skal du angive en adgangspolitik for robotter. Filen skal være tilgængelig via HTTP på den lokale URL-adresse **/robots.txt**. Robots.txt-filen hjælper søgemaskiner med at indeksere indholdet på dit websted.

Dynamics 365 Commerce giver dig mulighed for at uploade en robots.txt-fil til dit domæne. Du kan uploade en robots.txt-fil for hvert domæne i dit Commerce-miljø og knytte den til det pågældende domæne.

Du finder flere oplysninger om robots-txt-filer på [Siderne om webrobotter](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Overfør en robots.txt-fil

Når du har oprettet og redigeret din robots.txt-fil i henhold til [robots exclusion-standarden](https://www.robotstxt.org/orig.html), skal du sørge for, at filen er tilgængelig på den computer, hvor du vil bruge Commerce-oprettelsesværktøjerne. Filen skal have navnet **robots.txt**. Hvis du ønsker de bedste resultater, skal det være i det format, der er angivet i standarden. Hver Commerce-kunde er ansvarlig for at validere og vedligeholde indholdet af robots.txt-filen. Hvis du vil overføre en robots.txt-fil, skal du være logget på Commerce som systemadministrator.

Følg disse trin for at overføre en robots.txt-fil i Commerce.

1. Log ind på Commerce som systemadministrator.
2. I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.
3. Under **Lejerindstillinger** skal du vælge **Robots.txt**. En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.
4. Vælg **Administrer** for at overføre en robots.txt-fil til et domæne i dit miljø.
5. I menuen til højre skal du vælge knappen **Overfør** (den opadpegende pil) ud for det domæne, der er knyttet til filen robots.txt. Der vises en dialogboks med en filbrowser.
6. Find og vælg den robots.txt-fil, du vil overføre til det tilknyttede domæne, i dialogboksen, og vælg derefter **Åbn** for at fuldføre overførslen.

> [!NOTE] 
> Under overførslen kontrollerer Commerce, at filen er en tekstfil, men den validerer ikke filens indhold.

## <a name="download-a-robotstxt-file"></a>Download en robots.txt-fil

Følg disse trin for at downloade en robots.txt-fil i Commerce.

1. Log ind på Commerce som systemadministrator.
2. I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.
3. Under **Lejerindstillinger** skal du vælge **Robots.txt**. En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.
4. Vælg **Administrer** for at downloade en robots.txt-fil til et domæne i dit miljø.
5. I menuen til højre skal du vælge knappen **Download** (den nedadpegende pil) ud for det domæne, der er knyttet til filen robots.txt. Der vises en dialogboks med en filbrowser.
6. Gå til den ønskede placering på det lokale drev i dialogboksen, bekræft eller indtast et filnavn, og vælg derefter **Gem** for at fuldføre downloadet.

> [!NOTE]
> Denne fremgangsmåde kan kun bruges til at hente robots.txt-filer, der tidligere er blevet overført via Commerce-oprettelsesværktøjerne.

## <a name="delete-a-robotstxt-file"></a>Slet en robots.txt-fil

Følg disse trin for at slette en robots.txt-fil i Commerce.

1. Log ind på Commerce som systemadministrator.
2. I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.
3. Under **Lejerindstillinger** skal du vælge **Robots.txt**. En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.
4. Vælg **Administrer** for at slette en robots.txt-fil for et domæne i dit miljø.
5. I menuen til højre skal du vælge knappen **Slet** (skraldespandssymbolet) ud for det domæne, der er knyttet til filen robots.txt. Der vises et vindue med en filbrowser.
6. Find og vælg den robots.txt-fil, du vil slette for det tilknyttede domæne, i filbrowservinduet, og vælg derefter **Åbn**. Der vises en advarselsmeddelelse.
7. I meddelelsesfeltet skal du vælge **Slet** for at bekræfte sletningen af robots.txt-filen.

> [!NOTE] 
> Denne fremgangsmåde kan kun bruges til at slette robots.txt-filer, der tidligere er blevet overført via Commerce-oprettelsesværktøjerne.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere en ny e-handelslejer](deploy-ecommerce-site.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
