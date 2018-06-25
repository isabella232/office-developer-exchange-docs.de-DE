---
title: OrganizationRelationshipSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 917481bb-46fc-4b88-8683-4cf812dcb0ab
description: Das Element OrganizationRelationshipSettings stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation. Das OrganizationRelationshipSettings-Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet.
ms.openlocfilehash: ed6cc0ef1891cd92c02a8e088e913886048623ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830660"
---
# <a name="organizationrelationshipsettings-soap"></a>OrganizationRelationshipSettings (SOAP)

Das Element **OrganizationRelationshipSettings** stellt eine Liste von organisationsbeziehungen für eine einzelne Organisation. Das **OrganizationRelationshipSettings** -Element ist nur zur internen Verwendung. Dieses Element wird von Clients nicht verwendet. 
  
```XML
<OrganizationRelationshipSettings>
    <DeliveryReportEnabled/>
    <DomainNames/>
    <FreeBusyAccessEnabled/>
    <FreeBusyAccessLevel/>
    <MailTipsAccessEnabled/>
    <MailTipsAccessLevel/>
    <MailboxMoveEnabled/>
    <Name/>
    <TargetApplicationUri/>
    <TargetAudodiscoverEpr/>
    <TargetSharingEpr/>
</OrganizationRelationshipSettings>
```

 **OrganizationRelationshipSettings**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeliveryReportEnabled (SOAP)](deliveryreportenabled-soap.md) <br/> |Stellt das [DeliveryReportEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) -Flag.  <br/> |
|[DomainNames (SOAP)](domainnames-soap.md) <br/> |Die Domain Names-Auflistung darstellt.  <br/> |
|[FreeBusyAccessEnabled (SOAP)](freebusyaccessenabled-soap.md) <br/> |Stellt das [FreeBusyAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) -Flag.  <br/> |
|[FreeBusyAccessLevel (SOAP)](freebusyaccesslevel-soap.md) <br/> |Stellt die [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) -Eigenschaft.  <br/> |
|[MailTipsAccessEnabled (SOAP)](mailtipsaccessenabled-soap.md) <br/> |Stellt das [MailTipsAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) -Flag.  <br/> |
|[MailTipsAccessLevel (SOAP)](mailtipsaccesslevel-soap.md) <br/> |Stellt die [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) -Eigenschaft.  <br/> |
|[MailboxMoveEnabled (SOAP)](mailboxmoveenabled-soap.md) <br/> |Stellt das [MailboxMoveEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) -Flag.  <br/> |
|[Name (SOAP)](name-soap.md) <br/> |Stellt den Namen der organisationsbeziehung an.  <br/> |
|[TargetApplicationUri (SOAP)](targetapplicationuri-soap.md) <br/> |Definiert die URI-Zielanwendung.  <br/> |
|[TargetAutodiscoverEpr (SOAP)](targetautodiscoverepr-soap.md) <br/> |Stellt die [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) -Eigenschaft.  <br/> |
|[TargetSharingEpr (SOAP)](targetsharingepr-soap.md) <br/> |Stellt die [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) -Eigenschaft.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[OrganizationRelationshipSettingsCollection (SOAP)](organizationrelationshipsettingscollection-soap.md) <br/> |Stellt eine Liste von organisationsbeziehungen, die mit die Abfrage übereinstimmen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

