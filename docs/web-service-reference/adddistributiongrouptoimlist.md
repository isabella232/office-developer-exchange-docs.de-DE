---
title: AddDistributionGroupToImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: adbffbfc-e436-4620-acfc-5dfd41a88cb8
description: Das AddDistributionGroupToImList-Element definiert eine Anforderung an eine Verteilerliste zu einer Sofortnachricht Liste hinzufügen.
ms.openlocfilehash: b63daeb8b1d60123215bfcdec307f2f948d2ec39
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757222"
---
# <a name="adddistributiongrouptoimlist"></a><span data-ttu-id="89da7-103">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="89da7-103">AddDistributionGroupToImList</span></span>

<span data-ttu-id="89da7-104">Das **AddDistributionGroupToImList** -Element definiert eine Anforderung an eine Verteilerliste zu einer Sofortnachricht Liste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89da7-104">The **AddDistributionGroupToImList** element defines a request to add a distribution list to an instant message list.</span></span> 
  
```XML
<AddDistributionGroupToImList>
   <SmtpAddress/>
   <DisplayName/>
</AddDistributionGroupToImList>
```

 <span data-ttu-id="89da7-105">**AddDistributionGroupToImListType**</span><span class="sxs-lookup"><span data-stu-id="89da7-105">**AddDistributionGroupToImListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89da7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="89da7-106">Attributes and elements</span></span>

<span data-ttu-id="89da7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="89da7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89da7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="89da7-108">Attributes</span></span>

<span data-ttu-id="89da7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="89da7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89da7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89da7-110">Child elements</span></span>

<span data-ttu-id="89da7-111">[SmtpAddress](smtpaddress.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="89da7-111">[SmtpAddress](smtpaddress.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89da7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89da7-112">Parent elements</span></span>

<span data-ttu-id="89da7-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="89da7-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89da7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89da7-114">Remarks</span></span>

<span data-ttu-id="89da7-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="89da7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="89da7-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="89da7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89da7-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="89da7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89da7-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="89da7-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="89da7-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="89da7-119">Schema name</span></span>  <br/> |<span data-ttu-id="89da7-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="89da7-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="89da7-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="89da7-121">Validation file</span></span>  <br/> |<span data-ttu-id="89da7-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="89da7-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="89da7-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="89da7-123">Can be empty</span></span>  <br/> |<span data-ttu-id="89da7-124">false</span><span class="sxs-lookup"><span data-stu-id="89da7-124">false</span></span>  <br/> |
   

