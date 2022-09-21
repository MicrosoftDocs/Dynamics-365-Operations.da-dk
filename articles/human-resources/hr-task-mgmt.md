---
title: Opgavestyring
description: Denne artikel forklarer den opgavestyringsfunktionalitet, der findes i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 29b547ff4f55b572ab774e7e70949ec8cb53ef42
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445888"
---
# <a name="task-management"></a>Opgavestyring

[!INCLUDE [PEAP](../includes/peap-1.md)]

Med Opgavestyring kan du oprette opgaver, der skal fuldføres for at ansætte (onboard), fratræde (offboard) og overføre (stillingsskift) medarbejdere. I opgavestyring bruges begrebet tjeklister. En tjekliste er en liste over opgaver for onboarding, offboarding eller stillingsskift. I opgavestyring bruges tjeklister til at gruppere opgaver og tildele dem til personer eller grupper. Tjeklistefunktionaliteten til onboarding, offboarding og stillingsskift ligner hinanden.

## <a name="checklist-overview"></a>Oversigt over tjekliste

En tjekliste er en gruppe opgaver. Tjeklister giver dig en fleksibel metode til gruppering af opgaver, og de kan genbruges (f.eks. når du ansætter flere medarbejdere). Du kan oprette lige så mange tjeklister, du har brug for, og du kan tildele de samme opgaver til flere tjeklister.

### <a name="examples"></a>Eksempler

I følgende eksempler vises, hvordan tjeklister kan bruges i onboardingprocessen. Men da tjeklistefunktionaliteten for onboarding, offboarding og stillingsskift ligner hinanden, gælder oplysningerne også for processerne for offboarding og stillingsskift.

Som en del af onboardingprocessen kan HR-medarbejdere oprette opgaver, der sporer onboardingstatus for kommende og nyligt ansatte medarbejdere. Da onboardingprocessen kan variere, afhængigt af medarbejderens stilling eller geografiske placering, kan du oprette flere onboarding-tjeklister for at tage højde for forskellige ansættelsessituationer.

**Eksempel 1**

Alle medarbejdere, der ansættes i USA, skal udføre opgaver som f.eks. udfyldelse af blanketter for A-skat. Opgaver som f.eks. tildeling af firmabil gælder måske kun for medarbejdere på lederniveau. I dette tilfælde kan der oprettes to tjeklister til onboarding: **Medarbejdere med base i USA** og **Kun ledere**. Når der derefter ansættes en chef på mellemniveau i USA, vælges tjeklisten **Medarbejdere med base i USA**. Når der ansættes en leder i USA, vil begge tjeklister dog blive valgt for at sikre, at alle nødvendige onboardingopgaver er fuldført.

**Eksempel 2**

Et firma har både sæsonarbejdere og fuldtidsmedarbejdere. Selvom nogle opgaver (f.eks. kontrol af den nye medarbejders ankomsttidspunkt) gælder for medarbejdere af begge typer, gælder nogle ekstra opgaver kun for almindelige fuldtidsmedarbejdere. I dette tilfælde kan du oprette to tjeklister. Begge tjeklister omfatter de opgaver, der gælder for både sæson- og fuldtidsmedarbejdere, men kun én tjekliste indeholder opgaver, der er specifikke for almindelige fuldtidsmedarbejdere.

## <a name="task-management-workspace"></a>Arbejdsområdet til opgavestyring

Arbejdsområdet **Opgavestyring** indeholder en oversigt over alle de opgaver, som personerne har fået tildelt i onboarding-, offboarding- og stillingsskift-processerne. Hvis du vil have vist opgaverne for en proces, skal du vælge den relevante fane i øverste venstre hjørne: **Onboarding**, **Offboarding** eller **Stillingsskift**. Som standard er det kun HR-medarbejdere, der har adgang til arbejdsområdet **Opgavestyring**.

Fanen **Onboarding** indeholder en **Starter snart**-liste over kommende medarbejdere og en liste over **Seneste ansættelser**, der viser nyansatte medarbejdere. Du kan kun vælge én medarbejder på begge lister. Når du vælger en medarbejder, vises alle opgaver, der vedrører den pågældende medarbejders onboarding, i højre side af siden. Fanen **Onboarding** indeholder også en liste over **Alle opgaver**, der viser alle opgaver for alle kommende eller nyansatte medarbejdere. Endelig indeholder den en liste over forfaldne opgaver og en liste over opgaver, der er tildelt den aktuelle bruger.

Fanen **Offboarding** indeholder en liste over medarbejdere, der forlader firmaet, og en liste over medarbejdere, som allerede har forladt firmaet. Du kan kun vælge én medarbejder på begge lister. Når du vælger en medarbejder, vises alle opgaver, der vedrører den pågældende medarbejders offboarding. Fanen **Offboarding** indeholder også en liste over **Alle opgaver**, der viser alle opgaver for alle fratrædende eller fratrådte medarbejdere. Endelig indeholder den en liste over forfaldne opgaver og en liste over opgaver, der er tildelt den aktuelle bruger.

Fanen **Stillingsskift** indeholder en liste over **Alle opgaver**, der viser alle opgaver for alle medarbejdere, der skal skifte stilling, eller som har skiftet stilling for nylig. Der er også en liste over forfaldne opgaver og en liste over opgaver, der er tildelt den aktuelle bruger.

Under alle tre faner kan HR-assistenter og -ledere udføre følgende aktiviteter:
- Anvende en tjekliste på en medarbejder
- Opdatere statussen for en opgave
- Tildele en opgave til en anden
- Opdatere forfaldsdatoen for en opgave

> [!NOTE]
> Fanen **Onboarding** viser som standard medarbejdere, der er ansat inden for de seneste syv dage. Hvis du vil ændre denne indstilling, skal du angive en tidsramme i feltet **Nye ansættelser** på siden **Human Resources-parametre** under fanen **Generelt**. Dataene på listen **Nye ansættelser** kan vises for et bestemt antal dage, måneder eller år. Hvis du for eksempel vil have vist listen over medarbejdere, der er ansat inden for de seneste 14 dage, skal du angive feltet **Periode** til **14** og feltet **Enhed** til **Dage**.
> På siden **Human Resources-parametre** kan du også opdatere datointervallet for listerne over fratrædende og fratrådte medarbejdere, der vises under fanen **Offboarding**. Disse indstillinger gælder også for arbejdsområdet **Personalestyring**.

## <a name="setting-up-tasks"></a>Konfigurere opgaver

Du kan oprette opgaver enkeltvist og derefter genbruge dem på flere tjeklister. Hvis du vil oprette en opgave, skal du vælge **Ny** under fanen **Opgaver** på siden **Opsætning af onboarding**.

Du kan tildele en oprettet opgave til flere checklister ved at markere opgaven og derefter vælge **Anvend på checklister** i menuen.

Du kan også føje opgaver direkte til tjeklisten. Hvis du vil føje en opgave til en tjekliste, skal du enten oprette en ny tjekliste, som opgaven skal føjes til, på siden **Opsætning af onboarding** under fanen **Tjekliste** eller føje opgaven til en eksisterende tjekliste.

Hvis du vil redigere en opgave i biblioteket, skal du vælge **Rediger** i menuen Opgavebibliotek. Hvis opgaven er knyttet til nogen checklister, vises disse checklister på siden **Rediger opgave**. Hvis opgaverne i checklisterne skal opdateres med redigeringerne, skal du markere disse checklister i afsnittet **Anvend på checklister**.

Hvis du vil slette opgaver fra biblioteket, skal du vælge indstillingen **Slet**. Hvis der er knyttet en opgave til en checkliste, slettes opgaven ikke fra checklisten. Opgaven skal fjernes fra checklisten i en separat handling.

> [!NOTE]
> Hvis du føjer en opgave direkte til en tjekliste, kan du ikke genbruge den på andre tjeklister.

Følgende tabel beskriver de felter, der er tilgængelige, når du opretter en opgave efter en af metoderne.

| Felt           | Beskrivelse |
|-----------------|-------------|
| Opgave            | Angiv navnet på opgaven. |
| Beskrivelse     | Angiv en beskrivelse af opgaven. |
| Valgfri        | Angiv, om opgaven er valgfri og kun er oplysende. |
| Opgavelink       | Indtast URL-adressen på en ekstern webside eller en bestemt side i appen, hvor brugeren skal fuldføre opgaven. Du kan finde flere oplysninger i sektionen [Opgavelinks](#task-links). |
| Tildelingstype | Opgaver kan tildeles til en bestemt arbejder, stilling eller gruppe af stillinger, chefen for den berørte medarbejder (dvs. den medarbejder, der er en del af onboarding-, offboarding- eller stillingsskift-processen) eller den berørte medarbejder. Vælg tildelingstypen. Du kan finde flere oplysninger i sektionen [Tildelingstyper](#assignment-types). |
| Tildelt     | Vælg den specifikke arbejder, stilling eller gruppe af stillinger, som opgaven skal tildeles. |
| Kontaktperson  | Angiv den person, der skal kontaktes, hvis der er spørgsmål til opgaven. |
| Forskydning af forfaldsdato | Angiv det antal dage før eller efter den onboarding-, fratrædelses- eller stillingsskiftsdato, hvor opgaven forfalder. Yderligere oplysninger finder du i afsnittet [Opgaveforfaldsdatoer og feltet Forskydning af forfaldsdato](#task-due-dates-and-the-due-date-offset-field). |
| Instruktioner    | Angiv instruktioner til fuldførelse af opgaven. Du kan finde flere oplysninger i afsnittet [Instruktioner](#instructions). |

### <a name="task-links"></a>Opgavelinks

Et opgavelink giver et link til en ekstern webside eller en side i Dynamics 365-appen. Du kan angive et opgavelink, hvis den person, der har fået opgaven tildelt, skal gå til en bestemt webside eller en bestemt side i Dynamics 365-appen for at fuldføre opgaven. Når du opretter et opgavelink, kan du vælge en af følgende indstillinger:

- **Menupunkt** – Hvis du vælger denne indstilling, vises en liste over alle sider i Dynamics 365-appen. Vælg en side på listen.
- **URL-adresse** – Hvis du vælger denne indstilling, skal du angive URL-adressen på den webside, du ønsker, at den person, der har fået opgaven tildelt, skal gå til. Den angivne side kan være en side, som ikke er en del af Dynamics 365-appen.
- **Arbejderoplysninger** – Hvis du vælger denne indstilling, skal du vælge en af følgende indstillinger:

    - **Medarbejder-selvbetjeningshandlinger** – Denne indstilling viser en liste over sider, der er tilgængelige i **Medarbejderselvbetjening**. Brug den, hvis den opgave, der er tildelt den onboardede medarbejder, skal fuldføres i **Medarbejderselvbetjening**. Hvis medarbejderen f.eks. skal angive sine personlige kontaktoplysninger, skal du vælge **Medarbejder-selvbetjeningshandlinger** og derefter vælge **Personlige detaljer&gt;Personlige oplysninger**.
    - **Arbejderstyringshandlinger** – Denne indstilling viser en liste over sider, der er relateret til arbejderens post, men som medarbejderen ikke har adgang til. Hvis ejeren af opgaven f.eks. skal angive oplysninger, der er specifikke for en onboardet arbejder, f.eks. kompensationsoplysninger, skal du vælge **Arbejderstyringshandlinger** og derefter vælge **Kompensation&gt;Fast kompensation**.

### <a name="assignment-types"></a>Tildelingstyper

Når en medarbejder ansættes, fratræder eller skifter stilling, kan du vælge en eller flere tjeklister. Når der er valgt en tjekliste, og ansættelses-, fratrædelses- eller stillingsskifteprocessen er fuldført, oprettes der opgaver, som tildeles brugerne for at følge med i forløbet.

Når en opgave oprettes, tildeles den til en bestemt bruger. Den bruger, som en opgave er tildelt, afhænger af den tildelingstype, der er valgt for opgaven. Du kan vælge mellem følgende værdier i feltet **Tildelingstype**:

- **Arbejder** – Tildel opgaven til en bestemt arbejder. Når du har valgt denne værdi, skal du vælge arbejderen i feltet **Tildelt til**.
- **Stilling** – Tildel opgaven til en bestemt stilling. Når du har valgt denne værdi, skal du vælge stillingen i feltet **Tildelt til**.

    En it-tekniker vil f.eks. altid være ansvarlig for at klargøre en bærbar computer til en ny medarbejder. Når du i dette tilfælde opretter konfigurationsopgaven for den bærbare computer, skal du vælge **Stilling** som tildelingstype og derefter vælge **It-tekniker** som stilling. Når en medarbejder ansættes, og tjeklisten er tildelt, tildeles konfigurationsopgaven for computeren til en arbejder i it-teknikerstilling på det tidspunkt, hvor ansættelseshandlingen angives.

- **Gruppe** – Tildel opgaven til en gruppe af stillinger (tildelingsgruppe). Når du har valgt denne værdi, skal du vælge gruppen i feltet **Tildelt til**. Yderligere oplysninger finder du i afsnittet [Konfigurere tildelingsgrupper (valgfrit)](#setting-up-assignment-groups-optional).
- **Leder** – Tildel opgaven til chefen for den medarbejder, der ansættes, fratræder eller skifter stilling.

    > [!IMPORTANT]
    > Når der anvendes en tjekliste, kan chefen ikke fastlægges, hvis der i øjeblikket ikke er tildelt en stilling til den ansatte, fratrådte eller skiftede medarbejder. I dette tilfælde tildeles opgaven til ejeren af tjeklisten. Du kan finde flere oplysninger i afsnittet [Konfigurere tjeklister](#setting-up-checklists).

- **Medarbejder** – Tildel den medarbejder, der ansættes, fratræder eller skifter stilling.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Forfaldsdatoer for opgaver og feltet Forskydning af forfaldsdato

Forfaldsdatoer for opgaver er baseret på medarbejderens startdato, fratrædelsesdato eller stillingsskiftedato. Nogle opgaver skal fuldføres før en medarbejders startdato, mens andre opgaver kan fuldføres senere. Når du definerer en opgave, skal du angive feltet **Forskydning af forfaldsdato** til en relativ forfaldsdato i forhold til startdato, fratrædelsesdato eller stillingsskiftedato. En it-tekniker skal f.eks. klargøre en bærbar computer til en ny medarbejder to dage før den pågældende medarbejders startdato. I dette tilfælde skal du angive feltet **Forskydning af forfaldsdato** til **-2**, når du opretter konfigurationsopgaven til computeren. Hvis en medarbejders startdato er 5. maj, forfalder opgaven den 3. maj.

> [!NOTE]
> Forfaldsdatoer kan justeres, når opgaven er oprettet.

Forfaldsdatoerne beregnes på basis af den kalender, der er knyttet til tjeklisten. Du kan finde flere oplysninger i afsnittet [Konfigurere tjeklister](#setting-up-checklists).

### <a name="instructions"></a>Instruktioner

Komplekse opgaver kan kræve flere trin, eller den person, der udfører opgaven, skal måske angive yderligere oplysninger. I feltet **Instruktioner** kan du angive instruktioner eller yderligere oplysninger til den person, der er tildelt opgaven, om hvordan den skal fuldføres.

## <a name="setting-up-checklists"></a>Konfigurere tjeklister

En tjekliste er en gruppe opgaver. Du kan oprette lige så mange tjeklister, du har brug for, og du kan tildele de samme opgaver til flere tjeklister.

Hvis du vil oprette en ny opgave på en kontrolliste, skal du vælge **Ny** på menulinjen **Opgaver**. Når du opretter en ny opgave, kan du vælge at føje den til opgavebiblioteket, så den kan deles på tværs af flere checklister. Du kan kun føje opgaven til biblioteket, hvis indstillingen **Anvend opgave på biblioteket** er angivet til **Ja**. Hvis du føjer opgaven til opgavebiblioteket, kan du også føje den til andre checklister samtidig ved at vælge disse checklister i afsnittet **Anvend på checklister**. Hvis du ikke føjer opgaven til biblioteket, findes den kun på den checkliste, du opretter den i.

Hvis du vil redigere en opgave på kontrollisten, skal du vælge **Rediger**. Hvis opgaven er knyttet til nogen checklister, vises disse checklister på siden **Rediger opgave**. Hvis opgaverne i andre checklister skal opdateres med redigeringerne, skal du markere disse checklister i afsnittet **Anvend på checklister**.

Hvis du vil fjerne opgaver fra checklisten, skal du vælge **Fjern**. Denne handling fjerner blot opgaver fra checklisten. De slettes ikke fra opgavebiblioteket. Hvis du vil slette en opgave fra biblioteket, skal du gå til opgavebiblioteket og vælge **Slet**.

Når du opretter en tjekliste, skal du angive en ejer og en kalender.

Hvis feltet **Tildelingstype** for en opgave er angivet til **Stilling**, **Leder** eller **Gruppe**, men der ikke kan udledes nogen bestemt person af tildelingstypen, tildeles opgaven til ejeren af tjeklisten. Her vises nogle eksempler på situationer, hvor ejeren af tjeklisten tildeles opgaver:

- Ingen stilling er tildelt den medarbejder, der ansættes eller fratræder. Da medarbejderen ikke har en stillingstildeling, kan den pågældendes chef ikke bestemmes.
- Feltet **Tildelingstype** er angivet til **Stilling**, men der er ikke tildelt nogen medarbejder til stillingen på det tidspunkt, hvor opgaven oprettes. Opgaven **Opsætning af bærbar computer** er f.eks. tildelt stillingsnummer 000876 (**Teknisk supportspecialist**). Når en medarbejder ansættes, er der ikke tildelt en medarbejder til stillingen 000876. Derfor oprettes der en opgave til tjeklistens ejer.
- Feltet **Tildelingstype** er angivet til **Gruppe**, men der er ikke tildelt nogen medarbejder til stillingerne i gruppen på det tidspunkt, hvor opgaven oprettes.

Den kalender, der er angivet for en tjekliste, bruges til at beregne forfaldsdatoen for opgaver, der er en del af tjeklisten. Arbejdsdage og ikke-arbejdsdage defineres i kalenderopsætningen. Arbejdsdage medtages, når forfaldsdatoen for opgaver beregnes, og ikke-arbejdsdage udelukkes. Ikke-arbejdsdage omfatter weekender og helligdage. 

Når der er oprettet en kalender, er den knyttet til en tjeklisteskabelon. På den måde beregnes forfaldsdatoen for hver opgave på tjeklisten på samme måde. Du kan oprette flere kalendere, men der kan kun knyttes én kalender til hver tjekliste.

## <a name="setting-up-assignment-groups-optional"></a>Konfigurere tildelingsgrupper (valgfrit)

Nogle gange er en gruppe personer ansvarlig for en opgave. En gruppe it-arbejdere kan f.eks. være ansvarlig for klargøring af bærbare computere til nyansatte.

Følg disse trin for at konfigurere en tildelingsgruppe.

1. På siden **Tildeling af gruppe** skal du vælge **Ny**.
1. Angiv et navn (f.eks. **IT bærbar**) og en beskrivelse af gruppen.
1. Vælg **Gem**.
1. Vælg **Tilføj** i oversigtspanelet **Medlemmer**.
1. Vælg alle de stillinger, der er ansvarlige for opgaven, i feltet **Stillinger**.

Når der er oprettet en tildelingsgruppe, kan den vælges, når der oprettes en opgave. Hvis du vil vælge en bestemt gruppe til en opgave, skal du vælge **Gruppe** i **Tildelingstype**. Den gruppe, du har oprettet, kan derefter vælges i feltet **Tildelt til**.

> [!IMPORTANT]
> Hvis en opgave er tildelt til en gruppe, markeres opgaven som **Fuldført**, når én person i gruppen fuldfører den. Opgaver oprettes tidspunktet for ansættelse, fratrædelse eller stillingsskift. De oprettes for de brugere, der er tildelt de stillinger, der er inkluderet i gruppen.

## <a name="setting-up-task-groups-optional"></a>Konfigurere opgavegrupper (valgfrit)

Der kan inkluderes mange opgaver i en onboarding-, offboarding- eller stillingsskifteproces. Du kan gøre det lettere at tildele alle de nødvendige opgaver til en tjekliste ved at oprette valgfrie opgavegrupper til kategorisering af relaterede opgaver. Afdelingerne HR, IT og Løn skal f.eks. hver udføre specifikke opgaver for at ansætte en ny medarbejder. Derfor opretter du følgende opgavegrupper: **HR**, **IT** og **Løn**. Når du derefter opretter en opgave, kan du knytte en af disse opgavegrupper til den.

Når du vil føje en opgave til en tjekliste, kan du filtrere listen over opgaver efter den opgavegruppe, som den ønskede opgave er tildelt. Når du f.eks. opretter en tjeklisteskabelon, kan du filtrere listen, så det kun er de it-opgaver, der er tildelt til opgavegruppen **IT**, der vises. Du kan derfor sikre dig, at der kun vælges de relevante it-opgaver.

## <a name="using-checklists"></a>Bruge tjeklister

Når en arbejder ansættes, fratræder eller skifter stilling, kan du vælge en eller flere tjeklister. Forfaldsdatoer for opgaver og arbejdertildelinger oprettes, når ansættelses-, fratrædelses- eller stillingsskifteprocessen er fuldført. Når du f.eks. vælger knappen **Ansæt** eller **Ansæt og tilføj detaljer**, oprettes der opgaver for personer baseret på tildelingstypen.

Der knyttes en forfaldsdato til hver opgave ved at lægge forskydningen af forfaldsdatoen til eller trække den fra medarbejderens startdato. Yderligere oplysninger finder du i afsnittet [Opgaveforfaldsdatoer og feltet Forskydning af forfaldsdato](#task-due-dates-and-the-due-date-offset-field).

Hvis du bruger personalehandlinger, oprettes opgaverne, når knappen **Fuldført** er valgt, eller handlingen godkendes.

I arbejdsområdet i **Opgavestyring** kan du anvende en tjekliste til en medarbejder ved at vælge medarbejderen på siden med den simple liste eller detaljer og derefter vælge **Anvend tjekliste**. Værdien i feltet **Måldato** bruges til at beregne forfaldsdatoen for opgaverne. Måldatoen skal typisk svare til medarbejderens ansættelses-, fratrædelses- eller stillingsskiftedato.

Du kan også anvende en tjekliste til en medarbejder ved at åbne dennes **Arbejder**-side og vælge **Tjeklister** i menuen.

## <a name="completing-tasks"></a>Fuldførelse af opgaver

På siden **Medarbejderselvbetjening** kan en medarbejder se alle de opgaver, der er knyttet til dem. For hver tildelte opgave vises værdier for **Opgave**, **Beskrivelse**, **Instruktioner** og **Kontaktperson**. Derudover kan medarbejderen for hver opgave åbne den tilknyttede eksterne webside eller den tilknyttede side i Dynamics 365-appen.

Opgaver kan også vises på standarddashboardet. Sådan vises opgaver på standarddashboardet:
1. Gå til **Brugerindstillinger – Indstillinger – Opgavestyring** 
2. Angiv **Vis opgaver på standarddashboard** til **Til**:  

>[!Note] 
>Funktionen **Opgavestyring** skal være aktiveret i **Funktionsstyring**, for at indstillingen kan vises i **Brugerindstillinger**.

Opgaver kan markeres som **Igangværende**, **Annulleret** eller **Fuldført**. Hvis en opgave er tildelt til en gruppe, markeres den som **Fuldført**, når én person i gruppen fuldfører den.

Opgaver kan også tildeles igen.
