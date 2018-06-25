---
title: Adressen (ArrayOfAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 711acc90-8e5b-4658-92d2-16cd441db56e
description: Das Adressen-Element gibt ein Array von Address-Elementen.
ms.openlocfilehash: c1ee79611da1d19ce85202f9e3c0f68c421e98c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757245"
---
# <a name="addresses-arrayofaddressestype"></a><span data-ttu-id="ef70e-103">Adressen (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="ef70e-103">Addresses (ArrayOfAddressesType)</span></span>

<span data-ttu-id="ef70e-104">Das **Adressen** -Element gibt ein Array von **Address** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="ef70e-104">The **Addresses** element specifies an array of **Address** elements.</span></span> 
  
```XML
<Addresses>
    <Address></Address>
</Addresses>
```

 <span data-ttu-id="ef70e-105">**ArrayOfAddressesType**</span><span class="sxs-lookup"><span data-stu-id="ef70e-105">**ArrayOfAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef70e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef70e-106">Attributes and elements</span></span>

<span data-ttu-id="ef70e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef70e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef70e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef70e-108">Attributes</span></span>

<span data-ttu-id="ef70e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef70e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef70e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef70e-110">Child elements</span></span>

|<span data-ttu-id="ef70e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef70e-111">**Element**</span></span>|<span data-ttu-id="ef70e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef70e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef70e-113">Adresse (Kontakttyp den)</span><span class="sxs-lookup"><span data-stu-id="ef70e-113">Address (ContactType)</span></span>](address-contacttype.md) <br/> |<span data-ttu-id="ef70e-114">Gibt die Adresse eines Kontakts.</span><span class="sxs-lookup"><span data-stu-id="ef70e-114">Specifies the address of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef70e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef70e-115">Parent elements</span></span>

|<span data-ttu-id="ef70e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef70e-116">**Element**</span></span>|<span data-ttu-id="ef70e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef70e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef70e-118">Kontakt (Kontakttyp den)</span><span class="sxs-lookup"><span data-stu-id="ef70e-118">Contact (ContactType)</span></span>](contact-contacttype.md) <br/> |<span data-ttu-id="ef70e-119">Gibt einen Kontakt in der einheitliche Kontaktspeicher an.</span><span class="sxs-lookup"><span data-stu-id="ef70e-119">Specifies a contact in the Unified Contact Store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef70e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef70e-120">Remarks</span></span>

<span data-ttu-id="ef70e-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ef70e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef70e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ef70e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef70e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ef70e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef70e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef70e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef70e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef70e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ef70e-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="ef70e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ef70e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef70e-127">Validation File</span></span>  <br/> |<span data-ttu-id="ef70e-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef70e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef70e-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ef70e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ef70e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef70e-130">See also</span></span>

- [<span data-ttu-id="ef70e-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ef70e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

