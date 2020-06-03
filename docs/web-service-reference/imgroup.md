---
title: Imgroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: Das imgroup-Element stellt eine Sofortnachrichten Gruppe dar.
ms.openlocfilehash: a0ff3fcb82e7f18837af5a6f5daa16e90043034d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460687"
---
# <a name="imgroup"></a><span data-ttu-id="a5e64-103">Imgroup</span><span class="sxs-lookup"><span data-stu-id="a5e64-103">ImGroup</span></span>

<span data-ttu-id="a5e64-104">Das **imgroup** -Element stellt eine Sofortnachrichten Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="a5e64-104">The **ImGroup** element represents an instant messaging group.</span></span> 
  
```XML
<ImGroup>
   <DisplayName/>
   <GroupType/>
   <ExchangeStoreId/>
   <MemberCorrelationKey/>
   <ExtendedProperties/>
   <SmtpAddress/>
</ImGroup>
```

 <span data-ttu-id="a5e64-105">**Imgrouptype**</span><span class="sxs-lookup"><span data-stu-id="a5e64-105">**ImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5e64-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a5e64-106">Attributes and elements</span></span>

<span data-ttu-id="a5e64-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a5e64-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5e64-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a5e64-108">Attributes</span></span>

<span data-ttu-id="a5e64-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a5e64-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5e64-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5e64-110">Child elements</span></span>

<span data-ttu-id="a5e64-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)  |  [GroupType](grouptype.md)  |  [ExchangeStoreId](exchangestoreid.md)  |  [MemberCorrelationKey](membercorrelationkey.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)  |  [SmtpAddress](smtpaddress.md)</span><span class="sxs-lookup"><span data-stu-id="a5e64-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md) | [SmtpAddress](smtpaddress.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a5e64-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5e64-112">Parent elements</span></span>

<span data-ttu-id="a5e64-113">[Gruppen (ArrayOfImGroupType)](groups-arrayofimgrouptype.md)  |  [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)  |  [AddImGroupResponse](addimgroupresponse.md)</span><span class="sxs-lookup"><span data-stu-id="a5e64-113">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5e64-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5e64-114">Remarks</span></span>

<span data-ttu-id="a5e64-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a5e64-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a5e64-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a5e64-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5e64-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a5e64-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5e64-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5e64-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a5e64-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a5e64-119">Schema name</span></span>  <br/> |<span data-ttu-id="a5e64-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a5e64-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a5e64-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a5e64-121">Validation file</span></span>  <br/> |<span data-ttu-id="a5e64-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a5e64-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a5e64-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a5e64-123">Can be empty</span></span>  <br/> ||
   

