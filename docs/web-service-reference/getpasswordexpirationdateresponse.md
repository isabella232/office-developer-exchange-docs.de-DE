---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: Das GetPasswordExpirationDateResponse-Element definiert die Antwort auf eine Anforderung des GetPasswordExpirationDate-Vorgangs Vorgangs.
ms.openlocfilehash: c925b2b37879ba0f8f25b2dd73737ed2f3202555
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530204"
---
# <a name="getpasswordexpirationdateresponse"></a>GetPasswordExpirationDateResponse

Das **GetPasswordExpirationDateResponse** -Element definiert die Antwort auf eine Anforderung des [GetPasswordExpirationDate-Vorgangs](getpasswordexpirationdate-operation.md) Vorgangs. 
  
- [ResponseMessages](responsemessages.md)
- [GetPasswordExpirationDateResponse](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 **GetPasswordExpirationDateResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status der Antwort. <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:  <br/><br/>-Success  <br/>-Warnung  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.<br/><br/> Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:  <br/><br/>-Der Exchange-Informationsspeicher ist während des Batches offline.  <br/>-Active Directory-Domänendienste (AD DS) ist offline.  <br/>-Postfächer wurden verschoben.  <br/>-Die Nachrichtendatenbank (MDB) ist offline.  <br/>-Ein Kennwort ist abgelaufen.  <br/>-Ein Kontingent wurde überschritten.  <br/> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Im folgenden finden Sie Beispiele für Fehlerquellen:  <br/><br/>-Ungültige Attribute oder Elemente.  <br/>-Attribute oder Elemente außerhalb des gültigen Bereichs.  <br/>-Ein unbekanntes Tag.  <br/>-Ein Attribut oder Element, das im Kontext nicht gültig ist.  <br/>-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client.  <br/>-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf.  <br/><br/>  Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Elementname**|**Beschreibung**|
|:-----|:-----|
|[PasswordExpirationDate](passwordexpirationdate.md) <br/> |Gibt das Ablaufdatum für das Kennwort für das in der Anforderung angegebene e-Mail-Konto an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Elementname**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange-Webdienste Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetPasswordExpirationDate-Vorgang](getpasswordexpirationdate-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

