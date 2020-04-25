---
title: Tilstandsvurdering
description: Dette emne forklarer, hvordan du opretter en skabelon til tilstandsvurdering og registrering af et aktiv i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2694b3ee51e2619a94e7ea2f4039fb52adddbbc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208909"
---
# <a name="condition-assessment"></a>Tilstandsvurdering

[!include [banner](../../includes/banner.md)]

 

Dette emne forklarer, hvordan du opretter en skabelon til tilstandsvurdering og registrering af et aktiv i Styring af aktiver. Tilstandsvurdering udføres med jævne mellemrum, og det primære formål er at oprette og vedligeholde tilstandsdata for aktiver. Set fra et forebyggende vedligeholdelsesperspektiv er det vigtigt at overvåge nøgleoplysninger såsom aktuel tilstand og resterende levetid. Desuden, hvis du udfører tilstandsvurdering med jævne mellemrum, vil du være i stand til at overvåge og sammenligne tilstande på maskinerne i din fabrik.

Tilstandsvurdering kan bruges til at måle og overvåge mange tilstande på dit udstyr. Eksempel: Du kan måle vibrationer på dine maskiner. Når du har registreret vibrationsmålinger i Styring af aktiver på forskellige typer udstyr, kan du søge efter den seneste registrerede vurdering og se vibrationsmålinger.

Tilstandsvurdering oprettes på aktiver. Du konfigurerer en tilstandsvurderingsskabelon på en aktivtype, før du udfører proceduren for tilstandsvurdering. Årsagen til at bruge skabeloner til tilstandsvurdering er at undgå variation af tilstandsdata for lignende aktiver. Rækkefølgen for opsætning og brug af tilstandsvurdering i Styring af aktiver er: Først skal du oprette de påkrævede skabeloner til tilstandsvurdering. Derefter knytter du skabeloner til aktivtyper i formen **Aktivtyper**. Endelig kan du oprette registreringer af tilstandsvurderinger for et aktiv i formen **Aktiv**.

## <a name="create-a-condition-assessment-template"></a>Oprette en skabelon til tilstandsvurdering

1. Vælg **Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tilstandsvurdering**.
2. Vælg **Ny** for at oprette en ny skabelon.
3. I feltet **Skabelon** skal du skrive skabelon-id'et.
4. Angiv et navn til skabelonen i feltet **Navn**.
5. I oversigtspanelet **Tilstandsvurderingslinjer** skal du tilføje de linjer, der kræves til tilstandsvurderingen, herunder valg af den relevante tilstandstype og måleenhed.
6. Brug oversigtspanelet **Aktivtyper** til at tilføje de aktivtyper, der skal bruge skabelonen til tilstandsvurdering.
7. I felterne **Linjer** og **Aktivtyper** i gruppen **Detaljer** øverst på skærmen kan du se antallet af vurderingslinjer og aktivtyper, der er relateret til den valgte tilstandsvurderingsskabelon.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Oprette registrering af tilstandsvurdering på et aktiv

1. Vælg **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.
2. På listen skal du vælge det aktiv, du vil oprette en registrering af tilstandsvurdering for.
3. Klik på **Tilstandsvurdering** under fanen **Generelt**.
4. Klik på **Ny** for at foretage en ny registrering.
5. Vælg datoen for tilstandsvurderingen i feltet **Dato**.
6. Vælg navnet på den arbejder, der foretog vurderingsregistreringen, i feltet **Arbejder**.
7. I feltet **Linjer** får du vist antallet af vurderingslinjer, der er konfigureret på tilstandsvurderingen.
8. Vælg en skabelon for tilstandsvurderingen i feltet **Skabelon**. Navnet på skabelonen indsættes automatisk i feltet **Navn**, og de relaterede registreringslinjer indsættes i oversigtspanelet **Tilstandsvurderingslinjer**.
9. Du kan indsætte noter vedrørende den valgte tilstandsvurdering i oversigtspanelet **Noter**.
10. For hver tilstandsvurderingslinje skal du indsætte måledata i feltet **Værdi**.
11. Du kan indsætte en kommentar, der vedrører den valgte registreringslinje, i oversigtspanelet **Tilstandsvurderingslinjer** > feltet **Kommentarer**. Hvis du tilføjer en kommentar på en linje, markeres afkrydsningsfeltet **Kommentar** automatisk.

Når du har foretaget en registrering af tilstandsvurdering for et aktiv, kan du udskrive en tilstandsvurderingsrapport.

>[!NOTE]
>Du kan også registrere tilstandsvurdering på en arbejdsordre (**Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Alle arbejdsordrer** > **Tilstandsvurdering**-knap).
