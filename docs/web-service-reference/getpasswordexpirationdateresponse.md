---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: Das GetPasswordExpirationDateResponse-Element definiert die Antwort auf eine GetPasswordExpirationDate-Vorgangsanforderung.
ms.openlocfilehash: bad4cf5ea70e669ccfb98cc9e2eb7d0e5924949e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535024"
---
# <a name="getpasswordexpirationdateresponse"></a>GetPasswordExpirationDateResponse

Das **GetPasswordExpirationDateResponse-Element** definiert die Antwort auf eine [GetPasswordExpirationDate-Vorgangsanforderung.](getpasswordexpirationdate-operation.md) 
  
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
|**ResponseClass** <br/> | Beschreibt den Status der Antwort. <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:  <br/><br/>– Erfolg  <br/>- Warnung  <br/>- Fehler  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten.<br/><br/> Es folgen Beispiele für Warnungsquellen:  <br/><br/>– Der Exchange Speicher ist während des Batches offline.  <br/>– Active Directory Domain Services (AD DS) ist offline.  <br/>– Postfächer wurden verschoben.  <br/>– Die Nachrichtendatenbank (MDB) ist offline.  <br/>– Ein Kennwort ist abgelaufen.  <br/>– Ein Kontingent wurde überschritten.  <br/> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Es folgen Beispiele für Fehlerquellen:  <br/><br/>– Ungültige Attribute oder Elemente.  <br/>– Attribute oder Elemente, die außerhalb des Gültigen liegen.  <br/>– Ein unbekanntes Tag.  <br/>– Ein Attribut oder Element, das im Kontext ungültig ist.  <br/>– Ein nicht autorisierter Zugriffsversuch durch einen Beliebigen Client.  <br/>– Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf.  <br/><br/>  Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Elementname**|**Beschreibung**|
|:-----|:-----|
|[PasswordExpirationDate](passwordexpirationdate.md) <br/> |Gibt das Ablaufdatum des Kennworts für das in der Anforderung angegebene E-Mail-Konto an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Elementname**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine EWS-Anforderung (Exchange Web Services).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetPasswordExpirationDate-Vorgang](getpasswordexpirationdate-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

