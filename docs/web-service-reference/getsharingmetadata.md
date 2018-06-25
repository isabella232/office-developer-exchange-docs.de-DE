---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: Das GetSharingMetadata-Element definiert eine Anforderung an ein undurchsichtiger Authentifizierungstoken erhalten möchten, die die Einladung zur Freigabe identifiziert. Dieses Element ist das Basiselement für den Vorgang GetSharingMetadata.
ms.openlocfilehash: 5283d35e11350ef10ed8cc01527e787ef54be927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829677"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

Das **GetSharingMetadata** -Element definiert eine Anforderung an ein undurchsichtiger Authentifizierungstoken erhalten möchten, die die Einladung zur Freigabe identifiziert. Dieses Element ist das Basiselement für den [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md).
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 **GetSharingMetadataType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |Stellt den Bezeichner des Ordners auf dem Server, der freigegeben werden sollen. Dieses Element ist erforderlich.  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |Stellt die SMTP-e-Mail-Adresse, die entspricht an das Postfach, das den Ordner enthält, der durch das [IdOfFolderToShare](idoffoldertoshare.md) -Element identifiziert wird. Dieses Element ist erforderlich.  <br/> |
|[Empfänger (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Stellt die SMTP-e-Mail-Adressen eine oder mehrere Entitäten, die Zugriff auf die Daten in den Ordner erteilt werden, die durch das [IdOfFolderToShare](idoffoldertoshare.md) -Element identifiziert wird. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

