---
title: EncryptedSharedFolderData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderData
api_type:
- schema
ms.assetid: c1d4ca18-c5ce-41ff-bab4-f75e358c8b9f
description: Das EncryptedSharedFolderData-Element enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.
ms.openlocfilehash: 52e91eaf1ded31602b11e50c1b62159f72c101cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530663"
---
# <a name="encryptedsharedfolderdata"></a>EncryptedSharedFolderData

Das **EncryptedSharedFolderData** -Element enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren. 
  
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
|[Token](token.md) <br/> |Enthält verschlüsselte Daten, die das Identifikations Token für die freigegebenen Daten darstellen.  <br/> |
|[Daten](data.md) <br/> |Enthält verschlüsselte Daten, die die freigegebenen Daten darstellen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) <br/> |Stellt eine Auflistung von Datenstrukturen dar, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
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

