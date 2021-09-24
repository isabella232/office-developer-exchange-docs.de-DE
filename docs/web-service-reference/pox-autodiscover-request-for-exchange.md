---
title: POX-Anforderung der AutoErmittlung für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: Die AutoErmittlungsanforderung enthält eine Abfrage für die Clientzugriffskonfiguration eines Benutzers.
ms.openlocfilehash: 8a0960dcff21276baf723512befacc4eca35950f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523866"
---
# <a name="pox-autodiscover-request-for-exchange"></a>POX-Anforderung der AutoErmittlung für Exchange

Die AutoErmittlungsanforderung enthält eine Abfrage für die Clientzugriffskonfiguration eines Benutzers.
  
## <a name="autodiscover-request-example"></a>Beispiel für AutoErmittlungsanforderung

### <a name="description"></a>Beschreibung

Das folgende XML-Beispiel zeigt einen Anforderungstext für die AutoErmittlung.
  
### <a name="code"></a>Code

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a>Anforderungsheader

Die folgenden HTTP-Header sind optional, wenn AutoErmittlungsanforderungen gesendet werden.
  
**Tabelle 1. HTTP-Anforderungsheader**

|**Header**|**Beschreibung**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |Wenn vorhanden und auf "1" festgelegt, gibt an, dass der Client Informationen anfordert, die zum Herstellen einer Verbindung mit dem Server mithilfe des MAPI/HTTP-Protokolls verwendet werden können. Dieser Header gilt für Clients, die das MAPI/HTTP-Protokoll implementieren.  <br/> |
|X-ClientCanHandle  <br/> |Dieser Header enthält eine durch Trennzeichen getrennte Liste von Funktionen, die der Client unterstützt. Die möglichen Werte sind in Tabelle 2 angegeben.  <br/> |
   
**Tabelle 2. X-ClientCanHandle-Headerwerte**

|**X-ClientCanHandle-Wert (Groß-/Kleinschreibung nicht beachtet)**|**Mindestversion des Servers**|**Beschreibung**|
|:-----|:-----|:-----|
|Verhandeln  <br/> |15.00.0995.014  <br/> |Wenn dieser Wert vorhanden ist, gibt der Server den Wert "Negotiate" im [AuthPackage (POX)-Element](authpackage-pox.md) zurück, wenn der Server so konfiguriert ist, dass er die Negotiate-Authentifizierung akzeptiert. Wenn dieser Wert nicht vorhanden ist, gibt der Server den Wert "Negotiate" im **AuthPackage-Element** nicht zurück.  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |Wenn dieser Wert vorhanden ist, gibt der Server ein [POX-Element (Protocol)](protocol-pox.md) zurück, bei dem ein [POX-Element (Type)](type-pox.md) auf "EXHTTP" festgelegt ist, wenn der Server so konfiguriert ist, dass RPC/HTTP-Verbindungen akzeptiert werden. Wenn dieser Wert nicht vorhanden ist, gibt der Server kein **Protokollelement** zurück, bei dem ein **Type-Element** auf "EXHTTP" festgelegt ist.  <br/> |
   
### <a name="request-elements"></a>Anfordern von Elementen

Die folgenden Elemente werden im Anforderungstext verwendet:
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
    
- [Anforderung (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [EMailAddress (POX)](emailaddress-pox.md)
    
> [!NOTE]
> Das [LegacyDN (POX)-Element](legacydn-pox.md) kann anstelle des [EMailAddress (POX)-Elements](emailaddress-pox.md) verwendet werden. 
  
### <a name="version-differences"></a>Versionsunterschiede

Der X-MapiHttpCapability-Header ist ab Build 15.00.0847.032 (Exchange Server 2013 SP1) in Office 365, Exchange Online und lokalen Versionen von Exchange verfügbar.
  
Der X-ClientCanHandle-Header ist ab Build 15.00.0995.014 in Office 365, Exchange Online und lokalen Versionen von Exchange verfügbar.
  
## <a name="see-also"></a>Siehe auch



[POX-AutoErmittlungsantwort für Exchange](pox-autodiscover-response-for-exchange.md)


[POX AutoErmittlung Webdienstverweis für Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
  
[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

