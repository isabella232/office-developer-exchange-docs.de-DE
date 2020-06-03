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
description: Das GetSharingMetadata-Element definiert eine Anforderung zum Abrufen eines nicht transparenten Authentifizierungstokens, das die Freigabeeinladung identifiziert. Dieses Element ist das Basiselement für den GetSharingMetadata-Vorgang.
ms.openlocfilehash: 406908e566d6d4249003b1a19a9ce79b8b328c4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530846"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

Das **GetSharingMetadata** -Element definiert eine Anforderung zum Abrufen eines nicht transparenten Authentifizierungstokens, das die Freigabeeinladung identifiziert. Dieses Element ist das Basiselement für den [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md).
  
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
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |Stellt den Bezeichner des Ordners auf dem Server dar, der freigegeben werden soll. Dieses Element ist erforderlich.  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |Stellt die SMTP-e-Mail-Adresse dar, die dem Postfach entspricht, das den Ordner enthält, der durch das [IdOfFolderToShare](idoffoldertoshare.md) -Element identifiziert wird. Dieses Element ist erforderlich.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Stellt die SMTP-e-Mail-Adressen von einer oder mehreren Entitäten dar, denen der Zugriff auf die Daten in dem Ordner gewährt wird, der durch das [IdOfFolderToShare](idoffoldertoshare.md) -Element identifiziert wird. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

