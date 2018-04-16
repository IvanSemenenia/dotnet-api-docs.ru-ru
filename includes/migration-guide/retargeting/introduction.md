## <a name="introduction"></a><span data-ttu-id="30905-101">Вступление</span><span class="sxs-lookup"><span data-stu-id="30905-101">Introduction</span></span>
<span data-ttu-id="30905-102">Изменения при смене целевой платформы влияют на приложения, которые перекомпилируются с изменением целевой версии среды .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="30905-102">Retargeting changes affect apps that are recompiled to target a different .NET Framework.</span></span> <span data-ttu-id="30905-103">В их число входят следующее.</span><span class="sxs-lookup"><span data-stu-id="30905-103">They include:</span></span>

* <span data-ttu-id="30905-104">Изменения в среде разработки.</span><span class="sxs-lookup"><span data-stu-id="30905-104">Changes in the design-time environment.</span></span> <span data-ttu-id="30905-105">Например, инструменты построения могут начать выдавать предупреждения, тогда как раньше они этого не делали.</span><span class="sxs-lookup"><span data-stu-id="30905-105">For example, build tools may emit warnings when previously they did not.</span></span>

* <span data-ttu-id="30905-106">Изменения в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="30905-106">Changes in the runtime environment.</span></span> <span data-ttu-id="30905-107">Влияют только на приложения, которые предназначены специально для новой целевой платформы .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="30905-107">These affect only apps that specifically target the retargeted .NET Framework.</span></span> <span data-ttu-id="30905-108">Приложения, которые предназначены для предыдущих версий .NET Framework, работают нормально.</span><span class="sxs-lookup"><span data-stu-id="30905-108">Apps that target previous versions of the .NET Framework behave as they did when running under those versions.</span></span>

<span data-ttu-id="30905-109">В разделах с описанием изменений в среде выполнения используется следующая классификация отдельных элементов по их ожидаемому влиянию.</span><span class="sxs-lookup"><span data-stu-id="30905-109">In the topics that describe retargeting changes, we have classified individual items by their expected impact, as follows:</span></span>

<span data-ttu-id="30905-110">**Крупное изменение**. Это существенное изменение, влияющее на большое количество приложений или требующее объемного изменения кода.</span><span class="sxs-lookup"><span data-stu-id="30905-110">**Major** This is a significant change that affects a large number of apps or that requires substantial modification of code.</span></span>

<span data-ttu-id="30905-111">**Небольшое изменение**. Это изменение влияет на небольшое количество приложений или требует незначительного изменения кода.</span><span class="sxs-lookup"><span data-stu-id="30905-111">**Minor** This is a change that affects a small number of apps or that requires minor modification of code.</span></span>

<span data-ttu-id="30905-112">**Пограничный случай**. Это изменение влияет на приложения в исключительных ситуациях.</span><span class="sxs-lookup"><span data-stu-id="30905-112">**Edge case** This is a change that affects apps under very specific scenarios that are not common.</span></span>

<span data-ttu-id="30905-113">**Прозрачное изменение**. Это изменение не оказывает особого влияния на разработчиков и пользователей приложения.</span><span class="sxs-lookup"><span data-stu-id="30905-113">**Transparent** This is a change that has no noticeable effect on the app's developer or user.</span></span> <span data-ttu-id="30905-114">При этом вносить изменения в приложения не требуется.</span><span class="sxs-lookup"><span data-stu-id="30905-114">The app should not require modification because of this change.</span></span>