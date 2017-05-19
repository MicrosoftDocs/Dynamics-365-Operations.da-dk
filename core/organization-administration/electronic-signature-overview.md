---
title: Oversigt over elektroniske signaturer
description: Denne artikel giver et overblik over elektroniske signaturer og beskriver, hvordan de kan bruges i Microsoft Dynamics 365 for Operations.
author: maertenm
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: fdb52addb95aa3a3365d84a38cbd22bacc41779b
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="electronic-signature-overview"></a>Oversigt over elektroniske signaturer

[!include[banner](../includes/banner.md)]


Denne artikel giver et overblik over elektroniske signaturer og beskriver, hvordan de kan bruges i Microsoft Dynamics 365 for Operations.

<a name="what-is-an-electronic-signature"></a>Hvad er en elektronisk signatur?
--------------------------------

En elektronisk signatur bekræfter identiteten på en person, som skal starte eller godkende en computerproces. I nogle brancher er en elektronisk signatur lige så juridisk bindende som en håndskrevet signatur. Elektroniske signaturer er et lovmæssigt krav i adskillige regulerede brancher som f.eks. lægemiddelsektoren, fødevareindustrien samt luftfart og forsvar. De er også nødvendigt for at overholde forskrifterne i 21 CFR afsnit 11, der er udstedt af det amerikanske fødevareministerium FDA (Food and Drug Administration) i USA. **Bemærk:** En elektronisk signatur er i sig selv ikke det samme som en digital signatur. En elektronisk signatur er blot en erstatning for en håndskrevet signatur, mens en digital signatur omfatter yderligere sikkerhedsmæssige foranstaltninger. En digital signatur kan bidrage til at identificere, om en anden bruger eller proces har forfalsket dataene. En digital signatur kan også bekræftes, og denne bekræftelse kan ikke gendrives af ejeren af det certifikat, som blev brugt til at signere dataene. Som beskrevet nedenfor har elektroniske signaturer i Microsoft Dynamics 365 for Operations en indbygget funktion til digital signatur.

## <a name="electronic-signatures-in-dynamics-365-for-operations"></a>Elektroniske signaturer i Microsoft Dynamics 365 for Operations
I Microsoft Dynamics 365 for Operations kan du bruge elektroniske signaturer til kritiske forretningsprocesser. Nogle processer har indbyggede funktioner til elektronisk signatur. Du kan også oprette tilpassede signaturkrav for enhver databasetabel og ethvert felt. Elektroniske signaturer har en indbygget funktion til digitale signaturer. Alle brugere, som signerer dokumenter, skal have tildelt et gyldigt kryptografisk certifikat. Når et dokument signeres, godkendes den private nøgle, som er tilknyttet det pågældende certifikat. Dynamics 365 for Operations registrerer oplysninger om elektroniske signaturer i en log for at angive et revisionsspor. Hvis du vil oprette elektroniske signaturer, skal du se under [Opsætning af elektroniske signaturer (Opgaveguide)](http://ax.help.dynamics.com/en/wiki/set-up-electronic-signatures/).

## <a name="users-who-require-access-to-electronic-signatures"></a>Brugere, der kræver adgang til elektroniske signaturer
Tre slags brugere kræver normalt sikkerhedsadgang til elektroniske signaturer: administratorer af elektroniske signaturer, underskrivere og revisorer af elektroniske signaturer.

### <a name="electronic-signature-administrator"></a>Administratorer af elektroniske signaturer

Administratorer af elektroniske signaturer konfigurerer krav til signaturer, generelle parametre og godkendere, og de modtager besked, når signaturer ikke kan bekræftes. En bruger, der er tildelt sikkerhedsrollen **It-chef**, har som standard tilladelse til at administrere elektroniske signaturer.

### <a name="signer"></a>Underskriver

En underskriver angiver elektroniske signaturer på dokumenter og til processer, der kræver signaturer. En bruger, der er tildelt sikkerhedsrollen **Systembruger**, har som standard tilladelse til at signere dokumenter elektronisk. **Bemærk!** Underskriveren kan kræve yderligere tilladelser, før der gives adgang til data, der er relateret til det dokument eller den proces, der signeres. En bruger, der ændrer data, og derefter skal signere for disse ændringer, skal have tilladelse til at ændre dataene. En bruger, der signerer på vegne af en anden bruger, kan ikke kræve adgang til dataene. Et eksempel på denne type bruger er en tilsynsførende, der signerer for en medarbejders ændringer.

### <a name="electronic-signature-auditor"></a>Revisorer af elektroniske signaturer

Revisorer af elektroniske signaturer gennemgår databaseloggen og signaturgennemsynsloggen, der er tilgængelig fra databaseloggen. En bruger, der er tildelt sikkerhedsrollen **It-chef**, har som standard tilladelse til at overvåge elektroniske signaturer. Hvis du bruger en anden rolle end **It-chef**, skal du sikre dig, at rollen er tildelt følgende rettigheder:

-   Vis fejl i elektroniske signaturer
-   Vis databaselog

## <a name="signing-documents-electronically"></a>Elektronisk signering af dokumenter
### <a name="get-a-certificate"></a>Sådan hentes et certifikat

Før du signerer dokumenter digitalt i Dynamics 365 for Operations, skal du anmode om et certifikat. **Bemærk:** Dynamics 365 for Operations bruger Microsoft SQL Server-funktioner til at oprette certifikater og aktivere elektronisk signering. Der kræves ikke yderligere certifikater eller offentlige nøgleinfrastrukturer (PKI). Når du anmoder om et certifikat, oprettes der en offentlig nøgle og en privat nøgle til dig i Dynamics 365 for Operations-databasen. Den private nøgle er krypteret ved hjælp af en adgangskode, som kun du kender. Når du signerer et dokument digitalt, bekræftes din identitet, når du indtaster adgangskoden. Når du vil anmode om et certifikat, skal du på siden **Indstillinger** under fanen **Konti** klikke på **Hent certifikat**. Du skal indtaste og bekræfte den adgangskode, du vil bruge til signering. Adgangskoden bruges for at beskytte din private nøgle og godkende brugen af dit certifikat. Denne adgangskode gemmes ikke i databasen, og den er ikke tilgængelig for nogen anden, end ikke Dynamics 365 for Operations-administratoren. Hvis du glemmer den adgangskode, der er tilknyttet dit certifikat, skal du nulstille det pågældende certifikat. Hvis du nulstiller certifikatet, påvirker det ikke dokumenter, du har signeret ved hjælp af det tidligere certifikat. Du kan nulstille certifikatet ved på siden **Indstillinger** at klikke på **Nulstil certifikat**.

### <a name="sign-a-document-electronically"></a>Signere et dokument elektronisk

Siden **Dokumentsignering** vises, når du foretager en ændring, der kræver en elektronisk signatur.

1.  Klik på fanen **Dokument** på siden **Underskriv dokument** for at gennemse ændringerne i dokumentet.
2.  Vælg en årsagskode på fanen **Signatur**.
3.  Angiv en kommentar, hvis der kræves en kommentar.
4.  Hvis dit bruger-id ikke vises i feltet **Underskriver**, skal du vælge det på listen.
5.  Angiv din lokalitet, hvis disse oplysninger er påkrævet.
6.  Klik på **OK**.

### <a name="sign-for-another-users-changes"></a>Signere en anden brugers ændringer

Af og til vil du måske gerne have, at en bruger signerer for en anden brugers ændringer. Det kan f.eks. være nødvendigt, at en tilsynsførende signerer for ændringer, som en medarbejder foretager på styklister. Brug denne procedure til at angive en Dynamics 365 for Operations-bruger som underskriver for en anden bruger. **Bemærk:** Når en bruger underskriver for en anden brugers ændringer, skal signaturen angives på den arbejdsstation, hvor den bruger, der udførte ændringen, arbejder. Brugeren kan ikke gemme ændringen, før signaturen er blevet angivet. Udfør disse trin for at angive godkendere.

1.  På siden **Indstillinger** under fanen **Konti** skal du klikke på **Angiv godkender**.
2.  Vælg id'et for den bruger, som skal signere for en anden brugers ændringer, i feltet **Bruger-id for godkender**.
3.  Vælg id'et for den bruger, hvis ændringer der skal signeres for, i feltet **Signer for bruger-id**.





