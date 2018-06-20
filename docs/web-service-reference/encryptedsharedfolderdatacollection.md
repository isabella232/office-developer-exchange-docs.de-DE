---
title: EncryptedSharedFolderDataCollection
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderDataCollection
api_type:
- schema
ms.assetid: 25c6ae87-bbb9-4dd5-a85a-d669fcea137f
description: Das EncryptedSharedFolderDataCollection-Element enthält eine Auflistung von Datenstrukturen, die ein Client zum Autorisieren die Freigabe von dessen Kalender oder Kontaktdaten mit anderen Clients verwenden kann.
ms.openlocfilehash: e4d37f5df10f5e270be5126479485239f2205d6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758215"
---
# <a name="encryptedsharedfolderdatacollection"></a>EncryptedSharedFolderDataCollection

Das **EncryptedSharedFolderDataCollection** -Element enthält eine Auflistung von Datenstrukturen, die ein Client zum Autorisieren die Freigabe von dessen Kalender oder Kontaktdaten mit anderen Clients verwenden kann. 
  
```xml
<EncryptedSharedFolderDataCollection>   <EncryptedSharedFolderData/></EncryptedSharedFolderDataCollection>
```

 **ArrayOfEncryptedSharedFolderDataType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EncryptedSharedFolderData](encryptedsharedfolderdata.md) <br/> |Enthält die verschlüsselten Daten, die ein Client verwenden können, um die Freigabe von dessen Kalender zu autorisieren, oder wenden Sie Daten mit anderen Clients.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Definiert eine Antwort auf eine [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) an.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) -Anforderung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

