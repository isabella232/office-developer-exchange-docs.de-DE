---
title: EncryptionMethod (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bc632c85-ec74-4a00-baec-df5973e032fa
description: Das EncryptionMethod-Element stellt die kryptografische Methode dar, die für die Pop-, IMAP-und SMTP-Protokolle verwendet wird.
ms.openlocfilehash: 26236d9b08eae1bcabfd9aac59f5b01714ba9841
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530656"
---
# <a name="encryptionmethod-soap"></a>EncryptionMethod (SOAP)

Das **EncryptionMethod** -Element stellt die kryptografische Methode dar, die für die Pop-, IMAP-und SMTP-Protokolle verwendet wird. 
  
```XML
<EncryptionMethod/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ProtocolConnection (SOAP)](protocolconnection-soap.md) <br/> |Stellt die Protokollverbindung des Server-Webclients dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist die kryptografische Methode, die für das Pop-, IMAP-und SMTP-Protokoll verwendet wird.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)

