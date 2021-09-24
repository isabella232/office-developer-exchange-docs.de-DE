---
title: SearchableMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 339005cd-a3b9-47dd-bc7b-a860b699625b
description: Das SearchableMailbox -Element gibt ein Postfach aus einer Anforderung GetSearchableMailboxes zurückgegeben.
ms.openlocfilehash: 75d5680de8b0776b1ecf441ff71266ee74c4aa66
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524427"
---
# <a name="searchablemailbox"></a>SearchableMailbox

Das **SearchableMailbox** -Element gibt ein Postfach aus einer Anforderung **GetSearchableMailboxes** zurückgegeben. 
  
```XML
<SearchableMailbox>
   <Guid/>
   <PrimarySmtpAddress/>
   <IsExternalMailbox/>
   <ExternalEmailAddress/>
   <DisplayName/>
   <IsMembershipGroup/>
   <ReferenceId/>
</SearchableMailbox>
```

 **SearchableMailboxType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Guid](guid-ex15websvcsotherref.md) | [PrimarySmtpAddress (Zeichenfolge)](primarysmtpaddress-string.md) | [IsExternalMailbox](isexternalmailbox.md) | [ExternalEmailAddress](externalemailaddress.md) | [DisplayName (Zeichenfolge)](displayname-string.md) | [IsMembershipGroup](ismembershipgroup.md) | [ReferenceId](referenceid.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchableMailboxes](searchablemailboxes.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

