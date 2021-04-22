---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788587"
---
<span data-ttu-id="4b561-101">Cuando introduce fechas y horas, que son una fecha y una hora combinadas en un campo, debe introducir un espacio entre la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="4b561-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="4b561-102">La parte de la fecha solo puede contener espacios en la forma del separador de fecha oficial de la configuración de su región.</span><span class="sxs-lookup"><span data-stu-id="4b561-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="4b561-103">El tiempo puede contener espacios alrededor del indicador AM/PM en la configuración regional correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4b561-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="4b561-104">En la tabla siguiente se muestran varias formas de introducir fechas y horas y cómo se interpretan.</span><span class="sxs-lookup"><span data-stu-id="4b561-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="4b561-105">Movimiento</span><span class="sxs-lookup"><span data-stu-id="4b561-105">Entry</span></span>|<span data-ttu-id="4b561-106">Interpretación</span><span class="sxs-lookup"><span data-stu-id="4b561-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="4b561-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="4b561-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="4b561-108">08\-01\-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="4b561-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="4b561-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="4b561-109">131222 132455</span></span>|<span data-ttu-id="4b561-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="4b561-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="4b561-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="4b561-111">1-12-22 10</span></span>|<span data-ttu-id="4b561-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="4b561-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="4b561-113">1.12.22 5</span></span>|<span data-ttu-id="4b561-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="4b561-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="4b561-115">1.12.22</span></span>|<span data-ttu-id="4b561-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="4b561-117">11 12</span><span class="sxs-lookup"><span data-stu-id="4b561-117">11 12</span></span>|<span data-ttu-id="4b561-118">11/mes actual/año actual 12:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="4b561-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="4b561-119">1112 12</span></span>|<span data-ttu-id="4b561-120">11/12/año actual 12:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="4b561-121">h u hoy</span><span class="sxs-lookup"><span data-stu-id="4b561-121">t or today</span></span>|<span data-ttu-id="4b561-122">fecha de hoy 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="4b561-123">h hora</span><span class="sxs-lookup"><span data-stu-id="4b561-123">t time</span></span>|<span data-ttu-id="4b561-124">fecha de hoy hora real</span><span class="sxs-lookup"><span data-stu-id="4b561-124">today's date actual time</span></span>|
|<span data-ttu-id="4b561-125">h 10:30</span><span class="sxs-lookup"><span data-stu-id="4b561-125">t 10:30</span></span>|<span data-ttu-id="4b561-126">fecha de hoy 10:30:00</span><span class="sxs-lookup"><span data-stu-id="4b561-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="4b561-127">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="4b561-127">t 3:3:3</span></span>|<span data-ttu-id="4b561-128">fecha de hoy 03:03:03</span><span class="sxs-lookup"><span data-stu-id="4b561-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="4b561-129">l o fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="4b561-129">w or workdate</span></span>|<span data-ttu-id="4b561-130">la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="4b561-131">l o lunes</span><span class="sxs-lookup"><span data-stu-id="4b561-131">m or Monday</span></span>|<span data-ttu-id="4b561-132">Lunes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="4b561-133">ma o martes</span><span class="sxs-lookup"><span data-stu-id="4b561-133">tu or Tuesday</span></span>|<span data-ttu-id="4b561-134">Martes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="4b561-135">mi o miércoles</span><span class="sxs-lookup"><span data-stu-id="4b561-135">we or Wednesday</span></span>|<span data-ttu-id="4b561-136">Miércoles de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="4b561-137">ju o jueves</span><span class="sxs-lookup"><span data-stu-id="4b561-137">th or Thursday</span></span>|<span data-ttu-id="4b561-138">Jueves de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="4b561-139">v o viernes</span><span class="sxs-lookup"><span data-stu-id="4b561-139">f or Friday</span></span>|<span data-ttu-id="4b561-140">Viernes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="4b561-141">s o sábado</span><span class="sxs-lookup"><span data-stu-id="4b561-141">s or Saturday</span></span>|<span data-ttu-id="4b561-142">Sábado de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="4b561-143">do o domingo</span><span class="sxs-lookup"><span data-stu-id="4b561-143">su or Sunday</span></span>|<span data-ttu-id="4b561-144">Domingo de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="4b561-145">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="4b561-145">tu 10:30</span></span>|<span data-ttu-id="4b561-146">Martes de la semana actual 10:30:00</span><span class="sxs-lookup"><span data-stu-id="4b561-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="4b561-147">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="4b561-147">tu 3:3:3</span></span>|<span data-ttu-id="4b561-148">Martes de la semana actual 03:03:03</span><span class="sxs-lookup"><span data-stu-id="4b561-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="4b561-149">m23 h</span><span class="sxs-lookup"><span data-stu-id="4b561-149">t23 t</span></span>|<span data-ttu-id="4b561-150">Martes de la semana 23 del año de la fecha de trabajo, hora del día actual</span><span class="sxs-lookup"><span data-stu-id="4b561-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="4b561-151">m23</span><span class="sxs-lookup"><span data-stu-id="4b561-151">t23</span></span>|<span data-ttu-id="4b561-152">Martes de la semana 23 del año de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="4b561-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="4b561-153">m 23</span><span class="sxs-lookup"><span data-stu-id="4b561-153">t 23</span></span>|<span data-ttu-id="4b561-154">Hoy 23:00:00</span><span class="sxs-lookup"><span data-stu-id="4b561-154">Today 23:00:00</span></span>|
|<span data-ttu-id="4b561-155">m-1</span><span class="sxs-lookup"><span data-stu-id="4b561-155">t-1</span></span>|<span data-ttu-id="4b561-156">Martes de la semana 1 del año de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="4b561-156">Tuesday of week 1 of the work date year</span></span>|


