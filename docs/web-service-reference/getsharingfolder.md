---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: Das GetSharingFolder-Element definiert eine Anforderung zum Abrufen des lokalen Ordnerbezeichners eines angegebenen freigegebenen Ordners. Es ist das Basiselement für den GetSharingFolder-Vorgang.
ms.openlocfilehash: 5d6362dff3ff29b0dc5100780cc70b21ec9bee9d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509770"
---
# <a name="getsharingfolder"></a>GetSharingFolder

Das **GetSharingFolder-Element** definiert eine Anforderung zum Abrufen des lokalen Ordnerbezeichners eines angegebenen freigegebenen Ordners. Es ist das Basiselement für den [GetSharingFolder-Vorgang.](getsharingfolder-operation.md)
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 **GetSharingFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Stellt die SMTP-E-Mail-Adresse der anderen Partei in der Freigabebeziehung dar. Dieses Element ist erforderlich.  <br/> |
|[DataType](datatype.md) <br/> |Beschreibt den Datentyp, der von einem freigegebenen Ordner freigegeben wird. Dieses Element ist optional.  <br/> |
|[SharedFolderId](sharedfolderid.md) <br/> |Stellt den Bezeichner des freigegebenen Ordners dar, dessen lokaler Ordnerbezeichner zurückgegeben werden soll. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Ein GetSharingFolder-Element muss ein [SmtpAddress-Element](smtpaddress.md) enthalten. Ein GetSharingFolder-Element muss auch ein [DataType-Element](datatype.md) oder ein [SharedFolderId-Element](sharedfolderid.md) enthalten, kann jedoch nicht beides enthalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange Webdienste des Computers hostet, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingFolder-Vorgang](getsharingfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

