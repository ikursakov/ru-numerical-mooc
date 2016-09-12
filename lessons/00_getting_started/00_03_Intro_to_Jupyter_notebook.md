# Введение в Jupyter notebooks 
## Что такое Jupyter Notebook?

В этом курсе мы будем интенсивно использовать [Jupyter Notebooks](https://jupyter-notebook.readthedocs.org/en/latest/notebook. html) (ранее это всё называлось IPython Notebooks). Блокноты это мультимедийные документы, в которых можно использовать текст в формате Markdown, математические формулы, набранные в  LaTeX  и отрендеренные при помощи MathJax, и исполняемый код Python.

Лучший способ понять, что такое ноутбук Jupyter -- попробовать, как это все работает, так что вперед! 

## Запуск сервера блокнотов
Для запуска сервера блокнотов откройте терминал и введите

```Bash jupyter notebook ```

Эта команда запустит сервер блокнотов. После этого в браузере по умолчанию *должна* автоматически открыться заглавная страница сервера. Если этого не произошло, просто откройте браузер и введите в адресной строке 

``` http://localhost:8888/tree ```

На заглавной странице отображается файловая структура директории, из которой был запущен сервер. Для того, чтобы создать свой первый блокнот, кликните на кнопку `New Notebook`, а затем выберите пункт меню **Python 3** в самом низу списка.

![newnotebook](./images/newnotebook.gif)

##Выполнение ячейки кода

Под панелью инструментов расположена ячейка кода, начинающаяся с префикса `In [ ]:`. Такая ячейка может содержать произвольный кусок кода, но мы начнем с чего-нибудь простого. В единственной (пока) ячейке наберите

```Python x = 5 ```,

а затем нажмите *Shift+Enter*. Если вы нажмете просто Enter, то обнаружите, что в ячейке просто появилась еще одна строка. Итак, запомните: для того, чтобы **выполнить** команды, содержащиеся в ячейке кода, необходимо нажать *Shift+Enter*.

Что же произошло? Мы приписали ярлык `x` числу 5. Кроме того, как можно увидеть, префикс самой ячейки изменился и теперь выглядит как `In[1]:`, так как это первое выражение, выполненное данным ядром Python. Также можно заметить, что в блокноте появилась новая ячейка, поскольку единственная сущестоввавшая до этого уже использована нами. 

В новой ячейке попробуем вывести значение, присвоенное переменной x -- введем  

```Python print(x) ```

и нажмем **Shift+Enter**. Полуим ожидаемый результат. У новой ячейки появился префикс `In[2]:`, а результат выполнения команды выводится в ячейке, расположенной прямо под той, в которую мы вводили команду. 

Весь процесс должен выглядеть примерно следующим образом:

![runandprint](./images/runandprint.gif)

##Ядро

Нам сейчас не требуется детально разбираться, что такое "ядро" ("kernel"), главное отметить, что можно присвоить значение переменной в одной ячейке, а вызвать ее в другой, и это сработает. Ячейки позволяют *нам* разделить на логические блоки наши мысли и код, сохранив связи между блоками.

##Перезапись переменных 

Поскольку каждая ячейка может взаимодействовать с одним и тем же экземпляром интерпетатра Python, если присвоить переменной `x` новое значение, а затем ввести `print(x)`, то выведется это новое значение. Это довольно ожидаемый результат, но что если удалить ячейку, в которой происходило присваивание нового значения `x`?

Сказано -- сделано!

![overwrite](./images/overwrite.gif)

Даже если удалить ячейку с кодом, в которой выполнялось присвоение `x = 7`, оно по-прежнему будет корректным, и при вызове `x`  будет выводиться `7`. Более того, ситуация не изменится до тех пор пока переменной `x` не будет присвоено новое значение, или пока не бдет перпзапущен весь блокнот целиком.

##Markdown 
Markdown is a *writing format* that makes it easy to type well-formatted text that is rendered into properly formatted XHTML.  It's seriously awesome.  Cells in Jupyter notebooks can be used for many things: to run Python, to embed media, or to write text in Markdown.  This allows us to write notes about what we're doing, what the code is doing, what we're *trying* to do, whatever we like! These notes can be for ourselves, to document our work, or to share with others.

To create a Markdown cell in a notebook, click on an empty cell, then click on the Dropdown list (by default, it will say "Code") and select "Markdown"—as shown below.

Markdown is also (sort of) code, so after you type some text, you will also hit *Shift+Enter* to execute the cell and render the Markdown text. Try it out!  Just type out a sentence or two in a markdown cell, then hit *Shift+Enter* to render the text.

![render](./images/rendermarkdown.gif)

##Markdown Math ## 
Markdown can do more than just render simple text, it can also render LaTeX-style equations using **MathJax**!

* For inline math, wrap LaTeX inside single `$` signs `$...$` * For single-line rendering, wrap LaTeX inside double `$$` signs `$$...$$`

![mathjax](./images/mathjax.gif)

**Note:**

Be aware that math typesetting is handled by MathJax and not by LaTeX. While the vast majority of MathJax syntax is identical to LaTeX, there are a few small differences (especially when it comes to matrix commands).  So if you find something doesn't typeset the way you expect, Google around to make sure you're using the correct command.

##More Markdown Syntax 
There are several references to learn Markdown tricks, but we especially like the summary by [John Gruber](http://daringfireball.net/projects/markdown/syntax).  A few features that we find particularly useful are listed below.

For italics, wrap text in single `*`: `*this will be italic*` For bold, wrap text in double `**`: `**this will be bold**` For a bulleted list, start the line with an `*`, then type a space followed by the bullet item ``` * list item * another list item * and another ```

##Moving Cells Around
You'll often find that you want to add or delete cells, or just move them around.  To move a cell, just click on it to select it, then use the Up- and Down-arrows in the toolbar to change the position of the cell.

![movecells](./images/movingcells.gif)

To add a cell, you can click the + button in the toolbar.  Once you're comfortable with the notebook layout, you can also click on Help -> Keyboard Shortcuts to find out various shortcuts for adding, deleting and managing cell position and type.
