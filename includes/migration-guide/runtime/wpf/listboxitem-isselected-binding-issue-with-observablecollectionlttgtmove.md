### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a><span data-ttu-id="2e041-101">Проблема привязки ListBoxItem IsSelected ObservableCollection&lt;T&gt;. Перемещение</span><span class="sxs-lookup"><span data-stu-id="2e041-101">ListBoxItem IsSelected binding issue with ObservableCollection&lt;T&gt;.Move</span></span>

|   |   |
|---|---|
|<span data-ttu-id="2e041-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="2e041-102">Details</span></span>|<span data-ttu-id="2e041-103">Вызов <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> или <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> с коллекцией, привязанный к <xref:System.Windows.Controls.ListBox?displayProperty=name> с выбранным элементов может привести к страницам с выделением будущих или unselection из <xref:System.Windows.Controls.ListBox?displayProperty=name> элементов.</span><span class="sxs-lookup"><span data-stu-id="2e041-103">Calling <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> or <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> on a collection bound to a <xref:System.Windows.Controls.ListBox?displayProperty=name> with items selected can lead to erratic behavior with future selection or unselection of <xref:System.Windows.Controls.ListBox?displayProperty=name> items.</span></span>|
|<span data-ttu-id="2e041-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="2e041-104">Suggestion</span></span>|<span data-ttu-id="2e041-105">Вызов <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> и <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> вместо <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> будет решить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="2e041-105">Calling <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> and <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> instead of <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> will work around this issue.</span></span> <span data-ttu-id="2e041-106">Кроме того, эта проблема была устранена в .NET Framework 4.6 и может быть решена путем обновления до этой версии платформы .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="2e041-106">Alternatively, this issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="2e041-107">Область</span><span class="sxs-lookup"><span data-stu-id="2e041-107">Scope</span></span>|<span data-ttu-id="2e041-108">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="2e041-108">Minor</span></span>|
|<span data-ttu-id="2e041-109">Версия</span><span class="sxs-lookup"><span data-stu-id="2e041-109">Version</span></span>|<span data-ttu-id="2e041-110">4.5</span><span class="sxs-lookup"><span data-stu-id="2e041-110">4.5</span></span>|
|<span data-ttu-id="2e041-111">Тип</span><span class="sxs-lookup"><span data-stu-id="2e041-111">Type</span></span>|<span data-ttu-id="2e041-112">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="2e041-112">Runtime</span></span>|
|<span data-ttu-id="2e041-113">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="2e041-113">Affected APIs</span></span>|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|
