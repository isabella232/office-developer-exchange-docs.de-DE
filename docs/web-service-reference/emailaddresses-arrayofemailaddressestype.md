---
title: Emails (ArrayOfEmailAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95084659-aa5a-4bac-8977-00db3b87883e
description: Das addresses-Element gibt ein Array aller e-Mail-Adressen der zugeordneten persona an.
ms.openlocfilehash: e6132e9ef4ed13ea2546783f65d184fafeed5530
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463419"
---
# <a name="emailaddresses-arrayofemailaddressestype"></a><span data-ttu-id="be7a4-103">Emails (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="be7a4-103">EmailAddresses (ArrayOfEmailAddressesType)</span></span>

<span data-ttu-id="be7a4-104">Das addresses **-Element gibt** ein Array aller e-Mail-Adressen der zugeordneten persona an.</span><span class="sxs-lookup"><span data-stu-id="be7a4-104">The **EmailAddresses** element specifies an array of all email addresses of the associated persona.</span></span> 
  
```XML
<EmailAddresses>
    <Address></Address>
</EmailAddresses>
```

 <span data-ttu-id="be7a4-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="be7a4-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be7a4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="be7a4-106">Attributes and elements</span></span>

<span data-ttu-id="be7a4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="be7a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be7a4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="be7a4-108">Attributes</span></span>

<span data-ttu-id="be7a4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="be7a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be7a4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be7a4-110">Child elements</span></span>

|<span data-ttu-id="be7a4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="be7a4-111">**Element**</span></span>|<span data-ttu-id="be7a4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="be7a4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be7a4-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="be7a4-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="be7a4-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="be7a4-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="be7a4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="be7a4-115">Parent elements</span></span>

|<span data-ttu-id="be7a4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="be7a4-116">**Element**</span></span>|<span data-ttu-id="be7a4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="be7a4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be7a4-118">Persona</span><span class="sxs-lookup"><span data-stu-id="be7a4-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="be7a4-119">Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be7a4-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be7a4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be7a4-120">Remarks</span></span>

<span data-ttu-id="be7a4-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="be7a4-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="be7a4-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="be7a4-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be7a4-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="be7a4-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be7a4-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="be7a4-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be7a4-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="be7a4-125">Schema Name</span></span>  <br/> |<span data-ttu-id="be7a4-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="be7a4-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="be7a4-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="be7a4-127">Validation File</span></span>  <br/> |<span data-ttu-id="be7a4-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="be7a4-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="be7a4-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="be7a4-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="be7a4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be7a4-130">See also</span></span>



- [<span data-ttu-id="be7a4-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="be7a4-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

