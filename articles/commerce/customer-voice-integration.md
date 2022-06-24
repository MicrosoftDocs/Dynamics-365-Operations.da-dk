---
title: Integrer Customer Voice i e-handelswebstedssider
description: Denne artikel indeholder en beskrivelse af, hvordan du kan integrere Microsoft Dynamics 365 Customer Voice i Dynamics 365 Commerce-e-handelswebsider.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850324"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Integrer Customer Voice i e-handelswebstedssider

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan integrere Microsoft Dynamics 365 Customer Voice i Dynamics 365 Commerce-e-handelswebsider.

Du kan integrere [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) i dit e-handelswebsted for at indsamle, analysere og spore kundefeedback i realtid. For at komme i gang med integrationen skal du oprette en konto og vælge en projektskabelon til Customer Voice for den type feedback, du vil indsamle.

## <a name="integrate-the-customer-voice-service"></a>Integrere Customer Voice-tjenesten

Hvis du vil oprette en Customer Voice-konto, skal du gå til [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) og følge prompterne.

Når du har oprettet en Customer Voice-konto og er logget på den, skal du vælge en projektskabelon for den type feedback, du vil indsamle.

Benyt følgende fremgangsmåde for at vælge en projektskabelon til Customer Voice.

1. Gå til [siden med projektskabeloner til Customer Voice](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Vælg **Start her**.
1. Vælg projektskabelonen for den type feedback, du vil indsamle, og vælg derefter **Næste**.
1. Vælg et integrationsformat under **Vælg et integrationsformat** under fanen **Send**. Feltet **Integreret kode** viser den kode, der skal være integreret i Commerce-webstedsgeneratoren.

Eksemplerne i denne artikel bruger projektskabelonen **Periodisk kundeundersøgelse** og integreringsformatet **Knap**.

I følgende eksempelillustration vises siden med projektskabelonen **Periodisk kundeundersøgelse**, hvor indstillingen for integreringsformatet **Knap** er valgt, og integrationskoden for denne indstilling vises i feltet **Integreret kode**. Der kræves tre separate handlinger for at integrere den angivne kode i webstedets sider, som beskrevet i følgende afsnit.

![Siden Periodisk kundeundersøgelse i Customer Voice med indstillingen Knap valgt.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Integrere URL-adressen til det eksterne script

På alle de websider, der skal have en Customer Voice-undersøgelse, skal du integrere den eksterne script-URL-adresse, som Customer Voice har angivet i integrationskoden. Den bedste måde at integrere scriptet på flere websider på er at oprette et fragment i webstedsgeneratoren, der indeholder den eksterne script-URL-adresse, og derefter føje fragmentet til de relevante sideskabeloner. Når du har publiceret en opdateret skabelon, ligner den integrerede eksterne scriptkode følgende eksempel på de berørte websider.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Du kan finde oplysninger om fragmenter i [Arbejd med fragmenter](work-with-fragments.md).

> [!NOTE]
> Du skal kun føje URL-adressen til fragmentet. Det eksterne scriptmodul tilføjer den anden scriptkode.

Hvis du vil integrere den eksterne script-URL-adresse i et fragment, skal du følge disse trin.

1. I webstedsgeneratoren skal du oprette et fragment, der er baseret på [modulet Eksternt script](script-module.md).
1. Vælg pladsen **Eksternt standardscript** i det nye fragment.
1. Angiv den eksterne URL-adresse for scriptet i feltet **Script-kilde** i egenskabsruden **Eksternt standardscript**, som vist i følgende illustration af eksemplet.

    ![Ekstern URL-adresse for scriptet i feltet Scriptkilde for det nye fragment.](media/customer-voice-integration-2.png)

1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer** for at publicere fragmentet.

Det nye fragment, der indeholder den integrerede eksterne scriptblok, er nu klar til at blive føjet til den relevante sideskabelon.

### <a name="embed-the-external-style-sheet-code"></a>Integrere den eksterne typografiarkskode

På alle de websider, der skal have en Customer Voice-undersøgelse, skal du derefter integrere den eksterne typografiarkskode, som Customer Voice har angivet i integrationskoden. Som i ovenstående sektion er den bedste måde at integrere den eksterne typografiarkskode på flere websider at oprette et fragment i webstedsgeneratoren, der indeholder den eksterne typografiarkskode, og derefter føje fragmentet til de relevante sideskabeloner. Den integrerede eksterne typografiarkskode ligner følgende eksempelkode.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Hvis du vil integrere den eksterne typografiarkskode i et fragment, skal du følge disse trin.

1. I webstedsgeneratoren skal du oprette et fragment, der er baseret på [modulet Metatags](metatags-module.md).
1. Vælg pladsen **Standardmetatags** i fragmentet.
1. Angiv typografiarkskoden i feltet **Metakoder** i egenskabsruden **Standardmetatags**, som vist i følgende illustration af eksemplet.

    ![Ekstern typografiarkskode i feltet Metakoder for det nye fragment.](media/customer-voice-integration-3.png)

1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer** for at publicere fragmentet.

Det nye fragment, der indeholder den integrerede eksterne typografiarkskode, er nu klar til at blive føjet til den relevante sideskabelon.

### <a name="embed-the-inline-script-code"></a>Integrere den indbyggede scriptkode 

På alle de websider, der skal have en Customer Voice-undersøgelse, skal du derefter integrere den indbyggede scriptkode, som Customer Voice har angivet i integrationskoden. Som i ovenstående sektioner er den bedste måde at integrere den indbyggede scriptkode på flere websider at oprette et fragment i webstedsgeneratoren, der indeholder den indbyggede scriptkode, og derefter føje fragmentet til de relevante sideskabeloner.

I følgende eksempel er den indbyggede scriptkode **SURVEY\_KEY** en pladsholder. Værdien for **SURVEY\_KEY** skal svare til den faktiske undersøgelsesnøgle, som Customer Voice har angivet i integrationskoden. Den sidste linje kalder koden for at gengive undersøgelsesknappen efter et sekund for at sikre, at scriptene har tilstrækkelig tid til at blive indlæst. Afhængigt af den undersøgelse, du har valgt, kan du også være nødt til at tilføje eller opdatere andre metadata, f.eks. firmanavnet.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Hvis du vil integrere den indbyggede scriptkode i et fragment, skal du følge disse trin.

1. I webstedsgeneratoren skal du oprette et fragment, der er baseret på [modulet Indbygget script](script-module.md).
1. Vælg pladsen **Indbygget standardscript** i fragmentet.
1. Angiv den indbyggede scriptkode i feltet **Indbygget script** i egenskabsruden **Indbygget standardscript**, som vist i følgende illustration af eksemplet.

    ![Indbygget scriptkode i feltet Indbygget script for det nye fragment.](media/customer-voice-integration-4.png)

1. Vælg **Gem**, og vælg derefter **Afslut redigering**.
1. Vælg **Publicer** for at publicere fragmentet.

Det nye fragment, der indeholder den integrerede indbyggede scriptkode, er nu klar til at blive føjet til den relevante sideskabelon.

## <a name="add-fragments-to-a-template"></a>Føje fragmenter til en skabelon

Når du er færdig med at oprette de fragmenter, der indeholder den integrerede kunde til Customer Voice, skal du føje dem til de sideskabeloner, der er knyttet til de websider, hvor du vil bruge dem. I følgende eksempelillustration er de tre eksempelfragmenter føjet til en PDP-skabelon (side med produktdetaljer).

![Eksempel på fragmenter, der er føjet til en PDP-skabelon.](media/customer-voice-integration-5.png)

Når den opdaterede skabelon er publiceret, vises Customer Voice-undersøgelsen på alle sider, der styres af skabelonen.

Du kan finde oplysninger om skabeloner i [Arbejde med skabeloner](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Konfigurere sikkerhedspolitik for indhold

Som standard tillader sikkerhedspolitik for indhold (CSP) ikke kald til andre tjenester, medmindre der er udført yderligere konfiguration. Når du har publiceret de opdaterede skabeloner, er det derfor sandsynligt, at undersøgelsen ikke bliver indlæst på de relevante websider. Hvis du vil have vist de CSP-relaterede fejl, skal du åbne webbrowserens udviklerværktøjer (F12) og derefter gå til en side, der indeholder undersøgelsen. De CSP-relaterede fejl vises i konsoloutputtet.

Hvis du vil konfigurere CSP i webstedsgeneratoren for at rette fejl, skal du følge disse trin.

1. Gå til **Webstedsindstillinger \> Udvidelser**.
1. Under fanen **Sikkerhedspolitik for indhold** skal du føje `https://customervoice.microsoft.com/` til direktivet **child-src**.
1. Føj `https://customervoice.microsoft.com/` til direktivet **frame-src**.
1. Føj `https://mfpembedcdnmsit.azureedge.net` og **.azureedge.net** til direktivet **img-src**.

Du kan finde flere oplysninger under [Sikkerhedspolitik for indhold](manage-csp.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulet Eksternt script](script-module.md)

[Metatags-modul](metatags-module.md)

[Modulet Indbygget script](script-module.md)

[Sikkerhedspolitik for indhold](manage-csp.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Arbejde med skabeloner](work-with-templates.md)
