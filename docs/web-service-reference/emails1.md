---
title: Emails1
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cc02bd86-c618-446a-92f0-749423cbc4ee
description: Das Emails1-Element gibt ein Array von EmailAddressAttributedValue-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.
ms.openlocfilehash: 916f87038cfe959045c93dba749f1dc3b85296e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456171"
---
# <a name="emails1"></a><span data-ttu-id="a8425-103">Emails1</span><span class="sxs-lookup"><span data-stu-id="a8425-103">Emails1</span></span>

<span data-ttu-id="a8425-104">Das **Emails1** -Element gibt ein Array von **EmailAddressAttributedValue** -Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete persona an.</span><span class="sxs-lookup"><span data-stu-id="a8425-104">The **Emails1** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails1>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails1>
```

 <span data-ttu-id="a8425-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="a8425-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8425-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a8425-106">Attributes and elements</span></span>

<span data-ttu-id="a8425-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a8425-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8425-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8425-108">Attributes</span></span>

<span data-ttu-id="a8425-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8425-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8425-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8425-110">Child elements</span></span>

|<span data-ttu-id="a8425-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8425-111">**Element**</span></span>|<span data-ttu-id="a8425-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8425-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8425-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="a8425-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="a8425-114">Gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Zuschreibungen an.</span><span class="sxs-lookup"><span data-stu-id="a8425-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8425-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8425-115">Parent elements</span></span>

|<span data-ttu-id="a8425-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8425-116">**Element**</span></span>|<span data-ttu-id="a8425-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8425-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8425-118">Persona</span><span class="sxs-lookup"><span data-stu-id="a8425-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="a8425-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8425-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8425-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8425-120">Remarks</span></span>

<span data-ttu-id="a8425-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a8425-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a8425-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a8425-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8425-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a8425-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8425-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8425-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8425-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a8425-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a8425-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="a8425-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="a8425-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a8425-127">Validation File</span></span>  <br/> |<span data-ttu-id="a8425-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a8425-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8425-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a8425-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a8425-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8425-130">See also</span></span>



- [<span data-ttu-id="a8425-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a8425-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

