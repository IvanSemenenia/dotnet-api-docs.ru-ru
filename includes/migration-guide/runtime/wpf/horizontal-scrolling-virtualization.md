### <a name="horizontal-scrolling-and-virtualization"></a><span data-ttu-id="1849e-101">Горизонтальная прокрутка и виртуализации</span><span class="sxs-lookup"><span data-stu-id="1849e-101">Horizontal scrolling and virtualization</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1849e-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="1849e-102">Details</span></span>|<span data-ttu-id="1849e-103">Это изменение относится к <xref:System.Windows.Controls.ItemsControl?displayProperty=name> , который выполняет свой собственный виртуализации в направлении, независимая от основного направления прокрутки (главный пример является <xref:System.Windows.Controls.DataGrid?displayProperty=name> EnableColumnVirtualization =&quot;True&quot;).</span><span class="sxs-lookup"><span data-stu-id="1849e-103">This change applies to an <xref:System.Windows.Controls.ItemsControl?displayProperty=name> that does its own virtualization in the direction orthogonal to the main scrolling direction (the chief example is <xref:System.Windows.Controls.DataGrid?displayProperty=name> with EnableColumnVirtualization=&quot;True&quot;).</span></span>  <span data-ttu-id="1849e-104">Результат определенных горизонтальной прокрутки операций был изменен на более понятные и более аналогом результаты операций сопоставимых вертикальной результатов. Следующие операции &quot;прокрутки здесь&quot; и &quot;правый край&quot;, чтобы использовать имена из меню, получить, щелкнув правой кнопкой мыши горизонтальную полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="1849e-104">The outcome of certain horizontal scrolling operations has been changed to produce results that are more intuitive and more analogous to the results of comparable vertical operations.The operations include &quot;Scroll Here&quot; and &quot;Right Edge&quot;, to use the names from the menu obtained by right-clicking a horizontal scrollbar.</span></span>  <span data-ttu-id="1849e-105">Оба этих вычислений кандидата смещение и вызова <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>. После прокрутки новому смещению понятие &quot;здесь&quot; или &quot;правый угол&quot; могло измениться, поскольку вновь отменяется виртуализированных содержимое было изменено значение <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>. До .net 4.6.2 операции прокрутки просто использует смещение кандидата, даже если он не может быть &quot;здесь&quot; или &quot;правый угол&quot; больше.</span><span class="sxs-lookup"><span data-stu-id="1849e-105">Both of these compute a candidate offset and call <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>.After scrolling to the new offset, the notion of &quot;here&quot; or &quot;right edge&quot; may have changed because newly de-virtualized content has changed the value of <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>.Prior to .Net 4.6.2, the scroll operation simply uses the candidate offset, even though it may not be &quot;here&quot; or at the &quot;right edge&quot; any more.</span></span>  <span data-ttu-id="1849e-106">Это приведет к эффектов, как &quot;перебрасываются&quot; ползунком, наиболее показано в примере.</span><span class="sxs-lookup"><span data-stu-id="1849e-106">This results in effects like &quot;bouncing&quot; the scroll thumb, best illustrated by example.</span></span> <span data-ttu-id="1849e-107">Предположим, что <xref:System.Windows.Controls.DataGrid?displayProperty=name> имеет ExtentWidth = 1000 и ширина = 200.</span><span class="sxs-lookup"><span data-stu-id="1849e-107">Suppose a <xref:System.Windows.Controls.DataGrid?displayProperty=name> has ExtentWidth=1000 and Width=200.</span></span>  <span data-ttu-id="1849e-108">Перейдите к &quot;правый край&quot; использует кандидата смещение 1000 200 = 800.</span><span class="sxs-lookup"><span data-stu-id="1849e-108">A scroll to &quot;Right Edge&quot; uses candidate offset 1000 - 200 = 800.</span></span>  <span data-ttu-id="1849e-109">Во время прокрутки на это смещение новые столбцы, de-виртуализировать; давайте предположим, что они являются очень широкий, чтобы <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name> изменяет до 2000.</span><span class="sxs-lookup"><span data-stu-id="1849e-109">While scrolling to that offset, new columns are de- virtualized; let's suppose they are very wide, so that the <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name> changes to 2000.</span></span>  <span data-ttu-id="1849e-110">Scroll заканчивается HorizontalOffset = 800 и бегунка &quot;клики&quot; обратно в центре полосы прокрутки - точно в 800/2000 = 40%. Изменение является для повторного вычисления нового кандидата смещения при возникновении такой ситуации и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="1849e-110">The scroll ends with HorizontalOffset=800, and the thumb &quot;bounces&quot; back to near the middle of the scrollbar - precisely at 800/2000 = 40%.The change is to recompute a new candidate offset when this situation occurs, and try again.</span></span> <span data-ttu-id="1849e-111">(Это как вертикальную прокрутку, уже работает.) Изменение обеспечивает взаимодействие с большей предсказуемостью и интуитивно понятный для конечного пользователя, но он также может повлиять на любое приложение, от которого зависит точное значение <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name> после горизонтальной прокрутки ли вызван конечным пользователем, либо путем явного вызова <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>.</span><span class="sxs-lookup"><span data-stu-id="1849e-111">(This is how vertical scrolling works already.)The change produces a more predictable and intuitive experience for the end user, but it could also affect any app that depends on the exact value of <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name> after a horizontal scroll, whether invoked by the end user or by an explicit call to <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>.</span></span>|
|<span data-ttu-id="1849e-112">Предложение</span><span class="sxs-lookup"><span data-stu-id="1849e-112">Suggestion</span></span>|<span data-ttu-id="1849e-113">Приложения, использующего прогнозируемое значение для <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name> должны изменяться, чтобы получить фактическое значение (и значение <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>) после любой горизонтальной прокрутки, которые могут измениться <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name> из-за отмены виртуализации.</span><span class="sxs-lookup"><span data-stu-id="1849e-113">An app that uses a predicted value for <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name> should be changed to fetch the actual value (and the value of <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>) after any horizontal scroll that could change <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name> due to de-virtualization.</span></span>|
|<span data-ttu-id="1849e-114">Область</span><span class="sxs-lookup"><span data-stu-id="1849e-114">Scope</span></span>|<span data-ttu-id="1849e-115">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="1849e-115">Minor</span></span>|
|<span data-ttu-id="1849e-116">Версия</span><span class="sxs-lookup"><span data-stu-id="1849e-116">Version</span></span>|<span data-ttu-id="1849e-117">4.6.2</span><span class="sxs-lookup"><span data-stu-id="1849e-117">4.6.2</span></span>|
|<span data-ttu-id="1849e-118">Тип</span><span class="sxs-lookup"><span data-stu-id="1849e-118">Type</span></span>|<span data-ttu-id="1849e-119">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="1849e-119">Runtime</span></span>|
|<span data-ttu-id="1849e-120">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="1849e-120">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.Primitives.IScrollInfo?displayProperty=nameWithType></li></ul>|
