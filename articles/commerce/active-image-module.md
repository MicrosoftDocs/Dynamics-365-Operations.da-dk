---
title: Modulet Aktivt billede
description: Dette emne omhandler aktive billedmoduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6cc2f9bafcdd17ac33d5591b8c21f3354d95d92e
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479427"
---
# <a name="active-image-module"></a>Modulet Aktivt billede

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler aktive billedmoduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Et aktivt billedmodul kan bruges til at integrere produktmærkater i et billede. Brugere af e-handelswebstedet kan derefter gennemse mærkaterne for at få vist produkter, der vises på billedet. Forhåndsvisninger vises i pop op-vinduer. Hvis du vælger et pop op-vindue med forhåndsvisninger, kan brugerne gå direkte til PDP (product details page) for det tilsvarende produkt.

Mærkaterne defineres ved hjælp af X- og Y-koordinater på billedet. Alle mærkede punkter skal konfigureres med produkt-id'et for det produkt, der vises på billedet.

I følgende illustration vises et eksempel på et pop op-vindue til forhåndsvisning på et billede af Adventure Works på startsiden.

![Eksempel på et pop op-vindue til forhåndsvisning i et aktivt billedmodul](./media/Active_image.PNG)

> [!IMPORTANT]
> - Modulet Aktiv billede er tilgængeligt fra frigivelsen af Dynamics 365 Commerce version 10.0.20.
> - Det aktive billedmodul aktiveres med emnet Adventure Works.

## <a name="active-image-module-properties"></a>Egenskaber for modulet Aktivt billede

| Egenskabsbetegnelse      | Værdier | Betegnelse |
|--------------------|--------|-------------|
| Billede              | Billedfil | Der kan bruges et billede til at vise et eller flere produkter. Billedet kan overføres til mediebiblioteket i Commerce Site Builder, eller der kan bruges et eksisterende billede. |
| Bredde              | Antal pixel | Denne egenskab definerer bredden af billedet. De aktive koordinater beregnes ud fra bredden af billedet.|
| Aktive koordinater | X- og Y-koordinater og et produkt-id-nummer | Hvert aktivt billed array består af X- og Y-koordinater og et produkt-id-nummer.|
| Overskrift            | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard bruges **H2** overskriften, men koden kan ændres efter behov for at opfylde tilgængelighedskravene. |
| Afsnit          | Afsnitstekst | Modulet understøtter afsnitstekst i RTF-format. Nogle grundlæggende RTF-funktioner understøttes, f. eks. hyperlinks og fed, understreget og kursiv tekst. Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet. |
| Binding               | Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane** | Modulet understøtter et eller flere links til "handlingsplaner". Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet. ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene. Links kan konfigureres, så de åbnes under en ny fane. |
| Undertekst           | Overskrift, tekst og link | Der kan tilføjes yderligere sammenhæng for billedet, f.eks. en forfatter eller et designernavn, eller links til personlige blogs.|
| Teksttema         | **Lys** eller **Mørk** | Denne egenskab giver en bruger mulighed for at angive teksten til lys eller mørk på baggrund af baggrundsbillederne. Den er tilgængelig som lokalnummer under emnet Adventure Works. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Føje et aktivt billedmodul til en ny side

Hvis du vil føje et aktivt billedmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og åbn marketingskabelonen for webstedets startside (eller opret en ny marketingskabelon).
1. På pladsen **Hoved** på standardsiden skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Aktivt billede** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og åbn webstedets startside (eller opret en ny startside ved hjælp af marketingskabelonen).
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Aktivt billede** og derefter **OK**.
1. Tilføj et billede i egenskabsruden i det aktive billedmodul, og angiv lærredets bredde til billedets størrelse.
1. Angiv X- og Y-koordinaterne, og tilføj det relevante produkt-id-nummer.
1. Tilføj og konfigurer yderligere aktive billedmoduler efter behov.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
