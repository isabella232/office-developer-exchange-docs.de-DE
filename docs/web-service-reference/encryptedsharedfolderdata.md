---
title: EncryptedSharedFolderData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EncryptedSharedFolderData
api_type:
- schema
ms.assetid: c1d4ca18-c5ce-41ff-bab4-f75e358c8b9f
description: Das EncryptedSharedFolderData-Element enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seines Kalenders oder seiner Kontaktdaten für andere Clients zu autorisieren.
ms.openlocfilehash: c86f615e8936a379f465afab337a264d27238537
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546623"
---
# <a name="encryptedsharedfolderdata"></a>EncryptedSharedFolderData

Das **EncryptedSharedFolderData-Element** enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seines Kalenders oder seiner Kontaktdaten für andere Clients zu autorisieren. 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 **EncryptedSharedFolderDataType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Token](token.md) <br/> |Enthält verschlüsselte Daten, die das Identifikationstoken für die freigegebenen Daten darstellen.  <br/> |
|[Daten](data.md) <br/> |Enthält verschlüsselte Daten, die die freigegebenen Daten darstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) <br/> |Stellt eine Sammlung von Datenstrukturen dar, die ein Client verwenden kann, um die Freigabe seines Kalenders oder seiner Kontaktdaten für andere Clients zu autorisieren.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange Webdienste des Computers hostet, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

