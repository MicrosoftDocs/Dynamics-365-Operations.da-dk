---
title: Hjælp-system (indeholder video)
description: Denne artikel indeholder en oversigt over Hjælp-systemet for programmer til finans og drift.
author: edupont04
ms.date: 08/16/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16381,  ""intro-internal
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.form: SystemParameters
ms.openlocfilehash: fa1a120fac66997658908a61469d45e96bcc4912
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538831"
---
# <a name="help-system"></a>Hjælp-system

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Brugere af følgende apps kan få adgang til kontekstafhængig hjælp og andet indhold, der er baseret på det samme hjælpesystem:

- Dynamics 365 Commerce
- Dynamics 365 Finance
- Dynamics 365 Human Resources
- Dynamics 365 Supply Chain Management

I alle disse apps kan du få adgang til produktspecifik hjælp fra ruden **Hjælp**.

![Hjælp-rude.](./media/help-pane-ops-help.png)

## <a name="help-on-microsoft-learn"></a>Hjælp til Microsoft Learn

([Microsoft Dynamics 365-dokumentation](/dynamics365/)) i Microsoft Learn er standardkilden til produktdokumentation for de tidligere angivne apps. Dette websted indeholder følgende funktioner:

- **Adgang til det mest opdaterede indhold** – webstedet giver Microsoft en hurtigere og mere fleksibel måde at oprette, levere og opdatere produktdokumentationen på. Derfor kan du få nem adgang til de seneste tekniske oplysninger.
- **Indhold, der er skrevet af eksperter** – indholdet af webstedet er åbent for bidrag fra gruppemedlemmer både inden for og uden for Microsoft.

Du kan finde indhold på Microsoft Learn ved hjælp af en søgemaskine. For at få de bedste resultater anbefaler vi, at du bruger en webstedssøgning som f.eks. **site:learn.microsoft.com dynamics 365 "søgeord"**.

## <a name="get-notified-about-changes-through-an-rss-feed"></a>Få besked om ændringer via et RSS-feed

Hvis du vil abonnere på et RSS-feed af alle opdateringer, der er foretaget til indholdet på Microsoft tekniske dokumentation på tværs af programmer til finans og drift, skal du bruge følgende link:

[RSS-feed](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finops%27)&locale=en-us)

> [!NOTE]
> RSS-feed'et returnerer en liste over de 100 emner, der er opdateret sidst. Listen er sorteret efter dato, men den kan tage op til en uge, før de senest opdaterede artikler kommer på listen.  

Du kan også abonnere på et RSS-feed via app:

- [Commerce](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-commerce%27)&locale=en-us)  
- [Finance](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finance%27)&locale=en-us)  
- [Human Resources](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-hr%27)&locale=en-us)  
- [Forsyningskæde](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-supplychain%27)&locale=en-us)  
- [Talent](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-talent%27)&locale=en-us)  

### <a name="leave-us-feedback"></a>Give os feedback

Hvis du har feedback eller spørgsmål om en artikel, kan du sende en kommentar til os i bunden af siden.

1. Vælg **Feedback** for at komme til kommentarerne i bunden af siden. Vælg derefter enten **Produktfeedback** eller **Log på for at give dokumentationsfeedback**.

2. Begynd at skrive dine kommentarer, og vælg derefter **Send feedback**.

    ![Send kommentar.](./media/feedback.png)

> [!NOTE]
> Hvis du vil sende feedback om dokumentation, skal du logge på ved hjælp af en GitHub-konto. Få flere oplysninger i [Indstille og administrere din GitHub-profil](https://help.github.com/github/setting-up-and-managing-your-github-profile).

## <a name="contribute-to-the-documentation"></a>Bidrag til dokumentationen

Du kan bidrage til og foretage redigeringer til dokumentationen. For at komme i gang skal du vælge knappen **Rediger** (blyantsymbol) på en artikel. Følgende video viser, hvordan du kan bidrage til vores dokumentation.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE36liB]

Videoen [Sådan kan du bidrage til Microsoft Dynamics 365-dokumentation](https://youtu.be/m5djioozRbg) (vist ovenfor ) findes i Microsoft Dynamics 365-kanalen på YouTube.

Få flere oplysninger i [Microsoft Docs-bidragyderguide](/contribute), der udgives af det team, der har bygget webstedet Microsoft Learn.

> [!NOTE]
> Vi accepterer kun oprettelse af bidrag til vores engelske indhold på nuværende tidspunkt.

## <a name="task-guides"></a>Opgaveguider

En opgaveguide er en kontrolleret, automatiseret, interaktiv oplevelse, der fører dig gennem trinene i en opgave eller forretningsproces. Du kan åbne (afspille) en opgaveguide fra ruden **Hjælp**. Når du først vælger på en opgaveguide, viser ruden **Hjælp** de trinvise instruktioner til opgaven. Der er nu lokaliserede opgaveguider.

Microsoft udgav opgaveguidebiblioteker til til produktversioner via december 2017-udgaven af Dynamics 365 Finance and Operations. Afsnittet [Adgang til opgaveguider fra ruden Hjælp](#accessing-task-guides-from-the-help-pane) i denne artikel forklarer, hvordan du finder de rigtige opgaveguider til dit produkt.

![Opgaveguidens læsevisning.](./media/task-guide-ops.png)

For at starte den automatiserede, interaktive oplevelse skal du vælge på **Start opgaveguiden** nederst i ruden **Hjælp**. En sort markør viser, hvor du skal gå hen først. Følg instruktionerne, der vises i brugergrænsefladen (UI), og indtast data som anvist.

![Opgaveguidens trinvise instruktion.](./media/task-guide-step-1-ops.png)

> [!IMPORTANT]
> Vigtigt: De data, du indtaster, når du afspiller en opgaveguide, er faktiske. Hvis du er i et produktionsmiljø, indsættes dataene i det firma, du aktuelt bruger.

Du kan bruge Arbejdsrutineoptager til at oprette dine egne brugerdefinerede opgaveguider. Du kan finde flere oplysninger under [Opret dokumentation eller kursus med Arbejdsrutineoptager](../../dev-itpro/user-interface/task-recorder-training-docs.md).

## <a name="in-product-help"></a>Hjælp i produkterne

Nogle felter indeholder feltbeskrivelser, der kan hjælpe brugerne med at få fjernet spærringen, når de er usikker på de data, som feltet indeholder, f.eks. Desuden giver **Hjælp** i produktet giver kontekstafhængig adgang til indhold, der kan hjælpe brugere med at komme i gang, få spærringer fjernet og få mere at vide.

Hvis du vil have adgang til hjælp-indhold, skal du vælge knappen **Hjælp** (**?**) og derefter vælge **Hjælp**. Du kan også trykke på **Ctrl+Skift+?**. I begge tilfælde åbnes ruden **Hjælp**. I ruden **Hjælp** kan du få adgang til konceptuelle emner eller opgaveguider, der er relevante for det område af produktet, som du aktuelt arbejder i.

![Hjælp-rude.](./media/help-pane-ops-help.png)

### <a name="accessing-help-topics-from-the-help-pane"></a>Adgang til emner i Hjælp fra ruden Hjælp

Fra ruden **Hjælp** kan du få adgang til emner, der gælder for klienten. Når du først åbner **Hjælp**-ruden, viser fanen **Hjælp** de emner, der gælder for den aktuelle side. Hvis der ikke findes emner, kan du angive nøgleord for at indsnævre søgningen. Når du vælger en artikel i **Hjælp**-ruden, åbnes det under en ny fane i din browser.

> [!IMPORTANT]
> Dette afsnit gælder ikke for Dynamics 365 Human Resources. Hjælpesystemet til Personale er automatisk tilknyttet opgaveguider til produktet. Du kan ikke oprette brugerdefinerede opgaveguider til Personale.

### <a name="accessing-task-guides-from-the-help-pane"></a>Adgang til opgaveguider fra ruden Hjælp

Før du kan få adgang til opgaveguider fra ruden **Hjælp**, skal en systemadministrator konfigurere nogle indstillinger på siden **Systemparametre** i Finans, Supply Chain Management eller Commerce. Få flere oplysninger i [Tilføje opgaveguider](help-connect.md#adding-task-guides).

<!-- > [!NOTE]
> - In order to configure Help, you must be signed in with an account in the same tenant as the tenant in which the app is deployed.
> - It is not possible to connect to an LCS library from an instance of the app running in a local virtual hard drive (VHD).

![System Parameters form with Help settings.](./media/system-parameters_ops-1024x437.png)

On the **System parameters** page, follow these steps:

1. **Important:** The first time that you open the Help tab, you must connect to Lifecycle Services. Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the parameters form.

    ![Connect to LCS.](./media/connect-to-lcs-crop-1024x365.png)

2. Select the Lifecycle Services project to connect to.
3. Select BPM libraries (within the selected project) to retrieve task recordings from.
4. Set the display order of the BPM libraries. This setting determines the order in which task recordings from the libraries will appear in the Help pane.-->

Når en systemadministrator har fuldført disse trin, kan du åbne ruden **Hjælp** og vælge fanen **Opgaveguider**. Nu kan du se opgaveguiderne, der gælder for den aktuelle side. Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen. Når du vælger en opgaveguide i ruden **Hjælp**, viser ruden **Hjælp** de trinvise instruktioner, og du kan afspille opgaveguiden.

![Opgaveguidens læsevisning.](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides-for-microsoft-libraries"></a>Hvor er de oversatte opgaveguider til Microsoft-biblioteker?

Oversatte opgaveguider udgives i biblioteker, der har "Alle sprog" i titlen. Hvis du vil se den lokaliserede Hjælp til opgaveguider, skal du sørge for, at der er forbindelse til et relevant bibliotek. Hver enkelt kan ændre det sprog, som en opgaveguide vises i, ved at ændre sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.

- Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.
- Hvis en opgaveguide ikke er blevet oversat, er det kun teksten i kontrolelementerne, der vises på det valgte sprog, når du åbner guiden.

## <a name="creating-custom-help"></a>Oprette tilpasset hjælp

Du kan oprette Hjælp for brugerne ved at oprette brugerdefinerede opgaveguider eller tilslutte dit eget websted til **Hjælp**-ruden. Du kan finde flere oplysninger under følgende emner:

- [Ressourcer til arbejdsrutineoptager](../../dev-itpro/user-interface/task-recorder.md)
- [Oversigt over brugerdefineret hjælp](../../dev-itpro/help/custom-help-overview.md)

## <a name="additional-resources"></a>Yderligere ressourcer

Følgende tabel viser vores websteder. Websteder, der har en stjerne (\*) ud for navnet, kræver, at du logger på med en konto, der er tilknyttet en serviceplan.

| Sted | Beskrivende tekst |
|------|-------------|
| [Microsoft Dynamics 365-dokumentation](/dynamics365/) | Dette websted er vært for eller indeholder hyperlinks til al produktdokumentation til Dynamics 365. |
| [Microsoft Learn-træning](/training/) | Dette websted er det gratis websted for Microsoft eLearning. |
| [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)\* | Dette websted indeholder et skybaseret arbejdsområde til samarbejde, som kunder og partnere kan bruge til at administrere projekter, lige fra førsalg til implementering og drift. Det er nyttigt i alle faserne i en installation. |
| [Supportblog](https://aka.ms/AXSupportBlog) | Dette websted indeholder tip og trick, der er oprettet af supportteamet. |
| [Tidligere versioner](/previous-versions/dynamics/) | Dette websted er vært for indhold fra tidligere versioner. |
| [Dynamics Community](https://community.dynamics.com/) | Dette websted er vært for blogs, fora og videoer. |
| [Microsoft.com/dynamics365](https://www.microsoft.com/dynamics365/home) | Dette websted indeholder oplysninger om evaluering og salg. |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
