<!-- default file list -->
*Files to look at*:

* [CellEnabledConverter.cs](./CS/WpfApplication241/CellEnabledConverter.cs) (VB: [CellEnabledConverter.vb](./VB/WpfApplication241/CellEnabledConverter.vb))
* [DateEditCalendarEx.cs](./CS/WpfApplication241/DateEditCalendarEx.cs) (VB: [DateEditCalendarEx.vb](./VB/WpfApplication241/DateEditCalendarEx.vb))
* **[MainWindow.xaml](./CS/WpfApplication241/MainWindow.xaml) (VB: [MainWindow.xaml.vb](./VB/WpfApplication241/MainWindow.xaml.vb))**
* [MainWindow.xaml.cs](./CS/WpfApplication241/MainWindow.xaml.cs) (VB: [MainWindow.xaml.vb](./VB/WpfApplication241/MainWindow.xaml.vb))
<!-- default file list end -->
# How to disable some dates in DateEdit


<p>This example shows how to disable a custom set of dates in the <strong>DateEdit</strong> control.<br><br></p>
<p>The main idea of the approach is to add a collection of disabled dates to the <strong>DateEdit</strong>'s <strong>Tag</strong> property and disable corresponding calendar buttons by using a <strong>DataTrigger</strong> with a custom <strong>MultiConverter</strong>. This <strong>MultiConverter</strong> checks if a date associated with a certain button exists in the collection of disabled dates. If so, the button's <strong>IsEnabled</strong> property is set to <strong>False</strong>.</p>
<p> </p>
<p>To avoid posting disabled data when the keyboard is used instead of the mouse, the implementation of the <strong>DateEditCalendar</strong> class and its <strong>OnCellButtonClick</strong> method was also changed. This custom <strong>DateEditCalendar</strong> is used in <strong>DateEdit</strong>'s popup with the help of an implicit style for the <strong>DateEdit</strong> type.<br><br>You can use a similar approach for disabling dates based on another rule, for example, prohibit selecting weekends. For this, modify the <strong>CellEnabledConverter</strong> class to implement the required logic.</p>

<br/>


