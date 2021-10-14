---
title: Kvalitetskontrol
description: Dette emne indeholder oplysninger om funktionen Kvalitetskontrol. Denne funktion giver lagermedarbejderne mulighed for hurtig spottjek af kvalitet, mens de modtager varer i modtagelsesområdet.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a3a565ea566dd2bf4d8c793b3340c78c9f4ed0a2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565297"
---
# <a name="quality-check"></a>Kvalitetskontrol

[!include [banner](../includes/banner.md)]

Funktionen *Kvalitetskontrol* giver lagermedarbejderne mulighed for hurtig spottjek af kvalitet, mens de modtager varer i modtagelsesområdet. Disse stikprøvekontroller er nyttige, når arbejderne kontrollerer emballagen eller andre let genkendelige dele af en vare. Funktionen hjælper medarbejderne med hurtigt at se, om noget er defekt eller forkert, før de lagrer varen på dens læg på lager-lokation.

Denne funktion er et alternativ til standardprocessen for kvalitetskontrol. Den giver større fleksibilitet og hurtigere behandling.

Når du bruger denne funktion, sker modtagelse og kvalitetskontrol på følgende måde:

1. Når en forsendelse ankommer, registrerer en lagermedarbejder ankomsten. Arbejderen scanner også et id for at registrere lokationen.
1. Arbejderen udfører en hurtig kvalitetskontrol og registrerer resultatet (bestået eller mislykket) for det pågældende id.
1. En af følgende handlinger sker:

    - Hvis kvalitetskontrollen er bestået, vil id'et blive accepteret og styret til en modtagelseslokalitet på normal vis.
    - Hvis kvalitetskontrollen er mislykket, afvises id'et, og eksisterende læg på lager-arbejde omdirigeres til en alternativ placering til yderligere inspektion. Der oprettes en ny kvalitetsordre. Hvis du vil have vist den kvalitetsordre, der er oprettet ud fra den mislykkede kvalitetskontrol, skal du gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.

Denne proces kan også konfigureres, så alle scannede id'er straks omdirigeres til kvalitetskontrollens lokation.

## <a name="turn-on-the-quality-check-feature"></a>Aktivere funktionen Kvalitetskontrol

Før du kan bruge funktionen *Kvalitetskontrol*, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Kvalitetskontrol*

## <a name="set-up-the-feature-for-the-example-scenario"></a>Konfigurere funktionen til eksempelscenariet

Dette afsnit indeholder retningslinjer og et eksempel, der viser, hvordan du kan konfigurere funktionen *Kvalitetskontrol* og forberede eksempeldata til det eksempelscenario, der er angivet senere i dette emne.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde dig gennem [eksempelscenariet](#example-scenario) ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

### <a name="quality-check-template"></a><a name="quality-template"></a>Kvalitetskontrolskabelon

Kvalitetskontrolskabelonen definerer reglerne for udførelse af hurtige stikprøvekontroller af kvaliteten på modtagelsestidspunktet.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Kvalitetskontrolskabelon**.
1. Vælg **Ny** for at føje en skabelon til gitteret.
1. Definer skabelonen ved at angive følgende værdier:

    - **Skabelonnavn for kvalitetskontrol:** *Dock check*

        Angiv et navn, der identificerer de politikker, der anvendes for denne skabelon.

    - **Acceptpolitik:** *Spørg bruger*

        Angiv, om brugere skal blive bedt om at acceptere eller afvise lagerkvaliteten, mens de behandler arbejdet, eller om kvaliteten skal afvises automatisk. De tilgængelige indstillinger er *Automatisk afvisning* og *Spørg brugeren*.

    - **Politik for kvalitetsbehandling:** *Opret kvalitetsordre*

        Vælg den politik, der skal bruges ved afvisning af lagerkvaliteten. Der findes følgende indstillinger:

        - *Opret kun arbejde* – Opret kun arbejde for at lette lagerbevægelse.
        - *Opret kvalitetsordre* – Opret en kvalitetsordre for at forenkle kvalitetstest.

    - **Testgruppe:** *Kabinet*

        Angiv den testgruppe, der skal bruges i den kvalitetsordre, der oprettes. Testgrupper konfigureres i modulet **Lagerstyring**.

        Lad indstillingen **Destruktiv tekst** være slået fra for testgruppen. Denne indstilling definerer, om prøven skal destrueres som en del af testene i testgruppen. Når der anvendes en destruktiv test, vil oprettelsen af en kvalitetsordre for en vare få systemet til at generere en lagertransaktion. Den nye lagerpostering foregriber lagerreduktionen for testantallet. Lagerreduktionen sker, når kvalitetsordren er fuldført via valideringstrinnet. Lagertransaktionen identificeres som en kvalitetsordre.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Arbejdsklasse – Kvalitetskontrol

Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som lagermedarbejdere kan behandle på en mobilenhed.

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.
1. Vælg **Ny** for at oprette en arbejdsklasse.
1. Angiv følgende værdier i overskriften:

    - **Arbejdsklasse-id:** *QC Check*

        Angiv et navn, der identificerer arbejdsklassen.

    - **Beskrivelse:** *QC Check*

        Angiv en kort beskrivelse, der angiver, hvad arbejdsklassen bruges til.

    - **Arbejdsordretype:** *Kvalitet i kvalitetskontrol*

        Vælg den type arbejdsordre, der oprettes af arbejdsklassen. Når du konfigurerer kvalitetskontrolarbejde, skal du altid vælge *Kvalitet i kvalitetskontrol*.

1. Lad feltet **Lokationstype** være tomt i oversigtspanelet **Gyldige lokationstyper**.

    Hvis du vælger en lokationstype, begrænser du de lokationer, hvor varer kan lægges på lager, efter at de er blevet plukket. Dette felt bruges, når en lokationsvejledning forsøger at finde lokationen, eller hvis en lagermedarbejder manuelt angiver lokationen for varen i mobilenhedsmenuen.

Du kan finde flere oplysninger om arbejdsklasser, og hvordan du opretter dem, under [Oprette en arbejdsklasse](tasks/create-work-class.md).

### <a name="work-template"></a>Arbejdsskabelon

Arbejdsskabeloner gør det muligt at definere arbejdshandlinger, der skal udføres på lagerstedet. Arbejdshandlinger på lagersted består typisk af parvise handlinger: en lagerarbejder plukker disponibel lagerbeholdning på ét sted og sætter derefter det plukkede lager ned på en anden placering. En arbejdsskabelon til kvalitetskontrol definerer de arbejdshandlinger, der skal udføres kvalitetskontrol for.

#### <a name="purchase-orders"></a>Indkøbsordrer

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Indstil feltet **Arbejdsordretype** i overskriften til *Indkøbsordrer*.
1. Vælg **Rediger** i handlingsruden.
1. Vælg en arbejdsskabelon, der skal omfatte et kvalitetskontroltrin. Vælg **51 indkøbsordremodtagelse** i feltet **Arbejdsskabelon** i sektionen *Oversigt*.
1. Bemærk, at gitteret indeholder to eksisterende linjer i sektionen **Arbejdsskabelondetaljer**: én til *Pluk* og én til *Læg på lager*.
1. Vælg **Ny** i sektionen **Arbejdsskabelondetaljer** for at føje en række for kvalitetskontrol til gitteret. Bemærk, at feltet **Linjenummer** for den nye linje er angivet til *3*.
1. Angiv følgende værdier på den nye linje. Acceptér standardværdierne for alle de andre felter.

    - **Arbejdstyp:** *Kvalitetskontrol*
    - **Arbejdsklasse-id:** *Indkøb*
    - **Skabelonnavn for kvalitetskontrol:** *Dock check*

        Vælg det entydige id for arbejdsklassen. Du bruger denne værdi til at konfigurere menupunkterne på mobilenheden og de typer arbejde, som disse menupunkter kan behandle.

1. Vælg **Gem** i handlingsruden for at gemme arbejdet indtil videre.

    Du modtager en meddelelse med oplysningen "Ugyldig - Kvalitetskontrol skal følge lige efter et pluk". Derfor skal du ændre **Linjenummer**-værdien for den linje, du lige har tilføjet.

1. Udfør følgende trin for at ændre **Linjenummer**-værdien for den nye linje:

    1. Vælg den linje, hvor feltet **Arbejdstype** i sektionen **Arbejdsskabelondetaljer** er angivet til *Kvalitetskontrol*.
    2. Vælg knappen **Flyt op** eller **Flyt ned** for at flytte *Kvalitetskontrol*-linjen, så den er efter *Pluk*-linjen.

1. Vælg **Gem** i handlingsruden.

#### <a name="quality-in-quality-check"></a>Kvalitet i kvalitetskontrol

Derefter skal du oprette en arbejdsskabelon til kvalitetskontrollen.

1. I overskriften på siden **Arbejdsskabeloner** skal du ændre værdien af feltet **Arbejdsordretype** til *Kvalitet i kvalitetskontrol*.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret i sektionen **Oversigt**.
1. Angiv følgende værdier i den nye række:

    - **Arbejdsskabelon:** *51 Kvalitetskontrol*

        Angiv et navn til skabelonen.

    - **Beskrivelse af arbejdsskabelon:** *51 Kvalitetskontrol*

1. Vælg **Gem** i handlingsruden for at gøre sektionen **Arbejdsskabelondetaljer** tilgængelig.
1. Mens den nye skabelon stadig er markeret i sektionen **Oversigt**, skal du vælge **Ny** i sektionen **Arbejdsskabelondetaljer** for at føje en række til gitteret der.
1. Angiv følgende værdier i den nye række:

    - **Arbejdstype:** *Pluk*
    - **Arbejdsklasse-id:** *QC Check*

        Vælg navnet på den [arbejdsklasse](#work-class), du oprettede tidligere til kvalitetskontrolarbejdet.

1. Vælg **Ny** igen i sektionen **Arbejdsskabelondetaljer** for at tilføje endnu en række.
1. Angiv følgende værdier i den nye række:

    - **Arbejdstype:** *Læg på lager*
    - **Arbejdsklasse-id:** *QC Check*

        Vælg navnet på den [arbejdsklasse](#work-class), du oprettede tidligere til kvalitetskontrolarbejdet.

1. Vælg **Gem** i handlingsruden.

Yderligere oplysninger om arbejdsskabeloner finder du under [Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver](control-warehouse-location-directives.md)

### <a name="location-directive--quality-failures"></a>Lokationsvejledning – Kvalitetsfejl

Lokationsvejledninger er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser. I f.eks. en salgsordretransaktion bestemmer en lokationsvejledning , hvor varerne plukkes, og hvor de plukkede varer skal lægges på lager. Du skal konfigurere en lokationsvejledningsregel for at definere, hvordan mislykkede kvalitetskontroller skal håndteres.

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I ruden til venstre skal du angive feltet **Arbejdsordretype** til *Indkøbsordrer* for at arbejde med lokationsvejledninger af den pågældende type.
1. Vælg **Ny** i handlingsruden for at oprette en lokationsvejledning til kvalitetskontrol.
1. Angiv følgende værdier i overskriften:

    - **Løbenummer:** Accepter standardværdien.
    - **Navn:** *51 til kvalitet*

1. I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier. Acceptér standardværdierne for alle de andre felter.

    - **Arbejdstype:** *Læg på lager*
    - **Lokation:** *5*
    - **Lagersted:** *51*

1. Vælg **Gem** i handlingsruden for at gemme vejledningen og gøre oversigtspanelet **Linjer** tilgængeligt.
1. Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje. Acceptér standardværdierne for alle de andre felter.

    - **Fra antal:** *1*
    - **Til antal:** *1000000*

1. Vælg **Gem** i handlingsruden for at gemme den nye linje og gøre oversigtspanelet **Handlinger for lokationsvejledninger** tilgængeligt.
1. Mens den nye linje stadig er valgt i oversigtspanelet **Linjer**, skal du vælge **Ny** i oversigtspanelet **Handlinger for lokationsvejledninger** for at føje en række til gitteret der, så du kan oprette en handling for linjen.
1. Angiv feltet **Navn** til *Kvalitet* i den nye række. Acceptér standardværdierne for alle de andre felter.
1. Vælg **Gem** i handlingsruden for at gøre knappen **Rediger forespørgsel** tilgængelig i oversigtspanelet **Handlinger i lokationsvejledning**.
1. Selvom den linje, du lige har tilføjet, stadig er valgt i oversigtspanelet **Handlinger for lokationsvejledninger**, skal du vælge **Rediger forespørgsel** for at åbne en dialogboks, hvor du kan redigere forespørgslen for handlingen.
1. Gå til fanen **Interval**, og vælg **Tilføj** for at føje en række til forespørgslen.
1. Angiv følgende værdier i den nye række:

    - **Tabel:** *Lokationer*
    - **Afledt tabel:** *Lokationer*
    - **Felt:** *Lokation*
    - **Kriterier:** *QMS*

    Lokationen *QMS* er en lagerlokation til kvalitet.

1. Vælg **OK** for at lukke dialogboksen.
1. Nu skal du ændre rækkefølgen af de eksisterende lokationsvejledninger for lagersted *51*. Gem den nye lokationsvejledning *51 til kvalitet*, opdater siden, og vælg lokationsvejledningen på listen. Brug derefter knapperne **Flyt op** og **Flyt ned** i handlingsruden til at placere lokationsvejledningen for lagersted *51* i følgende rækkefølge. (Før du vælger **Flyt op** eller **Flyt ned**, skal du vælge en lokationsvejledning på listen).

    1. 51 til kvalitet
    2. 51 PO Direct
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Menupunkter i mobilenhed

Konfigurere et menupunkt, så mobilenheder kan udføre funktionen **Kvalitetskontrol**.

#### <a name="purchase-putaway"></a>Læg indkøb på lager

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg menupunktet **Læg indkøb på lager** på listen.
1. Vælg **Rediger** i handlingsruden.
1. I sektionen **Arbejdsklasser** skal du vælge **Ny** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Arbejdsklasse-id:** *QC Check*

        Angiv navnet på den [arbejdsklasse](#work-class), du oprettede tidligere til kvalitetskontrolarbejdet.

    - **Arbejdsordretype:** *Kvalitet i kvalitetskontrol*

1. Vælg **Gem** i handlingsruden.

#### <a name="purchase-order-line-receiving"></a>Indkøbsordrelinje til modtagelse

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Navn på menupunkt:** *Modtagelse af indkøbsordrelinje*
    - **Titel:** *Modtagelse af indkøbsordrelinje*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Nej*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier. Acceptér standardværdierne for alle de andre felter.

    - **Arbejdsoprettelsesproces:** *Modtagelse og læg på lager for ordrelinje*
    - **Generer nummerplade:** *Ja*
    - **Arbejdsskabelon:** *51 indkøbsordremodtagelse*

1. Vælg **Gem** i handlingsruden.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Føje menupunktet til en mobilenhedsmenu

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg menuen **Indgående** i venstre rude.
1. Vælg **Rediger** i handlingsruden.
1. I kolonnen **Tilgængelig menuer og menupunkter** skal vælge menupunktet **Modtagelse af indkøbsordrelinje**.
1. Vælg den højre piletast for at flytte **Modtagelse af indkøbsordrelinje** til kolonnen **Menustruktur**.
1. Vælg **Modtagelse af indkøbsordrelinje** i kolonnen **Menustruktur**, og vælg derefter pil op eller pil ned for at flytte menupunktet til den ønskede placering i mobilenhedsmenuen.
1. Vælg **Gem** i handlingsruden.

## <a name="example-scenario"></a><a name="example-scenario"></a>Eksempelscenario

Når du har gjort alle de tidligere nævnte eksempeldata tilgængelige og konfigureret dem, kan du arbejde gennem dette scenario for at afprøve funktionen *Kvalitetskontrol*. De værdier, der vises i dette scenarie, forudsætter, at du arbejder med standarddemodataene, at du har valgt **USMF** som juridisk enhed, og at du har forberedt de eksempelposter, der er beskrevet tidligere i dette emne. Dette scenario fungerer også som et eksempel, der viser, hvordan funktionen kan bruges i en produktionsopsætning.

### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:

    - **Kreditorkonto:** *104*
    - **Lagersted:** *51*

1. Vælg **OK** for at åbne den nye indkøbsordre og lukke dialogboksen.
1. I oversigtspanelet **Indkøbsordrelinjer** indeholder gitteret en ny tom linje. Angiv følgende værdier på denne linje:

    - **Varenummer:** *M9203*
    - **Antal:** *3*
    - **Enhed:** *PL*

1. Vælg **Gem** i handlingsruden.

### <a name="process-quality-check-receiving"></a>Behandle kvalitetskontrol ved modtagelse

Når indkøbsordren er blevet oprettet, kan den modtages ved hjælp af menupunktet **Modtagelse af indkøbsordrelinje** og funktionaliteten af *Kvalitetskontrol*.

#### <a name="receive-pallet-1"></a>Modtage palle 1

1. Log på mobilappen Lokationsstyring som en bruger for lagersted *51*. (Angiv *51* som bruger-id og *1* som adgangskode).
1. Gå til **Indgående \> Modtagelse af indkøbsordrelinje**.
1. Angiv dit indkøbsordrenummer i feltet **IO-num**.
1. Bekræft indkøbsordrens nummer.
1. Angiv linjenummeret fra den indkøbsordre, der modtages, i feltet **LINJENUM**. Da ordren kun har én linje i dette scenario, skal du skrive *1* i feltet **LINJENUM** for hvert modtagelsestrin.
1. Bekræft linjenummeret.
1. Angiv det antal, der skal modtages, i feltet **Antal**. Da indkøbsordren er for tre paller (*PL*) i dette scenario, og der er tre modtagelsestrin, skal du skrive *1* i feltet **Antal** for hvert modtagelsestrin.
1. Bekræft antallet.

    Siden **Kvalitetskontrol** vises uden postfelter. Den har kun bekræftelsesknappen (markering) nederst og menuknappen (**≡**) øverst. (Menuknappen kaldes undertiden hamburgeren eller hamburgerknappen). Når pallen passerer kvalitetskontrollen, bekræfter brugeren blot kvalitetskontrollen på siden **Kvalitetskontrol**.

    ![Siden Kvalitetskontrol.](media/quality-check.png "Siden Kvalitetskontrol")

1. Vælg bekræftelsesknappen for at bestå kvalitetskontrollen af palle 1 fra linje 1.

    Siden **Indkøbsordrer: læg på lager** viser oplysninger om læg på lager-arbejdet:

    - **LOK:** Systemet har fastlagt lokationen

        Denne lokation er den angivne læg på lager-lokation for modtagelse af indkøbsordrer.

    - **LP:** Det systemgenererede id
    - **Vare:** *M9203*
    - **Antal:** *1 PL: 100 hver*

    Varebeskrivelsen vises også.

1. Bekræft læg på lager-arbejdet.

    På siden **Opgave** for modtagelse af indkøbsordrelinje vises meddelelsen "Arbejde fuldført". Feltet **LINJENUM** er tilgængeligt, så du kan begynde at modtage den næste palle.

#### <a name="receive-pallet-2"></a>Modtage palle 2

I dette scenario vil palle 2 blive afvist.

1. Angiv **1** i feltet *LINJENUM*, og bekræft linjenummeret.
1. Feltet **Antal** er nu tilgængeligt. Angiv *1*, og bekræft antallet.

    Siden **Kvalitetskontrol** vises. I forbindelse med denne modtagelse vil pallen blive afvist for kvalitet, og den vil blive placeret i *QMS*-kvalitetslokationen.

1. Vælg menuknappen (**≡**) øverst på siden, og vælg derefter **Afvis** i menuen.
1. På den **Opgave**-side, der vises, skal du angive **QMS** som den *Læg på lager*-lokation, hvor pallen skal sendes til yderligere inspektion.

    Siden **Kvalitet i kvalitetskontrol: læg på lager** viser oplysninger om læg på lager-arbejdet:

    - **LOK:** *QMS*

        Denne lokation er den angivne læg på lager-lokation for modtagelse af afvist kvalitet.

    - **LP:** Det systemgenererede id
    - **Vare:** *M9203*
    - **Antal:** *1 PL: 100 hver*

    Varebeskrivelsen vises også.

1. Bekræft læg på lager-arbejdet.

    På siden **Opgave** for modtagelse af indkøbsordrelinje vises meddelelsen "Arbejde fuldført". Feltet **LINJENUM** er tilgængeligt, så du kan begynde at modtage den næste palle.

Du har nu fuldført kvalitetskontrollen og oprettet en kvalitetsordre for den afviste palle. Hvis du vil se den ordre, der er oprettet, skal du gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.

Test af kvalitetsordre kan nu behandles. Kvalitetstesten beskrives ikke i dette emne.

Du kan finde flere oplysninger om kvalitetsstyring under [Oversigt over kvalitetsstyring](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Modtage palle 3

I dette scenario vil palle 3 blive accepteret.

1. Angiv **1** i feltet *LINJENUM*, og bekræft linjenummeret.
1. Feltet **Antal** er nu tilgængeligt. Angiv *1*, og bekræft antallet.

    Siden **Kvalitetskontrol** vises. I forbindelse med denne modtagelse vil pallen blive accepteret for kvalitet, og den vil blive placeret i lokationen for masselæg på lager.

1. Vælg bekræftelsesknappen for at bestå kvalitetskontrollen.

    Siden **Indkøbsordrer: læg på lager** viser oplysninger om læg på lager-arbejdet:

    - **LOK:** Systemet har fastlagt lokationen

        Denne lokation er den angivne læg på lager-lokation for modtagelse af indkøbsordrer.

    - **LP:** Det systemgenererede id
    - **Vare:** *M9203*
    - **Antal:** *1 PL: 100 hver*

    Varebeskrivelsen vises også.

1. Bekræft læg på lager-arbejdet.

    På siden **Opgave** for modtagelse af indkøbsordrelinje vises meddelelsen "Arbejde fuldført". Feltet **LINJENUM** er tilgængeligt, så du kan begynde at modtage den næste palle.

1. Vælg menuknappen (**≡**) øverst på siden, og vælg derefter **Annuller** i menuen for at gå tilbage til menuen.

Du kan nu lukke mobilappen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]