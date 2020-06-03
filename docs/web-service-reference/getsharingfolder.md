---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: Das GetSharingFolder-Element definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners. Es ist das Basiselement für den GetSharingFolder-Vorgang.
ms.openlocfilehash: cb76c534d9b30d0a9d1b267396551eb2871e638a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460505"
---
# <a name="getsharingfolder"></a>GetSharingFolder

Das **GetSharingFolder** -Element definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners. Es ist das Basiselement für den [GetSharingFolder-Vorgang](getsharingfolder-operation.md).
  
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
|[SmtpAddress](smtpaddress.md) <br/> |Stellt die SMTP-e-Mail-Adresse des anderen Teilnehmers in der Freigabebeziehung dar. Dieses Element ist erforderlich.  <br/> |
|[DataType](datatype.md) <br/> |Beschreibt den Typ der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden. Dieses Element ist optional.  <br/> |
|[SharedFolderId](sharedfolderid.md) <br/> |Stellt den Bezeichner des freigegebenen Ordners dar, dessen lokaler Ordner Bezeichner zurückgegeben werden soll. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Ein GetSharingFolder-Element muss ein [SmtpAddress](smtpaddress.md) -Element enthalten. Ein GetSharingFolder-Element muss auch entweder ein [DataType](datatype.md) -Element oder ein [SharedFolderId](sharedfolderid.md) -Element enthalten, aber nicht beides enthalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingFolder-Vorgang](getsharingfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

