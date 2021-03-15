---
title: Overføre og håndtere statiske filer
description: Dette emne beskriver, hvordan du overfører en statisk fil til Microsoft Dynamics 365 Commerce-webstedsgenerator, og hvordan du opretter en brugerdefineret URL-adresse og et filnavn, der kan bruges til at anmode om filen.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1d709d99737ad05af1fb19d9f3ef7b87a8db80d3
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031814"
---
# <a name="upload-and-serve-static-files"></a>Overføre og håndtere statiske filer

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du overfører en statisk fil til Microsoft Dynamics 365 Commerce-webstedsgenerator, og hvordan du opretter en brugerdefineret URL-adresse og et filnavn, der kan bruges til at anmode om filen.

Nogle tredjepartsconnectorer kræver, at en fil hostes og behandles på e-handelswebstedet. Disse connectorer forventer, at filen returneres efter anmodninger til en bestemt URL-adressesti til tilbagekald og filnavn. I dette emne kan du derfor læse, hvordan du kan overføre og håndtere en statisk fil, der har en brugerdefinerbar URL-adresse og et filnavn på et Dynamics 365 Commerce-e-handelswebsted.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Oprette en URL-adresse til et websted, der returnerer en statisk fil

Udfør følgende trin for at oprette en URL-adresse til et websted, der returnerer en statisk fil i Commerce-webstedsgenerator.

1. Gå til mediebiblioteket for webstedet, og overfør den fil, der skal behandles af anmodninger til den URL-adresse, du vil definere. Hvis du allerede har overført filen, kan du springe dette trin over.
1. Gå til **URL-adresser** for dit websted.
1. Vælg **Ny \> Ny URL-adresse**.
1. Vælg **Mediebiblioteksaktiv** i dialogboksen **Ny URL-adresse**.
1. Angiv **URL-stien** i feltet URL-sti. Medtag filnavnet i stien.
1. Vælg **Næste**. Mediebiblioteket åbnes og viser alle medieaktiver for den **dokument**-type, der er overført.
1. Vælg den fil, der skal behandles for anmodninger til den URL-adresse, du har defineret i trin 5.
1. Vælg **Gem**.

På dette tidspunkt er den URL-adresse, du har oprettet, i kladdetilstand. Den fil, som URL-adressen peger på, bliver ikke returneret, før du publicerer URL-adressen. Før du publicerer URL-adressen, kan du kontrollere, at den returnerer de korrekte data.

## <a name="validate-and-publish-a-url"></a>Validere og publicere URL-adresse

Hvis du vil validere en URL-adresse, før du publicerer den, skal du følge disse trin.

1. Gå til **URL-adresser** for dit websted, og vælg den URL-adresse, du vil have vist.
2. Vælg det korrekte URL-link under knappen **Rediger** i ruden med egenskaber til højre. Der åbnes et nyt browservindue, og du får vist en 404-fejlmeddelelse.
3. Tilføj **?preview=inprogress**-forespørgselsstrengen til URL-adressen (f. eks. `https://yoursite.com/callback.html?preview=inprogress`), og genindlæs siden. Den fil, du har overført til mediebiblioteket, skulle blive returneret med svaret.

Når du har godkendt URL-adressen, kan du publicere den.

1. Gå til **URL-adresser** for dit websted, og vælg URL-adressen.
2. Vælg **Publicer** på kommandolinjen.

## <a name="update-the-file-that-a-url-points-to"></a>Opdater den fil, som en URL-adresse peger på

Når en URL-adresse publiceres, kan du opdatere den, så den peger på en anden fil. Du kan også opdatere URL-adressen, så den peger på en anden ressourcetype, som det er beskrevet i næste afsnit. Du kan f.eks. lade URL-adressen pege på en intern side eller en omdirigering.

Hvis du vil opdatere den fil, som en URL-adresse peger på, skal du følge disse trin.

1. Gå til **URL-adresser** for dit websted, og vælg den URL-adresse, du vil opdatere.
1. Vælg **Rediger** i egenskabsruden til højre.
1. Under **Tildeling af URL-adresse** skal du markere afkrydsningsfeltet **Trin 2** og derefter vælge et nyt dokument fra mediebiblioteket.
1. Vælg **Anvend**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Opdater den aktivtype, som en URL-adresse peger på

Du kan også opdatere en URL-adresse, så den peger på en anden type aktiv (ressource), f.eks. en intern side eller en omdirigering.

Hvis du vil opdatere den aktivtype, som en URL-adresse peger på, skal du følge disse trin.

1. Gå til **URL-adresser** for dit websted, og vælg den URL-adresse, du vil opdatere.
1. Vælg **Rediger** i egenskabsruden til højre.
1. Under **Tildeling af URL-adresse** skal du vælge en anden aktivtype under **Trin 1**.
1. Marker afkrydsningsfeltet **Trin 2**, og vælg derefter det nye aktiv.
1. Vælg **Anvend**.

## <a name="change-the-url-path"></a>Redigere URL-stien

Når der er oprettet en URL-adresse, kan dens sti ikke ændres. Hvis du skal ændre den URL-sti, som en fil eller en anden type ressource sendes via, skal du oprette en ny URL-adresse, knytte den til den eksisterende fil eller anden ressource og derefter annullere publiceringen af og slette den gamle URL-adresse.

Benyt følgende fremgangsmåde for at ændre URL-adressestien.

1. Hvis du vil oprette en ny URL-adresse og knytte den til den eksisterende fil eller en anden ressource, skal du følge instruktionerne i afsnittet [Oprette en URL-adresse til et websted, der returnerer en statisk fil](#create-a-site-url-that-returns-a-static-file) tidligere i dette emne.
1. Vælg den nye URL-adresse, og vælg **Publicer** på kommandolinjen. Den nye URL-adresse publiceres.
1. Hvis du vil annullere publiceringen af den gamle URL-adresse, skal du markere den og derefter vælge **Annuller publicering** på kommandolinjen. Du kan nu evt. slette den gamle URL-adresse.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over styring af digitale aktiver](dam-overview.md)

[Overføre billeder](dam-upload-images.md)

[Uploade videoer](dam-upload-video.md)

[Overfør andre filer end billeder og videoer](dam-upload-files.md)

[Beskære billeder](dam-crop-images.md)

[Tilpasse billedets fokuspunkter](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]