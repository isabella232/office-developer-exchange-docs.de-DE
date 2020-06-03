---
title: EmailAddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20049467-c01a-4c7d-8ada-ca1801cc95ed
description: Das EmailAddressEntity-Element gibt eine einzelne e-Mail-Adress Entität an.
ms.openlocfilehash: b76b08f93e60c8492906f3cc94e60f5725c8a9dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526221"
---
# <a name="emailaddressentity"></a><span data-ttu-id="74ccd-103">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="74ccd-103">EmailAddressEntity</span></span>

<span data-ttu-id="74ccd-104">Das **EmailAddressEntity** -Element gibt eine einzelne e-Mail-Adress Entität an.</span><span class="sxs-lookup"><span data-stu-id="74ccd-104">The **EmailAddressEntity** element specifies a single email address entity.</span></span> 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 <span data-ttu-id="74ccd-105">**EmailAddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="74ccd-105">**EmailAddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="74ccd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="74ccd-106">Attributes and elements</span></span>

<span data-ttu-id="74ccd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="74ccd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="74ccd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="74ccd-108">Attributes</span></span>

<span data-ttu-id="74ccd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="74ccd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="74ccd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="74ccd-110">Child elements</span></span>

|<span data-ttu-id="74ccd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="74ccd-111">**Element**</span></span>|<span data-ttu-id="74ccd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="74ccd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74ccd-113">E-mailemail (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="74ccd-113">EmailAddress (string)</span></span>](emailaddress-string.md) <br/> |<span data-ttu-id="74ccd-114">Gibt eine einzelne e-Mail-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="74ccd-114">Specifies a single email address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="74ccd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="74ccd-115">Parent elements</span></span>

|<span data-ttu-id="74ccd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="74ccd-116">**Element**</span></span>|<span data-ttu-id="74ccd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="74ccd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74ccd-118">Emails (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="74ccd-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="74ccd-119">Gibt ein Array von e-Mail-Adress Entitäten an.</span><span class="sxs-lookup"><span data-stu-id="74ccd-119">Specifies an array of email address entities.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74ccd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74ccd-120">Remarks</span></span>

<span data-ttu-id="74ccd-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="74ccd-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="74ccd-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="74ccd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="74ccd-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="74ccd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74ccd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="74ccd-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="74ccd-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="74ccd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="74ccd-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="74ccd-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="74ccd-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="74ccd-127">Validation File</span></span>  <br/> |<span data-ttu-id="74ccd-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="74ccd-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="74ccd-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="74ccd-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="74ccd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74ccd-130">See also</span></span>



- [<span data-ttu-id="74ccd-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="74ccd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

