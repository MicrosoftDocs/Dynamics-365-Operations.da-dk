---
title: Nyheder eller ændringer i Dynamics AX-programversion 7.0.1 (maj 2016)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics AX-programversion 7.0.1. Denne version blev udgivet i maj 2016 og har build-nummer 7.0.1265.23014.
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 94cebad528facc5537226a3faa5ea9be8448092e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267194"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Nyheder eller ændringer i Dynamics AX-programversion 7.0.1 (maj 2016)

[!include [banner](../includes/banner.md)]

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics AX-programversion 7.0.1. Denne version blev udgivet i maj 2016 og har build-nummer 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektronisk rapportering (ER)

| Hvad kan du gøre? | Hvorfor er det vigtigt? |
|------------------|------------------------|
| Konfigurere kørselsdialogboks til design af elektronisk rapporteringsrapporter, så brugerne kan vælge de økonomiske dimensioner, som de ønsker. | På kørselstidspunktet kan brugerne vælge flere økonomiske dimensioner i dialogboksen til kørsel af en ER-rapport. Detaljerne for de valgte økonomiske dimensioner vises i det elektroniske dokument, der genereres. |
| Konfigurere adgang til flere økonomiske dimensioner under udarbejdelsen af en ER-rapport via en enkelt tilknytning til den ønskede datakilde. | Det samme ER-rapportkonfiguration kan bruges til at generere elektroniske dokumenter, der præsenterer transaktionsdata samt oplysninger om økonomiske dimensioner, uanset antallet af økonomiske dimensioner, der er enten valgt af brugeren eller er konfigureret for den aktuelle juridiske enhed eller forekomst. |
| Konfigurere en ER-rapport for at indtaste data i dynamisk genererede kolonner i et elektronisk dokument, som oprettet i OPENXML-regnearksformat. | En ER-rapport kan indtaste data i et OPENXML-regneark, der er genereret, ved at replikere kolonner vandret. Derfor kan den samme ER-konfiguration genbruges til at generere elektroniske dokumenter, der har et forskelligt antal dynamisk genererede kolonner. |
| Konfigurere ER-destinationer, så outputresultatet af et format dirigeres til en bestemt destination: fil, e-mail eller arkiv (Microsoft SharePoint-mappe eller Microsoft Azure Storage). | Tidligere, når du kørte en ER-konfiguration, vistes en meddelelsesboks, der krævede brugerhandling for at gemme eller åbne en fil. Nu kan du forudkonfigurere en destination til hver formatkonfiguration og til hver outputkomponent (en mappe eller en fil) separat. Brugere, der har de nødvendige adgangsrettigheder, kan også ændre indstillingerne for destinationen på kørselstidspunktet. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail

| Hvad kan du gøre? | Hvorfor er det vigtigt? |
|------------------|------------------------|
| Bruge Google Chrome-browseren. | Detailhandlere kan nu starte Cloud POS fra Chrome-browseren og kan opleve alle de funktioner, der er tilgængelige i Microsoft Edge og Internet Explorer-versionen af Cloud POS. |

## <a name="financial-reporting"></a>Økonomirapportering

| Hvad kan du gøre? | Hvorfor er det vigtigt? |
|------------------|------------------------|
| Genopbygge Økonomirapporterings-datacenteret. | Når du flytter Dynamics AX-databaser mellem miljøer eller foretager andre indgribende ændringer i miljøet, skal Økonomirapporteringsdatabasen evt. genopbygges. Der leveres nu et Windows PowerShell-script til at genopbygge databasen for dig. |
| Du kan ikke længere vælge rapportdesignerindstillinger, der ikke er gyldige. | Flere rapportdesignerindstillinger, der blev brugt i versioner af Management Reporter på markedet, gælder ikke for denne version af Dynamics AX. Disse indstillinger er relateret til økonomisk rapport-design, output og sammenkædning. Disse indstillinger er blevet fjernet fra designeren til økonomirapporter for at forhindre brugerfejl. |

## <a name="financial-management"></a>Økonomistyring

| Hvad kan du gøre? | Hvorfor er det vigtigt? |
|------------------|------------------------|
| Generere positive betalingsfiler til kreditorbetalinger. | Der kan genereres positive betalingsfiler for at hjælpe med at forebygge checkbedrageri. |

## <a name="warehouse-and-production"></a>Lager og produktion

<table>
<thead>
<tr>
<th>Hvad kan du gøre?</th>
<th>Hvorfor er det vigtigt?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definere en arbejdspolitik for lagerstedet, der styrer oprettelsen af arbejde for en række produkter på bestemte lokationer.</td>
<td>Lagerstedsprocesser omfatter ikke altid arbejde. Ved hjælp af den nye politik for lagerstedsarbejde kan du forhindre, at der oprettes arbejde med pluk af råmaterialer og læg-på-lager af færdigvarer for en række produkter på bestemte lokationer.</td>
</tr>
<tr>
<td>Angive, at en udlagringslokationen for produktion ikke er id-kontrolleret.</td>
<td>Du kan nu angive, at en produktudlagringslokation ikke er id-kontrolleret. Denne funktion er for eksempel nyttig, når en upstream-produktionsordre rapporterer varer som færdigmeldte direkte til et sted, der fungerer som produktionsindlagringslokation for en downstream-produktionsordre.</td>
</tr>
<tr>
<td>Understøtte styklister, der omfatter varer med forskellige produktdimensioner af samme vare.</td>
<td>Når du bruger en eller flere af produktdimensionerne i produktionen, kan der opstå situationer, hvor du vil producere en vare, der er baseret på en anden variant af den samme vare. Du kan finde flere oplysninger på <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">denne blog</a>.</td>
</tr>
<tr>
<td>Produktionsordrer med cirkulære strukturer på første niveau af deres styklister er udelukket fra kalkulation på styklisteniveau for materialeressourceplanlægning.</td>
<td>Det er ikke muligt at tildele korrekte styklisteniveauer til produktvarianter for produktionsordrer, der forårsager cirkularitet i styklistehierarkiet.</td>
</tr>
<tr>
<td>Beregne separate styklisteniveauer for materialeressourceplanlægning og omkostningsberegning:
<ul>
<li>For planlægning af materialeressource beregnes styklisteniveauer i den nye <strong>ReqItemLevel</strong>-tabel. Afsluttede produktionsordrer ignoreres i beregningen.</li>
<li>Til beregning af produktionsomkostninger beregnes styklisteniveauer i <strong>InventTable</strong>. Afsluttede produktionsordrer medtages i beregningen.</li>
</ul>
</td>
<td>
<ul>
<li>Når du kører materialeressourceplanlægning, eksempelvis planlægning og udfoldning af varedisponeringsplan, skal kun styklisteniveauer, der bruges til planlægning af materialeressourcer, genberegnes. Med andre ord er der ingen grund til at beregne styklisteniveauer, der anvendes til beregning af efterkalkulation af produktion.</li>
<li>Når du kører efterkalkulationsoperationer, for eksempel lagerlukning, skal kun styklisteniveauer, der anvendes til efterkalkulations-produktionsberegning, genberegnes.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Yderligere ressourcer

[Nyheder eller ændringer på startside for finans og drift](whats-new-changed.md)

[Nye eller opdaterede opgaveguider (maj 2016)](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
