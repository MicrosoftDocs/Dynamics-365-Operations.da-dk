---
title: Konfigurere et miljø til evaluering af e-handel
description: Denne vejledning giver trinvise instruktioner til klargøring og konfiguration af dit Microsoft Dynamics 365 Commerce-prøveversionsmiljø.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771674"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>Konfigurere et miljø til evaluering af e-handel

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Denne vejledning giver trinvise instruktioner til klargøring og konfiguration af dit Microsoft Dynamics 365 Commerce-prøveversionsmiljø. Før du går i gang, anbefales det, at du som minimum skimmer dokumentationen for at få en ide om, hvad processen indebærer, og hvad vejledningen indeholder.

*Bemærk! Hvis du ikke har fået adgang til Microsoft Dynamics 365 Commerce-prøveversionen endnu, kan du anmode om adgang til den fra [Commerce-webstedet](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Resume
For at klargøre miljøet korrekt skal projektet oprettes med et specifikt produktnavn og en bestemt type. Miljøet og Retail Cloud Scale Unit har nogle specifikke parametre, du skal bruge for at starte klargøringen af e-handel senere. Instruktionerne i denne vejledning indeholder alle de trin, du skal udføre, og de parametre, du skal bruge.

Når klargøringen er fuldført, er der nogle få efterfølgende trin, du skal udføre for at forberede dit prøveversionsmiljø. Nogle trin er valgfrie, afhængigt af hvilke aspekter af systemet du vil evaluere. Hvis du senere skifter mening, kan du altid køre valgfrie trin senere.

Hvis du har spørgsmål til klargøringstrinnene, eller du oplever problemer, bedes du fortælle det til [Microsoft Dynamics 365 Commerce-prøveversionens Yammer-gruppe](https://aka.ms/Dynamics365CommercePreviewYammer). 

## <a name="prerequisites"></a>Forudsætninger
Følgende er forudsætningerne for klargøring af dit Dynamics 365-prøveversionsmiljø:
* Du har adgang til **Lifecycle Services-portalen (LCS)**
* Du er blevet **godkendt til Dynamics 365 Commerce-prøveversionsprogrammet**
* Du har de nødvendige rettigheder til at oprette et projekt til **Mulige førsalg** eller **Overflyt, opret løsninger, og lær at bruge**
* Du er medlem af rollen **Miljøadministrator** eller **Projektejer** i det projekt, hvor du skal klargøre miljøet
* Du har administratoradgang til dit Azure-abonnement eller kontakt til en abonnementsadministrator, der kan udføre de to trin, der kræver administratorrettigheder, på dine vegne
* Du har dit **AAD-lejer-id** tilgængeligt
* Du har oprettet en **AAD-sikkerhedsgruppe**, der skal bruges som **administratorgruppe til e-handelssystemer**, og du har dens id til rådighed
* Du har oprettet en **AAD-sikkerhedsgruppe**, der skal bruges som **redaktørgruppe for vurderinger og anmeldelser**, og du har dens id tilgængeligt (kan være samme SG som systemadministratorgruppen ovenfor)
## <a name="provisioning-preview-environment"></a>Klargøring af prøveversionsmiljø
Disse instruktioner dækker klargøring af et Microsoft Dynamics 365 Commerce-prøveversionsmiljø. Når du har gennemført disse trin, vil du have et prøveversionsmiljø, der er klar til at blive konfigureret. Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.

*Bemærk, at adgangen til prøveversionen er bundet til den LCS-konto og -organisation, du har angivet i prøveversionsprogrammet. Du skal bruge den samme konto til klargøring. Hvis du skal bruge en anden LCS-konto eller -lejer til prøveversionsmiljøet, skal du give os disse oplysninger. Kontaktoplysninger finder du i afsnittet "Yderligere ressourcer" nedenfor*.
### <a name="before-starting"></a>Før du starter
##### <a name="grant-access-to-e-commerce-applications"></a>Give adgang til e-handelsprogrammer

*Bemærk: **Den person, der logger på, skal være AAD-lejeradministrator**. Uden at fuldføre dette trin mislykkes resten af klargøringstrinnene*.

1. I dette trin skal du bruge dit **AAD-lejer-id**. Du skal godkende e-handelsprogrammer for at få adgang til dit Azure-abonnement. Den nemmeste måde at opnå dette på er at sammensætte en URL-adresse som denne:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Du skal ikke klikke på URL-adressen direkte**, men i stedet kopiere den og sætte den ind i din browser eller teksteditor og erstatte **\{AAD_TENANT_ID\}** med dit **AAD-lejer-id**, før du navigerer til URL-adressen.
3. Du får vist dialogboksen Microsoft AAD-logon, hvor du skal bekræfte, at du vil tildele "Dynamics 365 Commerce (prøveversion)" adgang til dit abonnement.
4. Du vil blive sendt til en side, der bekræfter, om handlingen lykkedes.

##### <a name="log-in-to-the-lcs"></a>Logge på LCS
1. Log på LCS-portalen: https://lcs.dynamics.com
1. Sørg for, at du er logget på med den samme LCS-konto, som du brugte til at anmode om adgang til prøveversionen.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Bekræfte, at prøveversionens funktioner er tilgængelige og aktiverede
1. Rul helt til højre på LCS-forsiden, og klik på feltet **Styring af prøveversionsfunktion**.
1. Rul ned til "Funktioner i private prøveversioner", og sørg for, at følgende funktioner er tilgængelige og aktiverede:
    1. **Evaluering af e-handel**
    1. **Programmiljøer til Commerce-prøveversion**
1. Hvis du ikke kan se disse funktioner på listen, bedes du kontakte os med din arbejdsmail, LCS-konto og oplysninger om lejer. Se **Yderligere ressourcer** nedenfor angående, hvordan du kontakter os.

![Feltet Styring af prøveversionsfunktion](./media/preview1.png)

![Funktioner i prøveversion](./media/preview2.png)
### <a name="create-project"></a>Projektoprettelse
##### <a name="creating-new-project"></a>Oprette et nyt projekt
1. Klik på **+** for at oprette et nyt projekt.
1. Hvis du er partner, skal du vælge **Overflyt, opret løsninger, og lær at bruge**.
1. Hvis du er kunde, skal du vælge **Mulige førsalg**.
1. Angiv et navn, en beskrivelse og en branche efter behov.
1. Som **Produktnavn** skal du vælge **Dynamics 365 Retail**.
1. Som **Produktversion** skal du vælge **Dynamics 365 Retail**.
1. Som **Metode** skal du vælge **Dynamics Retail-implementeringsmetode**.
1. Du kan importere roller og brugere fra et eksisterende projekt, hvis det ønskes.
1. Klik på **Opret**.
1. Du bliver sendt til projektvisningen.
##### <a name="add-azure-connector"></a>Tilføje Azure-connector
1. Hvis du er partner, skal du klikke på **Projektindstillinger** i værktøjsfeltet længst til højre.
1. Hvis du er kunde, skal du vælge **Projektindstillinger** i den øverste menu.
1. Vælg **Azure-connectorer**.
1. Klik på **+ Tilføj** for at tilføje Azure-connector.
1. Skriv et navn.
1. Angiv dit **Azure-abonnements-id**.
1. Aktivér **Konfigurer til at bruge Azure Resource Manager (ARM)**.
1. Kontrollér, at **Azure-abonnement AAD-lejerdomæne (eller id)** er korrekt. Kontakt om nødvendigt din Azure-abonnementsadministrator.
1. Klik på **Næste**.
1. Følg instruktionerne på skærmen for at give det eller de nødvendige programmer adgang til dit abonnement. Kontakt om nødvendigt din Azure-abonnementsadministrator:
    1. Log på Azure-portalen: https://portal.azure.com/
    1. Sørg for, at du har valgt det korrekte bibliotek.
    1. Klik på **Abonnementer** i menuen til venstre.
    1. Find det korrekte abonnement på listen, og vælg det. Brug søgning, hvis det er nødvendigt.
    1. Vælg **Adgangsbegrænsning (IAM)** i menuen.
    1. Klik på **Tilføj** under **Tilføj en rolletildeling** i højre side. Ruden **Tilføj rolletildeling** åbnes.
    1. Vælg **Bidragyder** som **Rolle**.
    1. For **Tildel adgangsrettigheder til** skal du beholde **Azure AD-bruger, -gruppe eller -tjenesteprincipal**.
    1. Under **Vælg** skal du angive **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Vælg **Dynamics-installationstjenester [wsfed-enabled]** på listen.
    1. Klik på **Gem**.
1. Klik på **Næste**.
1. Følg instruktionerne på skærmen for at give det eller de nødvendige programmer adgang til dit abonnement. Kontakt om nødvendigt din Azure-abonnementsadministrator.
1. Klik på **Næste**.
1. Som **Azure-region** skal du vælge enten **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.
1. Klik på **Tilknyt**.
1. Din Azure-connector bør blive vist på listen.
### <a name="import-extension"></a>Importere udvidelse
1. Gå tilbage til projektets forside ved at klikke på projektnavnet øverst.
1. Hvis du er partner, skal du klikke på **Aktivbibliotek** i værktøjsfeltet længst til højre.
1. Hvis du er kunde, skal du vælge **Aktivbibliotek** i den øverste menu.
1. Vælg **Installerbar softwarepakke** på listen til venstre.
1. Klik på **Importér** i handlingsruden.
1. Vælg **Demobasisudvidelse til Commerce-prøveversion** på listen over aktiver under **Delt aktivbibliotek**.
1. Klik på **Pluk**.
1. Du kommer tilbage til aktivbiblioteket, og du bør kunne se udvidelsen på listen.

![Oprettelse af projekt – versioner](./media/import.png)
### <a name="deploy-environment"></a>Installer miljø

*Bemærk: Det er muligt, at trin 6, 7 og/eller 8 ikke vises, da skærmene med enkeltvalg springes over. Når du arbejder i **Miljøparameter**-visningen, skal du bekræfte, at du har teksten "Dynamics 365 Commerce (Prøveversion) – demo (10.0.6 med Platform update 30)" direkte over feltet **Miljønavn**. Se skærmbilledet nedenfor.*

1. Vælg **Skybaserede miljøer** i den øverste menu.
1. Klik på **+ Tilføj** for at tilføje et miljø.
1. Vælg **10.0.6** som **Programversion**.
1. Vælg **Platform Update 30** som **Platformsversion**.
1. Klik på **Næste**.
1. Vælg **Demo** som miljøtopologi.
1. Vælg **Dynamics 365 Commerce (Prøveversion) – demo** som miljøtopologi.
1. Hvis du har konfigureret en enkelt Azure-connector tidligere, bruges den til dette miljø. Hvis du har konfigureret flere Azure-connectorer, har du mulighed for at vælge, hvilken connector du vil bruge: **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2** (anbefales til den bedste totale ydeevne).
1. Angiv et **Miljønavn**.
1. Juster VM-størrelsen efter behov. (Vi anbefaler VM SKU **D13 v2**).
1. Lad **Avancerede indstillinger** være, som de er.
1. Når du har gennemset pris- og licensbetingelserne på skærmen, skal du markere afkrydsningsfeltet for at angive aftalesamtykke.
1. Klik på **Næste**.
1. Klik på **Installer** på skærmbilledet til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.
1. Du vender tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.
1. Det miljø, du har anmodet om, vises i køen og derefter som under installation. Det vil tage noget tid at fuldføre alle miljøarbejdsprocesserne, så kom tilbage efter nogle timer (ca. 6 – 9 timer).
1. Før du fortsætter, skal du kontrollere, at din miljøstatus **Installeret**.

![Oprettelse af projekt – versioner](./media/project1.png)

![Oprettelse af projekt – topologi 1](./media/project2.png)

![Oprettelse af projekt – topologi 2](./media/project3.png)

![Oprettelse af projekt – miljøparametre](./media/project4.png)
### <a name="initialize-rcsu"></a>Initialisere RCSU
1. Vælg dit miljø på listen i visningen **Skybaserede miljøer**.
1. Klik på **Alle detaljer** i miljøvisningen i højre side af skærmbilledet. Visningen med miljødetaljer åbnes.
1. Klik på **Administrer** under **Miljøfunktioner**.
1. Klik på **Initialiser** under fanen **Detail**. RCSU-initialiseringsparametrene vil blive vist.
1. Som **Område** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.
1. I forbindelse med **Version** skal du først vælge **Angiv en version** på rullelisten og derefter angive **9.16.19262.5** i det tekstfelt, der vises nedenfor. *Bemærk: Sørg for at **angive den nøjagtige version** her for at undgå at skulle opdatere RCSU senere til den korrekte version.*
1. Aktivér **Anvend udvidelse**.
1. Vælg **Demobasisudvidelse til Commerce-prøveversion** på listen over udvidelser.
1. Klik på **Initialiser**.
1. Klik på **Ja** på skærmbilledet til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.
1. Du vender tilbage til visningen **Detailstyring**, og fanen **Detail** er aktiveret. Din RCSU er sat i kø til klargøring.
1. Vent, indtil din RCSU-status er **Succes**, før du fortsætter (tager ca. 2-5 timer).
### <a name="initialize-e-commerce"></a>Initialisere e-handel
1. Skift til fanen **e-handel (prøveversion)**.
1. Klik på **Konfiguration**, når du har gennemset samtykket til prøveversionen.
1. Angiv et navn til **e-handels-lejernavn**. Bemærk dog, at dette vil være synligt i nogle af URL-adresserne, der peger på e-handelsforekomsten.
1. For **Retail Cloud Scale Unit-navn** skal du vælge din RCSU på listen (listen bør kun have én indstilling).
1. **Geografi for e-handel** udfyldes automatisk og kan ikke ændres.
1. Klik på **Næste** for at fortsætte.
1. Angiv et gyldigt domæne (f.eks. www.fabrikam.com) for **Understøttede værtsnavne**.
1. I **AaD-sikkerhedsgruppe for systemadministrator** skal du angive det AAD SG-id, du vil bruge som administratorgruppe i e-handelssystemet.
1. I **AAA-sikkerhedsgruppen for redaktør af vurderinger og anmeldelser** skal du angive det AAD SG-id, du vil bruge som redaktørgruppe for vurderinger og anmeldelser.
1. Lad **B2C**-værdierne være tomme (7 felter, der starter med B2C).
1. Bevar **Aktivér vurderinger og anmeldelser** aktiveret.
1. Klik på **Initialiser**.
1. Du vender tilbage til visningen **Detailstyring**, og fanen **e-handel (prøveversion)** er aktiveret. Din initialisering af e-handel er startet.
1. Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-handel er **Initialisering blev gennemført**.
1. Under **Links** nederst til højre.
    * Notér dig linket **websted for e-handel**. Dette er linket til roden af C2-webstedet.
    * Notér dig linket **Administrationsværktøj til websted for e-handel**. Dette er linket til administrationsværktøjet for webstedet (C1-oprettelsesværktøj).
## <a name="post-provisioning-steps"></a>Trin efter klargøring
På dette stadie er miljøet blevet klargjort fra ende til anden, men der er stadig konfigurationstrin, der skal udføres, før du kan begynde at evaluere miljøet.
### <a name="before-starting"></a>Før du starter
1. Vælg **Skybaserede miljøer** i den øverste menu.
1. Vælg dit miljø på listen.
1. Klik på **Alle detaljer** i miljøoplysningerne til højre.
1. Klik på **Logon** for at åbne en menu, og vælg **Log på miljøet**.

Kontrollér, at den juridiske enhed **USRT** er valgt (øverste højre hjørne).

### <a name="configure-pos"></a>Konfigurer POS
##### <a name="associate-worker-with-your-identity"></a>Tilknytte arbejder med din identitet
1. I menuen til venstre kan du gå til **Moduler > Detail > Medarbejdere > Arbejdere**.
1. Find og vælg posten **000713 - Andrew Collette** på listen.
1. Klik på **Detail** i handlingsruden.
1. Klik på **Tilknyt eksisterende identitet**.
1. Skriv din mailadresse i feltet **Mail** (til højre for **Søg ved hjælp af mail**).
1. Klik på **Søg**.
1. Vælg posten med dit navn.
1. Klik på **OK**.
1. Klik på **Gem**.
##### <a name="activate-cloud-pos"></a>Aktiverere sky POS
1. Log på LCS-portalen.
1. Naviger til dit projekt.
1. Vælg **Skybaserede miljøer** i den øverste menu.
1. Vælg dit miljø på listen.
1. Klik på **Alle detaljer** i miljøoplysningerne til højre.
1. Klik på **Logon** for at åbne en menu, og vælg **Log på Cloud POS**, så POS skulle blive indlæst.
1. Klik på **Næste**.
1. Log på med din AAD-konto.
1. Vælg **San Francisco** under **Butiksnavn**.
1. Klik på **Næste**.
1. Vælg **SANFRAN-1** under **Kasseapparat og enhed**.
1. Klik på **Aktiver**.
1. Du skulle nu blive logget af og komme til skærmen POS-logon.
1. Du kan nu logge på Cloud POS-oplevelsen med operatør-id **000713** og adgangskoden **123**.
### <a name="site-setup"></a>Webstedopsætning
1. Log på **administrationsværktøjet for webstedet** ved hjælp af den URL-adresse, du skrev ned tidligere.
1. Klik på webstedet **Fabrikam** for at åbne dialogboksen Webstedopsætning.
1. Som domæne skal du vælge det domæne, du tidligere har angivet under initialiseringen af e-handel.
1. Som standardkanal skal du vælge **Udvidet Fabrikam-onlinebutik**. *Bemærk: Sørg for at vælge den **udvidede** onlinebutik*.
1. Vælg **en-us** som standardsprog.
1. Lad **stien** være, som den er.
1. Klik på **OK**.
1. Du vil blive sendt til listen over sider på webstedet.
### <a name="enable-jobs"></a>Aktivere job
1. Log på miljøet (hovedkontor).
1. Brug menuen til venstre til at gå til **Detail > Forespørgsler og rapporter > Batchjob**.
1. For hvert af de følgende job skal du udføre disse trin:
    * **Behandling af e-mail-besked om detailordre**.
    * **Produkttilgængelighed**.
    * **P-0001**.
    * **Synkroniser ordrejob**.
1. Brug Quick Filter til at søge efter jobbet ved hjælp af dets navn (vises ovenfor).
1. Hvis status for jobbet er **Tilbagehold**, skal du udføre følgende trin:
    1. Vælg posten.
    1. Åbn **Batchjob**-båndet i handlingsruden, og klik på **Skift status**.
    1. Vælg **Venter**, og klik på **OK**.
### <a name="run-full-data-sync"></a>Kør fuld datasynkronisering
1. Brug menuen til venstre, og gå til **Moduler > Detail > Konfiguration af hovedkontor > Retail planlægger > Kanaldatabase**.
1. **Standard**-kanalen er valgt på listen til venstre. *Vælg den anden tilgængelige kanal (navnet **scXXXXXXXXX**)*.
1. Klik på **Fuld datasynkronisering** i handlingsruden.
1. Angiv **9999** som distributionsplanen.
1. Klik på **OK**.
1. Klik på **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Når du er færdig med disse trin, kan du begynde at evaluere dit prøveversionsmiljø!
Brug URL-adressen til **Administrationsværktøj til websted for e-handel** til at navigere til C1-oprettelsesoplevelsen og URL-adressen til **webstedet for e-handel** til at navigere til C2-webstedsoplevelsen.

## <a name="additional-resources"></a>Yderligere ressourcer
### <a name="how-to-find-your-aad-tenant-id"></a>Sådan finder du dit AAD-lejer-id
AAD-lejer-id er et GUID og ser ud som dette eksempel: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Fra Azure-portal
1. Log på Azure-portalen: https://portal.azure.com/
1. Sørg for, at du har valgt det korrekte bibliotek.
1. Klik på **Azure Active Directory** i menuen til venstre.
1. Vælg **Egenskaber** under **Administrer**.
1. AAD-lejer-id vises under **Mappe-id**.
##### <a name="from-openid-connect-metadata"></a>Fra OpenID Connect-metadata
Opret **OpenID URL-adresse** ved at erstatte **\{YOUR_DOMAIN\}** med dit domæne, f.eks. bliver microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration til https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Naviger til **OpenID-URL-adressen** med dit domæne i.
1. AAD-lejer-id kan ses i flere egenskabsværdier.
1. Find **authorization_endpoint**, og udtræk GUID'et direkte efter **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Sådan finder du id'et for din AAD-sikkerhedsgruppe
AAD-sikkerhedsgruppe-id er et GUID og ser ud som dette eksempel: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

I dette trin antages det, at brugeren er medlem af den gruppe, som brugeren forsøger at finde id'et for.
1. Gå til Graph-tester: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Klik på **Log på med Microsoft**, og log på ved hjælp af dine legitimationsoplysninger.
1. Når du er logget på, skal du klikke på **Vis flere eksempler** fra venstre.
1. Aktivér **Grupper** fra højre rude.
1. Luk den højre rude.
1. Klik på **alle grupper, som jeg tilhører**.
1. Find din gruppe i tekstfeltet **Vis svar**.
1. Sikkerhedsgruppe-id'et er angivet under **egenskabs-id**.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Teste oplysninger om kreditkort for at udføre testindkøb
Hvis du vil udføre testtransaktioner på webstedet, kan du bruge disse testkreditkortoplysninger:

Kortnummer: 4111-1111-1111-1111, udløbsdato: 10/20, CVV: 737

*Bemærk: Du bør ikke forsøge at bruge faktiske oplysninger om kreditkort på testwebstedet under nogen omstændigheder!*
### <a name="useful-links"></a>Nyttige links
* [LCS (Lifecycle Services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure-portal](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)
* [Hjælp-ressourcer til Dynamics 365 Retail](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Understøttelse af Microsoft Dynamics 365 Commerce-prøveversion
Hvis der opstår problemer under udførelse af klargøringstrinnene, kan du gå til [Microsoft Dynamics 365 Commerce-prøveversionens Yammer-gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) for at få hjælp. 

Hvis du har problemer med at få adgang til Yammer-gruppen, kan du også kontakte os via e-mail på **Dynamics365Commerce@microsoft.com**. Denne mailadresse overvåges ikke aktivt, så du kan forvente forsinkelse.
***
## <a name="prerequisites-for-optional-features"></a>Forudsætninger for valgfrie funktioner
Hvis du vil evaluere transaktionsfunktionerne for mail, skal følgende forudsætninger være opfyldt:
* Du har en tilgængelig mailserver (SMTP-server), som kan bruges fra Azure-abonnementet, hvor du klargør prøveversionsmiljøet.
* Du har serverens FQDN/IP, SMTP-portnummer og godkendelsesdetaljer ved hånden.

Hvis du vil evaluere funktioner til administration af digitale aktiver, specielt indtag af nye omni-kanalbilleder, skal følgende forudsætninger være opfyldt:
* Du skal have dit **CMS-lejernavn** til rådighed. Du kan finde oplysninger om at finde dette navn nedenfor.
### <a name="configure-image-backend-optional"></a>Konfigurere back end-billede (valgfrit)
##### <a name="finding-your-media-base-url"></a>Søgning efter din mediebases URL-adresse
*Bemærk: Før du kan fuldføre dette trin, skal du fuldføre **opsætningen af webstedet**.*
1. Log på administrationsværktøjet for webstedet ved hjælp af den URL-adresse, du skrev ned tidligere.
1. Åbn webstedet **Fabrikam**.
1. Vælg **Aktiver** i menuen til venstre.
1. Vælg et enkelt billedaktiv.
1. Find **Offentlig URL-adresse** fra egenskabsfremviseren til højre. Den indeholder en URL-adresse.
    * Eksempel på URL-adresse: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Erstat den sidste identifikator i URL-adressen (MA1nQC i URL-adressen ovenfor) med følgende streng: **search?fileName=**
    * Eksempel på URL-adresse efter erstatning: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Dette er din **mediebases URL-adresse**.
##### <a name="updating-the-media-base-url"></a>Opdatering af URL-adressen til mediebasen
1. Log på miljøet (hovedkontor).
1. Brug menuen til venstre, og gå til **Moduler > Detail > Konfiguration af kanal > Kanalprofiler**.
1. Klik på **Rediger**.
1. I **profilegenskaberne** skal du erstatte egenskabsværdien for **URL-basisadresse til medieserver** med den **URL-basisadresse til medie**, du har oprettet tidligere.
1. Vælg den anden kanal på listen til venstre under **Standard**-kanal.
1. Klik på **+ Tilføj** under **Profilegenskaber**.
1. For den egenskab, der blev tilføjet, skal du vælge **URL-basisadresse til medieserver** som egenskabsnøgle, og som egenskabsværdi skal du angive den **URL-basisadresse til medie**, du oprettede tidligere
1. Klik på **Gem**.

### <a name="configure-email-server-optional"></a>Konfigurere mailserver (valgfrit)
Bemærk, at den SMTP-server eller mailtjeneste, du angiver her, skal være tilgængelig fra det Azure-abonnement, du bruger til miljøet.
1. Log på miljøet (hovedkontor).
1. Brug menuen til venstre, og gå til **Moduler > Detail > Konfiguration af hovedkontor > Parameters > E-mail-parametre**.
1. Klik på fanen **SMTP-indstillinger**.
1. Angiv FQDN eller IP-adressen på SMTP-serveren eller e-mail-tjenesten i feltet **Udgående mailserver**.
1. Angiv portnummeret (standard er 25, når der ikke bruges SSL) i feltet **SMTP-portnummer**.
1. Skriv en værdi (hvis godkendelse er påkrævet) i feltet **Brugernavn**.
1. Skriv en værdi (hvis godkendelse er påkrævet) i feltet **Adgangskode**.
1. Klik på **Gem**.
1. Klik på **Opdater**.
1. Klik på fanen **Testmail**.
1. Vælg **SMTP** i feltet Mailudbyder.
1. Angiv den mailadresse, som testmailen skal leveres til, i feltet **Send til**.
1. Klik på **Send testmail**.
### <a name="configure-email-templates-optional"></a>Konfigurere mailskabeloner (valgfrit)
Mailskabelonen for hver transaktionshændelse, du vil sende mails for, skal opdateres med en gyldig afsendermailadresse.
1. Brug menuen til venstre, og gå til **Moduler > Organisationsadministration > Konfiguration > Parameters > Skabelon til organisationsmail**.
1. Klik på **Vis liste**.
1. For hver af skabelonerne på listen:
    1. Skriv afsenderens mailadresse for denne mailskabelon i feltet **Afsenders e-mailadresse**.
    1. (Valgfrit) Skriv et navn, der skal bruges som afsender for denne mailskabelon, i feltet **Afsendernavn**.
1. Klik på **Gem**.
### <a name="customizing-email-templates-optional"></a>Tilpasning af mailskabeloner (valgfrit)
Du kan tilpasse mailskabelonerne, så de bruger forskellige billeder, eller opdatere links i skabelonen for at oprette et link tilbage til dit prøveversionsmiljø. Nedenstående trin forklarer, hvordan du henter standardskabelonerne, tilpasser dem og opdaterer skabelonerne i systemet.
1. Brug en browser til at downloade [Microsoft Dynamics 365 Commerce-prøveversionens .zip-fil med standardmailskabeloner](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), som indeholder følgende HTML-dokumenter, til den lokale computer.
    1. Skabelon til ordrebekræftelse
    1. Skabelon til udstedelse af gavekort
    1. Skabelon til ny ordre
    1. Skabelon til pakkeordre
    1. Skabelon til plukordre
1. Tilpas skabelonerne ved hjælp af en tekst- eller HTML-editor. Du kan se en liste over understøttede tokens nedenfor.
1. Log på miljøet (hovedkontor).
1. Brug menuen til venstre, og gå til **Moduler > Detail > Konfiguration af hovedkontor > Parameters > Skabelon til organisationsmail**.
1. Udvid listen til venstre for at få vist alle skabelonerne.
1. Udfør følgende trin for hver af de skabeloner, du vil tilpasse:
    1. Vælg skabelonen på listen.
    1. Vælg den relevante sprogversion på listen under **E-mailbeskedens indhold** (standarden er **en-us**).
    1. Klik på **Rediger** under **E-mailbeskedens indhold**. Ruden **Overfør mailskabelon** åbnes.
    1. Klik på **Gennemse**, og find HTML-filen med det tilpassede indhold.
    1. Klik på **Overfør**. Din skabelon overføres til systemet, og der vises et eksempel.
    1. Klik på **OK**.
    1. (Valgfrit) Tilpas egenskaben **Emne** for skabelonen.
    1. Klik på **Gem**.

#### <a name="supported-tokens-in-the-email-template"></a>Understøttede tokens i mailskabelonen
Disse tokens erstattes på mailgengivelsestidspunktet med de faktiske værdier, der gælder for kunden og dennes ordre.

**Salgsordre** - Følgende tokens gælder for den overordnede salgsordre.

|Navn på token|Tokenet|
|---|---|
|Ordrenummer|%salesid%|
|Debitors navn|%customername%|
|Leveringsadresse|%deliveryaddress%|
|Faktureringsadresse|%customeraddress%|
|Bestillingsdato|%shipdate%|
|Leveringstilstand|%modeofdelivery%|
|Diskontering|%discount%|
|Moms|%tax%|
|Ordretotal|%total%|

**Salgslinje** - Der udfyldes følgende tokens for hvert produkt i ordren.

*Bemærk : Placer **Produktlist - start**- og **Produktliste - slut**-tokens i begyndelsen og slutningen af den HTML-blok, der gentages for hvert produkt.*

|Navn på token|Tokenet|
|---|---|
|Produktliste - start|\<!--%tablebegin.salesline% -->|
|Produktliste - slut|\<!--%tableend.salesline%-->|
|Produktnavn|%lineproductname%|
|Beskrivelse|%lineproductdescription%|
|Mængde|%linequantity%|
|Linjeprisenhed|%lineprice% (verify)|
|linjevaretotal|%linenetamount%|
|linjerabat|%linediscount%|
|Afsendelsesdato|%lineshipdate%|
|Indkøbsmetode|%linedeliverymode%|
|leveringsadresse|%linedeliveryaddress%|
|Salgsenhed for linjen|%lineunit%|

