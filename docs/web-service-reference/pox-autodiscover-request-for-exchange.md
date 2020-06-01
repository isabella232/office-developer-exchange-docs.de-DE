---
title: POX-Anforderung der AutoErmittlung für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: Die Auto Ermittlungsanforderung enthält eine Abfrage für die Clientzugriffs Konfiguration eines Benutzers.
ms.openlocfilehash: b2138f9813c7b75aef9afb90089b9b874aac7532
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461667"
---
# <a name="pox-autodiscover-request-for-exchange"></a>POX-Anforderung der AutoErmittlung für Exchange

Die Auto Ermittlungsanforderung enthält eine Abfrage für die Clientzugriffs Konfiguration eines Benutzers.
  
## <a name="autodiscover-request-example"></a>Beispiel für eine Auto Ermittlungsanforderung

### <a name="description"></a>Beschreibung

Das folgende XML-Beispiel zeigt einen Auto Ermittlungs Anforderungstext.
  
### <a name="code"></a>Code

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a>Anforderungs Kopfzeilen

Die folgenden HTTP-Header sind beim Senden von Auto Ermittlungsanforderungen optional.
  
**Tabelle 1. HTTP-Anforderungsheader**

|**Header**|**Beschreibung**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |Wenn vorhanden und auf "1" festgelegt, wird angegeben, dass der Clientinformationen anfordert, die zum Herstellen einer Verbindung mit dem Server mithilfe des MAPI/http-Protokolls verwendet werden können. Diese Kopfzeile gilt für Clients, die das MAPI/http-Protokoll implementieren.  <br/> |
|X-ClientCanHandle  <br/> |Diese Kopfzeile enthält eine durch trennzeichengetrennte Liste von Funktionen, die vom Client unterstützt werden. Die möglichen Werte sind in Tabelle 2 angegeben.  <br/> |
   
**Tabelle 2. X-ClientCanHandle-Headerwerte**

|**X-ClientCanHandle-Wert (Groß-/Kleinschreibung wird nicht berücksichtigt)**|**Minimale Server Version**|**Beschreibung**|
|:-----|:-----|:-----|
|Aushandeln  <br/> |15.00.0995.014  <br/> |Wenn dieser Wert vorhanden ist, gibt der Server den Wert "Negotiate" im [AuthPackage (POX)-](authpackage-pox.md) Element zurück, wenn der Server so konfiguriert ist, dass die Negotiate-Authentifizierung akzeptiert wird. Wenn dieser Wert nicht vorhanden ist, gibt der Server den Wert "Negotiate" im **AuthPackage** -Element nicht zurück.  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |Wenn dieser Wert vorhanden ist, gibt der Server ein [Pocken-Element (POX](protocol-pox.md) ) mit einem [Typ (POX)](type-pox.md) -Element auf "http" zurück, wenn der Server für die Annahme von RPC/HTTP-Verbindungen konfiguriert ist. Wenn dieser Wert nicht vorhanden ist, gibt der Server kein **Protocol** -Element zurück, dessen **Type** -Element auf "http" festgelegt ist.  <br/> |
   
### <a name="request-elements"></a>Anfordern von Elementen

Die folgenden Elemente werden im Anforderungstext verwendet:
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
    
- [Anforderung (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [E-mailemail (POX)](emailaddress-pox.md)
    
> [!NOTE]
> Das [LegacyDN (POX)-](legacydn-pox.md) Element kann anstelle des Elements [Email (POX)](emailaddress-pox.md) verwendet werden. 
  
### <a name="version-differences"></a>Versionsunterschiede

Der X-MapiHttpCapability-Header ist in Office 365-, Exchange Online-und lokalen Versionen von Exchange verfügbar, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).
  
Der X-ClientCanHandle-Header ist in Office 365, Exchange Online und lokalen Versionen von Exchange verfügbar, beginnend mit Build 15.00.0995.014.
  
## <a name="see-also"></a>Siehe auch



[POX-Auto Ermittlungs Antwort für Exchange](pox-autodiscover-response-for-exchange.md)


[POX AutoErmittlung Webdienstverweis für Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
  
[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

