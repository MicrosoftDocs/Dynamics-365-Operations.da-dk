---
title: Iframe-modul
description: Denne artikel dækker iframe-modulet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 248da5132d1a2c6dcf8f246628f969c8a200b26c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269889"
---
# <a name="iframe-module"></a>Iframe-modul

[!include [banner](includes/banner.md)]

Denne artikel dækker iframe-modulet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

Et iFrame-modul indeholder en iframe (indbygget ramme), der fungerer som vært for eksternt indhold på et websted. Det kan f.eks. bruges som vært for en YouTube-video eller PDF-filfremviser på en side på et websted. 

Et iFrame-modul kræver en URL-destination. Derefter vil den være vært for indholdet af målsiden i et HTML **iframe**-element. Eksterne URL-adresser skal være på listen over tilladte i henhold til direktiverne om indholdssikkerhedspolitik (CSP) pr. websted. Til iframe-indhold skal URL-adresser tillades ved hjælp af **frame-ancestor**-direktivet. Du kan finde flere oplysninger under [Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md).

> [!NOTE]
> iFrame-modulet er tilgængeligt i Dynamics 365 Commerce version 10.0.13.

Følgende billede viser eksempler på iFrame-moduler, der præsenterer eksterne videoer på websider.

![Eksempel på iFrame-moduler, der præsenterer eksterne videoer.](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Egenskaber for iFrame-modul

| Egenskabsbetegnelse             | Værdi                 | Betegnelse |
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
1. Angiv **Marketingside** under **Sidenavn** i dialogboksen **Opret en ny side**, og vælg derefter **Næste**.
1. Vælg den **Marketingskabelon**, du oprettede, under **Vælg en skabelon**, og vælg derefter **Næste**.
1. Vælg et sidelayout (f.eks. **Fleksibelt layout**) under **Vælg et layout**, og vælg derefter **Næste**.
1. Gennemse sidekonfigurationen under **Gennemse og afslut**. Hvis du vil redigere sideoplysningerne, skal du vælge **Tilbage**. Hvis sideoplysningerne er korrekte, skal du vælge **Opret side**. 
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. Angiv **Bredde**-værdien til **Fuld container** i egenskabsruden for modulet.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **iFrame** og derefter **OK**.
1. I ruden med egenskaber for modulet skal du indstille **Mål-URL-adresse** til en ekstern URL-adresse til en video.
1. Angiv andre egenskaber, f.eks **Overskrift** og **Højde**, som du har brug for.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til siden Marketing på dit websted. Du bør kunne se, at videoen gengives i iFrame-modulet.

> [!NOTE]
> Da iFrame-modulet er vært for eksternt indhold, skal webstedsforfattere sikre, at indhold, der har et iFrame-modul som vært, ikke overtræder politikker for indholdsbegrænsning på det pågældende marked. Hvis der er en indholdsovertrædelse på en side, der bruger modulet iFrame, kan webstedsopretter fjerne iFrame-modulet ved at åbne siden i Site Builder, vælge **Fjern modul** på iFrame-modulets plads og derefter gemme og publicere siden igen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
