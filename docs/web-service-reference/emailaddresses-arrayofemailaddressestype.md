---
title: EmailAddresses (ArrayOfEmailAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95084659-aa5a-4bac-8977-00db3b87883e
description: Das Element EmailAddresses gibt ein Array von allen e-Mail-Adressen der zugeordneten Rolle.
ms.openlocfilehash: 292d4c3f12b01f25fd094b2ab6d9c2d484d37694
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758176"
---
# <a name="emailaddresses-arrayofemailaddressestype"></a><span data-ttu-id="8a846-103">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="8a846-103">EmailAddresses (ArrayOfEmailAddressesType)</span></span>

<span data-ttu-id="8a846-104">Das Element **EmailAddresses** gibt ein Array von allen e-Mail-Adressen der zugeordneten Rolle.</span><span class="sxs-lookup"><span data-stu-id="8a846-104">The **EmailAddresses** element specifies an array of all email addresses of the associated persona.</span></span> 
  
```XML
<EmailAddresses>
    <Address></Address>
</EmailAddresses>
```

 <span data-ttu-id="8a846-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="8a846-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a846-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8a846-106">Attributes and elements</span></span>

<span data-ttu-id="8a846-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8a846-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a846-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8a846-108">Attributes</span></span>

<span data-ttu-id="8a846-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8a846-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a846-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a846-110">Child elements</span></span>

|<span data-ttu-id="8a846-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a846-111">**Element**</span></span>|<span data-ttu-id="8a846-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a846-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a846-113">Adresse (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="8a846-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="8a846-114">Stellt eine vollständig aufgelöster E-mail-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="8a846-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8a846-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8a846-115">Parent elements</span></span>

|<span data-ttu-id="8a846-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="8a846-116">**Element**</span></span>|<span data-ttu-id="8a846-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a846-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a846-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="8a846-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="8a846-119">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a846-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a846-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a846-120">Remarks</span></span>

<span data-ttu-id="8a846-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8a846-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8a846-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8a846-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a846-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8a846-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a846-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a846-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8a846-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8a846-125">Schema Name</span></span>  <br/> |<span data-ttu-id="8a846-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="8a846-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="8a846-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8a846-127">Validation File</span></span>  <br/> |<span data-ttu-id="8a846-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8a846-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8a846-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8a846-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8a846-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a846-130">See also</span></span>



- [<span data-ttu-id="8a846-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8a846-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

