---
title: Konto (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: Das Account-Element gibt Kontoeinstellungen für den Benutzer an oder enthält Fehlerantworten.
ms.openlocfilehash: 89799ab62a2aa4945b0e8f3209ab1fbc7d2fa2e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534053"
---
# <a name="account-pox"></a>Konto (POX)

Das **Account-Element** gibt Kontoeinstellungen für den Benutzer an oder enthält Fehlerantworten. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
- [Response (POX)](response-pox.md)
- [Konto (POX)](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AccountType (POX)](accounttype-pox.md) <br/> |Stellt den Kontotyp dar.  <br/> |
|[Aktion (POX)](action-pox.md) <br/> |Stellt Informationen bereit, die verwendet werden, um zu bestimmen, ob eine andere AutoErmittlungsanforderung erforderlich ist, um die Benutzerkonfigurationsinformationen zurückzugeben.  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |Enthält einen Wert, der angibt, ob das Postfach des Benutzers in Exchange Online oder Exchange Online als Teil Office 365 gehostet wird.  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |Enthält die URL des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist, die zum Abrufen von AutoErmittlungseinstellungen verwendet werden soll.  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |Gibt die E-Mail-Adresse an, die für eine nachfolgende AutoErmittlungsanforderung verwendet werden soll.  <br/> |
|[Bild (POX)](image-pox.md) <br/> |Enthält den Pfad eines Bilds, das zum Branding der Konfigurationsumgebung verwendet wird.  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |Enthält die URL der Startseite des Internetdienstanbieters (Internet Service Provider, ISP).  <br/> |
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Clientzugriffsserver.  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Enthält Informationen, mit denen Clients eine AutoErmittlungsanforderung senden können, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln.  <br/> |
|[Fehler (POX)](error-pox.md) <br/> |Enthält eine AutoErmittlungsfehlerantwort.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Enthält die Antwort des AutoErmittlungsdiensts.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

