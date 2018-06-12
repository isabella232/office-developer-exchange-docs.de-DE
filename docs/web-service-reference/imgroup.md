---
title: ImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: Das ImGroup-Element darstellt, eine instant messaging-Gruppe.
ms.openlocfilehash: 2a444158dbc6a73b1aee7b306cc251d33d005c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829890"
---
# <a name="imgroup"></a><span data-ttu-id="ac1a1-103">ImGroup</span><span class="sxs-lookup"><span data-stu-id="ac1a1-103">ImGroup</span></span>

<span data-ttu-id="ac1a1-104">Das **ImGroup** -Element darstellt, eine instant messaging-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ac1a1-104">The **ImGroup** element represents an instant messaging group.</span></span> 
  
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

 <span data-ttu-id="ac1a1-105">**ImGroupType**</span><span class="sxs-lookup"><span data-stu-id="ac1a1-105">**ImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac1a1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac1a1-106">Attributes and elements</span></span>

<span data-ttu-id="ac1a1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac1a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac1a1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac1a1-108">Attributes</span></span>

<span data-ttu-id="ac1a1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ac1a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac1a1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac1a1-110">Child elements</span></span>

<span data-ttu-id="ac1a1-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)  |  [ SmtpAddress](smtpaddress.md)</span><span class="sxs-lookup"><span data-stu-id="ac1a1-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md) | [SmtpAddress](smtpaddress.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ac1a1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac1a1-112">Parent elements</span></span>

<span data-ttu-id="ac1a1-113">[Gruppen (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span><span class="sxs-lookup"><span data-stu-id="ac1a1-113">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac1a1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac1a1-114">Remarks</span></span>

<span data-ttu-id="ac1a1-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ac1a1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ac1a1-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ac1a1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac1a1-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ac1a1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac1a1-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac1a1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac1a1-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac1a1-119">Schema name</span></span>  <br/> |<span data-ttu-id="ac1a1-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ac1a1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ac1a1-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac1a1-121">Validation file</span></span>  <br/> |<span data-ttu-id="ac1a1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ac1a1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac1a1-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ac1a1-123">Can be empty</span></span>  <br/> ||
   

