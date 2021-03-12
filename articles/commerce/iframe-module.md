---
title: iFrame-modul
description: I dette emne dækkes iFrame-modulet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b7b5935a81377e0cb6acfc497eece6148bf1eeee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993363"
---
# <a name="iframe-module"></a>iFrame-modul

[!include [banner](includes/banner.md)]

I dette emne dækkes iFrame-modulet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Et iFrame-modul indeholder en iframe (indbygget ramme), der fungerer som vært for eksternt indhold på et websted. Det kan f.eks. bruges som vært for en YouTube-video eller PDF-filfremviser på en side på et websted. 

Et iFrame-modul kræver en URL-destination. Derefter vil den være vært for indholdet af målsiden i et HTML **iframe**-element. Eksterne URL-adresser skal være på listen over tilladte i henhold til direktiverne om indholdssikkerhedspolitik (CSP) pr. websted. Til iframe-indhold skal URL-adresser tillades ved hjælp af **frame-ancestor**-direktivet. Du kan finde flere oplysninger under [Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md).

> [!NOTE]
> iFrame-modulet er tilgængeligt i Dynamics 365 Commerce version 10.0.13.

Følgende billede viser eksempler på iFrame-moduler, der præsenterer eksterne videoer på websider.

![Eksempel på iFrame-moduler, der præsenterer eksterne videoer](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Egenskaber for iFrame-modul

| Egenskabsbetegnelse             | Værdi                 | Beskrivende tekst |
|---------------------------|-----------------------|-------------|
| Overskrift | Tekst | Overskrift for modulet. |
| Mål-URL-adresse | URL | Den URL-adresse, der har modulet som vært. |
| Højde | Antal eller procentdel | Højden på modulet i pixel eller som en procentdel. Værdien **100** vil f.eks. blive behandlet som et antal pixel, og værdien **100 %** vil blive behandlet som en procentdel. |
| Aria-label | Tekst | En tilgængelig ARIA-etiket (Accessible Rich Internet Applications) kan defineres af hensyn til tilgængelighed. |

## <a name="add-an-iframe-module-to-a-page"></a>Føj et iFrame-modul til en side

Hvis du vil føje et iFrame-modul til en side, der viser en ekstern video, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Marketingskabelon** og derefter klikke på **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge skabelonen **Marketingskabelon**. Under **Sidenavn** skal du angive **Marketingside** og derefter vælge **OK**.
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. Angiv **Bredde**-værdien til **Fuld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **iFrame** og derefter **OK**.
1. I ruden med egenskaber for modulet skal du indstille **Mål-URL-adresse** til en ekstern URL-adresse til en video.
1. Angiv andre egenskaber, f.eks **Overskrift** og **Højde**, som du har brug for.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til siden Marketing på dit websted. Du bør kunne se, at videoen gengives i iFrame-modulet.
 
## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md)
