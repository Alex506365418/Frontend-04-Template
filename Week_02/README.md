学习笔记

1. e.which
<table>
<tbody>
<tr ><th>event.which属性值</th><th>对应的鼠标按钮</th></tr>
<tr>
<td>1</td>
<td>鼠标左键</td>
</tr>
<tr>
<td>2</td>
<td>鼠标中键(滚轮键)</td>
</tr>
<tr>
<td>3</td>
<td>鼠标右键</td>
</tr>
</tbody>
</table>

<table >
<tbody>
<tr ><th>which属性值(或范围)</th><th>对应的输入字符</th></tr>
<tr>
<td>48 - 57</td>
<td>对应字符 0 - 9</td>
</tr>
<tr>
<td>65 - 90</td>
<td>对应字符 A - Z</td>
</tr>
<tr>
<td>97 - 122</td>
<td>对应字符 a - z</td>
</tr>
</tbody>
</table>

<table>
<tbody>
<tr class="firstRow"><th>which属性值(或范围)</th><th>对应的键盘按键</th></tr>
<tr>
<td>8</td>
<td>Backspace键</td>
</tr>
<tr>
<td>9</td>
<td>Tab键</td>
</tr>
<tr>
<td>13</td>
<td>Enter键</td>
</tr>
<tr>
<td>16</td>
<td>Shift键</td>
</tr>
<tr>
<td>17</td>
<td>Ctrl键</td>
</tr>
<tr>
<td>20</td>
<td>Alt键</td>
</tr>
<tr>
<td>20</td>
<td>Caps Lock键(大小写锁定)</td>
</tr>
<tr>
<td>27</td>
<td>Esc键</td>
</tr>
<tr>
<td>33 - 36</td>
<td>对应按键 PageUp、PageDown、End、Home</td>
</tr>
<tr>
<td>37 - 40</td>
<td>对应按键 左、上、右、下(方向键)</td>
</tr>
<tr>
<td>45 - 46</td>
<td>对应按键 Insert、Delete</td>
</tr>
<tr>
<td>48 - 57</td>
<td>对应按键 0 - 9(非小键盘)</td>
</tr>
<tr>
<td>65 - 90</td>
<td>对应按键 A - Z</td>
</tr>
<tr>
<td>91</td>
<td>Windows键</td>
</tr>
<tr>
<td>96 - 105</td>
<td>对应按键 0 - 9(小键盘)</td>
</tr>
<tr>
<td>106、107、109、110、111</td>
<td>对应按键*、+、-、.、/(小键盘)</td>
</tr>
<tr>
<td>112 - 123</td>
<td>对应按键 F1 - F12</td>
</tr>
</tbody>
</table>
1. JavaScript exec() 方法：
   exec(string) 方法用于检索字符串中的正则表达式的匹配。必传参数 string

1. yield
   什么是 yield？
   yield 是 ES6 的新关键字，使生成器函数执行暂停，yield 关键字后面的表达式的值返回给生成器的调用者。它可以被认为是一个基于生成器的版本的 return 关键字。
   yield 关键字实际返回一个 IteratorResult（迭代器）对象，它有两个属性，value 和 done，分别代表返回值和是否完成。
   yield 无法单独工作，需要配合 generator(生成器)的其他函数，如 next，懒汉式操作，展现强大的主动控制特性。
