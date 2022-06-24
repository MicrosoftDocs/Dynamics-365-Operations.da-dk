---
title: Dynamics 365 Commerce e-Commerce-lokaliseringsvejledning
description: Denne artikel beskriver, hvordan et Microsoft Dynamics 365 Commerce-e-handelswebsted lokaliseres til flere sprog og konfigurerer webstedet, så det understøtter flere kanaler.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 955a85340f6d35f1e203d74920d07b5dc6ff8654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873378"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce e-Commerce-lokaliseringsvejledning

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan et Microsoft Dynamics 365 Commerce-e-handelswebsted lokaliseres til flere sprog, og webstedet konfigureres til at understøtte flere kanaler, og det dækker også de begreber og den terminologi, der er knyttet til processen.

Funktionerne til e-handel i Dynamics 365 Commerce er designet til at aktivere onlineerfaringer, der kan tilpasses bestemte lande og sprog, men samtidig tillade maksimal genbrug af skabeloner, sider, indhold og medier. Du kan også oprette et grundlæggende websted og derefter udvide til nye markeder ved at tilføje understøttelse af flere lande og sprog over tid.

## <a name="definitions"></a>Definitioner

**Landestandard, landestandard-id:** En landestandard (også kendt som en landestandard-id) definerer et sprog, der er tilknyttet et land eller et område. Landestandard-id "fr-ca" er f.eks. tilknyttet canadisk fransk.

**Basissprog**: Det sprog, du udvikler indholdet af webstedet på, før du eksporterer det til lokalisering.

**Kanal, onlinebutik**: En kanal (også kendt som en onlinebutik) definerer betalingsmåder, prisgrupper, produkthierarkier, sortimenter og produkter til en online-e-handelsbutik.

## <a name="concepts"></a>Begreber

### <a name="url-driven-experience"></a>URL-baseret erfaring

Dynamics 365 Commerce-e-handelswebsteder leverer entydige markedsbaserede og lokale erfaringer for kunder via kanaler og landestandard-id'er. Kanaler definerer de entydige produkter, kategorier, valutaer og betalingsmetoder for et marked, og landestandard-id'er bestemmer sproget i det indhold, kunderne ser. Et e-handelswebsted bruger URL-adresser til at skelne mellem markedsbaserede og lokale erfaringer. URL-adresser til websteder for disse entydige kanal- og landestandardoplevelse defineres for et websted på siden **Webstedsindstillinger \> Kanaler** i Dynamics 365 Commerce-webstedgenerator.

I webstedgenerator er en URL-adresse en kombination af et domæne og en sti, der definerer indgangsstedet for en entydig kombination af en kanal og en landestandard. I det følgende eksempel definerer en fiktiv onlinebutik med navnet Fabrikam Inc fire entydige kombinationer af en kanal og en landestandard og knytter hver kombination til en entydig URL-adresse, der tjener indhold til kunderne.

| Domæne                     |  Sti      | Kanal       |   Landestandard     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikams udvidede onlinebutik | da  |
| `https://fabrikam.com` | /es    | Fabrikams udvidede onlinebutik | es     |
| `https://fabrikam.ca`  | /      | Contoso onlinebutik    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso onlinebutik    | en-ca  |

#### <a name="domain"></a>Domæne

Domæner oprettes, når du konfigurerer e-handelswebstedet i Microsoft Dynamics Lifecycle Services (LCS). Når e-handelsmiljøet er klargjort, kan du tilføje flere domæner ved at åbne en serviceanmodning. Du kan finde flere oplysninger om, hvordan du konfigurerer domæner til dit e-commerce-websted i [Domæner i Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Sti

- En sti er en tilfældig streng, der sammen med domænet knyttes til en entydig kombination af en kanal og en landestandard. I det foregående eksempel svarer den streng, der bruges som sti, til den landestandard, som stien er tilknyttet. Du kan dog bruge en anden indfaldsvinkel.
- En kombination af en kanal og landestandard kan knyttes til et domæne og en tom sti ("/"). I det foregående eksempel henter kunder, der besøger `https://fabrikam.ca/`, produkterne og sortimenterne til det canadiske marked på canadisk fransk.
- Commerce site builder forhindrer, at du opretter dubletkombinationer af et domæne og en sti. Du kan dog knytte dublerede kombinationer af en kanal og landestandarder til en anden kombination af et domæne og en sti.

#### <a name="channel"></a>Kanal

- Kanaler (også kendt som onlinebutikker) definerer betalingsmåder, prisgrupper, produkthierarkier, sortimenter og produkter til en online-e-handelsbutik.
- Kanaler defineres, konfigureres og udgives i Dynamics 365 Commerce Headquarters.
- Site Builder kan registrere de onlinebutikker, der er konfigureret i Commerce Headquarters, og som er tilgængelige, så de kan knyttes til et websted.

Du kan finde flere oplysninger om kanaler i [Oversigt over kanaler](channels-overview.md). Du kan finde flere oplysninger om, hvordan du konfigurerer en onlinekanal, i [Konfigurere en onlinekanal](channel-setup-online.md).

#### <a name="locale"></a>Landestandard

- Landestandarden er det faktiske id, der bruges, når du afleverer XML-filer (Localization Interchange File Format) til lokalisering. Landestandarder defineres og udgives for hver kanal i Commerce Headquarters. Du kan finde flere oplysninger om konfiguration af sprog og kanaler i Site Builder i næste afsnit.
- Den samme landestandard kan knyttes til flere kanaler. På denne måde kan der tilbydes et fælles sprog på tværs af flere markeder.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Konfigurere sprog og kanaler til e-handelswebstedet

Som standard er alle Dynamics 365 Commerce e-handelswebsteder konfigureret til at bruge en enkelt onlinekanal og et enkelt sprog, uanset om du starter med Fabrikam-demowebstedet eller opretter et nyt websted helt fra bunden.

I denne konfiguration udvikler kunder og partnere typisk alle de aktiver, der skal bruges på tværs af lande og sprog. Dette indhold omfatter skabeloner, sider, fragmenter, indhold og medier. Alt webstedsindhold udvikles på det første sprog, du har valgt til dit websted, eller hvis du bruger fabrikam-demowebstedet, vil indholdet af webstedet blive udviklet på engelsk.

![Standard Dynamics 365 Commerce e-commerce-websted](media/loc-guide-1.png)

> [!NOTE]
> Du kan konfigurere Fabrikam-demowebstedet til et yderligere sprog, så der kan udføres indholdsudvikling på det pågældende sprog. Du kan finde oplysninger om, hvordan du føjer et nyt sprog til et websted og en kanal, i afsnittet [Konfigurere et ekstra sprog til webstedet](#configure-an-additional-language-for-your-site) senere i denne artikel.

Indholdsstyringssystemet (CMS) og sidemodellen for Dynamics 365 Commerce e-handelswebsteder er dog designet til at aktivere udvidelse til nye markeder og landestandarder. Derfor kan du via et enkelt e-handelswebsted administrere aktiverne for en onlinebutik, der dækker over flere markeder og sprog.

![Dynamics 365 Commerce e-handelswebsted, der dækker flere markeder og sprog](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Konfigurer et ekstra sprog til dit websted

Der er tre trin til konfiguration af et nyt sprog til et e-handelswebsted.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Trin 1: Føje sproget til kanalen (onlinebutik) i Commerce Headquarters

1. I Commerce Headquarters skal du gå til den kanal, du vil føje det nye sprog til. Gå til **Detail og handel \> Kanaler \> Onlinebutikker** for at få adgang til listen over online butikker, der er konfigureret til dit miljø.
1. Åbn den onlinebutik, der er knyttet til dit websted, ved at vælge værdien for **Detailkanal-id**. Du kan kontrollere den onlinebutik, der er knyttet til dit websted, ved at åbne indstillingssiden **Kanaler**-webstedet i Commerce Site Builder og se på navnet på onlinebutikken i kolonnen **Kanaler**. 
1. Vælg **Tilføj** i oversigtspanelet **Sprog**. I feltet **Sprog** skal du vælge landestandarden for det nye sprog. Vælg derefter **Gem**.
1. Gå derefter til **Detail og handel \> Detail og handels-it \> Dostributionsplan**, og kør job **1070 Kanalkonfiguration**. Når jobbet er kørt færdigt, kan du gå videre til trin 2 og føje sproget til en kanal til dit websted i Site Builder.

![Oversigtspanelet Sprog i en onlinebutik i Commerce Headquarters](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Trin 2: Føje sproget til en kanal i Site Builder

Hvis du vil tilføje sproget til en kanal i webstedsgeneratoren, skal du følge disse trin.

1. I Commerce site builder skal du åbne dit websted og derefter åbne siden **Kanaler** i indstillinger for websted.
1. Vælg navnet på kanalen til de labels, du vil tilføje sprog til.
1. Vælg **Tilføj landestandard** i højre rude.
1. I dialogboksen **Tilføj landestandard** skal du vælge landestandard for det sprog, du tidligere har føjet til kanalen i Commerce Headquarters, under **Tilføj landestandard**.
1. Vælg det domæne og den sti, som kunder vil anmode om at få vist dit websted på i denne kanal og dette sprog.
1. Hvis sproget skal være standardsprog til visning, oprettelse og opdatering af sider og fragmenter i Site Builder, skal du markere afkrydsningsfeltet **Brug som standard for oprettelse af kanalsprog**. 
    > [!NOTE]
    > Denne indstilling påvirker kun Site Builder. Den har ingen indflydelse på kundernes publicerede webstedsoplevelse.
1. Vælg **OK**.
1. Vælg **Gem og udgiv**.

#### <a name="step-3-localize-your-site-content"></a>Trin 3: Lokalisere indholdet af dit websted

Når du vender tilbage til visningen **Sider** i Commerce Site Builder, vil det nye sprog være tilgængeligt i kanalen og landestandardvælger i øverste højre hjørne. Du kan nu oprette lokale versioner af sider på dit basissprog.

Processen til lokalisering af indholdet af dine sider og fragmenter dækkes senere i afsnittet [Lokaliser e-commerce-webstedsindhold](#localize-e-commerce-site-content) senere i denne artikel.

### <a name="configure-a-new-channel-for-your-site"></a>Konfigurere en ny kanal til dit websted

Dynamics 365 Commerce e-handelswebsteder kan tjene erfaringer, der er defineret på tværs af flere onlinekanaler, der er konfigureret i Commerce Headquarters. Et websted bruger flere kanaler til at vise kunderne en entydig konfiguration af betalingsmåder, prisgrupper, produkthierarkier, sortimenter og et sæt produkter. En kanal bruges typisk til at konfigurere disse dimensioner, så den opfylder kravene og indstillingerne for den erfaring, der er knyttet til de enkelte lande. Denne indfaldsvinkel er dog en forretningsmæssig beslutning, som kunden træffer. Det er ikke et krav.

De forudsætninger og opgaver, der er forbundet med opsætning af en kanal (onlinebutik), ligger uden for området for dette dokument. Du kan finde flere oplysninger om, hvordan du konfigurerer en onlinekanal, i Commerce headquarters i [Konfigurere en kanal](channels-overview.md#channel-setup-basics). Du kan finde oplysninger om de trin og krav, der er specifikke for onlinekanaler [, i Konfigurere en onlinekanal](channel-setup-online.md).

Hvis du vil tilføje kanalen til webstedsgeneratoren, skal du følge disse trin.

1. i Commerce-webstedsgeneratoren skal du gå til **Webstedsindstillinger \> Kanaler**. 
1. Vælg **Tilføj en kanal**.
1. Vælg den kanal, du vil tilføje, under **Kanal** i dialogboksen **Tilføj en kanal**. 
    > [!NOTE]
    > Du kan kun tilføje kanaler, der ikke allerede er blevet føjet til dit websted.
1. Vælg standardlandestandarden for kanalen. Hvis du føjer nye sprog til kanalen, kan du ændre standardsproget for et af dem.
1. Angiv det domæne og den sti, der udgør den URL-adresse, der fungerer som indhold og erfaring for denne kombination af en kanal og et sprog.
1. Vælg **OK**.
1. Vælg **Gem og udgiv**.

## <a name="localize-e-commerce-site-content"></a>Lokaliser indhold på e-handelswebsted

### <a name="xliff-basics"></a>XLIFF-basis

XLIFF er et branchestandardfilformat, der bruges til at overføre indhold, der kan lokaliseres, mellem værktøjer til indholdsstyring. På commerce site builder bruges XLIFF-filformatet til eksport af side-, fragment- og billedmetadataindhold, så det kan lokaliseres og importeres igen.

Microsoft Dynamics-kunder arbejder typisk med lokale tredjepartsleverandører, f.eks. [Translated.com](https://translated.com/welcome) at oversætte deres XLIFF-filer til de sprog, de har brug for.

### <a name="localize-assets-in-site-builder"></a>Lokaliser aktiver i Site Builder

Følgende aktiver på e-handelswebstedet kan lokaliseres i Site Builder:

- Sider
- Fragmenter
- Medieaktiver
- Moduler

Alle nye sider, fragmenter og medieaktiver oprettes inden for rammerne af den kanal og det sprog, der aktuelt er valgt i kanalen og landestandardplukkeren. Dette sprog er normalt dit "basissprog", hvis du ikke har konfigureret yderligere sprog eller kanaler. På websteder, hvor der er konfigureret flere kanaler og sprog, defineres "basissproget" af kanalen og landestandarden, som du har angivet som standard på siden **Kanaler** i webstedsindstillinger.

Trinnene til lokalisering af indhold til sider, fragmenter og medieaktiver er ens. Der påpeges undtagelser og forskelle i de følgende afsnit. Trinnene til lokalisering af modulindholdet er dog forskellige. Du kan finde flere oplysninger i afsnittet [Lokaliser moduler](#localize-modules) nedenfor i denne artikel.

#### <a name="step-1-export-an-xliff-file"></a>Trin 1: Eksportere en XLIFF-fil

Udfør følgende trin for at eksportere en XLIFF-fil til en side, et fragment eller et billede i webstedsgeneratoren.

1. Åbn det aktiv, du vil eksportere basissprogindhold for, så det kan lokaliseres.
1. Vælg **Lokalisering \> Eksport XLIFF** på kommandolinjen.
    > [!NOTE]
    > Indstillingen **Lokalisering** kan kun ses, når aktivet er i tilstanden **Rediger**.

Der hentes en **\<assetname\>.xlf** med XLIFF-navnet til browserens overførselsmappe. Denne XLIFF-fil er specifik for det aktiv, du er ved at lokalisere. Du skal eksportere en XLIFF-fil for hvert aktiv, der skal lokaliseres.

#### <a name="step-2-localize-the-xliff-file"></a>Trin 2: Lokalisere XLIFF-filen

I de fleste tilfælde vil du arbejde med en oversættelsesleverandør for at oversætte XLIFF-filerne. Hvis du lokaliserer aktiver internt, eller hvis du blot vil teste lokaliseringsprocessen, skal du dog foretage følgende ændringer i en XLIFF-fil:

- Føj en destinationssprogattribut til /xliff/filelementet, og angiv værdien til landestandard-id for det sprog, du oversætter til. 
    > [!NOTE]
    > Dette landestandard-id skal svare til landestandard-id fra siden **Kanaler** i indstillinger for websted.
- For hvert //kildeelement skal du tilføje et målelement, der søger efter det sted, hvor tekstværdien er den oversatte version af indholdet af det pågældende kildeelement.

Du kan finde oplysninger om det skema, der styrer XLIFF-filer, i [XLIFF 1.2-specifikationen](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Hvis du vil lokalisere et aktiv på flere sprog, skal du oprette en lokaliseret XLIFF-fil for hvert af disse sprog.

#### <a name="step-3-import-the-localized-xliff-file"></a>Trin 3: Importere den lokale XLIFF-fil

Benyt følgende fremgangsmåde for at importere en XLIFF-fil for et aktiv.

1. Åbn det aktiv, du vil importere en XLIFF-fil for, i Commerce site builder.
1. Vælg den kanal og den sprog, du importerer lokaliseret indhold for, i kanalen og landestandardplukkeren øverst til højre.
1. Vælg **Lokalisering \> Import af XLIFF** på kommandolinjen. Gå derefter til, og vælg den lokaliserede XLIFF-fil for det valgte aktiv og det valgte sprog.

Når XLIFF-filen er importeret, oprettes der en "variant" af siden, fragmenter eller aktivet. Fra dette punkt og fremefter påvirker alle de ændringer, der foretages i den lokale variant, kun denne variant. De påvirker ikke det basisaktiv, som varianten er afledt af. På samme måde påvirker ændringer i basisaktivet ikke varianten for det pågældende aktiv. 

Hvis der er sider, kan du dog foretage ændringer på tværs af varianter ved at redigere den skabelon eller det layout, som disse sider er bundet til. På samme måde påvirker ændringer i et fragmenter alle sider, der er afhængige af den pågældende variant.

### <a name="images"></a>Billeder

Billeder kan kun gengives i en side- eller modulvariant, hvis det indholdsmetadata, der er knyttet til disse billeder, er lokaliseret. Aktuelt kan følgende metadata i et medieaktiv lokaliseres:

- Alternativ tekst
- Beskrivende tekst
- Stilling

Aktuelt kan du ikke lokalisere binær for et digitalt aktiv, f.eks. et billede eller en video. Produktteamet Dynamics 365 Commerce arbejder i øjeblikket på denne egenskab.

### <a name="localize-modules"></a>Lokalisere moduler

Strenge, der gengives som en del af selve modulet (f.eks. "Forrige" og "Næste" i et karruselmodul) er lokaliseret separat i forhold til modulindholdet. Yderligere oplysninger finder du i [Lokalisere et modul](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Ordliste til sidemodel](page-elements-overview.md)

[Dele kanal tværs af kanaler](cross-channel-sharing.md)

[Lokalisere et modul](e-commerce-extensibility/localize-module.md)

[Moduldefinitionsfil](e-commerce-extensibility/module-definition-file.md)

[Oversætte ressourcer til Commerce-udvidelser og labelfiler](dev-itpro/extension-resource-localization.md)

[Globalisere moduler ved hjælp af klassen CultureInfoFormatter](e-commerce-extensibility/globalize-modules.md)

[Appindstillinger: Temaer](e-commerce-extensibility/app-settings.md#themes-section)
