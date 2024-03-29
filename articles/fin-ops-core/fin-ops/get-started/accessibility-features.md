---
title: Tilgængelighedsfunktioner
description: Denne artikel beskriver den funktionalitet, der er udviklet til at hjælpe brugere med forskellige typer handicap.
author: jasongre
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 4e6a077cc7848448233ed5f94f9b1ba5b385c3fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284017"
---
# <a name="accessibility-features"></a>Tilgængelighedsfunktioner

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikel beskriver den funktionalitet, der er udviklet til at hjælpe brugere med forskellige typer handicap med at bruge denne app. Der er f.eks. funktioner til personer, der bruger synsteknologiske hjælpemidler som f.eks. Microsoft Windows Oplæser.

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows Oplæser og kun tastaturadgang

Hvert felt og kontrolelementet har en etiket og en beskrivelse af gældende genveje. En skærmlæser kan læse etiketten og beskrivelsen.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>Genveje til de hyppigst udførte handlinger

For de fleste brugere omfatter den daglige systembrug mange dataindtastninger og -interaktioner. For at give dig en bedre brugeroplevelse har vi oprettet genveje, der kan hjælpe dig med at "springe" rundt på skærmen, samt genveje til specialiserede handlinger. Du kan finde flere oplysninger under [Tastaturgenveje](shortcut-keys.md).

## <a name="navigation-search"></a>Navigationssøgning

Alle sider, der åbnes ved hjælp af menuen i navigationsruden, ruden længst til venstre, er også tilgængelige i feltet **Søg**. Tryk på Alt + G for at flytte fokus til feltet **Søg** og derefter skrive navnet på eller beskrivelsen af siden.

!["Bankkonti", der er angivet i Søgefeltet](media/6d08b0be32808221023e2aa92d69fd70.png "'bankkonti' indtastet i Søgefeltet")

Du kan finde flere oplysninger i [Navigationssøgning](navigation-search.md).

> [!NOTE]
> Du kan kun gå direkte til sider på øverste niveau. Sekundære sider er afhængige af oplysninger eller kontekst fra deres overordnede side.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Handlingssøgning for brugere, der kun bruger tastaturet, eller for fokuseret dataindtastning

Der er adgang til alle handlinger, der kan udføres på en side, fra et tastatur, via tabulatornavigation. Oplysninger om tabulatornavigation finder du senere i denne artikel. Du kan udføre handlinger mere direkte ved hjælp af handlingssøgningsfunktionen.

### <a name="example"></a>Eksempel

Du vil udføre handlingen **Log for e-mail-besked**, der vises i gruppen **E-mail-besked** under fanen **Salgsordre** i handlingsruden.

![Loghandling for e-mailbesked i handlingsruden.](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg "'Loghandling for e-mailbesked' i Handlingsruden")

Én mulighed er at bruge tastaturet. Tryk på Ctrl + F6 for at flytte fokus til handlingsruden, og tryk derefter på Tab flere gange for at flytte gennem alle faner og handlinger, indtil handlingen **Log for e-mail-besked** er i fokus.

Men du kan også køre handlingen mere direkte. Fra et vilkårligt sted på siden skal du trykke på Ctrl + apostrof (') for at få vist søgefeltet for handlinger.

![Søgefelt for handlinger.](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg "Søgefelt for handlinger")

Skriv ord, der beskriver handlingen, i søgefeltet. Handlingen gøres tilgængelig for dig, og du kan køre den direkte. For eksempel ved at skrive **e-mail**, **besk** (et delvist ord) eller **log** kan du "springe" til Log for e-mail-besked-funktionen.

!["E-mail" indtastet i søgefeltet](media/image4.png "'e-mail' indtastet i Søgefeltet")

!["Besked" indtastet i søgefeltet](media/image5.png "'besked' indtastet i Søgefeltet")

!["Log" indtastet i søgefeltet](media/image6.png "'log' indtastet i Søgefeltet")

Når du er færdig, kan du trykke på Ctrl + apostrof igen for at returnere fokus til det felt, du arbejdede med, før du udførte handlingssøgningen.

Du kan finde flere oplysninger i [Handlingssøgning](action-search.md).

## <a name="tab-sequence"></a>Tabulatornavigation

Ikke alle felter er nødvendige for at udføre almindelige opgaver i den daglige systembrug. Derfor er tabulatornavigation som standard "optimeret". Tabulatorstop er kun indstillet for de felter, der er vigtige for typiske scenarier.

Dog kan nogle af de felter, du ofte bruger til at udføre opgaver, være udeladt i standardtabulatornavigationen. Hvis det er tilfældet, og du bruger Windows Oplæser, kan du bruge Windows Oplæser-tastaturhandlinger til få adgang til disse felter og kontrollere deres indhold. Alternativt kan du slå indstillingen **Udvidet tabulatornavigation** til på siden **Indstillinger**. Denne indstilling gør alle felter, der kan redigeres, og skrivebeskyttede felter til en del af tabulatornavigationen. Du kan derefter bruge tilpasningssiden til at oprette en brugerdefineret tabulatornavigation og udelade felter, der ikke behøver at indgå i tabulatornavigationen. Du kan finde flere oplysninger om brugertilpasning i [Tilpasse brugeroplevelsen](personalize-user-experience.md).

![Indstillingen "Udvidet tabulatornavigation"](media/8c0f12bbb3f26032997ef0ba95d89b6a.png "Indstillingen 'Udvidet tabulatornavigation'")

## <a name="form-patterns"></a>Formularmønstre

Næsten 90 procent af siderne i appen er baseret på et lille sæt mønstre. Disse mønstre betegnes som *formularmønstre*. Hvert formularmønster bruges til at give adgang til de handlinger, der oftest udføres på siden. Med et formularmønster kan du sikre kendskab og øget forståelse, fordi ofte benyttede handlinger og data altid vises på samme sted på forskellige sider. På grund af det lave antal formularmønstre, kan brugerne nemt finde ud af systemet, uafhængigt af antallet af sider i mønsteret, og kan trygt bruge det, når de har genkendt formular mønstrene.

Hvis du vil vide mere om formularmønstre, kan du se under [Formulartypografier og -mønstre](../../dev-itpro/user-interface/form-styles-patterns.md).

## <a name="responsive-layout"></a>Responsivt layout

Produktet er udviklet til brug på forskellige enheder og formfaktorer, fra de mindste skærmbilleder til store skærme med høj opløsning. Med vores program til responsivt layout kan brugere zoome ind på et forstørrelsesniveau på 200 % (eller i nogle situationer mere end 200 %).

På smartphones og andre små skærme tilpasser betjenings- og formularlayoutet sig responsivt for at sikre, at de centrale data er begunstiget. Disse responsive funktionsmåder kan også omfatte at reducere antallet af kolonner i grupper og faner til en enkelt kolonne, skjule skalelementer og skjule Handlingsruden.

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Vejledning i, hvordan udviklere og kunder kan inkorporere tilgængelighed i deres tilpasninger

Du kan finde flere oplysninger om Microsofts bedste fremgangsmåder for implementering af hjælp til handicappede under [Tilgængelighed i formularer, produkter og kontrolelementer](../../dev-itpro/user-interface/enable-accessibility.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
