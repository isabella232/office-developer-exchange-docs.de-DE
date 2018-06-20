---
title: POX Anforderung der AutoErmittlung für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: Die Anforderung der AutoErmittlung enthält eine Abfrage für Access-Clientkonfiguration eines Benutzers.
ms.openlocfilehash: 48d6c30946e75936ed93a6f4507d8a8d3ae47d40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830865"
---
# <a name="pox-autodiscover-request-for-exchange"></a>POX Anforderung der AutoErmittlung für Exchange

Die Anforderung der AutoErmittlung enthält eine Abfrage für Access-Clientkonfiguration eines Benutzers.
  
## <a name="autodiscover-request-example"></a>AutoErmittlung-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende XML-Beispiel zeigt einen AutoErmittlung-Anforderungstext.
  
### <a name="code"></a>Code

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a>Anforderungsheader

Die folgenden HTTP-Header sind optional, wenn für die AutoErmittlung-Anforderungen senden.
  
**In Tabelle 1. Gemeinsam genutzte HTTP-Anforderung**

|**Header**|**Beschreibung**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |Wenn vorhanden und auf "1", gibt an, dass der Client Informationen anfordert, die Verbindung mit dem Server mithilfe von MAPI/HTTP-Protokoll verwendet werden können. Diese Kopfzeile gilt für Clients, mit die das MAPI/HTTP-Protokoll implementiert.  <br/> |
|X-ClientCanHandle  <br/> |Diese Kopfzeile enthält eine durch Trennzeichen getrennte Liste der Funktionen, die der Client unterstützt. In Tabelle 2 sind die möglichen Werte angegeben.  <br/> |
   
**In Tabelle 2. X-ClientCanHandle-Headerwerte**

|**X-ClientCanHandle Wert (Groß-/Kleinschreibung unterschieden)**|**Minimale Serverversion**|**Beschreibung**|
|:-----|:-----|:-----|
|Verhandeln  <br/> |15.00.0995.014  <br/> |Wenn dieser Wert vorhanden ist, gibt der Server einen Wert "Negotiate" im Element [AuthPackage (POX)](authpackage-pox.md) zurück, wenn der Server für die Annahme Negotiate-Authentifizierung konfiguriert ist. Wenn dieser Wert nicht vorhanden ist, gibt der Server einen Wert "Negotiate" nicht im **AuthPackage** -Element zurück.  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |Wenn dieser Wert vorhanden ist, gibt der Server zurück, ein [Protokoll (POX)](protocol-pox.md) -Element mit einem [Typ (POX)](type-pox.md) Element auf "EXHTTP" festgelegt, wenn der Server für die Annahme von RPC/HTTP-Verbindungen konfiguriert ist. Wenn dieser Wert nicht vorhanden ist, wird der Server kein **Protokoll** -Element mit einem **Typ** Element auf "EXHTTP" festgelegt zurückgegeben.  <br/> |
   
### <a name="request-elements"></a>Anfordern von Elementen

Die folgenden Elemente werden im Textkörper Anforderung verwendet:
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
    
- [Anforderung (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [EMailAddress (POX)](emailaddress-pox.md)
    
> [!NOTE]
> Das Element [LegacyDN (POX)](legacydn-pox.md) kann anstelle der [EMailAddress (POX)](emailaddress-pox.md) -Elements verwendet werden. 
  
### <a name="version-differences"></a>Versionsunterschiede

Die X-MapiHttpCapability Kopfzeile steht in Office 365 und Exchange Online und lokaler, beginnend mit Exchange-Versionen 15.00.0847.032 (Exchange Server 2013 SP1) erstellen.
  
Die X-ClientCanHandle Kopfzeile steht in Office 365 und Exchange Online und lokaler, beginnend mit Exchange-Versionen 15.00.0995.014 erstellen.
  
## <a name="see-also"></a>Siehe auch



[POX Antwort der AutoErmittlung für Exchange](pox-autodiscover-response-for-exchange.md)


[POX AutoErmittlung Webdienstverweis für Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
  
[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

